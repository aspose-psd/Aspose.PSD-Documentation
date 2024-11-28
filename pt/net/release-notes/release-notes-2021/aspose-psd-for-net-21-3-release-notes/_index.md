---
title: Notas da versão Aspose.PSD para .NET 21.3
type: docs
weight: 100
url: /pt/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}}

Esta página contém as notas de lançamento para [Aspose.PSD para .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-823|Adicionar o SectionDividerLayer para melhorar a experiência com grupos de camadas|Melhoria|
|PSDNET-694|Ao ler PattResource, largura e altura foram trocadas|Erro|
|PSDNET-789|Blendagem incorreta de mais de um Efeito de Camada|Erro|
|PSDNET-805|Ordem e lógica de blendagem incorretas quando há mais de um Efeito de Camada|Erro|
|PSDNET-842|Propriedades de efeito de contorno que não são salvas no arquivo PSD|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDNET-694. Ao ler PattResource, largura e altura foram trocadas**

{{< highlight csharp >}}
            string arquivoOrigem = "Untitled-1.psd";
            string arquivoSaida = "output.png";

            using (var imagem = (PsdImage)Image.Load(arquivoOrigem))
            {
                var camadaPreenchimento = (FillLayer)imagem.Layers[1];
                camadaPreenchimento.Update(); // invocar renderização de padrão

                imagem.Save(arquivoSaida, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Blendagem incorreta de mais de um Efeito de Camada**

{{< highlight csharp >}}
            string arquivoFonte = "source_789.psd";
            string caminhoSmartObjectSaida = "output789.png";
            string arquivoSaida = "output789.psd";

            using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var comprimento = imagem.Layers.Length;
                for (int i = 0; i < comprimento; i++)
                {
                    var smart = imagem.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imagemNoSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imagemNoSmart.Layers.Length; j++)

                                {
                                    // Procurando pela Camada de Texto
                                    var camadaTexto = imagemNoSmart.Layers[j] as TextLayer;
                                    if (camadaTexto != null)
                                    {
                                        var dadosTexto = camadaTexto.TextData;

                                        dadosTexto.Items[0].Text = "Melhor";
                                        dadosTexto.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imagemNoSmart);
                            }
                        }

                        break;
                    }
                }
                // Dessa forma, estamos salvando o arquivo PSD alterado
                imagem.Save(caminhoSmartObjectSaida, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                imagem.Save(arquivoSaida);
            }
{{< /highlight >}}

**PSDNET-805. Ordem e lógica de blendagem incorretas quando há mais de um Efeito de Camada**

{{< highlight csharp >}}
            string arquivoOrigem = "1_200x200.psd";
            string arquivoConteudo = "Numbers1Best.png";

            string arquivoSaidaPng = "output.png";
            string arquivoSaidaPsd = "output.psd";

            using (PsdImage imagem = (PsdImage)Image.Load(arquivoOrigem, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var comprimento = imagem.Layers.Length;
                for (int i = 0; i < comprimento; i++)
                {
                    var smart = imagem.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(arquivoConteudo);
                        break;
                    }
                }

                //Dessa forma, estamos salvando o arquivo PSD alterado
                imagem.Save(arquivoSaidaPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                imagem.Save(arquivoSaidaPsd);
            }
{{< /highlight >}}

**PSDNET-823. Adicionar o SectionDividerLayer para melhorar a experiência com grupos de camadas**

{{< highlight csharp >}}
            // O código a seguir demonstra camadas SectionDividerLayer e como obter o grupo de camadas relacionado.

            // Hierarquia de camadas
            //    [0]: '</Layer group>' SectionDividerLayer para Grupo 1
            //    [1]: 'Camada 1' Regular Layer
            //    [2]: '</Layer group>' SectionDividerLayer para Grupo 2
            //    [3]: '</Layer group>' SectionDividerLayer para Grupo 3
            //    [4]: 'Grupo 3' GroupLayer
            //    [5]: 'Grupo 2' GroupLayer
            //    [6]: 'Grupo 1' GroupLayer

            void AssertAreEqual(object esperado, object atual, string mensagem = null)
            {
                if (!object.Equals(esperado, atual))
                {
                    throw new FormatException(mensagem ?? "Os objetos não são iguais.");
                }
            }

            using (var imagem = new PsdImage(100, 100))
            {
                // Criando hierarquia de camadas
                // Adiciona o LayerGroup 'Grupo 1'
                LayerGroup grupo1 = imagem.AddLayerGroup("Grupo 1", 0, true);
                // Adiciona camada regular
                Layer camada1 = new Layer();
                camada1.DisplayName = "Camada 1";
                grupo1.AddLayer(camada1);
                // Adiciona o LayerGroup 'Grupo 2'
                LayerGroup grupo2 = grupo1.AddLayerGroup("Grupo 2", 1);
                // Adiciona o LayerGroup 'Grupo 3'
                LayerGroup grupo3 = grupo2.AddLayerGroup("Grupo 3", 0);

                // Obtém os SectionDividerLayer's
                SectionDividerLayer divisor1 = (SectionDividerLayer)imagem.Layers[0];
                SectionDividerLayer divisor2 = (SectionDividerLayer)imagem.Layers[2];
                SectionDividerLayer divisor3 = (SectionDividerLayer)imagem.Layers[3];

                // usando o método SectionDividerLayer.GetRelatedLayerGroup(), obtém a instância relacionada do LayerGroup.
                AssertAreEqual(grupo1.DisplayName, divisor1.GetRelatedLayerGroup().DisplayName); // o mesmo LayerGroup
                AssertAreEqual(grupo2.DisplayName, divisor2.GetRelatedLayerGroup().DisplayName); // o mesmo LayerGroup
                AssertAreEqual(grupo3.DisplayName, divisor3.GetRelatedLayerGroup().DisplayName); // o mesmo LayerGroup

                LayerGroup pasta1 = divisor1.GetRelatedLayerGroup();
                AssertAreEqual(5, pasta1.Layers.Length); // 'Grupo 1' contém 5 camadas
            }
{{< /highlight >}}

**PSDNET-842. Propriedades de efeito de contorno que não são salvas no arquivo PSD**

{{< highlight csharp >}}
            void AssertAreEqual(object esperado, object atual, string mensagem = null)
            {
                if (!object.Equals(esperado, atual))
                {
                    throw new FormatException(mensagem ?? "Os objetos não são iguais.");
                }
            }

            string arquivoFonte = "badStrokeEffect.psd";
            string resultado = "output.psd";

            using (var imagem = (PsdImage)Image.Load(arquivoFonte, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var camada1 = new Layer();
                imagem.AddLayer(camada1);
                camada1.BlendingOptions.AddStroke(FillType.Color); // Não lançará ArgumentNullException

                StrokeEffect efeitoContorno = imagem.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                efeitoContorno.Size = 10;
                efeitoContorno.Position = StrokePosition.Outside;
                efeitoContorno.Overprint = true;

                imagem.Save(resultado);
            }

            // Verifica os valores salvos
            using (var imagem = (PsdImage)Image.Load(resultado, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect efeitoContorno = (StrokeEffect)imagem.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, efeitoContorno.Size);
                AssertAreEqual(StrokePosition.Outside, efeitoContorno.Position);
                AssertAreEqual(true, efeitoContorno.Overprint);
            }
{{< /highlight >}}
