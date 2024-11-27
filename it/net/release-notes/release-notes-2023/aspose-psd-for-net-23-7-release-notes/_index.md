---
title: Note sulla versione di rilascio di Aspose.PSD per .NET 23.7
type: docs
weight: 60
url: /it/net/aspose-psd-for-net-23-7-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chiave**   | **Sommario**                                                                                              | **Categoria** |
|:------------|:-----------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-802  | Aggiunta la capacità di esportare ogni livello del file PSD in un file GIF animato                            | Funzionalità |
| PSDNET-1441 | Assegna la proprietà Fill dello strato di forma dalla risorsa vscg                                            | Funzionalità |
| PSDNET-1534 | Aggiunti nuovi tipi di deformazione (arco e arch)                                                            | Funzionalità |
| PSDNET-1543 | Cambia l'applicazione che salva il file PSD in Aspose.PSD se la proprietà UpdateMetadata è impostata su true  | Funzionalità |
| PSDNET-1567 | Aumenta l'area di calcolo dell'immagine deformata                                                             | Funzionalità |
| PSDNET-1471 | Il livello di regolazione bianco e nero processa l'effetto di semitrasparenza in modo errato                 | Bug     |
| PSDNET-1505 | SmartObject ReplaceContents (quando l'opzione AllowWarpRepaint è attiva) si interrompe dopo 2 minuti di calcolo | Bug     |
| PSDNET-1585 | Aggiunta la capacità di ottenere la vera posizione a sinistra e in alto del Gruppo di Livelli                | Bug     |
| PSDNET-1589 | Il ridimensionamento dello strato funziona in modo errato quando il file PSD contiene VogkResource con strutture in punti | Bug     |
| PSDNET-1608 | TextBound non funziona come previsto                                                                         | Bug     |
| PSDNET-1612 | Aggiungere uno strato creato con il costruttore predefinito all'immagine PSD non aggiunge le risorse predefinite | Bug     |
| PSDNET-1623 | Timeline.LoopesCount è ignorato durante l'esportazione in GIF animato                                      | Bug     |


## **Modifiche API pubbliche**
# **API aggiunte:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **API rimosse:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **Esempi di utilizzo:**

**PSDNET-802. Aggiungi la capacità di esportare ogni livello del file PSD in un file GIF animato**

{{< highlight csharp >}}
string src = "EachLayerIsFrame.psd";
string outputGif = "out_EachLayerIsFrame.gif";
string outputPsd = "out_EachLayerIsFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // Crea frame per ogni livello.
    int framesCount = psdImage.Layers.Length;
    var timeline = psdImage.Timeline;

    Frame[] frames = new Frame[framesCount];
    for (int i = 0; i < framesCount; i++)
    {
        frames[i] = new Frame();
        LayerState[] layerStates = new LayerState[framesCount];

        for (int j = 0; j < framesCount; j++)
        {
            layerStates[j] = new LayerState();
            layerStates[j].Enabled = i == j;
        }

        frames[i].LayerStates = layerStates;
    }

    timeline.Frames = frames;

    // Aggiorna gli stati correnti
    Layer[] layers = psdImage.Layers;
    LayerState[] states = timeline.Frames[timeline.ActiveFrameIndex].LayerStates;
    for (int i = 0; i < framesCount; i++)
    {
        layers[i].IsVisible = states[i].Enabled;
    }

    timeline.Save(outputGif, new GifOptions());
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1441. Assegna la proprietà Fill dello strato di forma dalla risorsa vscg**

{{< highlight csharp >}}
string srcFile = "ShapeInternalSolid.psd";
string outFile = "ShapeInternalSolid.psd.out.psd";

using (PsdImage image = (PsdImage)Image.Load(
    srcFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    fillSettings.Color = Color.Red;

    shapeLayer.Update();

    image.Save(outFile);
}

// Verifica le modifiche salvate
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;

    AssertAreEqual(Color.Red, fillSettings.Color);

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Gli oggetti non sono uguali.");
    }
}
{{< /highlight >}}

**PSDNET-1471. Il livello di regolazione bianco e nero processa l'effetto di semitrasparenza in modo errato**

{{< highlight csharp >}}
string srcFile = "frog_nosymb.psd";
string outFile = "frog_nosymb.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddBlackWhiteAdjustmentLayer();
    psdImage.Save(outFile);
}

// Verifica le modifiche salvate
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer)image.Layers[1];

    if (blackWhiteAdjustmentLayer == null)
    {
        throw new Exception("Lo strato 2 dovrebbe essere BlackWhiteAdjustmentLayer");
    }

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Gli oggetti non sono uguali.");
    }
}
{{< /highlight >}}

**PSDNET-1505. SmartObject ReplaceContents (quando l'opzione AllowWarpRepaint è attiva) si interrompe dopo 2 minuti di calcolo**

{{< highlight csharp >}}
string sourceFile = "mug 4.psd";
string changeFile = "artwork for replace.png";
string outputFile = "export.png";

int newHeight = 300;

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    SmartObjectLayer smartObjectLayer = (SmartObjectLayer)psdImage.Layers[3];

    var scale = (double)newHeight / smartObjectLayer.Height;
    var newWidth = (int)Math.Round(smartObjectLayer.Width * scale);

    PsdImage innerImage = new PsdImage(newWidth, newHeight);
    innerImage.SetResolution(72, 72);

    Stream innerStream = new FileStream(changeFile, FileMode.Open);
    Layer layer = new Layer(innerStream) { HorizontalResolution = 72, VerticalResolution = 72 };
    try
    {
        innerImage.AddLayer(layer);

        smartObjectLayer.ReplaceContents(innerImage);
        smartObjectLayer.UpdateModifiedContent();

        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
    finally
    {
        innerImage.Dispose();
        innerStream.Dispose();
        layer.Dispose();
    }
}
{{< /highlight >}}

**PSDNET-1534. Aggiunta nuovi tipi di deformazione (arco e arch)**

{{< highlight csharp >}}
string sourceArcFile = "arc_warp.psd";
string outputArcFile = "arc_export.png";

string sourceArchFile = "arch_warp.psd";
string outputArchFile = "arch_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceArcFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArcFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}

using (var psdImage = (PsdImage)Image.Load(sourceArchFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArchFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1543. Cambia l'applicazione che salva il file PSD in Aspose.PSD se la proprietà UpdateMetadata è impostata su true**

{{< highlight csharp >}}
string path = "output.psd";
using (var image = new PsdImage(100, 100))
{
    // Se si desidera modificare il creatore dell'immagine, assicurarsi che la proprietà "UpdateMetadata" sia impostata su true. Di default è impostata su true.
    var psdOptions = new PsdOptions();
    psdOptions.UpdateMetadata = true;

    // Salvataggio dell'immagine. 
    image.Save(path, psdOptions);

    // Controllo del creatore dell'immagine nel codice.
    var xmpData = image.XmpData;
    var basicPackage = image.XmpData.GetPackage(Namespaces.XmpBasic);

    // Qui verranno aggiornate le informazioni sul creatore dell'immagine.
    var currentCreatorTool = (string)basicPackage[":CreatorTool"];
}
{{< /highlight >}}

**PSDNET-1567. Aumenta l'area di calcolo dell'immagine deformata**

{{< highlight csharp >}}
string sourceFile = "mug4_warp.psd";
string outputFile = "mug4_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1585. Aggiunta la capacità di ottenere la vera posizione sinistra e in alto del Gruppo di Livelli**

{{< highlight csharp >}}
string sourceFile = "layerGroupFigures.psd";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Gli oggetti non sono uguali.");
    }
}

using (var image = (PsdImage)Image.Load(sourceFile))
{
    var layers = image.Layers;

    for (int i = 0; i < layers.Length; i++)
    {
        var layer = layers[i];

        if (layer is LayerGroup)
        {
            // Ottenere il LayerGroup.
            var group = (LayerGroup)layer;

            var expectedLeft = int.MaxValue;
            var expectedTop = int.MaxValue;
            var expectedRight = 0;
            var expectedBottom = 0;

            // Calcolo delle vere posizioni a sinistra, in alto, a destra e in basso.
            foreach (var innerLayer in group.Layers)
            {
                if (innerLayer is AdjustmentLayer || innerLayer.Bounds.IsEmpty)
                {
                    continue;
                }

                expectedLeft = Math.Min(expectedLeft, innerLayer.Left);
                expectedTop = Math.Min(expectedTop, innerLayer.Top);
                expectedRight = Math.Max((expectedLeft + group.Width), (innerLayer.Left + innerLayer.Width));
                expectedBottom = Math.Max((expectedTop + group.Height), (innerLayer.Top + innerLayer.Height));
            }

            // Le posizioni Left, Top, Right e Bottom del LayerGroup sono calcolate correttamente ora.
            AssertAreEqual(group.Left, expectedLeft);
            AssertAreEqual(group.Top, expectedTop);
            AssertAreEqual(group.Right, expectedRight);
            AssertAreEqual(group.Bottom, expectedBottom);
        }
    }
}
{{< /highlight >}}

**PSDNET-1589. Il ridimensionamento dello strato funziona in modo errato quando il file PSD contiene VogkResource con strutture in punti**

{{< highlight csharp >}}
string[] sourceFiles = new string[]
{
    "PointsVectorOrigin.psd",
    "TopVogkResStruct.psd"
};

foreach (string sourceFile in sourceFiles)
{
    using (PsdImage image = (PsdImage)Image.Load(sourceFile))
    {
        Layer layer = image.Layers[0];

        layer.Resize(50, 50);

        AssertAreEqual(layer.Height, 50);
        AssertAreEqual(layer.Width, 50);
    }
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Gli oggetti non sono uguali.");
    }
}
{{< /highlight >}}

**PSDNET-1608. TextBound non funziona come previsto**

{{< highlight csharp >}}
string sourceFile = "input_Test_forTicket.psd";
string outFile = "out_1608.psd";

Size newTextBox = new Size(-1, -1);
using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    //Passo: Sostituisci testo
    TextLayer textLayer = (TextLayer)psdImage.Layers[3];
    textLayer.TextData.Items[0].Text = "Testo di prova sostituito";

    //Passo: Aggiorna TextBoundBox
    textLayer.TextData.UpdateLayerData();
    newTextBox = new Size((int)Math.Ceiling(textLayer.TextBoundBox.Width), textLayer.Height);

    textLayer.TextBoundBox = new Aspose.PSD.RectangleF(PointF.Empty, newTextBox);
    textLayer.TextData.UpdateLayerData();

    psdImage.Save(outFile);
}

// Verifica le modifiche
using (var psdImage = (PsdImage)Image.Load(outFile))
{
    Txt2Resource txt2Resource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    string textData = Encoding.GetEncoding("Windows-1251").GetString(txt2Resource.Data);

    string search = "<< /0 << /1 << /0 ["; // set di caratteri specifico per trovare il valore della casella di testo in questo file.

    int startIndex = textData.IndexOf(search) + search.Length;
    int endIndex = textData.IndexOf("]", startIndex);
    string boxItems = textData.Substring(startIndex, endIndex - startIndex);

    string height = newTextBox.Height.ToString("0.0####").Replace(",", ".");
    string width = newTextBox.Width.ToString("0.0####").Replace(",", ".");

    if (!boxItems.Contains(height) || !boxItems.Contains(width))
    {
        throw new Exception("La casella di testo non è stata aggiornata.");
    }
}
{{< /highlight >}}

**PSDNET-1612. Aggiungere uno strato creato con il costruttore predefinito all'immagine PSD non aggiunge le risorse predefinite**

{{< highlight csharp >}}
string output = "newLayer.psd";

using (var psdImage = new PsdImage(500, 500))
{
    var layer = new Layer();
    psdImage.AddLayer(layer);

    LyidResource lyidResource = (LyidResource)FindResource(LyidResource.TypeToolKey, layer.Resources);

    int layerId = lyidResource.Value; // Lanciava NullReferenceException

    psdImage.Save(output);
}
    
LayerResource FindResource(int resType, LayerResource[] resources)
{
    if (resources != null)
    {
        foreach (var layerResource in resources)
        {
            if (layerResource.Key == resType)
            {
                return layerResource;
            }
        }
    }

    return null;
}
{{< /highlight >}}

**PSDNET-1623. Timeline.LoopesCount è ignorato durante l'esportazione in GIF animato**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputGif = "out_4_animated.psd.gif";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    psdImage.Timeline.Save(outputGif, new GifOptions());
}
{{< /highlight >}} 