---
title: Notas de Lançamento do Aspose.PSD para .NET 21.1
type: docs
weight: 120
url: /pt/net/aspose-psd-para-net-21-1-notas-de-lancamento/
---

{{% alert color="primary" %}} 

Esta página contém notas de lançamento do [Aspose.PSD para .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Exceção ao tentar converter arquivo Psd específico para png|Bug|
|PSDNET-792|Exceção ao salvar PSD com objeto inteligente para PNG|Bug|

## **Alterações na API Pública**
# **APIs Adicionadas:**
- Nenhuma

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**
**PSDNET-766. Aspose.PSD 20.10: Exceção ao tentar converter arquivo Psd específico para png**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET766_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "school-admission-flyer-template-05052019.psd";
            string outputFilePath = outputFolder + "chool-admission-flyer-template-05052019_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions();
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. Exceção ao salvar PSD com objeto inteligente para PNG**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder+ "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // Procurando por Objeto Inteligente
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // Estamos carregando a Camada de Objeto Inteligente do Fluxo de Memória,
                        // Mas podemos usar smart smart.ExportContents(somePath) para exportar o objeto inteligente para um arquivo
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // Procurando por Camada de Texto
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // Podemos usar simples UpdateText, mas dessa forma nos dá a capacidade de editar o texto por partes
                                        // Criar camadas de texto com várias linhas e outras características de estilização de texto e parágrafo
                                        // Por favor, tenha cuidado. Se o Conteúdo do Objeto Inteligente não for PSD, você não pode usar esse método de edição de texto
                                        // Nesse caso, você deve usar a API Gráfica: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "Melhor";

                                        // Você deve alterar o tamanho do texto se quiser que a imagem fique bem.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // É melhor usar ReplaceContents. Ele irá reprocessar automaticamente o Objeto Inteligente
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // Desta forma, estamos salvando o Arquivo PSD alterado
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
