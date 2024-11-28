---
title: Note sulla versione di Aspose.PSD per .NET 23.3
type: docs
weight: 100
url: /it/net/aspose-psd-per-net-23-3-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 23.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-146|Supporto del Livello di regolazione Posterize|Caratteristica|
|PSDNET-1366|Implementare il supporto di VscgResource|Caratteristica|
|PSDNET-1437|Aggiungere supporto di risorsa PostResource per i dati del Livello di regolazione Posterize|Caratteristica|
|PSDNET-931|Esportazione non corretta al livello PNG con regolazione delle Curve e modalità di colore CMYK|Errore|
|PSDNET-1403|Lo stile del Paragrafo viene perso dopo il salvataggio del file e l'aggiornamento del file da parte di PS|Errore|
|PSDNET-1453|Rendering interrotto degli effetti di bagliore e ombra sul testo|Errore|


## **Cambiamenti nell'API pubblica**
# **API aggiunte:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Angle
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.KeyForData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.TypeToolKey


# **API rimosse:**
- Nessuna


## **Esempi d'uso:**

**PSDNET-146. Supporto del Livello di regolazione Posterize**

{{< highlight csharp >}}
string fileSorgente = "zendeya_posterize.psd";
string fileOutput = "zendeya_posterize_10.psd";

using (var immagine = (PsdImage)Image.Load(fileSorgente, new PsdLoadOptions()))
{
    foreach (Layer livello in immagine.Layers)
    {
        if (livello is PosterizeLayer)
        {
            ((PosterizeLayer)livello).Levels = 10;
            immagine.Save(fileOutput);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-931. Esportazione non corretta al livello PNG con regolazione delle Curve e modalità di colore CMYK**

{{< highlight csharp >}}
string fileSrc = "input_LevelsLayerWithLayerMaskCmyk.psd";
string fileOutput = "output_LevelsLayerWithLayerMaskCmykTest.png";
string fileOutputPsd = "output.psd";

var opzioniCaricamentoPsd = new PsdLoadOptions() { LoadEffectsResource = true };
using (PsdImage immagine = (PsdImage)Image.Load(fileSrc, opzioniCaricamentoPsd))
{
    immagine.Save(fileOutputPsd, new PsdOptions()); // la ', new PsdOptions()' provoca un errore.
    immagine.Save(fileOutput, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1366. Implementare il supporto di VscgResource**

{{< highlight csharp >}}
string fileSorgente = "StrokeInternalFill_src.psd";
string fileOutput = "StrokeInternalFill_res.psd";

void AreEqual(double atteso, double attuale, double tolleranza = 0.1)
{
    if (Math.Abs(atteso - attuale) > tolleranza)
    {
        throw new Exception(
        $"I valori non sono uguali.\nAtteso: {atteso}\nRisultato: {attuale}\nDifferenza: {atteso - attuale}");
    }
}

using (PsdImage immagine = (PsdImage)Image.Load(fileSorgente))
{
    VscgResource risorsaVscg = (VscgResource)immagine.Layers[1].Resources[0];
    DescriptorStructure strutturaColoreRgb = (DescriptorStructure)risorsaVscg.Items[0];

    AreEqual(89.8, ((DoubleStructure)strutturaColoreRgb.Structures[0]).Value);
    AreEqual(219.6, ((DoubleStructure)strutturaColoreRgb.Structures[1]).Value);
    AreEqual(34.2, ((DoubleStructure)strutturaColoreRgb.Structures[2]).Value);

    ((DoubleStructure)strutturaColoreRgb.Structures[0]).Value = 255d; // Rosso
    ((DoubleStructure)strutturaColoreRgb.Structures[1]).Value = 0d; // Verde
    ((DoubleStructure)strutturaColoreRgb.Structures[2]).Value = 0d; // Blu

    immagine.Save(fileOutput);
}

// verifica delle modifiche
using (PsdImage immagine = (PsdImage)Image.Load(fileOutput))
{
    VscgResource risorsaVscg = (VscgResource)immagine.Layers[1].Resources[0];
    DescriptorStructure strutturaColoreRgb = (DescriptorStructure)risorsaVscg.Items[0];

    AreEqual(255, ((DoubleStructure)strutturaColoreRgb.Structures[0]).Value);
    AreEqual(0, ((DoubleStructure)strutturaColoreRgb.Structures[1]).Value);
    AreEqual(0, ((DoubleStructure)strutturaColoreRgb.Structures[2]).Value);
}
{{< /highlight >}}

**PSDNET-1403. Lo stile del Paragrafo viene perso dopo il salvataggio del file e l'aggiornamento del file da parte di PS**

{{< highlight csharp >}}
string fileSorgente = "PSDTest3.psd";
string fileOutput = "output.psd";

string[] nuovoTesto = new string[]
{
    "Titolo \r",
    "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui dicta minus molestiae vel beatae natus"
};

using (PsdImage immagine = (PsdImage)Aspose.PSD.Image.Load(fileSorgente))
{
    TextLayer livelloTesto = immagine.AddTextLayer("Nuovo livello", new Aspose.PSD.Rectangle(117, 150, 350, 100));
    var datiTesto = livelloTesto.TextData;

    ITextStyle stilePredefinito = datiTesto.ProducePortion().Style;

    ITextParagraph paragrafoPredefinito = datiTesto.ProducePortion().Paragraph;
    ITextPortion[] nuoveParti = datiTesto.ProducePortions(nuovoTesto, stilePredefinito, paragrafoPredefinito);

    nuoveParti[0].Style.FontSize = 14;
    nuoveParti[0].Style.FontName = "TwCenMT-Bold";

    nuoveParti[1].Style.Leading = 20;
    nuoveParti[1].Style.FontSize = 10;
    nuoveParti[1].Style.FontName = "TwCenMT-Bold";

    // Rimozione del vecchio testo
    datiTesto.RemovePortion(0);

    // Aggiunta delle nuove parti di testo
    foreach (var nuovaParte in nuoveParti)
    {
        datiTesto.AddPortion(nuovaParte);
    }

    datiTesto.UpdateLayerData();

    immagine.Save(fileOutput);
}

using (PsdImage immaginePsd = (PsdImage)Aspose.PSD.Image.Load(fileOutput))
{
    Txt2Resource risorsaTxt2Output = (Txt2Resource)immaginePsd.GlobalLayerResources[1];
    byte[] bytes = risorsaTxt2Output.Data;
    string datiTxt2 = "";
    for (int i = 18900; i < bytes.Length; i++)
    {
        datiTxt2 += (char)bytes[i];
    }

    string chiave0 = @" >> /6 0 >> >> /1 "; // prefisso alla lunghezza del paragrafo 0
    string chiave1 = @" >> /6 1 >> >> /1 "; // prefisso alla lunghezza del paragrafo 1
    int indice0 = datiTxt2.IndexOf(chiave0);
    int indice1 = datiTxt2.IndexOf(chiave1);

    string lunghezzaPar0 = datiTxt2.Substring(indice0 + chiave0.Length, 1);
    string lunghezzaPar1 = datiTxt2.Substring(indice1 + chiave1.Length, 3);

    string attesa0 = nuovoTesto[0].Length.ToString();
    string attesa1 = (nuovoTesto[1].Length + 1).ToString();

    if (lunghezzaPar0 != attesa0 || lunghezzaPar1 != attesa1)
    {
        throw new Exception(
            $"La lunghezza dei paragrafi è errata.\nAtteso: {attesa0} e {attesa1}\nRisultato: {lunghezzaPar0} e {lunghezzaPar1}\n");
    }
}
{{< /highlight >}}

**PSDNET-1437. Aggiungere supporto di risorsa PostResource per i dati del Livello di regolazione Posterize**

{{< highlight csharp >}}
string fileSorgente = "zendeya_posterize.psd";
string fileOutput = "zendeya_posterize_10.psd";

using (var immagine = (PsdImage)Image.Load(fileSorgente, new PsdLoadOptions()))
{
    Layer livello = immagine.Layers[1];

    foreach (LayerResource risorsa in livello.Resources)
    {
        if (risorsa is PostResource)
        {
            ((PostResource)risorsa).Levels = 10;
            immagine.Save(fileOutput);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-1453. Rendering interrotto degli effetti di bagliore e ombra sul testo**

{{< highlight csharp >}}
string outputPsd = "effetto_errore.psd";
string outputPng = "effetto_errore.png";

using (var immaginePsd = new PsdImage(500, 500))
{
    // Aggiungi livelli di testo
    Aspose.PSD.Rectangle areaTesto1 = new Aspose.PSD.Rectangle(50, 0, 400, 100);
    Aspose.PSD.Rectangle areaTesto2 = new Aspose.PSD.Rectangle(50, 150, 400, 100);
    Aspose.PSD.Rectangle areaTesto3 = new Aspose.PSD.Rectangle(50, 300, 400, 100);

    TextLayer livelloTesto1 = immaginePsd.AddTextLayer("Testo Con Effetti", areaTesto1);
    TextLayer livelloTesto2 = immaginePsd.AddTextLayer("Testo Con Effetti", areaTesto2);
    TextLayer livelloTesto3 = immaginePsd.AddTextLayer("Testo Con Effetti", areaTesto3);

    // Modifica dei livelli di testo
    livelloTesto1.TextData.Items[0].Style.FontSize = 150;
    livelloTesto1.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    livelloTesto1.TextData.UpdateLayerData();

    livelloTesto2.TextData.Items[0].Style.FontSize = 150;
    livelloTesto2.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    livelloTesto2.TextData.UpdateLayerData();

    livelloTesto3.TextData.Items[0].Style.FontSize = 150;
    livelloTesto3.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    livelloTesto3.TextData.UpdateLayerData();

    // Aggiungi effetti
    OuterGlowEffect bagliore = livelloTesto1.BlendingOptions.AddOuterGlow(); // interruzione
    bagliore.Spread = 15;
    ((ColorFillSettings)bagliore.FillColor).Color = Color.Red;

    var ombra = livelloTesto2.BlendingOptions.AddDropShadow(); // interruzione con testo lungo
    ombra.Distance = 25;
    ombra.Color = Color.DarkBlue;

    var ombraInterni = livelloTesto3.BlendingOptions.AddInnerShadow(); // interruzione con testo lungo
    ombraInterni.UseGlobalLight = false;
    ombraInterni.Angle = -179;
    ombraInterni.Distance = 10;
    ombraInterni.Size = 8;
    ombraInterni.Color = Color.HotPink;

    // esporta
    immaginePsd.Save(outputPsd);
    immaginePsd.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}