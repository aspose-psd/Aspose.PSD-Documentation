---
title: Note sulla versione di Aspose.PSD for .NET 22.11
type: docs
weight: 20
url: /it/net/aspose-psd-for-net-22-11-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD for .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Questo rilascio ha una regressione nel caso delle esportazioni a 16 bit, quindi consigliamo cautela nell'utilizzare questa funzionalità in questo rilascio. Si prega di non aggiornare Aspose.PSD alla versione 22.9-22.11 se l'elaborazione dell'immagine a 16 bit è la funzionalità principale.

Stiamo lavorando per risolvere questi problemi.

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-1320|Impossibile esportare file PSB estremamente grandi|Potenziamento|
|PSDNET-659|Rendi il centro del gradiente radiale mobile|Caratteristica|
|PSDNET-1330|Metodo di compressione ZipWithoutPrediction non supportato per i file specifici|Caratteristica|
|PSDNET-735|Dopo aver utilizzato un metodo di trasformazione solo per uno strato, lo strato salvato ha un riquadro delimitatore errato|Errore|
|PSDNET-1234|Eccezione durante il caricamento dell'immagine PSD con motivo|Errore|
|PSDNET-1244|Esportazione dell'immagine non riuscita (IndexOutOfRangeException) durante il salvataggio del file PSD con simboli cinesi|Errore|
|PSDNET-1303|Il TimeLine ActiveFrame applica in modo errato|Errore|
|PSDNET-1307|Regressione 22.7: rendering errato del testo con caratteri arabi|Errore|
|PSDNET-1321|La maschera vettoriale sullo strato di gruppo funziona in modo errato. L'immagine finale ha il buco nero ma non dovrebbe|Errore|


## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **API Rimosse:**
- Nessuna


## **Esempi di utilizzo:**

**PSDNET-659. Rendi il centro del gradiente radiale mobile**

{{< highlight csharp >}}
string fileSorgente = "psdnet659.psd";
string fileOutput = "output.png";

using (var immaginePsd = (PsdImage)Image.Load(fileSorgente))
{
    FillLayer stratoRadiale = (FillLayer)immaginePsd.Layers[5];
    GradientFillSettings impostazioni = (GradientFillSettings)stratoRadiale.FillSettings;

    // Aggiorna il punto di offset
    impostazioni.HorizontalOffset = 10;
    impostazioni.VerticalOffset = -25;

    immaginePsd.Save(fileOutput, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. Dopo aver utilizzato un metodo di trasformazione solo per uno strato, lo strato salvato ha un riquadro delimitatore errato**

{{< highlight csharp >}}
string nomeFileSorgente = @"TextLayer.psd";
string fileOutput = "TextLayerResized_output.psd";

using (PsdImage immagine = (PsdImage)Image.Load(nomeFileSorgente, new PsdLoadOptions()))
{
    TextLayer stratoTesto = (TextLayer)immagine.Layers[1];

    // Imposta la nuova dimensione dello strato di testo
    const int NuovaLarghezza = 250;
    const int NuovaAltezza = 250;

    // Imposta il meccanismo di ridimensionamento per ridimensionare lo strato (valore predefinito)
    ResizeType tipoRidimensionamento = ResizeType.NearestNeighbourResample;

    // Nuovo meccanismo di ridimensionamento per lo strato di testo
    // Non solo lo strato ma anche la matrice di trasformazione dello strato di testo verrà cambiata
    stratoTesto.Resize(NuovaLarghezza, NuovaAltezza, tipoRidimensionamento);

    immagine.Save(fileOutput, new PsdOptions(immagine));
}

using (PsdImage immagine = (PsdImage)Image.Load(fileOutput, new PsdLoadOptions()))
{
    TextLayer stratoTxt = (TextLayer)immagine.Layers[1];

    // Il motivo del delta è un carattere di default diverso
    if (stratoTxt.TransformMatrix[4] >= 65 
        && stratoTxt.TransformMatrix[4] <= 67
        && stratoTxt.TransformMatrix[5] >= 234
        && stratoTxt.TransformMatrix[5] <= 237)
    {
        // Tutto ok
    }
    else
    {
        throw new Exception("Punto di posizione errato");
    }
}
{{< /highlight >}}

**PSDNET-1234. Eccezione durante il caricamento dell'immagine PSD con motivo**

{{< highlight csharp >}}
string fileSorgente = "test.psd";
string output = "output1234.png";

using (PsdImage immaginePsd = (PsdImage)PsdImage.Load(fileSorgente,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions opzioniPng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    immaginePsd.Save(output, opzioniPng);
}
{{< /highlight >}}

**PSDNET-1244. Esportazione dell'immagine non riuscita (IndexOutOfRangeException) durante il salvataggio del file PSD con simboli cinesi**

{{< highlight csharp >}}
string fileSorgente = "input.psd";
string percorsoOutput = "output.psd";

var opzioniCaricamento = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var immagine = (PsdImage)Image.Load(fileSorgente, opzioniCaricamento))
{
    foreach (var strato in immagine.Layers)
    {
        if (strato.Name == "1")
        {
            var stratoTesto = (TextLayer)strato;

            stratoTesto.UpdateText("测试测试");
        }
    }

    // Qui non dovrebbe esserci alcuna eccezione.
    immagine.Save(percorsoOutput, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. Il frame attivo di TimeLine è applicato in modo errato**

{{< highlight csharp >}}
string sorgente = "timeline1303.psd";
string output = "out_timeline.psd";

using (var immaginePsd = (PsdImage)Image.Load(sorgente))
{
    TimeLine timeLine = TimeLine.InitializeFrom(immaginePsd);

    timeLine.ActiveFrame = 2;
    timeLine.ApplyTo(immaginePsd);

    immaginePsd.Save(output);
}
{{< /highlight >}}

**PSDNET-1307. Regressione 22.7: rendering errato del testo con caratteri arabi**

{{< highlight csharp >}}
string cartellaFontDiProva = "Fonts";
FontSettings.SetFontsFolder(cartellaFontDiProva);
FontSettings.UpdateFonts();

string percorsoFileSorgente = "sarbarg.fin12.psd";
string percorsoFileOutput = "result.tiff";

using (var immaginePsd = (PsdImage)Image.Load(percorsoFileSorgente))
{
    immaginePsd.Save(percorsoFileOutput, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. Impossibile esportare file PSB estremamente grandi**

{{< highlight csharp >}}
string fileSorgente = "hf-mim-liman-han-guc-art-kuvvet.psb";
string percorsoEsportazionePsd = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var immagine = (PsdImage)Image.Load(fileSorgente, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    immagine.Save(percorsoEsportazionePsd, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. La maschera vettoriale sullo strato di gruppo funziona in modo errato. L'immagine finale ha il buco nero ma non dovrebbe**

{{< highlight csharp >}}
string fileSorgente = "demo.psd";
string output = "demo_net.png";

using (PsdImage immagine = (PsdImage)PsdImage.Load(fileSorgente))
{
    PngOptions opzioniPng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    immagine.Save(output, opzioniPng);
}
{{< /highlight >}}

**PSDNET-1330. Metodo di compressione ZipWithoutPrediction non supportato per i file specifici**

{{< highlight csharp >}}
string fileSorgente = "20221017_220706_0000.psd";
string fileOutput = "20221017_220706_0000.jpg";

using (var immagine = (PsdImage)Image.Load(fileSorgente, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase opzioniBase = new JpegOptions() { Quality = 80 };
    immagine.Save(fileOutput, opzioniBase);
}
{{< /highlight >}}
