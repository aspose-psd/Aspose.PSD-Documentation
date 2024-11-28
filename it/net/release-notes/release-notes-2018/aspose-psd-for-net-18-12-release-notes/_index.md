---
title: Note sulla versione di rilascio di Aspose.PSD per .NET 18.12
type: docs
weight: 10
url: /it/net/aspose-psd-for-net-18-12-release-notes/
---

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-76|Supporto dello Strato di Tracciato|Funzionalità|
|PSDNET-83|Supporto dell'Effetto Gradiente|Funzionalità|
|PSDNET-84|Supporto dell'Effetto Modello|Funzionalità|
|PSDNET-89|Possibilità di aggiungere il nuovo strato regolare generato a PsdImage|Funzionalità|
|PSDNET-93|Dopo l'aggiornamento del contenuto dello strato di testo con il carattere \ (backslash), il file risultante non può essere aperto in Photoshop|Bug|
|PSDNET-39|Immagini danneggiate dopo l'esportazione con dati immagine sovradimensionati nella Modalità Colore CMYK|Bug|
|PSDNET-52|Possibile: La rotazione in PSD non funziona|Bug|
|PSDNET-88|Possibile: I metodi di ritaglio in Aspose.Psd non funzionano|Bug|
|PSDNET-91|Applicare le modifiche di Aspose.Imaging a Aspose.PSD|Miglioramento|

## **Cambiamenti nell'API pubblica**
Metodo    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

Classe    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Metodo    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Metodo    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Classe    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Classe    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Classe    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Classe    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

Classe    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Classe    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

Classe    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

Classe    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

Classe    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Classe    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

Classe    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

Campo/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

Classe    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddGradientOverlay

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddPatternOverlay

Metodo    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

Classe    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Settings

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.BlendMode

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.IsVisible

Proprietà    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Opacity

## **Esempi d'uso:**
**PSDNET-76. Supporto dello Strato di Tracciato**

**1) Tipo di riempimento - Modello**

{{< highlight it >}}

     // Effetto strato di tracciato. Tipo di riempimento - Modello. Esempio

    string sourceFileName = "Tracciato.psd";

    string exportPath = "TracciatoModelloModificato.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    // Preparazione dei nuovi dati

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

    // File di test dopo la modifica

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

            throw new Exception("Risorsa Patt non trovata");

        }

        // Verifica dei dati del modello

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



**Tipo di riempimento - Gradiente**

{{< highlight it >}}

     // Effetto strato di tracciato. Tipo di riempimento - Gradiente. Esempio

    string sourceFileName = "Tracciato.psd";

    string exportPath = "TracciatoGradienteModificato.psd";

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

        Assert.IsTrue(Math.Abs(90 - fillSettings.Angle) < 0.001, "L'angolo non è corretto");

        Assert.AreEqual(false, fillSettings.Dither);

        Assert.IsTrue(Math.Abs(0 - fillSettings.HorizontalOffset) < 0.001, "Lo spostamento orizzontale non è corretto");

        Assert.IsTrue(Math.Abs(0 - fillSettings.VerticalOffset) < 0.001, "Lo spostamento verticale non è corretto");

        Assert.AreEqual(false, fillSettings.Reverse);

        // Punti colore

        var colorPoints = fillSettings.ColorPoints;

        Assert.AreEqual(2, colorPoints.Length);

        Assert.AreEqual(Color.Black, colorPoints[0].Color);

        Assert.AreEqual(0, colorPoints[0].Location);

        Assert.AreEqual(50, colorPoints[0].MedianPointLocation);

        Assert.AreEqual(Color.White, colorPoints[1].Color);

        Assert.AreEqual(4096, colorPoints[1].Location);

        Assert.AreEqual(50, colorPoints[1].MedianPointLocation);

        // Punti di trasparenza

        var transparencyPoints = fillSettings.TransparencyPoints;

        Assert.AreEqual(2, transparencyPoints.Length);

        Assert.AreEqual(0, transparencyPoints[0].Location);

        Assert.AreEqual(50, transparencyPoints[0].MedianPointLocation);

        Assert.AreEqual(100, transparencyPoints[0].Opacity);

        Assert.AreEqual(4096, transparencyPoints[1].Location);

        Assert.AreEqual(50, transparencyPoints[1].MedianPointLocation);

        Assert.AreEqual(100, transparencyPoints[1].Opacity);

        // Modifica

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

        // Aggiungi nuovo punto colore

        var colorPoint = fillSettings.AddColorPoint();

        colorPoint.Color = Color.Green;

        colorPoint.Location = 4096;

        colorPoint.MedianPointLocation = 75;

        // Modifica la posizione del punto precedente

        fillSettings.ColorPoints[1].Location = 1899;

        // Aggiungi nuovo punto di trasparenza

        var transparencyPoint = fillSettings.AddTransparencyPoint();

        transparencyPoint.Opacity = 25;

        transparencyPoint.MedianPointLocation = 25;

        transparencyPoint.Location = 4096;

        // Modifica la posizione del punto di trasparenza precedente

        fillSettings.TransparencyPoints[1].Location = 2411;

        im.Save(exportPath);

    }

    // File di test dopo la modifica

    using (var im = (PsdImage)Image.Load(exportPath, loadOptions))

    {

        var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Color, gradientStroke.BlendMode);

        Assert.AreEqual(127, gradientStroke.Opacity);

        Assert.AreEqual(true, gradientStroke.IsVisible);

        var fillSettings = (GradientFillSettings)gradientStroke.FillSettings;

        Assert.AreEqual(Color.Green, fillSettings.Color);

        Assert.AreEqual(FillType.Gradient, fillSettings.FillType);

        // Verifica dei punti colore

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

        // Verifica dei punti di trasparenza

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



**Tipo di riempimento - Colore**

{{< highlight it >}}

   // Effetto strato di tracciato. Tipo di riempimento - Colore. Esempio

    var sourceFileName = "Tracciato.psd";

    var exportPath = "TracciatoColoreModificato.psd";

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

    // File di test dopo la modifica

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



**PSDNET-83. Supporto dell'Effetto Gradiente.**

{{< highlight it >}}

 // Effetto sovrapposizione gradiente. Esempio

    string sourceFileName = "GradienteSovrapposizione.psd";

    string exportPath = "GradienteSovrapposizioneModificato.psd";

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

         Assert.IsTrue(Math.Abs(33 - settings.Angle) < 0.001, "L'angolo non è corretto");

         Assert.AreEqual(false, settings.Dither);

         Assert.IsTrue(Math.Abs(129 - settings.HorizontalOffset) < 0.001, "Lo spostamento orizzontale non è corretto");

         Assert.IsTrue(Math.Abs(156 - settings.VerticalOffset) < 0.001, "Lo spostamento verticale non è corretto");

         Assert.AreEqual(false, settings.Reverse);

         // Punti colore

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

         // Punti di trasparenza

         var transparencyPoints = settings.TransparencyPoints;

         Assert.AreEqual(2, transparencyPoints.Length);

         Assert.AreEqual(0, transparencyPoints[0].Location);

         Assert.AreEqual(50, transparencyPoints[0].MedianPointLocation);

         Assert.AreEqual(100, transparencyPoints[0].Opacity);

         Assert.AreEqual(4096, transparencyPoints[1].Location);

         Assert.AreEqual(50, transparencyPoints[1].MedianPointLocation);

         Assert.AreEqual(100, transparencyPoints[1].Opacity);

         // Modifica

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

         // Aggiungi nuovo punto colore

         var colorPoint = settings.AddColorPoint();

         colorPoint.Color = Color.Green;

         colorPoint.Location = 4096;

         colorPoint.MedianPointLocation = 75;

         // Modifica la posizione del punto precedente

         settings.ColorPoints[2].Location = 3000;

         // Aggiungi nuovo punto di trasparenza

         var transparencyPoint = settings.AddTransparencyPoint();

         transparencyPoint.Opacity = 25;

         transparencyPoint.MedianPointLocation = 25;

         transparencyPoint.Location = 4096;

         // Modifica la posizione del punto di trasparenza precedente

         settings.TransparencyPoints[1].Location = 2315;

         im.Save(exportPath);

    }

    // File di test dopo la modifica

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

         var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

         Assert.AreEqual(BlendMode.Lighten, gradientOverlay.BlendMode);

         Assert.AreEqual(193, gradientOverlay.Opacity);

         Assert.AreEqual(true, gradientOverlay.IsVisible);

         var fillSettings = gradientOverlay.Settings;

         Assert.AreEqual(Color.Empty, fillSettings.Color);

         Assert.AreEqual(FillType.Gradient, fillSettings.FillType);

         // Verifica dei punti colore

         Assert.AreEqual(4, fillSettings.ColorPoints.Length);

         var point = fillSettings.ColorPoints[0];

         Assert.AreEqual(50, point.MedianPointLocation);

         Assert.AreEqual(Color.FromArgb(9, 0, 178), point.Color);

         Assert.AreEqual(0, point.Location);

         point = fillSettings.ColorPoints[1];

         Assert.AreEqual(50, point.MedianPointLocation);

         Assert.AreEqual(Color.Red, point.Color);

         Assert.AreEqual(2048, point.Location);

         point = fillSettings.ColorPoints[2];

         Assert.AreEqual(50, point.MedianPointLocation);

         Assert.AreEqual(Color.FromArgb(255, 252, 0), point.Color);

         Assert.AreEqual(3000, point.Location);

         point = fillSettings.ColorPoints[3];

         Assert.AreEqual(75, point.MedianPointLocation);

         Assert.AreEqual(Color.Green, point.Color);

         Assert.AreEqual(4096, point.Location);

         // Verifica dei punti di trasparenza

         Assert.AreEqual(3, fillSettings.TransparencyPoints.Length);

         var transparencyPoint = fillSettings.TransparencyPoints[0];

         Assert.AreEqual(50, transparencyPoint.MedianPointLocation);

         Assert.assertEqual(100, transparencyPoint.Opacity);

         Assert.assertEqual(0, transparencyPoint.Location);

         transparencyPoint = fillSettings.TransparencyPoints[1]; 

         Assert.assertEqual(50, transparencyPoint.MedianPointLocation);

         Assert.assertEqual(100, transparencyPoint.Opacity);

         Assert.assertEqual(2315, transparencyPoint.Location);

         transparencyPoint = fillSettings.TransparencyPoints[2];

         Assert.assertEqual(25, transparencyPoint.MedianPointLocation);

         Assert.assertEqual(25, transparencyPoint.Opacity);

         Assert.assertEqual(4096, transparencyPoint.Location);

    }

{{< /highlight >}}



**PSDNET-84. Supporto dell'Effetto Modello.**

{{< highlight it >}}

    // Effetto sovrapposizione modello. Esempio

    string sourceFileName = "ModelloSovrapposizione.psd";

    string exportPath = "ModelloSovrapposizioneModificato.psd";

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

        Assert.AreEqual(BlendMode.Normal, patternOverlay.BlendMode);

        Assert.AreEqual(127, patternOverlay.Opacity);

        Assert.AreEqual(true, patternOverlay.IsVisible);

        var settings = patternOverlay.Settings;

        Assert.AreEqual(Color.Empty, settings.Color);

        Assert.AreEqual(FillType.Pattern, settings.FillType);

        Assert.AreEqual("85163837-eb9e-5b43-86fb-e6d5963ea29a\0", settings.PatternId);

        Assert.AreEqual("$$$/Presets/Patterns/OpticalSquares=Optical Squares\0", settings.PatternName);

        Assert.AreEqual(null, settings.PointType);

        Assert.AreEqual(100, settings.Scale);

        Assert.AreEqual(false, settings.Linked);

        Assert.IsTrue(Math.Abs(0 - settings.HorizontalOffset) < 0.001, "Lo spostamento orizzontale non è corretto");

        Assert.IsTrue(Math.Abs(0 - settings.VerticalOffset) < 0.001, "Lo spostamento verticale non è corretto");

        // Modifica

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

    // File di test dopo la modifica

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

        var patternOverlay = (PatternOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Difference, patternOverlay.BlendMode);

        Assert.AreEqual(193, patternOverlay.Opacity);

        Assert.AreEqual(true, patternOverlay.IsVisible);

        var fillSettings = patternOverlay.Settings;

        Assert.AreEqual(Color.Empty, fillSettings.Color);

        Assert.AreEqual(FillType.Pattern, fillSettings.FillType);

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

             throw new Exception("Risorsa Patt non trovata");

        }

        // Verifica dei dati del modello

        Assert.AreEqual(newPattern, resource.PatternData);

        Assert.AreEqual(newPatternBounds, new Rectangle(0, 0, resource.Width, resource.Height));

        Assert.AreEqual(guid.ToString(), resource.PatternId);

    }

{{< /highlight >}}



**PSDNET-89. Possibilità di aggiungere il nuovo strato regolare generato a PsdImage.**

{{< highlight it >}}

  // Possibilità di aggiungere il nuovo strato regolare generato a PsdImage

    string sourceFileName = "UnicoStrato.psd";

    string exportPath = "UnicoStratoModificato.psd";

    string exportPathPng = "UnicoStratoModificato.png";

    using (var im = (PsdImage)Image.Load(sourceFileName))

    {

       // Preparazione di due matrici di interi

       var data1 = new int[2500];

       var data2 = new int[2500];

       var rect1 = new Rectangle(0, 0, 50, 50);

       var rect2 = new Rectangle(