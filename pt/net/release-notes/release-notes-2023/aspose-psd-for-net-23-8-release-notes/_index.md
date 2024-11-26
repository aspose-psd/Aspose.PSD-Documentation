---
title: Notas da Versão Aspose.PSD para .NET 23.8
type: docs
weight: 50
url: /pt/net/aspose-psd-para-net-23-8-notas-da-versao/
---

{{% alert color="primary" %}}

Esta página contém as notas de versão para [Aspose.PSD para .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                              | **Categoria** |
|:------------|:---------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | Adicionar novo tipo de deformação (Flag) | Recurso |
| PSDNET-1621 | Adicionar novos tipos de deformação: curva para cima, curva para baixo, esfera | Recurso |
| PSDNET-1682 | Implementar novo método PsdImage.AddPosterizeAdjustmentLayer para adicionar nova camada Posterize | Recurso |
| PSDNET-913  | Informações do PSD perdidas apenas ao abrir e salvar | Bug     |
| PSDNET-1352 | Falha ao carregar imagem | Bug     |
| PSDNET-1553 | Falha ao carregar imagem: Não é possível converter objeto do tipo UnknownStructure para o tipo DescriptorStructure | Bug     |
| PSDNET-1631 | Arquivo alterado na biblioteca de terceiros corrompe o arquivo PSD, mas pode ser aberto no Photoshop | Bug     |


## **Alterações na API Pública**
# **APIs Adicionadas:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

**PSDNET-913. Informações do PSD perdidas apenas ao abrir e salvar**

{{< highlight csharp >}}
string src = "Arquivo original.psd";
string outputPsd = "out_Arquivo original.psd";
string outputPng = "out_Arquivo original.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Falha ao carregar imagem**

{{< highlight csharp >}}
string srcFile1 = "test_text.psd";
string srcFile2 = "test_smart_object.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. Falha ao carregar imagem: Não é possível converter objeto do tipo UnknownStructure para o tipo DescriptorStructure**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // Deve carregar corretamente
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. Arquivo alterado na biblioteca de terceiros corrompe o arquivo PSD, mas pode ser aberto no Photoshop**

{{< highlight csharp >}}
string sourceFile = "output.psd";
string outputFile = "export.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Adicionar novo tipo de deformação (Flag)**

{{< highlight csharp >}}
string sourceFile = "flag_warp.psd";
string outputFile = "flag_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. Adicionar novos tipos de deformação: curva para cima, curva para baixo, esfera**

{{< highlight csharp >}}
string sourceFileArcUpper = "arc_upper_warp.psd";
string sourceFileArcLower = "arc_lower_warp.psd";
string sourceFileBulge =  "bulge_warp.psd";

string outputFileArcUpper ="ArcUpper_export.png";
string outputFileArcLower = "ArcLower_export.png";
string outputFileBulge = "Bulge_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFileArcUpper, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcUpper, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(sourceFileArcLower, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcLower, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(sourceFileBulge, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileBulge, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. Implementar novo método PsdImage.AddPosterizeAdjustmentLayer para adicionar nova camada Posterize**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// Verificar as alterações salvas
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Os objetos não são iguais.");
    }
}
{{< /highlight >}}
