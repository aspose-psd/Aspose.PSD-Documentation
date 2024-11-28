---
title: Note sulla versione di Aspose.PSD for .NET 23.2
type: docs
weight: 110
url: /it/net/aspose-psd-for-net-23-2-release-notes/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD for .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-1359|Rielaborazione del rendering del testo per migliorare il posizionamento, la resa e il supporto del testo|Miglioramento|
|PSDNET-1270|Aggiunta della capacità di elaborare l'Effetto di deformazione tramite l'API pubblica|Caratteristica|
|PSDNET-1391|Aggiunta del supporto delle modalità di leading Da fondo a fondo e Da cima a cima dalle impostazioni dei paragrafi|Caratteristica|
|PSDNET-912|Cambiare il font e il colore per il livello del testo PSD|Errore|
|PSDNET-1022|Esportazione errata del testo nel test TextUpdateTests, testo mancante|Errore|
|PSDNET-1221|Il testo extra piccolo manca dopo il ridimensionamento dell'immagine PSD più grande|Errore|
|PSDNET-1301|Aspose.Psd per .NET textLayer.UpdateText() stampa '-' (trattino) come underscore in modo casuale per diversi set di dati|Errore|
|PSDNET-1379|Le impostazioni di risoluzione non si applicano all'esportazione da PSD a PDF|Errore|


## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **API Rimosse:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manuale


## **Esempi di utilizzo:**

**PSDNET-912. Cambia il Font e il Colore per il livello del testo PSD**

{{< highlight csharp >}}
string cartellaFont = "Fonts";
string fileSorgente = "M1PDTT26052021001.psd";
string outputPsd = "risultato.psd";
string outputPng = "risultato.png";

FontSettings.SetFontsFolder(cartellaFont);

using (var immagine = (PsdImage)Image.Load(fileSorgente))
{
    TextLayer layerNome = (TextLayer)immagine.Layers[9];
    var porzioneTesto = layerNome.TextData.Items[0];

    porzioneTesto.Text = "MODESTO SR";
    porzioneTesto.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    porzioneTesto.Style.FillColor = Color.Red;

    layerNome.TextData.UpdateLayerData();

    immagine.Save(outputPsd);
    immagine.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1022. Esportazione errata del testo nel test TextUpdateTests, testo mancante**

{{< highlight csharp >}}
string fileSorgente = "ComplexKerningExample.psd";
string outputPsd = "TextUpdateComplexKerningExample_.psd";
string outputPng = "TextUpdateComplexKerningExample_.png";

using (var immagine = (PsdImage)Image.Load(fileSorgente))
{
    for (int i = 0; i < immagine.Layers.Length; i++)
    {
        var layer = immagine.Layers[i] as TextLayer;

        if (layer != null)
        {
            layer.UpdateText("Il testo è stato aggiornato");
        }
    }

    immagine.Save(outputPsd);
    immagine.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. Il testo extra piccolo manca dopo il ridimensionamento dell'immagine PSD più grande**

{{< highlight csharp >}}
string sorgente = "textTest.psd";
string output = "output.png";

using (var immaginePsd = (PsdImage)Image.Load(sorgente))
{
    immaginePsd.Resize(30, 30);

    immaginePsd.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. Aggiunta della capacità di elaborare l'Effetto di deformazione tramite l'API pubblica**

{{< highlight csharp >}}
string fileSorgente = "source.psd";
string pngDeformatoEsportazione = "deformato.png";
string psdDeformatoEsportazione = "fileDeformazione.psd";

var opzioniCaricamentoDeformazione = new PsdLoadOptions() { AllowWarpRepaint = true };

using (var immagine = (PsdImage)Image.Load(fileSorgente, opzioniCaricamentoDeformazione))
{
    immagine.Save(pngDeformatoEsportazione, new PngOptions());
    immagine.Save(psdDeformatoEsportazione, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1301. Aspose.Psd per .NET textLayer.UpdateText() stampa '-' (trattino) come underscore in modo casuale per diversi set di dati**

{{< highlight csharp >}}
string sorgente = "TEST_PSD_FILE.PSD";
string output = "IMMAGINEOUTPUT.jpg";

using (PsdImage immaginePsd = (PsdImage)Image.Load(sorgente))
{
    foreach (var layer in immaginePsd.Layers.Where(x => x.IsVisible))
    {
        if (layer is TextLayer)
        {
            TextLayer textLayer = layer as TextLayer;
            switch (layer.Name.Trim().ToUpper())
            {
                case "NOME":
                    textLayer.UpdateText("MR. JACK SMITH");
                    break;
                case "IDNO":
                    textLayer.UpdateText("OFF-022/GRP - 016");
                    break;
                case "DESIGNAZIONE":
                    textLayer.UpdateText("UFFICIALE-001");
                    break;
                case "GRUPPOSANGUIGNO":
                    textLayer.UpdateText("AB-");
                    break;
                case "INDIRIZZO":
                    textLayer.UpdateText("BLOCCO-A, STRADA-7, APP.TO N - 047, SETTORE-024");
                    break;
                case "INDIRIZZOPERM":
                    textLayer.UpdateText("CASA N - 42, VIA -025, SOCIETÀ DI VISTA VERDE PALM, SETTORE - 45");
                    break;
            }
        }
    }

    immaginePsd.Save(output, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1379. Le ResolutionSettings non si applicano all'esportazione da PSD a PDF**

{{< highlight csharp >}}
string input = "Datensatz 1.psd";
string output = "Datensatz 1.pdf";

using (var immagine = Image.Load(input, new PsdLoadOptions()))
{
    ResolutionSetting impostazioneRisoluzione = new ResolutionSetting(300, 300);

    immagine.Save(output, new PdfOptions()
    {
        ResolutionSettings = impostazioneRisoluzione
    });
}
{{< /highlight >}}

**PSDNET-1391. Aggiunta del supporto delle modalità di leading Da fondo a fondo e Da cima a cima dalle impostazioni dei paragrafi**

{{< highlight csharp >}}
string input = "leadingMode.psd";
string output = "output_leadingMode.png";

using (var immaginePsd = (PsdImage)Image.Load(input, new PsdLoadOptions()))
{
    IText testo1 = ((TextLayer)immaginePsd.Layers[1]).TextData;
    foreach (var porzioneTesto in testo1.Items)
    {
        porzioneTesto.Paragraph.LeadingType = LeadingType.TopToTop; // Cambia il valore LeadingType   
    }
    testo1.Items[8].Text = "Da cima a cima";
    testo1.Items[8].Style.FillColor = Color.ForestGreen;
    testo1.UpdateLayerData();

    IText testo2 = ((TextLayer)immaginePsd.Layers[2]).TextData;
    foreach (var porzioneTesto in testo2.Items)
    {
        porzioneTesto.Paragraph.LeadingType = LeadingType.BottomToBottom; // Cambia il valore LeadingType   
    }
    testo2.Items[8].Text = "Da fondo a fondo";
    testo2.Items[8].Style.FillColor = Color.ForestGreen;
    testo2.UpdateLayerData();

    immaginePsd.Save(output, new PngOptions());
}
{{< /highlight >}}
