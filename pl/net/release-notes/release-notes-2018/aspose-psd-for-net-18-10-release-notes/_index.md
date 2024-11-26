---
title: Aspose.PSD dla .NET 18.10 - Informacje o wersji
type: docs
weight: 30
url: /pl/net/aspose-psd-dla-net-18-10-informacje-o-wersji/
---

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-14|Dodano obsługę trybów mieszania oprócz Normalnego|Funkcja|
|PSDNET-69|Dodano obsługę efektu Nakładanie Koloru|Funkcja|
|PSDNET-70|Dodano obsługę efektu Cień|Funkcja|
|PSDNET-71|Rdzenie dla eksportu efektu Nakładanie Koloru|Funkcja|
|PSDNET-72|Rdzenie dla eksportu efektu Cień|Funkcja|
|PSDNET-74|Wsparcie dla dodawania Efektów Warstwy w czasie wykonania|Funkcja|
|PSDNET-73|Optymalizacja wydajności wczytywania zasobów zawierających struktury osType|Błąd|
|PSDNET-79|Udoskonalenia i naprawy wycieków pamięci w LayerAndMaskInfo|Zwiększenie|

## **Przykłady użycia:**
**PSDNET-14 Dodano obsługę trybów mieszania oprócz Normalnego**

{{< highlight java >}}

 var files = new string[]

{

    "Normal",

    "Dissolve",

    "Darken",

    "Multiply",

    "ColorBurn",

    "LinearBurn",

    "DarkerColor",

    "Lighten",

    "Screen",

    "ColorDodge",

    "LinearDodgeAdd",

    "LightenColor",

    "Overlay",

    "SoftLight",

    "HardLight",

    "VividLight",

    "LinearLight",

    "PinLight",

    "HardMix",

    "Difference",

    "Exclusion",

    "Subtract",

    "Divide",

    "Hue",

    "Saturation",

    "Color",

    "Luminosity",

};

foreach (var fileName in files)

{

    using (var im = LoadFile(fileName + ".psd"))

    {

        // Eksportowanie do formatu PNG

        var saveOptions = new PngOptions();

        saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

        var pngExportPath100 = "BlendMode" + fileName + "_Test100.png";

        im.Save(pngExportPath100, saveOptions);

        // Ustawienie przezroczystości na 50%

        im.Layers[1].Opacity = 127;

        var pngExportPath50 = "BlendMode" + fileName + "_Test50.png";

        im.Save(pngExportPath50, saveOptions);

    }

}

{{< /highlight >}}

**PSDNET-69 Dodano obsługę efektu Nakładanie Koloru**

{{< highlight java >}}

     // Edytowanie efektu Nakładanie Koloru

    string sourceFileName = "ColorOverlay.psd";

    string psdPathAfterChange = "ColorOverlayChanged.psd";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlay)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       colorOverlay.Color = Color.Green;

       colorOverlay.Opacity = 128;

       im.Save(psdPathAfterChange);

    }

{{< /highlight >}}

**PSDNET-70 Dodano obsługę efektu Cień**

{{< highlight java >}}

     // Edytowanie efektu Cienia

    string sourceFileName = "Shadow.psd";

    string psdPathAfterChange = "ShadowChanged.psd";

    using (var im = LoadFile(sourceFileName))

    {

       var shadowEffect = (DropShadowEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Black, shadowEffect.Color);

       Assert.AreEqual(255, shadowEffect.Opacity);

       Assert.AreEqual(3, shadowEffect.Distance);

       Assert.AreEqual(7, shadowEffect.Size);

       Assert.AreEqual(true, shadowEffect.UseGlobalLight);

       Assert.AreEqual(90, shadowEffect.Angle);

       Assert.AreEqual(0, shadowEffect.Spread);

       Assert.AreEqual(0, shadowEffect.Noise);

       shadowEffect.Color = Color.Green;

       shadowEffect.Opacity = 128;

       shadowEffect.Distance = 11;

       shadowEffect.UseGlobalLight = false;

       shadowEffect.Size = 9;

       shadowEffect.Angle = 45;

       shadowEffect.Spread = 3;

       shadowEffect.Noise = 50;

       im.Save(psdPathAfterChange);

    }

{{< /highlight >}}



**PSDNET-71 Rdzenie dla eksportu efektu Nakładanie Koloru**

{{< highlight java >}}

    // Edytowanie efektu Nakładanie Koloru

    string sourceFileName = "ColorOverlay.psd";

    string pngExportPath = "ColorOverlay.png";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlayEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       // Zapisz do PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-72 Rdzenie dla eksportu efektu Cień**

{{< highlight java >}}

     // Eksport efektu Cienia

    string sourceFileName = "Shadow.psd";

    string pngExportPath = "Shadow.png";

    using (var im = LoadFile(sourceFileName))

    {

       var shadowEffect = (DropShadowEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Black, shadowEffect.Color);

       Assert.AreEqual(255, shadowEffect.Opacity);

       Assert.AreEqual(3, shadowEffect.Distance);

       Assert.AreEqual(7, shadowEffect.Size);

       Assert.AreEqual(true, shadowEffect.UseGlobalLight);

       Assert.AreEqual(90, shadowEffect.Angle);

       Assert.AreEqual(0, shadowEffect.Spread);

       Assert.AreEqual(0, shadowEffect.Noise);

       // Zapisz do PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-74 Wsparcie dla dodawania Efektów Warstwy w czasie wykonania**

{{< highlight java >}}

     // Dodanie efektu nakładania koloru warstwy w czasie wykonania

    string sourceFileName = "ThreeRegularLayersWithLayerEffect.psd";

    string psdExportPath = "ThreeRegularLayersWithLayerEffectChanged.psd";

    string pngExportPath = "ThreeRegularLayersWithLayerEffectChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };



    var testFolder = string.Empty;

    var im = (PsdImage)Image.Load(testPath, loadOptions) 

    using (im)

    {

        var effect = im.Layers[1].BlendingOptions.AddColorOverlay();

        effect.Opacity = 128;

        effect.Color = Color.Green;

        effect.BlendMode = BlendMode.Normal;

        var effect = im.Layers[1].BlendingOptions.AddDropShadow();

        effect.Color = Color.Red;

        effect.Opacity = 128;

        effect.BlendMode = BlendMode.Normal;



        // Zapisz PSD    

        im.Save(psdExportPath);



        // Zapisz PNG

        var saveOptions = new PngOptions();

        im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

