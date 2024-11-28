---
title: Note sulla versione di Aspose.PSD per .NET 22.10
type: docs
weight: 30
url: /it/net/aspose-psd-per-net-22-10-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Questa versione ha una regressione nel caso delle esportazioni a 16 bit, quindi raccomandiamo cautela nell'utilizzo di questa funzionalità in questa release.
Si prega di non aggiornare Aspose.PSD alla versione 22.9-22.10 se l'elaborazione di immagini a 16 bit è la tua funzionalità principale.

Stiamo lavorando a soluzioni per questi problemi.

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-1287|Rimuovere le proprietà obsolete in Lfx2Resource|Miglioramento|
|PSDNET-1071|Aspose.PSD non riesce ad aprire PSD (RGB/16bit) con compressione ZipWithoutPrediction|Bug|
|PSDNET-1257|Gli effetti della timeline scompaiono e vengono visualizzati in modo strano. (in Photoshop)|Bug|
|PSDNET-1278|La trasparenza non funziona per l'effetto Stroke con Posizione Interna|Bug|
|PSDNET-1279|Regressione: Errore nell'apertura del file PSD|Bug|
|PSDNET-1284|L'aggiornamento del testo fallisce con alcuni simboli asiatici. Errore con l'analisi di simboli specifici|Bug|
|PSDNET-1291|L'aggiornamento del testo fallisce con alcuni simboli asiatici. Errore nella rappresentazione di simboli specifici|Bug|
|PSDNET-1292|Errore nell'apertura del file esportato da Photoshop dopo il salvataggio di simboli asiatici specifici|Bug|


## **Modifiche all'API pubblica**
# **API aggiunte:**
- Nessuna


# **API rimosse:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Esempi di utilizzo:**

**PSDNET-1071. Aspose.PSD non riesce ad aprire PSD (RGB/16bit) con compressione ZipWithoutPrediction**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Gli effetti della timeline scompaiono e vengono visualizzati in modo strano. (in Photoshop)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Crea una timeline con pochi frame.
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    List<Frame> frames = new List<Frame>(timeLine.Frames);
    for (int i = 0; i < 3; i++)
    {
        frames.Add(new Frame(timeLine));
    }
    timeLine.Frames = frames.ToArray();

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddColorOverlay();

    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.AddGradientOverlay();
    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1278. La trasparenza non funziona per l'effetto Stroke con Posizione Interna**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Regressione: Errore nell'apertura del file PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. L'aggiornamento del testo fallisce con alcuni simboli asiatici. Errore con l'analisi di simboli specifici**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // seleziona il simbolo problematico

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Rimuovere le proprietà obsolete in Lfx2Resource**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // Aggiorna l'opzione BlendMode dell'effetto
    effect.BlendMode = BlendMode.Darken;

    // Aggiorna l'opzione di Opacity dell'effetto
    effect.Opacity = 128; // 50%

    // Aggiorna l'opzione di riempimento del colore dell'effetto stroke
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. L'aggiornamento del testo fallisce con alcuni simboli asiatici. Errore nel rendering di simboli specifici**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // seleziona i simboli problematici

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. Errore nell'apertura del file esportato da Photoshop dopo il salvataggio di simboli asiatici specifici**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

string srcFile = "TestFileForAsianCharsBig 2.psd";
string outFile = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);

    image.Save(outFile);
}
{{< /highlight >}}
