---
title: Note sulla versione di Aspose.PSD per .NET 23.8
type: docs
weight: 50
url: /it/net/aspose-psd-for-net-23-8-release-notes/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                                                 | **Categoria** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | Aggiunta nuovo tipo di curvatura (Flag) | Funzionalità |
| PSDNET-1621 | Aggiunti nuovi tipi di curvatura: arco su, arco giù, sfera | Funzionalità |
| PSDNET-1682 | Implementato nuovo metodo PsdImage.AddPosterizeAdjustmentLayer per aggiungere un nuovo livello di posterizzazione | Funzionalità |
| PSDNET-913  | Informazioni PSD perse con l'apertura e il salvataggio | Errore     |
| PSDNET-1352 | Caricamento dell'immagine non riuscito | Errore     |
| PSDNET-1553 | Caricamento dell'immagine non riuscito: Impossibile eseguire il cast dell'oggetto di tipo UnknownStructure in tipo DescriptorStructure | Errore     |
| PSDNET-1631 | File modificato nella libreria di terze parti corrompe il file PSD ma può essere aperto in Photoshop | Errore     |


## **Cambiamenti nell'API pubblica**
# **API aggiunte:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **API rimosse:**
- Nessuna


## **Esempi di utilizzo:**

**PSDNET-913. Informazioni PSD perse con l'apertura e il salvataggio**

{{< highlight csharp >}}
string src = "File originale.psd";
string outputPsd = "out_File originale.psd";
string outputPng = "out_File originale.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Caricamento dell'immagine non riuscito**

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

**PSDNET-1553. Caricamento dell'immagine non riuscito: Impossibile eseguire il cast dell'oggetto di tipo UnknownStructure in tipo DescriptorStructure**

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
            // Dovrebbe caricarsi correttamente
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. File modificato nella libreria di terze parti corrompe il file PSD ma può essere aperto in Photoshop**

{{< highlight csharp >}}
string sourceFile = "output.psd";
string outputFile = "export.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Aggiunta nuovo tipo di curvatura (Flag)**

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

**PSDNET-1621. Aggiunti nuovi tipi di curvatura: arco su, arco giù, sfera**

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

**PSDNET-1682. Implementato nuovo metodo PsdImage.AddPosterizeAdjustmentLayer per aggiungere un nuovo livello di posterizzazione**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// Verifica delle modifiche salvate
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
        throw new Exception(message ?? "Gli oggetti non sono uguali.");
    }
}
{{< /highlight >}}
