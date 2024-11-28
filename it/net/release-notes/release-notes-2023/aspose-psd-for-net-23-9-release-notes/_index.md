---
title: Note sulla versione di Aspose.PSD per .NET 23.9
type: docs
weight: 40
url: /it/net/aspose-psd-for-net-23-9-release-notes/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 23.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                                                             | **Categoria** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1638 | Implementare la creazione di una maschera per nuovi livelli di regolazione                                                 | Funzionalità |
| PSDNET-1654 | Aggiungere il supporto per i livelli di ritaglio ibridi come opzione di miscelazione dei gruppi                            | Funzionalità |
| PSDNET-1194 | Il file PSD con modalità di colore a 16 bit non applica la maschera per i livelli di regolazione                              | Errore    |
| PSDNET-1235 | Rendering non corretto delle parentesi nel livello di testo                                                                | Errore    |
| PSDNET-1559 | Impossibile aggiornare gli stili nei livelli di testo                                                                      | Errore    |
| PSDNET-1583 | Dopo l'esportazione del file PSD con CMYK i colori nel PSD esportato si rompono                                         | Errore    |
| PSDNET-1619 | Specifico file PSB genera l'eccezione "Il rettangolo non ha un'area di elaborazione comune"                                | Errore    |
| PSDNET-1648 | Caricamento dell'immagine fallito. OverflowException: L'operazione aritmetica ha comportato un overflow                     | Errore    |


## **Modifiche all'API pubblica**
# **API aggiunte:**
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


# **API rimosse:**
- Nessuna


## **Esempi d'uso:**

**PSDNET-1638. Implementare la creazione di una maschera per nuovi livelli di regolazione**

{{< highlight csharp >}}
string fileSorgente = "zendeya_BW.psd";
string fileDestinazione = "zendeya_BW_out.psd";

using (var im = (PsdImage)Image.Load(fileSorgente))
{
    im.AddBlackWhiteAdjustmentLayer();

    im.Save(fileDestinazione);
}

using (var im = (PsdImage)Image.Load(fileDestinazione))
{
    Layer layer = im.Layers[1];

    AssertAreEqual((ushort)5, layer.ChannelsCount);
    AssertAreEqual((short)-2, layer.ChannelInformation[4].ChannelID);
}

void AssertAreEqual(object atteso, object effettivo, string messaggio = null)
{
    if (!object.Equals(atteso, effettivo))
    {
        throw new Exception(messaggio ?? "Gli oggetti non sono uguali.");
    }
}
{{< /highlight >}}

**PSDNET-1654. Aggiungere il supporto per i livelli di ritaglio ibridi come opzione di miscelazione nei gruppi**

{{< highlight csharp >}}
string fileSorgente = "esempio_sorgente.psd";
string filePsdOutput = "esempio_output.psd";
string filePngOutput = "esempio_output.png";

using (var immagine = (PsdImage)Image.Load(fileSorgente))
{
    immagine.Layers[1].BlendClippedElements = false;
    immagine.Save(filePsdOutput);
    immagine.Save(filePngOutput, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1194. Il file PSD con modalità di colore a 16 bit non applica la maschera per i livelli di regolazione**

{{< highlight csharp >}}
string fileSorgente = "source.psd";
string filePngOutput = "current.png";

using (var immagine = (PsdImage)Image.Load(fileSorgente))
{
    immagine.Save(filePngOutput, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1235. Rendering non corretto delle parentesi nel livello di testo**

{{< highlight csharp >}}
string file = "file1.psd";
string output = "output_1235.png";

using (var immaginePsd = (PsdImage)Image.Load(file))
{
    foreach (var layer in immaginePsd.Layers)
    if (layer is TextLayer textLayer)
    textLayer.TextData.UpdateLayerData();

    var opzioniImmagine = new PsdOptions(immaginePsd);
    immaginePsd.Save(output, opzioniImmagine);
}
{{< /highlight >}}

**PSDNET-1559. Impossibile aggiornare gli stili nei livelli di testo**

{{< highlight csharp >}}
string fileSorgente = "Esempio_DimensioneCarattere.psd";
string fileOutput = "output_Esempio_DimensioneCarattere.psd";

using (var immaginePsd = (PsdImage)Image.Load(fileSorgente, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var l1 = (TextLayer)immaginePsd.Layers[4];
    var l2 = (TextLayer)immaginePsd.Layers[5];

    var elementiTesto1 = l1.TextData.ProducePortions(new string[] { "testo1", "testo2" }, l1.TextData.Items[0].Style, l1.TextData.Items[0].Paragraph);

    l1.TextData.RemovePortion(0);
    foreach (var elemento in elementiTesto1)
    {
        l1.TextData.AddPortion(elemento);
    }

    var elementiTesto2 = l2.TextData.ProducePortions(new string[] { "livello di testo 1", "livello di testo 22" }, l2.TextData.Items[0].Style, l2.TextData.Items[0].Paragraph);

    foreach (var elemento in elementiTesto2)
    {
        l2.TextData.AddPortion(elemento);
    }

    l1.TextData.UpdateLayerData();
    l2.TextData.UpdateLayerData();

    immaginePsd.Save(fileOutput);
}
{{< /highlight >}}

**PSDNET-1583. Dopo l'esportazione del file PSD con CMYK si rompono i colori nel PSD esportato**

{{< highlight csharp >}}
string fileSorgente = "canyon.psd";
string fileOutputPng = "output_canyon.png";

using (var flussoOutput = new MemoryStream())
{
    using (var immaginePsd = (PsdImage)Image.Load(fileSorgente))
    {
        immaginePsd.Save(flussoOutput);
    }

    flussoOutput.Position = 0;
    using (var immaginePsd = (PsdImage)Image.Load(flussoOutput))
    {
        immaginePsd.Save(fileOutputPng, new PngOptions());
    }
}
{{< /highlight >}}

**PSDNET-1619. Specifico file PSB genera l'eccezione "Il rettangolo non ha un'area di elaborazione comune"**

{{< highlight csharp >}}
var input = "1619_src.psb";
var output = "1619_output.png";
using (PsdImage img = (PsdImage)Image.Load(input, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(output,
    new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1648. Caricamento dell'immagine fallito. OverflowException: L'operazione aritmetica ha comportato un overflow**

{{< highlight csharp >}}
string fileSorgente = "9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(fileSorgente))
{
    Layer layer = im.Layers[28];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    AssertAreEqual("自定", grdmResource.GradientName);
}

void AssertAreEqual(object atteso, object effettivo, string messaggio = null)
{
    if (!object.Equals(atteso, effettivo))
    {
        throw new Exception(messaggio ?? "Gli oggetti non sono uguali.");
    }
}
{{< /highlight >}}
