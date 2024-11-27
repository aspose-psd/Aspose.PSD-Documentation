---
title: Notas de lanzamiento de Aspose.PSD for .NET 18.12
type: docs
weight: 10
url: /es/net/aspose-psd-for-net-18-12-release-notes/
---

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-76|Soporte de la Capa de Trazo|Característica|
|PSDNET-83|Soporte del Efecto de Degradado|Característica|
|PSDNET-84|Soporte del Efecto de Patrón|Característica|
|PSDNET-89|Capacidad de agregar la nueva capa regular generada a PsdImage|Característica|
|PSDNET-93|Después de la actualización del contenido de la capa de texto con el carácter \ (barra invertida), el archivo resultante no se puede abrir en Photoshop|Error|
|PSDNET-39|Imágenes rotas después de la exportación con datos de imagen excesivamente grandes en Modo de Color CMYK|Error|
|PSDNET-52|Posible: La rotación en PSD no funciona|Error|
|PSDNET-88|Posible: Los métodos de recorte en Aspose.Psd no funcionan|Error|
|PSDNET-91|Aplicar cambios de Aspose.Imaging a Aspose.PSD|Mejora|

## **Cambios en la API pública**
Método    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

Clase    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Método    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Método    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Clase    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Clase    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Clase    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Clase    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

Clase    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Clase    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

Clase    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

Clase    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

Clase    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Clase    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

Clase    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

Clase    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddGradientOverlay

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddPatternOverlay

Método    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

Clase    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Settings

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.BlendMode

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.IsVisible

Propiedad    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Opacity

## **Ejemplos de uso:**
**PSDNET-76. Soporte de la Capa de Trazo**

**1) Tipo de relleno - Patrón**

{{< highlight java >}}

     // Efecto de trazo. Tipo de relleno - Patrón. Ejemplo

    string sourceFileName = "Stroke.psd";

    string exportPath = "StrokePatternChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    // Preparando nuevos datos

    var newPattern = new int[]

    {

         Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

    };

   var newPatternBounds = new Rectangle(0, 0, 4, 4);

   var guid = Guid.NewGuid();

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

         var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

         Assert.AreEqual(BlendMode.Normal, patternStroke.BlendMode);

         Assert.AreEqual(255, patternStroke.Opacity);

         Assert.AreEqual(true, patternStroke.IsVisible);

         var fillSettings = (PatternFillSettings)patternStroke.FillSettings;

         Assert.AreEqual(FillType.Pattern, fillSettings.FillType);

         patternStroke.Opacity = 127;

         patternStroke.BlendMode = BlendMode.Color;

         PattResource resource;

         foreach (var globalLayerResource in im.GlobalLayerResources)

         {

             if (globalLayerResource is PattResource)

             {

                  resource = (PattResource)globalLayerResource;

                  resource.PatternId = guid.ToString();

                  resource.Name = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";        

                  resource.SetPattern(newPattern, newPatternBounds);               

             }

         }

         ((PatternFillSettings)patternStroke.FillSettings).PatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";

         ((PatternFillSettings)patternStroke.FillSettings).PatternId = guid.ToString() + "\0";

        im.Save(exportPath);

    }

    // Archivo de prueba después de la edición

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

        var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

        PattResource resource = null;

        foreach (var globalLayerResource in im.GlobalLayerResources)

        {

            if (globalLayerResource is PattResource)

            {

                resource = (PattResource)globalLayerResource;

            }

        }

        if (resource == null)

        {

            throw new Exception("Recurso Patt no encontrado");

        }

        // Verificar los datos del patrón

        Assert.AreEqual(newPattern, resource.PatternData);

        Assert.AreEqual(newPatternBounds, new Rectangle(0, 0, resource.Width, resource.Height));

        Assert.AreEqual(guid.ToString(), resource.PatternId);

        Assert.AreEqual(BlendMode.Color, patternStroke.BlendMode);

        Assert.AreEqual(127, patternStroke.Opacity);

        Assert.AreEqual(true, patternStroke.IsVisible);

        var fillSettings = (PatternFillSettings)patternStroke.FillSettings;

        Assert.AreEqual(FillType.Pattern, fillSettings.FillType);

    }

{{< /highlight >}}

**Tipo de relleno - Degradado**

{{< highlight java >}}

     // Efecto de trazo. Tipo de relleno - Degradado. Ejemplo

    string sourceFileName = "Stroke.psd";

    string exportPath = "StrokeGradientChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

        var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Normal, gradientStroke.BlendMode);

        Assert.AreEqual(255, gradientStroke.Opacity);

        Assert.AreEqual(true, gradientStroke.IsVisible);

        var fillSettings = (GradientFillSettings)gradientStroke.FillSettings;

        Assert.AreEqual(Color.Black, fillSettings.Color);

        Assert.AreEqual(FillType.Gradient, fillSettings.FillType);

        Assert.AreEqual(true, fillSettings.AlignWithLayer);

        Assert.AreEqual(GradientType.Linear, fillSettings.GradientType);

        Assert.IsTrue(Math.Abs(90 - fillSettings.Angle) < 0.001, "El ángulo es incorrecto");

        Assert.AreEqual(false, fillSettings.Dither);

        Assert.IsTrue(Math.Abs(0 - fillSettings.HorizontalOffset) < 0.001, "La compensación horizontal es incorrecta");

        Assert.IsTrue(Math.Abs(0 - fillSettings.VerticalOffset) < 0.001, "La compensación vertical es incorrecta");

        Assert.AreEqual(false, fillSettings.Reverse);

        // Puntos de color

        var colorPoints = fillSettings.ColorPoints;

        Assert.AreEqual(2, colorPoints.Length);

        Assert.AreEqual(Color.Black, colorPoints[0].Color);

        Assert.AreEqual(0, colorPoints[0].Location);

        Assert.AreEqual(50, colorPoints[0].MedianPointLocation);

        Assert.AreEqual(Color.White, colorPoints[1].Color);

        Assert.AreEqual(4096, colorPoints[1].Location);

        Assert.AreEqual(50, colorPoints[1].MedianPointLocation);

        // Puntos de transparencia

        var transparencyPoints = fillSettings.TransparencyPoints;

        Assert.AreEqual(2, transparencyPoints.Length);

        Assert.AreEqual(0, transparencyPoints[0].Location);

        Assert.AreEqual(50, transparencyPoints[0].MedianPointLocation);

        Assert.AreEqual(100, transparencyPoints[0].Opacity);

        Assert.AreEqual(4096, transparencyPoints[1].Location);

        Assert.AreEqual(50, transparencyPoints[1].MedianPointLocation);

        Assert.AreEqual(100, transparencyPoints[1].Opacity);

        // Prueba de edición

        fillSettings.Color = Color.Green;

        gradientStroke.Opacity = 127;

        gradientStroke.BlendMode = BlendMode.Color;

        fillSettings.AlignWithLayer = false;

        fillSettings.GradientType = GradientType.Radial;

        fillSettings.Angle = 45;

        fillSettings.Dither = true;

        fillSettings.HorizontalOffset = 15;

        fillSettings.VerticalOffset = 11;

        fillSettings.Reverse = true;

        // Agregar nuevo punto de color

        var colorPoint = fillSettings.AddColorPoint();

        colorPoint.Color = Color.Green;        

        colorPoint.Location = 4096;

        colorPoint.MedianPointLocation = 75;

        // Cambiar la ubicación del punto anterior

        fillSettings.ColorPoints[1].Location = 1899;

        // Agregar nuevo punto de transparencia

        var transparencyPoint = fillSettings.AddTransparencyPoint();

        transparencyPoint.Opacity = 25;

        transparencyPoint.MedianPointLocation = 25;

        transparencyPoint.Location = 4096;

        // Cambiar la ubicación del punto de transparencia anterior

        fillSettings.TransparencyPoints[1].Location = 2411;

        im.Save(exportPath);

    }

    // Archivo de prueba después de la edición

    using (var im = (PsdImage)Image.Load(exportPath, loadOptions))

    {

        var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Color, gradientStroke.BlendMode);

        Assert.AreEqual(127, gradientStroke.Opacity);

        Assert.AreEqual(true, gradientStroke.IsVisible);

        var fillSettings = (GradientFillSettings)gradientStroke.FillSettings;

        Assert.AreEqual(Color.Green, fillSettings.Color);

        Assert.AreEqual(FillType.Gradient, fillSettings.FillType);

        // Verificar puntos de color

        Assert.AreEqual(3, fillSettings.ColorPoints.Length);

        var point = fillSettings.ColorPoints[0];

        Assert.AreEqual(50, point.MedianPointLocation);

        Assert.AreEqual(Color.Black, point.Color);

        Assert.AreEqual(0, point.Location);

        point = fillSettings.ColorPoints[1];

        Assert.AreEqual(50, point.MedianPointLocation);

        Assert.AreEqual(Color.White, point.Color);

        Assert.AreEqual(1899, point.Location);

        point = fillSettings.ColorPoints[2];

        Assert.AreEqual(75, point.MedianPointLocation);

        Assert.AreEqual(Color.Green, point.Color);

        Assert.AreEqual(4096, point.Location);

        // Verificar puntos de transparencia

        Assert.AreEqual(3, fillSettings.TransparencyPoints.Length);

        var transparencyPoint = fillSettings.TransparencyPoints[0];

        Assert.AreEqual(50, transparencyPoint.MedianPointLocation);

        Assert.AreEqual(100, transparencyPoint.Opacity);

        Assert.AreEqual(0, transparencyPoint.Location);

        transparencyPoint = fillSettings.TransparencyPoints[1];

        Assert.AreEqual(50, transparencyPoint.MedianPointLocation);

        Assert.AreEqual(100, transparencyPoint.Opacity);

        Assert.AreEqual(2411, transparencyPoint.Location);

        transparencyPoint = fillSettings.TransparencyPoints[2];

        Assert.AreEqual(25, transparencyPoint.MedianPointLocation);

        Assert.AreEqual(25, transparencyPoint.Opacity);

        Assert.assertEquals(4096, transparencyPoint.Location);

    }

{{< /highlight >}}

**Relleno de tipo - Color**

{{< highlight java >}}

   // Efecto de trazo. Relleno de tipo - Color. Ejemplo

    var sourceFileName = "Stroke.psd";

    var exportPath = "StrokeColorChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

        var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Normal, colorStroke.BlendMode);

        Assert.AreEqual(255, colorStroke.Opacity);

        Assert.AreEqual(true, colorStroke.IsVisible);                

        var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

        Assert.AreEqual(Color.Black, fillSettings.Color);

        Assert.AreEqual(FillType.Color, fillSettings.FillType);

        fillSettings.Color = Color.Yellow;

        colorStroke.Opacity = 127;

        colorStroke.BlendMode = BlendMode.Color;

        im.Save(exportPath);

    }

    // Archivo de prueba después de la edición

    using (var im = (PsdImage)Image.Load(exportPath, loadOptions))

    {

        var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Color, colorStroke.BlendMode);

        Assert.AreEqual(127, colorStroke.Opacity);

        Assert.AreEqual(true, colorStroke.IsVisible);

        var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

        Assert.AreEqual(Color.Yellow, fillSettings.Color);

        Assert.AreEqual(FillType.Color, fillSettings.FillType);

    }

{{< /highlight >}}

**PSDNET-83. Soporte del Efecto de Degradado.**

{{< highlight java >}}

 // Efecto de superposición de degradado. Ejemplo

    string sourceFileName = "GradientOverlay.psd";

    string exportPath = "GradientOverlayChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

         var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

         Assert.AreEqual(BlendMode.Normal, gradientOverlay.BlendMode);

         Assert.AreEqual(255, gradientOverlay.Opacity);

         Assert.AreEqual(true, gradientOverlay.IsVisible);

         var settings = gradientOverlay.Settings;

         Assert.AreEqual(Color.Empty, settings.Color);

         Assert.AreEqual(FillType.Gradient, settings.FillType);

         Assert.AreEqual(true, settings.AlignWithLayer);

         Assert.assertEquals(GradientType.Linear, settings.GradientType);

         Assert.assertTrue(Math.abs(33 - settings.Angle) < 0.001, "El ángulo es incorrecto");

         Assert.assertEquals(false, settings.Dither);

         Assert.assertTrue(Math.abs(129 - settings.HorizontalOffset) < 0.001, "La compensación horizontal es incorrecta");

         Assert.assertTrue(Math.abs(156 - settings.VerticalOffset) < 0.001, "La compensación vertical es incorrecta");

         Assert.assertEquals(false, settings.Reverse);

         // Puntos de color

         var colorPoints = settings.ColorPoints;

         Assert.assertEquals(3, colorPoints.Length);

         Assert.assertEquals(Color.FromArgb(9, 0, 178), colorPoints[0].Color);

         Assert.assertEquals(0, colorPoints[0].Location);

         Assert.assertEquals(50, colorPoints[0].MedianPointLocation);

         Assert.assertEquals(Color.Red, colorPoints[1].Color);

         Assert.assertEquals(2048, colorPoints[1].Location);

         Assert.assertEquals(50, colorPoints[1].MedianPointLocation);

         Assert.assertEquals(Color.FromArgb(255, 252, 0), colorPoints[2].Color);

         Assert.assertEquals(4096, colorPoints[2].Location);

         Assert.assertEquals(50, colorPoints[2].MedianPointLocation);

         // Puntos de transparencia

         var transparencyPoints = settings.TransparencyPoints;

         Assert.assertEquals(2, transparencyPoints.Length);

         Assert.assertEquals(0, transparencyPoints[0].Location);

         Assert.assertEquals(50, transparencyPoints[0].MedianPointLocation);

         Assert.assertEquals(100, transparencyPoints[0].Opacity);

         Assert.assertEquals(4096, transparencyPoints[1].Location);

         Assert.assertEquals(50, transparencyPoints[1].MedianPointLocation);

         Assert.assertEquals(100, transparencyPoints[1].Opacity);

         // Prueba de edición

         settings.Color = Color.Green;

         gradientOverlay.Opacity = 193;

         gradientOverlay.BlendMode = BlendMode.Lighten;

         settings.AlignWithLayer = false;

         settings.GradientType = GradientType.Radial;

         settings.Angle = 45;

         settings.Dither = true;

         settings.HorizontalOffset = 15;

         settings.VerticalOffset = 11;

         settings.Reverse = true;

         // Agregar nuevo punto de color

         var colorPoint = settings.AddColorPoint();

         colorPoint.Color = Color.Green;

         colorPoint.Location = 4096;

         colorPoint.MedianPointLocation = 75;

         // Cambiar la ubicación del punto anterior

         settings.ColorPoints[2].Location = 3000;

         // Agregar nuevo punto de transparencia

         var transparencyPoint = settings.AddTransparencyPoint();

         transparencyPoint.Opacity = 25;

         transparencyPoint.MedianPointLocation = 25;

         transparencyPoint.Location = 4096;

         // Cambiar la ubicación del punto de transparencia anterior

         settings.TransparencyPoints[1].Location = 2315;

         im.Save(exportPath);

    }

    // Archivo de prueba después de la edición

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

         var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

         Assert.assertEquals(BlendMode.Lighten, gradientOverlay.BlendMode);

         assert.assertEquals(193, gradientOverlay.Opacity);

         Assert.assertEquals(true, gradientOverlay.IsVisible);

         var fillSettings = gradientOverlay.Settings;

         Assert.assertEquals(Color.Empty, fillSettings.Color);

         Assert.assertEquals(FillType.Gradient, fillSettings.FillType);

         // Verificar puntos de color

         Assert.assertEquals(4, fillSettings.ColorPoints.Length);

         var point = fillSettings.ColorPoints[0];

         Assert.assertEquals(50, point.MedianPointLocation);

         Assert.assertEquals(Color.FromArgb(9, 0, 178), point.Color);

         Assert.assertEquals(0, point.Location);

         point = fillSettings.ColorPoints[1];

         Assert.assertEquals(50, point.MedianPointLocation);

         Assert.assertEquals(Color.Red, point.Color);

         Assert.assertEquals(2048, point.Location);

         point = fillSettings.ColorPoints[2];

         Assert.assertEquals(50, point.MedianPointLocation);

         Assert.assertEquals(Color.FromArgb(255, 252, 0), point.Color);

         Assert.assertEquals(3000, point.Location);

         point = fillSettings.ColorPoints[3];

         Assert.assertEquals(75, point.MedianPointLocation);

         Assert.assertEquals(Color.Green, point.Color);

         Assert.assertEquals(4096, point.Location);

         // Verificar puntos de transparencia

         Assert.assertEquals(3, fillSettings.TransparencyPoints.Length);

         var transparencyPoint = fillSettings.TransparencyPoints[0];

         Assert.assertEquals(50, transparencyPoint.MedianPointLocation);

         Assert.assertEquals(100, transparencyPoint.Opacity);

         Assert.assertEquals(0, transparencyPoint.Location);

         transparencyPoint = fillSettings.TransparencyPoints[1];

         Assert.assertEquals(50, transparencyPoint.MedianPointLocation);

         Assert.assertEquals(100, transparencyPoint.Opacity);

         Assert.assertEquals(2411, transparencyPoint.Location);

         transparencyPoint = fillSettings.TransparencyPoints[2];

         Assert.assertEquals(25, transparencyPoint.MedianPointLocation);

         Assert.assertEquals(25, transparencyPoint.Opacity);

         Assert.assertEquals(4096, transparencyPoint.Location);

    }

{{< /highlight >}}

**PSDNET-84. Soporte del Efecto de Patrón.**

{{< highlight java >}}

    // Efecto de superposición de patrón. Ejemplo

    string sourceFileName = "PatternOverlay.psd";

    string exportPath = "PatternOverlayChanged.psd";

    var newPattern = new int[]

    {

        Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

        Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

    };

    var newPatternBounds = new Rectangle(0, 0, 4, 2);

    var guid = Guid.NewGuid();

    var newPatternName = "$$$/Presets/Patterns/Pattern=Some new pattern name\0";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

        var patternOverlay = (PatternOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

        Assert.assertEquals(BlendMode.Normal, patternOverlay.BlendMode);

        Assert.assertEquals(127, patternOverlay.Opacity);

        Assert.assertEquals(true, patternOverlay.IsVisible);

        var settings = patternOverlay.Settings;

        Assert.assertEquals(Color.Empty, settings.Color);

        Assert.assertEquals(FillType.Pattern, settings.FillType);

        Assert.assertEquals("85163837-eb9e-5b43-86fb-e6d5963ea29a\0", settings.PatternId);

        Assert.assertEquals("$$$/Presets/Patterns/OpticalSquares=Optical Squares\0", settings.PatternName);

        Assert.assertEquals(null, settings.PointType);

        Assert.assertEquals(100, settings.Scale);

        Assert.assertEquals(false, settings.Linked);

        Assert.assertTrue(Math.abs(0 - settings.HorizontalOffset) < 0.001, "La compensación horizontal es incorrecta");

        Assert.assertTrue(Math.abs(0 - settings.VerticalOffset) < 0.001, "La compensación vertical es incorrecta");    

        // Prueba de edición

        settings.Color = Color.Green;

        patternOverlay.Opacity = 193;

        patternOverlay.BlendMode = BlendMode.Difference;        

        settings.HorizontalOffset = 15;

        settings.VerticalOffset = 11;

        PattResource resource;

        foreach (var globalLayerResource in im.GlobalLayerResources)

        {

            if (globalLayerResource is PattResource)

            {

                resource = (PattResource)globalLayerResource;

                resource.PatternId = guid.ToString();

                resource.Name = newPatternName;

                resource.SetPattern(newPattern, newPatternBounds);

            }

        }

        settings.PatternName = newPatternName;

        settings.PatternId = guid.ToString() + "\0";

        im.Save(exportPath);

    }

    // Archivo de prueba después de la edición

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

        var patternOverlay = (PatternOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

        Assert.assertEquals(BlendMode.Difference, patternOverlay.BlendMode);

        Assert.assertEquals(193, patternOverlay.Opacity);

        Assert.assertEquals(true, patternOverlay.IsVisible);

        var fillSettings = patternOverlay.Settings;

        Assert.assertEquals(Color.Empty, fillSettings.Color);

        Assert.assertEquals(FillType.Pattern, fillSettings.FillType);

        PattResource resource = null;

        foreach (var globalLayerResource in im.GlobalLayerResources)

        {

            if (globalLayerResource is PattResource)

            {

                resource = (PattResource)globalLayerResource;

            }

        }

        if (resource == null)

        {

            throw new Exception("Recurso Patt no encontrado");

        }

        // Verificar los datos del patrón

        Assert.assertEquals(newPattern, resource.PatternData);

        Assert.assertEquals(newPatternBounds, new Rectangle(0, 0, resource.Width, resource.Height));

        Assert.assertEquals(guid.ToString(), resource.PatternId);

    }

{{< /highlight >}}

**PSDNET-89. Capacidad de agregar la nueva capa regular generada a PsdImage.**

{{< highlight java >}}

  // Capacidad de agregar la nueva capa regular generada a PsdImage

    string sourceFileName = "OneLayer.psd";

    string exportPath = "OneLayerEdited.psd";

    string exportPathPng = "OneLayerEdited.png";

    using (var im = (PsdImage)Image.Load(sourceFileName))

    {

       // Preparando dos matrices de enteros

       var data1 = new int[2500];

       var data2 = new int[2500];

       var rect1 = new Rectangle(0, 0, 50, 50);

       var rect2 = new Rectangle(0, 0, 100, 25);

       for (int i = 0; i < 2500; i++)

       {

           data1[i] = -10000000;

           data2[i] = -10000000;

       }

       var layer1 = im.AddRegularLayer();

       layer1.Left = 25;

       layer1.Top = 25;

       layer1.Right = 75;

       layer1.Bottom = 75;

       layer1.SaveArgb32Pixels(rect1, data1);

       var layer2 = im.AddRegularLayer();

       layer2.Left = 25;

       layer2.Top = 150;

       layer2.Right = 125;

       layer2.Bottom = 175;

       layer2.SaveArgb32Pixels(rect2, data2);

       // Guardar psd

       im.Save(exportPath, new PsdOptions());

       // Guardar png

       im.Save(exportPathPng, new PngOptions());

    }

{{< /highlight >}}