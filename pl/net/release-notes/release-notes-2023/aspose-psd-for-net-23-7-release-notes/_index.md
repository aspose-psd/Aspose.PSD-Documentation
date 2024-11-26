---
title: Notatki wydania Aspose.PSD dla .NET 23.7
type: docs
weight: 60
url: /pl/net/aspose-psd-dla-net-23-7-notatki-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                                                           | **Kategoria** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-802  | Dodaj możliwość eksportowania każdej warstwy pliku PSD do pliku animowanego Gif                           | Funkcja |
| PSDNET-1441 | Przypisz właściwość wypełnienia warstwy kształtu z zasobu Vscg                                                | Funkcja |
| PSDNET-1534 | Dodaj nowe typy obwiedni (łuk & arch)                                                                       | Funkcja |
| PSDNET-1543 | Zmień aplikację zapisującą plik PSD na Aspose.PSD, jeśli właściwość UpdateMetadata jest ustawiona na true     | Funkcja |
| PSDNET-1567 | Zwiększ obszar obliczeń obrazu obwiedniowego                                                                | Funkcja |
| PSDNET-1471 | Warstwa dostosowania czerni i bieli źle przetwarza połprzezroczystość                                        | Błąd     |
| PSDNET-1505 | SmartObject ReplaceContents (gdy aktywna jest opcja AllowWarpRepaint) przestaje działać po 2 minutach obliczeń | Błąd     |
| PSDNET-1585 | Dodaj możliwość uzyskania rzeczywistej pozycji lewej i górnej warstwy grupy                                  | Błąd     |
| PSDNET-1589 | Zmiana rozmiaru warstwy działa źle, gdy plik psd zawiera zasób VogkResource z konstrukcjami w punktach        | Błąd     |
| PSDNET-1608 | TextBound nie działa zgodnie z oczekiwaniami                                                                | Błąd     |
| PSDNET-1612 | Dodanie warstwy utworzonej za pomocą konstruktora domyślnego do obrazu PSD nie dodaje do niej domyślnych zasobów | Błąd     |
| PSDNET-1623 | Wartość Timeline.LoopesCount jest ignorowana podczas eksportowania do animowanego GIF                       | Błąd     |


## **Zmiany w API publicznym**
# **Dodane API:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **Usunięte API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **Przykłady użycia:**

**PSDNET-802. Dodaj możliwość eksportowania każdej warstwy pliku PSD do pliku Gif**

{{< highlight csharp >}}
string src = "EachLayerIsFrame.psd";
string outputGif = "out_EachLayerIsFrame.gif";
string outputPsd = "out_EachLayerIsFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // Utwórz ramki dla każdej warstwy.
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

    // Zaktualizuj bieżące stany
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

**PSDNET-1441. Przypisz właściwość wypełnienia warstwy kształtu z zasobu vscg**

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

// Sprawdź zapisane zmiany
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
        throw new Exception(message ?? "Obiekty nie są równe.");
    }
}
{{< /highlight >}}

**PSDNET-1471. Warstwa dostosowania czerni i bieli źle przetwarza połprzezroczystość**

{{< highlight csharp >}}
string srcFile = "frog_nosymb.psd";
string outFile = "frog_nosymb.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddBlackWhiteAdjustmentLayer();
    psdImage.Save(outFile);
}

// Sprawdź zapisane zmiany
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer)image.Layers[1];

    if (blackWhiteAdjustmentLayer == null)
    {
        throw new Exception("Warstwa 2 powinna być warstwą dostosowania czerni i bieli");
    }

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Obiekty nie są równe.");
    }
}
{{< /highlight >}}

**PSDNET-1505. SmartObject ReplaceContents (gdy aktywna jest opcja AllowWarpRepaint) przestaje działać po 2 minutach obliczeń**

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

**PSDNET-1534. Dodaj nowe typy obwiedni (łuk & arch)**

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

**PSDNET-1543. Zmień aplikację zapisującą plik PSD na Aspose.PSD, jeśli właściwość UpdateMetadata jest ustawiona na true**

{{< highlight csharp >}}
string path = "output.psd";
using (var image = new PsdImage(100, 100))
{
    // Jeśli chcesz zmienić narzędzie twórcy, upewnij się, że właściwość "UpdateMetadata" jest ustawiona na true. Jest ona domyślnie ustawiona na true.
    var psdOptions = new PsdOptions();
    psdOptions.UpdateMetadata = true;

    // Zapisz obraz. 
    image.Save(path, psdOptions);

    // Sprawdź narzędzie twórcy w kodzie.
    var xmpData = image.XmpData;
    var basicPackage = image.XmpData.GetPackage(Namespaces.XmpBasic);

    // Tutaj zostanie zaktualizowane info o narzędziu twórcy.
    var currentCreatorTool = (string)basicPackage[":CreatorTool"];
}
{{< /highlight >}}

**PSDNET-1567. Zwiększ obszar obliczeń obrazu obwiedniowego**

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

**PSDNET-1585. Dodaj możliwość uzyskania prawdziwej pozycji lewej i górnej warstwy grupowej**

{{< highlight csharp >}}
string sourceFile = "layerGroupFigures.psd";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Obiekty nie są równe.");
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
            // Pobierz LayerGroup
            var group = (LayerGroup)layer;

            var expectedLeft = int.MaxValue;
            var expectedTop = int.MaxValue;
            var expectedRight = 0;
            var expectedBottom = 0;

            // Oblicz pozycje lewej, górnej, prawej i dolnej
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

            // Pozycje lewej, górnej, prawej i dolnej warstwy grupowej zostały poprawnie obliczone
            AssertAreEqual(group.Left, expectedLeft);
            AssertAreEqual(group.Top, expectedTop);
            AssertAreEqual(group.Right, expectedRight);
            AssertAreEqual(group.Bottom, expectedBottom);
        }
    }
}
{{< /highlight >}}

**PSDNET-1589. Zmiana rozmiaru warstwy działa źle, gdy plik psd zawiera zasób VogkResource z konstrukcjami w punktach**

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
        throw new Exception(message ?? "Obiekty nie są równe.");
    }
}
{{< /highlight >}}

**PSDNET-1608. TextBound nie działa zgodnie z oczekiwaniami**

{{< highlight csharp >}}
string sourceFile = "input_Test_forTicket.psd";
string outFile = "out_1608.psd";

Size newTextBox = new Size(-1, -1);
using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    // Zastąp tekst
    TextLayer textLayer = (TextLayer)psdImage.Layers[3];
    textLayer.TextData.Items[0].Text = "Tekst testowy zastąpiony";

    // Zaktualizuj TextBoundBox
    textLayer.TextData.UpdateLayerData();
    newTextBox = new Size((int)Math.Ceiling(textLayer.TextBoundBox.Width), textLayer.Height);

    textLayer.TextBoundBox = new Aspose.PSD.RectangleF(PointF.Empty, newTextBox);
    textLayer.TextData.UpdateLayerData();

    psdImage.Save(outFile);
}

// Sprawdź zmiany
using (var psdImage = (PsdImage)Image.Load(outFile))
{
    Txt2Resource txt2Resource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    string textData = Encoding.GetEncoding("Windows-1251").GetString(txt2Resource.Data);

    string search = "<< /0 << /1 << /0 ["; // specyficzny zestaw znaków do znalezienia wartości pola textBox w tym pliku.

    int startIndex = textData.IndexOf(search) + search.Length;
    int endIndex = textData.IndexOf("]", startIndex);
    string boxItems = textData.Substring(startIndex, endIndex - startIndex);

    string height = newTextBox.Height.ToString("0.0####").Replace(",", ".");
    string width = newTextBox.Width.ToString("0.0####").Replace(",", ".");

    if (!boxItems.Contains(height) || !boxItems.Contains(width))
    {
        throw new Exception("TextBox nie został zaktualizowany.");
    }
}
{{< /highlight >}}

**PSDNET-1612. Dodanie warstwy utworzonej za pomocą konstruktora domyślnego do obrazu PSD nie dodaje do niej domyślnych zasobów**

{{< highlight csharp >}}
string output = "newLayer.psd";

using (var psdImage = new PsdImage(500, 500))
{
    var layer = new Layer();
    psdImage.AddLayer(layer);

    LyidResource lyidResource = (LyidResource)FindResource(LyidResource.TypeToolKey, layer.Resources);

    int layerId = lyidResource.Value;

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

**PSDNET-1623. Wartość Timeline.LoopesCount jest ignorowana podczas eksportowania do animowanego GIF**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputGif = "out_4_animated.psd.gif";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
