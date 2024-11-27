---
title: Note sulla versione di Aspose.PSD per .NET 24.7
type: docs
weight: 60
url: /it/net/aspose-psd-per-net-24-7-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                                    | **Categoria** |
|:-----------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | Eccezione "Caricamento immagine non riuscito" durante l'apertura del documento AI                | Bug      |
| PSDNET-2022 | Testo renderizzato in modo non corretto nei file PDF di output                                    | Bug      |
| PSDNET-2061 | Risoluzione di ImageSaveException: Esportazione immagine non riuscita per il file specificato su Linux | Bug      |
| PSDNET-2080 | Risoluzione del caricamento dei font quando si utilizza Aspose.Drawing                              | Bug      |
| PSDNET-2085 | 'L'operazione aritmetica ha portato a un overflow' durante la creazione di un livello di oggetto intelligente utilizzando un JPEG grande | Bug      |
| PSDNET-2100 | Il file AI non può essere convertito in un file JPG                                                | Bug      |

## **Modifiche all'API pubblica**
# **API aggiunte:**
- Nessuna

# **API rimosse:**
- Nessuna

## **Esempi di utilizzo:**

**PSDNET-1029. Eccezione "Caricamento immagine non riuscito" durante l'apertura del documento AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Testo renderizzato in modo non corretto nei file PDF di output**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. Risoluzione di ImageSaveException: Esportazione immagine non riuscita per il file specificato su Linux**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. Risoluzione del caricamento dei font quando si utilizza Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Prima dell'aggiornamento. Numero di font installati: " + installedFonts.Families.Length);
    Console.WriteLine("- Piattaforma: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- Aggiorna la cache dei font cercando di ottenere il nome del font Adobe per 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- Dopo l'aggiornamento. Numero di font installati: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'L'operazione aritmetica ha portato a un overflow' durante la creazione di un livello di oggetto intelligente utilizzando un JPEG grande**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Test Layer";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. Il file AI non può essere convertito in un file JPG**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}
