---
title: Aspose.PSD für .NET 18.10 - Versionshinweise
type: docs
weight: 30
url: /de/net/aspose-psd-fuer-net-18-10-versionshinweise/
---

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-14|Hinzufügen der Unterstützung für Mischmodi neben Normal|Funktion|
|PSDNET-69|Hinzufügen der Unterstützung für den Farbüberlagerungseffekt|Funktion|
|PSDNET-70|Hinzufügen der Unterstützung für den Schlagschatten-Effekt|Funktion|
|PSDNET-71|Rendering für den Export des Farbüberlagerungseffekts|Funktion|
|PSDNET-72|Rendering für den Export des Schlagschatten-Effekts|Funktion|
|PSDNET-74|Unterstützung für das Hinzufügen von Ebeneneffekten zur Laufzeit|Funktion|
|PSDNET-73|Optimierung der Ladeleistung von Ressourcen, die osType-Strukturen enthalten|Fehler|
|PSDNET-79|Refactoring und Behebung von Speicherlecks in LayerAndMaskInfo|Verbesserung|

## **Beispiele zur Verwendung:**
**PSDNET-14 Hinzufügen der Unterstützung für Mischmodi neben Normal**

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

        // Export nach PNG

        var saveOptions = new PngOptions();

        saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

        var pngExportPath100 = "BlendMode" + fileName + "_Test100.png";

        im.Save(pngExportPath100, saveOptions);

        // Deckkraft auf 50% setzen

        im.Layers[1].Opacity = 127;

        var pngExportPath50 = "BlendMode" + fileName + "_Test50.png";

        im.Save(pngExportPath50, saveOptions);

    }

}

{{< /highlight >}}

**PSDNET-69 Hinzufügen der Unterstützung für den Farbüberlagerungseffekt**

{{< highlight java >}}

     // Farbüberlagerungseffekt bearbeiten

    string sourceFileName = "ColorOverlay.psd";

    string psdPathAfterChange = "ColorOverlayChanged.psd";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (Farbüberlagerung)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Farbe);

       Assert.AreEqual(153, colorOverlay.Deckkraft);

       colorOverlay.Farbe = Color.Green;

       colorOverlay.Deckkraft = 128;

       im.Save(psdPathAfterChange);

    }

{{< /highlight >}}

**PSDNET-70 Hinzufügen der Unterstützung für den Schlagschatten-Effekt**

{{< highlight java >}}

     // Schlagschatten-Effekt bearbeiten

    string sourceFileName = "Shadow.psd";

    string psdPathAfterChange = "ShadowChanged.psd";

    using (var im = LoadFile(sourceFileName))

    {

       var schattenEffekt = (SchlagschattenEffekt)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Schwarz, shadowEffect.Color);

       Assert.AreEqual(255, shadowEffect.Deckkraft);

       Assert.AreEqual(3, schattenEffekt.Entfernung);

       Assert.AreEqual(7, schattenEffekt.Größe);

       Assert.AreEqual(true, schattenEffekt.GlobalLightVerwenden);

       Assert.AreEqual(90, schattenEffekt.Winkel);

       Assert.AreEqual(0, schattenEffekt.Ausbreitung);

       Assert.AreEqual(0, schattenEffekt.Rauschen);

       shadowEffect.Color = Color.Grün;

       shadowEffect.Deckkraft = 128;

       shadowEffect.Entfernung = 11;

       shadowEffect.GlobalLightVerwenden = false;

       shadowEffect.Größe = 9;

       shadowEffect.Winkel = 45;

       shadowEffect.Ausbreitung = 3;

       shadowEffect.Rauschen = 50;

       im.Save(psdPathAfterChange);

    }

{{< /highlight >}}



**PSDNET-71 Rendering für Export des Farbüberlagerungseffekts**

{{< highlight java >}}

    // Farbüberlagerungseffekt bearbeiten

    string sourceFileName = "ColorOverlay.psd";

    string pngExportPath = "ColorOverlay.png";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (Farbüberlagerungseffekt)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Farbe);

       Assert.AreEqual(153, colorOverlay.Deckkraft);

       // PNG speichern

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-72 Rendering für Export des Schlagschatten-Effekts**

{{< highlight java >}}

     // Schlagschatten exportieren

    string sourceFileName = "Shadow.psd";

    string pngExportPath = "Shadow.png";

    using (var im = LoadFile(sourceFileName))

    {

       var shadowEffect = (SchlagschattenEffekt)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Schwarz, shadowEffect.Color);

       Assert.AreEqual(255, shadowEffect.Deckkraft);

       Assert.AreEqual(3, shadowEffect.Entfernung);

       Assert.AreEqual(7, shadowEffect.Größe);

       Assert.AreEqual(true, shadowEffect.GlobalLightVerwenden);

       Assert.AreEqual(90, shadowEffect.Winkel);

       Assert.AreEqual(0, shadowEffect.Ausbreitung);

       Assert.AreEqual(0, shadowEffect.Rauschen);

       // PNG speichern

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-74 Unterstützung für das Hinzufügen von Ebeneneffekten zur Laufzeit**

{{< highlight java >}}

     // Hinzufügen von Farbüberlagerungseffekt zur Laufzeit

    string sourceFileName = "ThreeRegularLayersWithLayerEffect.psd";

    string psdExportPath = "ThreeRegularLayersWithLayerEffectChanged.psd";

    string pngExportPath = "ThreeRegularLayersWithLayerEffectChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };



    var testFolder = String.Empty;

    var im = (PsdImage)Image.Load(testPath, loadOptions) 

    using (im)

    {

        var effect = im.Layers[1].BlendingOptions.AddColorOverlay();

        effect.Deckkraft = 128;

        effect.Farbe = Color.Grün;

        effect.Mischmodus = Normal;

        var effect = im.Layers[1].BlendingOptions.AddDropShadow();

        effect.Farbe = Color.Rot;

        effect.Deckkraft = 128;

        effect.Mischmodus = Normal;



        // PSD speichern    

        im.Save(psdExportPath);



        // PNG speichern

        var saveOptions = new PngOptions();

        im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

