---
title: Note sulla versione di Aspose.PSD per .NET 20.3
type: docs
weight: 100
url: /it/net/aspose-psd-for-net-20-3-release-notes/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-188|Supporto di .Net Core|Funzionalità|
|PSDNET-523|Converti file Adobe Illustrator in PDF|Funzionalità|
|PSDNET-212|Aggiungi la capacità di rendere diversi stili in un singolo livello di testo|Funzionalità|
|PSDNET-144|Supporto di Livello di regolazione Bianco e Nero|Funzionalità|
|PSDNET-233|Aggiungi supporto per l'esportazione del formato AI (Versione 8) in altri formati|Funzionalità|
|PSDNET-540|Supporto della modalità di blending PassThrough (Utilizzata solo per Gruppo di Livelli).|Funzionalità|
|PSDNET-539|Eccezione: Caricamento immagine non riuscito durante il caricamento dell'immagine con risorsa di nomi Unicode Alpha vuoti|Errore|
|PSDNET-541|Output incorretto dopo il cambiamento di visibilità di un LayerGroup|Errore|
|PSDNET-516|Eccezione durante il caricamento immagine PSD: la sezione del colore (Risorsa DropShadow) deve contenere 3 componenti di colore per RGB o 4 componenti di colore per CMYK|Errore|
|PSDNET-536|Eccezione se si cerca di disegnare su un livello appena creato se viene utilizzata la versione semplificata del Costruttore|Errore|

## **Modifiche all'API pubblica**
# **API aggiunte:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Sottolineatura
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Barrato
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **API rimosse:**
- Nessuna

## **Esempi di utilizzo:**
**PSDNET-523. Converti file Adobe Illustrator in PDF**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Aggiungi la capacità di rendere diversi stili in un singolo livello di testo**

{{< highlight java >}}

 string sourceFile = "text212.psd";

string ethalonFile = "Ethalon_text212.psd";

string outputFile = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(sourceFile))

{

    TextLayer textLayer = (TextLayer)img.Layers[1];

    IText textData = textLayer.TextData;

    ITextStyle defaultStyle = textData.ProducePortion().Style;

    ITextParagraph defaultParagraph = textData.ProducePortion().Paragraph;

    defaultStyle.FillColor = Color.DimGray;

    defaultStyle.FontSize = 51;

    textData.Items[1].Style.Strikethrough = true;

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Grassetto",  "Corsivo\r",  "Testo in maiuscolo" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Underline = true; // modifica stile testo "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // modifica stile testo "2\r"

    newPortions[2].Style.FauxBold = true; // modifica stile testo "Grassetto"

    newPortions[3].Style.FauxItalic = true; // modifica stile testo "Corsivo\r"

    newPortions[3].Style.BaselineShift = -25; // modifica stile testo "Corsivo\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // modifica stile testo "Testo in maiuscolo"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. Aggiungi supporto per l'esportazione del formato AI (Versione 8) in altri formati**

{{< highlight java >}}

 // Esempio di esportazione di un file AI nei formati PSD e PNG

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Supporto della modalità di blending PassThrough (Utilizzata solo per Gruppo di Livelli).**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Mela.psd";

string outputFileName = "Output" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "Non c'è il 23esimo livello.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "Il 23esimo livello non è un gruppo di livelli.");

    AssertIsTrue(layer.Name == "GruppoRegolazione", "Il nome del 23esimo livello non è 'GruppoRegolazione'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "Il livello di GruppoRegolazione dovrebbe avere la modalità di blending 'pass through'.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputMela.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normale" + outputFileName, new PsdOptions());

    image.Save("NormaleOutputMela.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. Aggiornamento del testo del livello di testo genera un'eccezione**

{{< highlight java >}}

 // L'aggiornamento del testo del livello di testo genera un'eccezione

string filePath = "RibaltamentoVerticale.psd";

string outputPath = "RibaltamentoVerticale_modificato.psd";

var nuovoTesto = "Test";

using (var image = Image.Load(filePath))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var layers = psdImage.Layers;

    for (var indice = layers.Length - 1; indice >= 0; indice--)

    {

        var livello = layers[indice] as TextLayer;

        if (livello == null)

        {

            continue;

        }

        livello.UpdateText(nuovoTesto);

    }

    var opzioniImmagine = new PsdOptions(psdImage);

    psdImage.Save(outputPath, opzioniImmagine);

}

{{< /highlight >}}

**PSDNET-182. Salvare l'immagine PSD dopo l'operazione RotateFlip produce un file corrotto che non può essere aperto.**

{{< highlight java >}}

 string nomeFileSorgente = "1.psd";

RotateFlipType tipoRibaltamento = RotateFlipType.Ruota270RibaltaXY;

string nomeFileOutputPsd = "ProvaRibaltamento2617.psd";

using (PsdImage immagine = (PsdImage)Image.Load(nomeFileSorgente))

{

    immagine.RotateFlip(tipoRibaltamento);

    immagine.Save(nomeFileOutputPsd);

}

// Dovrebbe essere eseguito senza eccezioni

using (PsdImage immagine = (PsdImage)Image.Load(nomeFileOutputPsd)) 

{

    // Non fare nulla

}

{{< /highlight >}}

**PSDNET-539. Eccezione: Caricamento immagine non riuscito durante il caricamento dell'immagine con risorsa di nomi Alpha Unicode vuoti**

{{< highlight java >}}

 string percorsoSorgente = "mela.psd";

using (var psdImage = (PsdImage)Image.Load(percorsoSorgente)) // Qui non dovremmo ottenere eccezioni

{

    // non fare nulla

}

{{< /highlight >}}

**PSDNET-541. Output incorretto dopo il cambiamento di visibilità di un LayerGroup**

{{< highlight java >}}

 string fileSorgente = "input.psd";

string fileOutput = "output.psd";

// effettua modifiche nei nomi dei livelli e salvalo

using (var immagine = (PsdImage)Image.Load(fileSorgente))

{

    for (int i = 0; i < immagine.Layers.Length; i++)

    {

        var livello = immagine.Layers[i];

        // Disattiva tutto all'interno di un gruppo

        if (livello is LayerGroup)

        {

            livello.IsVisible = false;

        }

    }

    immagine.Save(fileOutput);

}

{{< /highlight >}}

**PSDNET-516. Eccezione durante il caricamento immagine PSD: la sezione del colore (Risorsa DropShadow) deve contenere 3 componenti di colore per RGB o 4 componenti di colore per CMYK**

{{< highlight java >}}

 string fileSorgente = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(fileSorgente)) // Qui non dovremmo ottenere eccezioni

{

    // non fare nulla

}

{{< /highlight >}}

**PSDNET-536. Eccezione se si cerca di disegnare su un livello appena creato se viene utilizzata la versione semplificata del Costruttore**

{{< highlight java >}}

 string fileOutput = "output.psd";

int larghezza = 100;

int altezza = 100;

using (var immagine = new PsdImage(larghezza, altezza))

{

    var livello = new Layer();

    livello.Bottom = altezza;

    livello.Right = larghezza;

    immagine.AddLayer(livello);

    Graphics grafico = new Graphics(livello);

    grafico.Clear(Color.Yellow);

    // disegna un rettangolo con lo strumento Penna

    grafico.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // disegna un altro rettangolo con Pennello Solido in colore Blu

    grafico.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    immagine.Save(fileOutput);

}

{{< /highlight >}}

