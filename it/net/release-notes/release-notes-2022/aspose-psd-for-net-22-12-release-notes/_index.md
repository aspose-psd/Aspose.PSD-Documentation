---
title: Note sulla versione di Aspose.PSD per .NET 22.12
type: docs
weight: 10
url: /it/net/aspose-psd-for-net-22-12-release-notes/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- In questa versione è stato corretto un problema di regressione con l'esportazione a 16 bit.

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-1336|Aggiungi la proprietà TextOrientation modificabile all'interfaccia IText|Funzionalità|
|PSDNET-725|Il ridimensionamento del file PSD specificato con una maschera di livello produce una maschera incorretta|Bug|
|PSDNET-1277|Aggiungi la capacità di salvare e caricare una maschera per 16 immagini|Bug|
|PSDNET-1281|Trasparenza errata nel salvataggio di un'immagine a 16 bit in un'immagine a 16 o 8 bit|Bug|
|PSDNET-1375|Correggi lo spazio colore CMYK nei colori a 16 bit|Bug|


## **Variazioni dell'API pubblica**
# **API Aggiunte:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **API Rimosse:**
- Nessuna


## **Esempi di utilizzo:**

**PSDNET-725. Il ridimensionamento del file PSD specificato con una maschera di livello produce una maschera incorretta**

{{< highlight csharp >}}
string fileSorgente = "file_sorgente.psd";
string percorsoEsportazionePsd = "output.psd";
string percorsoEsportazionePng = "output.png";

// Apre il file PSD di origine
using (PsdImage immagine = (PsdImage)Image.Load(fileSorgente))
{
    const int Scala = 4;

    int nuovaLarghezza = immagine.Width * Scala;
    int nuovaAltezza = immagine.Height * Scala;

    // Esegue il ridimensionamento
    immagine.Resize(nuovaLarghezza, nuovaAltezza);
    immagine.Save(percorsoEsportazionePsd, new PsdOptions(immagine));
}

// Apre un file PSD ridimensionato
using (PsdImage immagine = (PsdImage)Image.Load(percorsoEsportazionePsd))
{
    // Salva in PNG
    immagine.Save(percorsoEsportazionePng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. Aggiungi la capacità di salvare e caricare una maschera per 16 immagini**

{{< highlight csharp >}}
string filePsd8bitSorgente = @"input_8bitColor.psd";
string filePsd16bitOutput = @"output_16bitColor.psd";

using (var immagine = (PsdImage)Image.Load(filePsd8bitSorgente))
{
    // Le opzioni consentono di salvare il colore a 16 bit
    PsdOptions opzioni16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // Il file PSD verrà salvato con la trasparenza
    immagine.Save(filePsd16bitOutput, opzioni16);
}
{{< /highlight >}}

**PSDNET-1281. Trasparenza errata nel salvataggio di un'immagine a 16 bit in un'immagine a 16 o 8 bit**

{{< highlight csharp >}}
string fileSorgente = @"Esempio_16bit.psd";
string fileRisalvato = @"Risalva_16bit.psd";
string fileImmagine = @"ImmagineTotale_16bit.png";

// Il file PSD a colori a 16 bit (con trasparenza) verrà aperto e salvato a 16 bit
using (var immagine = (PsdImage)Image.Load(fileSorgente))
{
    PsdOptions opzioni16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    immagine.Save(fileRisalvato, opzioni16);
}

// Il file PSD a colori a 16 bit salvato verrà convertito in un file PNG con trasparenza
using (var immagine = (PsdImage)Image.Load(fileRisalvato))
{
    immagine.Save(fileImmagine, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Aggiungi la proprietà modificabile TextOrientation all'interfaccia IText**

{{< highlight csharp >}}
// Il codice seguente dimostra la capacità di modificare la nuova proprietà TextOrientation.
// Questo non influisce attualmente sul rendering, ma consente solo di modificare il valore della proprietà.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var immagine = (PsdImage)Image.Load(src))
{
    var livelloTesto = immagine.Layers[1] as TextLayer;
    if (livelloTesto.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Lettura corretta
    }
    else
    {
        throw new Exception("Lettura non corretta del valore della proprietà TextOrientation");
    }

    livelloTesto.TextData.TextOrientation = TextOrientation.Horizontal;
    livelloTesto.TextData.UpdateLayerData();

    immagine.Save(output);
}

using (var immagine = (PsdImage)Image.Load(output))
{
    var livelloTesto = immagine.Layers[1] as TextLayer;
    if (livelloTesto.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // Lettura corretta
    }
    else
    {
        throw new Exception("Lettura non corretta del valore della proprietà TextOrientation");
    }
}
{{< /highlight >}}

**PSDNET-1375. Correggi spazio colore CMYK nei colori a 16 bit**

{{< highlight csharp >}}
string fileSrc = @"MascheraRitaglioRegolare.psd";
string percorsoEsportazione = @"esporta.psd";
string percorsoEsportazionePng = @"esporta.png";

// Imposta le opzioni di conversione
PsdOptions opzioniPsd = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// Converti e salva
using (var immagine = (PsdImage)Image.Load(fileSrc))
{
    immagine.Convert(opzioniPsd);
    immagine.Save(percorsoEsportazione);
}

// Apre il file convertito e lo rende in PNG
using (PsdImage immagine = (PsdImage)Image.Load(percorsoEsportazione))
{
    immagine.Save(percorsoEsportazionePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
