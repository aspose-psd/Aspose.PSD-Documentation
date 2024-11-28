---
title: Aspose.PSD für .NET 18.12 - Versionshinweise
type: docs
weight: 10
url: /de/net/aspose-psd-für-net-18-12-release-notes/
---

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-76|Unterstützung der Strichlayer|Feature|
|PSDNET-83|Unterstützung des Farbverlaufs-Effekts|Feature|
|PSDNET-84|Unterstützung des Muster-Effekts|Feature|
|PSDNET-89|Möglichkeit, den neu generierten regulären Layer zu PsdImage hinzuzufügen|Feature|
|PSDNET-93|Nach Aktualisierung des Textinhalts der Textebene mit dem Zeichen \ (Backslash) kann die resultierende Datei in Photoshop nicht geöffnet werden|Bug|
|PSDNET-39|Kaputte Bilder nach Export mit übergroßen Bilddaten im CMYK-Farbmodus|Bug|
|PSDNET-52|Möglich: Rotation in PSD funktioniert nicht|Bug|
|PSDNET-88|Möglich: Crop-Methoden in Aspose.PSD funktionieren nicht|Bug|
|PSDNET-91|Änderungen von Aspose.Imaging auf Aspose.PSD anwenden|Verbesserung|

## **Änderungen zu öffentlichen APIs**
Methode    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

Klasse    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Methode    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Methode    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Feld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Feld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Feld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Feld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

Feld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

Feld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

Feld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

Feld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

Feld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

Feld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddGradientOverlay

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddPatternOverlay

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Settings

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.BlendMode

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.IsVisible

Eigenschaft    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Opacity

## **Beispiel für die Verwendung:**
**PSDNET-76. Unterstützung des Strich-Layers**

**1) Fülltyp - Muster**

{{< highlight java >}}

     // Stricheffekt. Fülltyp - Muster. Beispiel

    string sourceFileName = "Stroke.psd";

    string exportPath = "StrokePatternChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    // Vorbereitung neuer Daten

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

                  resource.Name = "$$$/Presets/Patterns/HorizontalLine1=Horizontale Linie 9\0";        

                  resource.SetPattern(newPattern, newPatternBounds);               

             }

         }

         ((PatternFillSettings)patternStroke.FillSettings).PatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontale Linie 9\0";

         ((PatternFillSettings)patternStroke.FillSettings).PatternId = guid.ToString() + "\0";

        im.Save(exportPath);

    }

    // Testdatei nach Bearbeitung

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

            throw new Exception("PattResource nicht gefunden");

        }

        // Überprüfen der Mustereigenschaften

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

**Fülltyp - Farbverlauf**

{{< highlight java >}}

     // Stricheffekt. Fülltyp - Farbverlauf. Beispiel

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

        Assert.IsTrue(Math.Abs(90 - fillSettings.Angle) < 0.001, "Winkel ist inkorrekt");

        Assert.AreEqual(false, fillSettings.Dither);

        Assert.IsTrue(Math.Abs(0 - fillSettings.HorizontalOffset) < 0.001, "Horizontaler Versatz ist inkorrekt");

        Assert.IsTrue(Math.Abs(0 - fillSettings.VerticalOffset) < 0.001, "Vertikaler Versatz ist inkorrekt");

        Assert.AreEqual(false, fillSettings.Reverse);

        // Farbpunkte

        var colorPoints = fillSettings.ColorPoints;

        Assert.AreEqual(2, colorPoints.Length);

        Assert.AreEqual(Color.Black, colorPoints[0].Color);

        Assert.AreEqual(0, colorPoints[0].Location);

        Assert.AreEqual(50, colorPoints[0].MedianPointLocation);

        Assert.AreEqual(Color.White, colorPoints[1].Color);

        Assert.AreEqual(4096, colorPoints[1].Location);

        Assert.AreEqual(50, colorPoints[1].MedianPointLocation);

        // Transparenzpunkte

        var transparencyPoints = fillSettings.TransparencyPoints;

        Assert.AreEqual(2, transparencyPoints.Length);

        Assert.AreEqual(0, transparencyPoints[0].Location);

        Assert.AreEqual(50, transparencyPoints[0].MedianPointLocation);

        Assert.AreEqual(100, transparencyPoints[0].Opacity);

        Assert.AreEqual(4096, transparencyPoints[1].Location);

        Assert.AreEqual(50, transparencyPoints[1].MedianPointLocation);

        Assert.AreEqual(100, transparencyPoints[1].Opacity);

        // Bearbeitung testen

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

        // Farbpunkte hinzufügen

        var colorPoints = fillSettings.ColorPoints;

        Assert.AreEqual(2, colorPoints.Length);

        var point = fillSettings.ColorPoints[0];

        Assert.AreEqual(50, point.MedianPointLocation);

        Assert.AreEqual(Color.Black, point.Color);

        Assert.AreEqual(0, point.Location);

        point = fillSettings.ColorPoints[1];

        Assert.AreEqual(50, point.MedianPointLocation);

        Assert.AreEqual(Color.White, point.Color);

        Assert.AreEqual(1899, point.Location);

        // Transparenzpunkte hinzufügen

        var transparencyPoint = fillSettings.AddTransparencyPoint();

        transparencyPoint.Opacity = 25;

        transparencyPoint.MedianPointLocation = 25;

        transparencyPoint.Location = 4096;

        // Ändern der Lokalisierung des vorherigen Transparenzpunkts

        fillSettings.TransparencyPoints[1].Location = 2411;

        im.Save(exportPath);

    }

    // Testdatei nach Bearbeitung

    using (var im = (PsdImage)Image.Load(exportPath, loadOptions))

    {

        var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Color, gradientStroke.BlendMode);

        Assert.AreEqual(127, gradientStroke.Opacity);

        Assert.AreEqual(true, gradientStroke.IsVisible);

        var fillSettings = (GradientFillSettings)gradientStroke.FillSettings;

        Assert.AreEqual(Color.Green, fillSettings.Color);

        Assert.AreEqual(FillType.Gradient, fillSettings.FillType);

        // Farbpunkte überprüfen

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

        // Transparenzpunkte überprüfen

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

        Assert.AreEqual(4096, transparencyPoint.Location);

    }

{{< /highlight >}}

**Fülltyp - Farbe**

{{< highlight java >}}

   // Stricheffekt. Fülltyp - Farbe. Beispiel

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

    // Testdatei nach Bearbeitung

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

**PSDNET-83. Unterstützung des Farbverlauf-Effekts.**

{{< highlight java >}}

 // Farbverlauf-Überlagerungseffekt. Beispiel

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

         Assert.AreEqual(GradientType.Linear, settings.GradientType);

         Assert.IsTrue(Math.Abs(33 - settings.Angle) < 0.001, "Winkel ist inkorrekt");

         Assert.AreEqual(false, settings.Dither);

         Assert.IsTrue(Math.Abs(129 - settings.HorizontalOffset) < 0.001, "Horizontaler Versatz ist inkorrekt");

         Assert.IsTrue(Math.Abs(156 - settings.VerticalOffset) < 0.001, "Vertikaler Versatz ist inkorrekt");

         Assert.AreEqual(false, settings.Reverse);

         // Farbpunkte

         var colorPoints = settings.ColorPoints;

         Assert.AreEqual(3, colorPoints.Length);

         Assert.AreEqual(Color.FromArgb(9, 0, 178), colorPoints[0].Color);

         Assert.AreEqual(0, colorPoints[0].Location);

         Assert.AreEqual(50, colorPoints[0].MedianPointLocation);

         Assert.AreEqual(Color.Red, colorPoints[1].Color);

         Assert.AreEqual(2048, colorPoints[1].Location);

         Assert.AreEqual(50, colorPoints[1].MedianPointLocation);

         Assert.AreEqual(Color.FromArgb(255, 252, 0), colorPoints[2].Color);

         Assert.AreEqual(4096, colorPoints[2].Location);

         Assert.AreEqual(50, colorPoints[2].MedianPointLocation);

         // Transparenzpunkte

         var transparencyPoints = settings.TransparencyPoints;

         Assert.AreEqual(2, transparencyPoints.Length);

         Assert.AreEqual(0, transparencyPoints[0].Location);

         Assert.AreEqual(50, transparencyPoints[0].MedianPointLocation);

         Assert.assertEquals(100, transparencyPoints[0].Opacity);

         Assert.assertEquals(4096, transparencyPoints[1].Location);

         Assert.assertEquals(50, transparencyPoints[1].MedianPointLocation);

         Assert.assertEquals(100, transparencyPoints[1].Opacity);

         // Bearbeitung testen

         settings.Color = Color.Green;

         gradientOverlay.Opacity = 193;

         gradientOverlay.BlendMode = BlendMode.Lighten;

         settings.AlignWithLayer =

            false;

         settings.GradientType = GradientType.Radial;

         settings.Angle = 45;

         settings.Dither = true;

         settings.HorizontalOffset = 15;

         settings.VerticalOffset = 11;

         settings.Reverse = true;

         // Neue Farbpunkte hinzufügen

         var colorPoint = settings.AddColorPoint();

         colorPoint.Color = Color.Green;

         colorPoint.Location = 4096;

         colorPoint.MedianPointLocation = 75;

         // Ändern der Lokalisierung des vorherigen Punkts

         settings.ColorPoints[2].Location = 3000;

         // Neuen Transparenzpunkt hinzufügen

         var transparencyPoint = settings.AddTransparencyPoint();

         transparencyPoint.Opacity = 25;

         transparencyPoint.MedianPointLocation = 25;

         transparencyPoint.Location = 4096;

         // Ändern der Lokalisierung des vorherigen Transparenzpunkts

         settings.TransparencyPoints[1].Location = 2315;

         im.Save(exportPath);

    }

    // Testdatei nach Bearbeitung

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

         var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

         Assert.AreEqual(BlendMode.Lighten, gradientOverlay.BlendMode);

         Assert.assertEquals(193, gradientOverlay.Opacity);

         Assert.assertEquals(true, gradientOverlay.IsVisible);

         var fillSettings = gradientOverlay.Settings;

         Assert.AreEqual(Color.Empty, fillSettings.Color);

         Assert.assertEquals(FillType.Gradient, settings.FillType);

         // Farbpunkte überprüfen

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

         // Transparenzpunkte überprüfen

         Assert.assertEquals(3, fillSettings.TransparencyPoints.Length);

         var transparencyPoint = fillSettings.TransparencyPoints[0];

         Assert.assertEquals(50, transparencyPoint.MedianPointLocation);

         Assert.assertEquals(100, transparencyPoint.Opacity);

         Assert.assertEquals(0, transparencyPoint.Location);

         transparencyPoint = fillSettings.TransparencyPoints[1];

         Assert.assertEquals(50, transparencyPoint.MedianPointLocation);

         Assert.assertEquals(100, transparencyPoint.Opacity);

         Assert.assertEquals(2315, transparencyPoint.Location);

         transparencyPoint = fillSettings.TransparencyPoints[2];

         Assert.assertEquals(25, transparencyPoint.MedianPointLocation);

         Assert.assertEquals(25, transparencyPoint.Opacity);

         Assert.assertEquals(4096, transparencyPoint.Location);

    }

{{< /highlight >}}