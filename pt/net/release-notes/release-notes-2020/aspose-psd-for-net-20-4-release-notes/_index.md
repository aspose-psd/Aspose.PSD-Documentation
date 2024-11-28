---
title: Aspose.PSD for .NET 20.4 - Notas da Versão
type: docs
weight: 90
url: /pt/net/aspose-psd-for-net-20-4-release-notes/
---

{{% alert color="primary" %}} 

Esta página contém notas de lançamento para [Aspose.PSD for .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-567|Suporte ao recurso 'Vector Origination Data'|Recurso|
|PSDNET-373|Suporte a lclrResource (Configuração de cor da planilha)|Recurso|
|PSDNET-563|Suporte a propriedades de dados LengthRecord. (Operações de caminho (operações booleanas), índice da forma na camada, contagem dos registros de nó de bezier)|Recurso|
|PSDNET-425|Suporte ao recurso de Seção de Imagem #1010 Cor de fundo|Recurso|
|PSDNET-530|Adição de Camadas de Preenchimento em tempo de execução|Recurso|
|PSDNET-424|Suporte ao recurso de Seção de Imagem #1009 Informações de borda|Recurso|
|PSDNET-592|Suporte a Camadas em Arquivos de Formato AI|Recurso|
|PSDNET-256|Suporte à Leitura e Edição do Efeito de Sobreposição de Gradiente|Recurso|
|PSDNET-257|Renderização do Efeito de Sobreposição de Gradiente|Recurso|
|PSDNET-585|As alterações na propriedade GradientOverlayEffect.BlendMode não são exibidas no Photoshop|Erro|
|PSDNET-561|Correção ao salvar imagem PSD com ColorMode em Escala de Cinza e 16 bits por canal para formato PSD em escala de cinza|Erro|
|PSDNET-560|Correção ao salvar imagem PSD com ColorMode em Escala de Cinza e 16 bits por canal para formato PNG|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Name
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsTemplate
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsLocked
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsShown
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPrinted
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPreview
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsImagesDimmed
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.DimValue
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorNumber
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Red
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Green
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Blue
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- T:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.Color
- T:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Width
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Unit
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.#ctor(System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.BezierKnotRecordsCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.ShapeIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.ShapeOriginSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.#ctor(System.Boolean,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidated
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.OriginIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.ExcludeOverlappingShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.CombineShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.SubtractFrontShape
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.IntersectShapeAreas
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.#ctor(Aspose.PSD.Color,System.Int32,System.Int32)
# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**
**PSDNET-567. Suporte ao recurso 'Vector Origination Data'**

{{< highlight java >}}

         // Suporte a VogkResource

        static void ExemploDeSuporteAVectorOriginationData()

        {

            string nomeArquivo = "VectorOriginationDataResource.psd";

            string nomeArquivoSaida = "out_VectorOriginationDataResource_.psd";

            using (var imagemPsd = (PsdImage)Image.Load(nomeArquivo))

            {

                var recurso = ObterVogkResource(imagemPsd);

                // Leitura

                if (recurso.ShapeOriginSettings.Length != 1 ||

                    !recurso.ShapeOriginSettings[0].IsShapeInvalidated ||

                    recurso.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    throw new Exception("VogkResource foi lido incorretamente.");

                }

                // Edição

                recurso.ShapeOriginSettings = new[]

                {

                    recurso.ShapeOriginSettings[0],

                    new VectorShapeOriginSettings(true, 1)

                };

                imagemPsd.Save(nomeArquivoSaida);

            }

        }

        static VogkResource ObterVogkResource(PsdImage imagem)

        {

            var camada = imagem.Layers[1];

            VogkResource recurso = null;

            var recursos = camada.Resources;

            for (int i = 0; i < recursos.Length; i++)

            {

                if (recursos[i] is VogkResource)

                {

                    recurso = (VogkResource)recursos[i];

                    break;

                }

            }

            if (recurso == null)

            {

                throw new Exception("Recurso VogkResource não encontrado.");

            }

            return recurso;

        }   

{{< /highlight >}}



**PSDNET-373. Suporte a lclrResource (Configuração de cor da planilha)**

{{< highlight java >}}

         static void VerificarCoresDaPlanilhaEInverter(SheetColorHighlightEnum[] coresPlanilha, PsdImage img)

        {

            int contagemCamadas = img.Layers.Length;

            for (int indiceCamada = 0; indiceCamada < contagemCamadas; indiceCamada++)

            {

                Camada camada = img.Layers[indiceCamada];

                LayerResource[] recursos = camada.Resources;

                foreach (LayerResource recursoCamada in recursos)

                {

                    // O recurso lcrl está sempre presente na lista de recursos do arquivo psd.

                    LclrResource recurso = recursoCamada as LclrResource;

                    if (recurso != null)

                    {

                        if (recurso.Color != coresPlanilha[indiceCamada])

                        {

                            throw new Exception("A cor da Planilha foi lida incorretamente.");

                        }

                        // Inversão das cores da planilha. Configuração da cor de destaque da camada.

                        recurso.Color = coresPlanilha[contagemCamadas - indiceCamada - 1];

                        break;

                    }

                }

            }

        }

            string caminhoArquivoFonte = "TodasAsCoresLclrResource.psd";

            string caminhoArquivoSaida = "TodasAsCoresLclrResourceInvertidas.psd";

            // No arquivo as cores de destaque das camadas estão nessa ordem

            SheetColorHighlightEnum[] coresPlanilha = new SheetColorHighlightEnum[] {

                SheetColorHighlightEnum.Vermelho,

                SheetColorHighlightEnum.Laranja,

                SheetColorHighlightEnum.Amarelo,

                SheetColorHighlightEnum.Verde,

                SheetColorHighlightEnum.Azul,

                SheetColorHighlightEnum.Violeta,

                SheetColorHighlightEnum.Cinza,

                SheetColorHighlightEnum.SemCor

            };            

            // A Cor da Planilha é usada para destacar visualmente as camadas. 

            // Por exemplo, você pode atualizar algumas camadas no PSD e depois destacá-las por cor para chamar a atenção.

            using (PsdImage img = (PsdImage)Image.Load(caminhoArquivoFonte))

            {

                VerificarCoresDaPlanilhaEInverter(coresPlanilha, img);

                img.Save(caminhoArquivoSaida, new PsdOptions());

            }

            using (PsdImage img = (PsdImage)Image.Load(caminhoArquivoSaida))

            {

                // As cores devem ser invertidas

                Array.Reverse(coresPlanilha);

                VerificarCoresDaPlanilhaEInverter(coresPlanilha, img);

            }

{{< /highlight >}}



**PSDNET-563. Suporte a propriedades de dados LengthRecord. (Operações de caminho (operações booleanas), índice da forma na camada, contagem dos registros de nó de bezier)**

{{< highlight java >}}

            string nomeArquivo = "OperacoesDeCaminhoForma.psd";

            using (var im = (PsdImage)Image.Load(nomeArquivo))

            {

                VsmsResource recurso = null;

                foreach (var recursoCamada in im.Layers[1].Resources)

                {

                    if (recursoCamada is VsmsResource)

                    {

                        recurso = (VsmsResource)recursoCamada;

                        break;

                    }

                }

                LengthRecord registroComprimento0 = (LengthRecord)recurso.Paths[2];

                LengthRecord registroComprimento1 = (LengthRecord)recurso.Paths[7];

                LengthRecord registroComprimento2 = (LengthRecord)recurso.Paths[11];

                // Aqui estamos mudando a forma de combinar entre formas.

                registroComprimento0.PathOperations = PathOperations.ExcludeOverlappingShapes;

                registroComprimento1.PathOperations = PathOperations.IntersectShapeAreas;

                registroComprimento2.PathOperations = PathOperations.SubtractFrontShape;

                im.Save("out_" + nomeArquivo);

            }

{{< /highlight >}}



**PSDNET-425. Suporte ao recurso de Seção de Imagem #1010 Cor de fundo**

{{< highlight java >}}

             string caminhoArquivoFonte = "entrada.psd";

            string caminhoArquivoSaida = "saida.psd";

            using (var imagem = (PsdImage)Image.Load(caminhoArquivoFonte))

            {

                ResourceBlock[] recursosImagem = imagem.ImageResources;

                BackgroundColorResource recursoCorFundo = null;

                foreach (var recursoImagem in recursosImagem)

                {

                    if (recursoImagem is BackgroundColorResource)

                    {

                        recursoCorFundo = (BackgroundColorResource)recursoImagem;

                        break;

                    }

                }

                // atualizar BackgroundColorResource

                recursoCorFundo.Color = Color.VermelhoEscuro;

                imagem.Save(caminhoArquivoSaida);

            }

{{< /highlight >}}


**PSDNET-530. Adição de Camadas de Preenchimento em tempo de execução**

{{< highlight java >}}

             string psdSaida = "saida.psd";

            using (var imagem = new PsdImage(100, 100))

            {

                FillLayer camadaPreenchimentoCor = FillLayer.CreateInstance(FillType.Color);

                camadaPreenchimentoCor.DisplayName = "Camada de Preenchimento de Cor";

                imagem.AddLayer(camadaPreenchimentoCor);

                FillLayer camadaPreenchimentoGradiente = FillLayer.CreateInstance(FillType.Gradient);

                camadaPreenchimentoGradiente.DisplayName = "Camada de Preenchimento de Gradiente";

                imagem.AddLayer(camadaPreenchimentoGradiente);

                FillLayer camadaPreenchimentoPadrao = FillLayer.CreateInstance(FillType.Pattern);

                camadaPreenchimentoPadrao.DisplayName = "Camada de Preenchimento de Padrão";

                camadaPreenchimentoPadrao.Opacity = 50;

                imagem.AddLayer(camadaPreenchimentoPadrao);

                imagem.Save(psdSaida);

            }

{{< /highlight >}}


**PSDNET-424. Suporte ao recurso de Seção de Imagem #1009 Informações de borda**

{{< highlight java >}}

             string caminhoArquivoFonte = "entrada.psd";

            string caminhoArquivoSaida = "saida.psd";

            using (var imagem = (PsdImage)Image.Load(caminhoArquivoFonte))

            {

                ResourceBlock[] recursosImagem = imagem.ImageResources;

                BorderInformationResource recursoInfoBorda = null;

                foreach (var recursoImagem in recursosImagem)

                {

                    if (recursoImagem is BorderInformationResource)

                    {

                        recursoInfoBorda = (BorderInformationResource)recursoImagem;

                        break;

                    }

                }

                // atualizar BorderInformationResource

                recursoInfoBorda.Width = 0.1;

                recursoInfoBorda.Unit = PhysicalUnit.Polegadas;

                imagem.Save(caminhoArquivoSaida);

            }

{{< /highlight >}}


**PSDNET-592. Suporte a Camadas em Arquivos de Formato AI**

{{< highlight java >}}

         void AssertOneTrue(bool condicao, string mensagem)

        {

            if (!condicao)

            {

                throw new FormatException(mensagem);

            }

        }

        string nomeArquivoFonte = "form_8_2l3_7.ai";

        string nomeArquivoSaida = "form_8_2l3_7_export";

        using (AiImage imagem = (AiImage)Image.Load(nomeArquivoFonte))

        {

            AiLayerSection camada0 = imagem.Layers[0];

            AssertOneTrue(camada0 != null, "A Camada 0 não deveria ser nula.");

            AssertOneTrue(camada0.Name == "Camada 4", "A propriedade Nome da Camada 0 deveria ser Camada 4");

            AssertOneTrue(!camada0.IsTemplate, "A propriedade IsTemplate da Camada 0 deveria ser falsa.");

            AssertOneTrue(camada0.IsLocked, "A propriedade IsLocked da Camada 0 deveria ser verdadeira.");

            AssertOneTrue(camada0.IsShown, "A propriedade IsShown da Camada 0 deveria ser verdadeira.");

            AssertOneTrue(camada0.IsPrinted, "A propriedade IsPrinted da Camada 0 deveria ser verdadeira.");

            AssertOneTrue(!camada0.IsPreview, "A propriedade IsPreview da Camada 0 deveria ser falsa.");

            AssertOneTrue(camada0.IsImagesDimmed, "A propriedade IsImagesDimmed da Camada 0 deveria ser verdadeira.");

            AssertOneTrue(camada0.DimValue == 51, "A propriedade DimValue da Camada 0 deveria ser 51.");

            AssertOneTrue(camada0.ColorNumber == 0, "A propriedade ColorNumber da Camada 0 deveria ser 0.");

            AssertOneTrue(cam