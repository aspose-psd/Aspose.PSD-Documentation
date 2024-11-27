---
title: Notas de lanzamiento de Aspose.PSD para .NET 18.10
type: docs
weight: 30
url: /es/net/aspose-psd-para-net-18-10-notas-de-lanzamiento/
---

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-14|Agregar soporte de modos de mezcla además de Normal|Característica|
|PSDNET-69|Agregar soporte de efecto de superposición de color|Característica|
|PSDNET-70|Agregar soporte de efecto de sombra arrojada|Característica|
|PSDNET-71|Renderización para exportación de efecto de superposición de color|Característica|
|PSDNET-72|Renderización para exportación de efecto de sombra arrojada|Característica|
|PSDNET-74|Soporte para la adición de efectos de capa en tiempo de ejecución|Característica|
|PSDNET-73|Optimización del rendimiento de carga de recursos que contienen estructuras de osType|Error|
|PSDNET-79|Reestructuración y correcciones de fugas de memoria en LayerAndMaskInfo|Mejora|

## **Ejemplos de uso:**

**PSDNET-14 Agregar soporte de modos de mezcla además de Normal**

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

        // Exportar a PNG

        var saveOptions = new PngOptions();

        saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

        var pngExportPath100 = "BlendMode" + fileName + "_Test100.png";

        im.Save(pngExportPath100, saveOptions);

        // Establecer opacidad al 50%

        im.Layers[1].Opacity = 127;

        var pngExportPath50 = "BlendMode" + fileName + "_Test50.png";

        im.Save(pngExportPath50, saveOptions);

    }

}

{{< /highlight >}}

**PSDNET-69 Agregar soporte de efecto de superposición de color**

{{< highlight java >}}

     // Edición de efecto de superposición de color

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

**PSDNET-70 Agregar soporte de efecto de sombra arrojada**

{{< highlight java >}}

     // Edición del efecto de sombra arrojada

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

**PSDNET-71 Renderización para exportar el efecto de superposición de color**

{{< highlight java >}}

    // Edición del efecto de superposición de color

    string sourceFileName = "ColorOverlay.psd";

    string pngExportPath = "ColorOverlay.png";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlayEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       // Guardar PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-72 Renderización para exportar el efecto de sombra arrojada**

{{< highlight java >}}

     // Exportar sombra arrojada

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

       // Guardar PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-74 Soporte para la adición de efectos de capa en tiempo de ejecución**

{{< highlight java >}}

     // Agregar efecto de capa de superposición de color en tiempo de ejecución

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



        // Guardar PSD    

        im.Save(psdExportPath);



        // Guardar PNG

        var saveOptions = new PngOptions();

        im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

