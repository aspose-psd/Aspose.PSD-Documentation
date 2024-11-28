---
title: Notas de Lançamento do Aspose.PSD para .NET 23.9
type: docs
weight: 40
url: /pt/net/aspose-psd-for-net-23-9-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para .NET 23.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                                                | **Categoria** |
|:------------|:---------------------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1638 | Implementar a criação de máscara para novas camadas de ajuste                                                               | Recurso |
| PSDNET-1654 | Adicionar suporte para Camadas Recortadas em Modo de Grupo como opção de mesclagem                                         | Recurso |
| PSDNET-1194 | Arquivo PSD com modo de cor de 16 bits não aplica máscara para camadas de ajuste                                           | Defeito  |
| PSDNET-1235 | Renderização incorreta de colchetes na camada de texto                                                                     | Defeito  |
| PSDNET-1559 | Não é possível atualizar estilos nas camadas de texto                                                                      | Defeito  |
| PSDNET-1583 | Após exportar arquivo PSD com CMYK, as cores são alteradas no PSD exportado                                                | Defeito  |
| PSDNET-1619 | Arquivo PSB específico lança a exceção "O retângulo não possui área de processamento comum"                               | Defeito  |
| PSDNET-1648 | Falha no carregamento da imagem. OverflowException: A operação aritmética resultou em um estouro                           | Defeito  |


## **Mudanças na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Layer.BlendClippedElements
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.CustomFontHandler.CustomFontData.#ctor(System.String,System.Byte[])
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontName
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontData
- P:Aspose.PSD.FontSettings.GetSystemAlternativeFont
- P:Aspose.PSD.Graphics.PaintableImageOptions
- P:Aspose.PSD.Image.UsePalette
- M:Aspose.PSD.Region.Equals(System.Object)
- M:Aspose.PSD.Region.GetHashCode
- P:Aspose.PSD.StringFormat.CustomCharIdent
- M:Aspose.PSD.StringFormat.Equals(System.Object)
- M:Aspose.PSD.StringFormat.GetHashCode
- F:Aspose.PSD.StringFormatFlags.ExactAlignment


# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

**PSDNET-1638. Implementar a criação de máscara para novas camadas de ajuste**

{{< highlight csharp >}}
string srcFile = "zendeya_BW.psd";
string dstFile = "zendeya_BW_out.psd";

using (var im = (PsdImage)Image.Load(srcFile))
{
    im.AddBlackWhiteAdjustmentLayer();

    im.Save(dstFile);
}

using (var im = (PsdImage)Image.Load(dstFile))
{
    Layer layer = im.Layers[1];

    AssertAreEqual((ushort)5, layer.ChannelsCount);
    AssertAreEqual((short)-2, layer.ChannelInformation[4].ChannelID);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Os objetos não são iguais.");
    }
}
{{< /highlight >}}

**PSDNET-1654. Adicionar suporte para Camadas Recortadas em Modo de Grupo como opção de mesclagem**

{{< highlight csharp >}}
string sourceFile = "example_source.psd";
string outputPsd = "example_output.psd";
string outputPng = "example_output.png";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    image.Layers[1].BlendClippedElements = false;
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1194. Arquivo PSD com modo de cor de 16 bits não aplica máscara para camadas de ajuste**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string outputPng = "current.png";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1235. Renderização incorreta de colchetes na camada de texto**

{{< highlight csharp >}}
string file = "file1.psd";
string output = "output_1235.png";

using (var psdImage = (PsdImage)Image.Load(file))
{
    foreach (var layer in psdImage.Layers)
    if (layer is TextLayer textLayer)
    textLayer.TextData.UpdateLayerData();

    var imageOptions = new PsdOptions(psdImage);
    psdImage.Save(output, imageOptions);
}
{{< /highlight >}}

**PSDNET-1559. Não é possível atualizar estilos nas camadas de texto**

{{< highlight csharp >}}
string sourceFile = "Example_FontSize.psd";
string outputFile = "output_Example_FontSize.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var l1 = (TextLayer)psdImage.Layers[4];
    var l2 = (TextLayer)psdImage.Layers[5];

    var textItems1 = l1.TextData.ProducePortions(new string[] { "texto1", "texto2" }, l1.TextData.Items[0].Style, l1.TextData.Items[0].Paragraph);

    l1.TextData.RemovePortion(0);
    foreach (var item in textItems1)
    {
        l1.TextData.AddPortion(item);
    }

    var textItems2 = l2.TextData.ProducePortions(new string[] { "camada de texto 1", "camada de texto 22" }, l2.TextData.Items[0].Style, l2.TextData.Items[0].Paragraph);

    foreach (var item in textItems2)
    {
        l2.TextData.AddPortion(item);
    }

    l1.TextData.UpdateLayerData();
    l2.TextData.UpdateLayerData();

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1583. Após exportar arquivo PSD com CMYK, as cores são alteradas no PSD exportado**

{{< highlight csharp >}}
string sourceFile = "canyon.psd";
string outputFilePng = "output_canyon.png";

using (var outputStream = new MemoryStream())
{
    using (var psdImage = (PsdImage)Image.Load(sourceFile))
    {
        psdImage.Save(outputStream);
    }

    outputStream.Position = 0;
    using (var psdImage = (PsdImage)Image.Load(outputStream))
    {
        psdImage.Save(outputFilePng, new PngOptions());
    }
}
{{< /highlight >}}

**PSDNET-1619. O arquivo PSB específico lança a exceção "O retângulo não possui área de processamento comum"**

{{< highlight csharp >}}
var input = "1619_src.psb";
var output = "1619_output.png";
using (PsdImage img = (PsdImage)Image.Load(input, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(output,
    new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1648. Falha no carregamento da imagem. OverflowException: A operação aritmética resultou em um estouro**

{{< highlight csharp >}}
string sourceFile = "9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(sourceFile))
{
    Layer layer = im.Layers[28];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    AssertAreEqual("自定", grdmResource.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Os objetos não são iguais.");
    }
}
{{< /highlight >}}
