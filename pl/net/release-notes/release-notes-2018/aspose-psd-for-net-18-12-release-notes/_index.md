---
title: Aspose.PSD dla .NET 18.12 - Notatki dotyczące wydania
type: docs
weight: 10
url: /pl/net/aspose-psd-dla-net-18-12-notatki-o-wydaniu/
---

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-76|Obsługa warstwy kreślenia|Nowa funkcja|
|PSDNET-83|Obsługa efektu gradientu|Nowa funkcja|
|PSDNET-84|Obsługa efektu wzoru|Nowa funkcja|
|PSDNET-89|Dodanie możliwości dodania nowej warstwy regularnej do obiektu PsdImage|Nowa funkcja|
|PSDNET-93|Po aktualizacji zawartości warstwy tekstowej znakiem \ (backslash), plik wynikowy nie można otworzyć w programie Photoshop|Błąd|
|PSDNET-39|Uszkodzone obrazy po eksporcie z nadmiernymi danymi obrazu w trybie kolorów CMYK|Błąd|
|PSDNET-52|Problem z obracaniem w formacie PSD|Błąd|
|PSDNET-88|Problem z metodami przycinania w Aspose.Psd|Błąd|
|PSDNET-91|Zastosuj zmiany w Aspose.Imaging do Aspose.PSD|Udoskonalenie|

## **Zmiany w API publicznym**
Metoda    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

Klasa    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Metoda    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Metoda    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Klasa    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Klasa    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Klasa    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Pole/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Pole/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Pole/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Klasa    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

Klasa    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Klasa    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

Klasa    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

Klasa    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

Klasa    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Klasa    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Pole/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

Pole/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

Pole/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

Pole/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

Pole/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

Pole/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

Klasa    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

Pole/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

Klasa    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddGradientOverlay

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddPatternOverlay

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

Klasa    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Settings

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.BlendMode

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.IsVisible

Właściwość    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Opacity

## **Przykłady użycia:**
**PSDNET-76. Obsługa warstw kreślenia**

**1) Typ wypełnienia - Wzorzec**

{{< highlight java >}}

     // Efekt kreślenia. Typ wypełnienia - Wzorzec. Przykład

    string nazwaPlikuZrodlowego = "Stroke.psd";

    string exportPath = "StrokePatternChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    // Przygotowanie nowych danych

    var nowyWzorzec = new int[]

    {

         Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

    };

   var noweGraniceWzorca = new Rectangle(0, 0, 4, 4);

   var guid = Guid.NewGuid();

    using (var im = (PsdImage)Image.Load(nazwaPlikuZrodlowego, loadOptions))

    {

         var wzorzecKreślenia = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

         Assert.AreEqual(BlendMode.Normal, wzorzecKreślenia.BlendMode);

         Assert.AreEqual(255, wzorzecKreślenia.Opacity);

         Assert.AreEqual(true, wzorzecKreślenia.IsVisible);

         var fillSettings = (PatternFillSettings)wzorzecKreślenia.FillSettings;

         Assert.AreEqual(FillType.Pattern, fillSettings.FillType);

         wzorzecKreślenia.Opacity = 127;

         wzorzecKreślenia.BlendMode = BlendMode.Color;

         PattResource zasób;

         foreach (var globalLayerResource in im.GlobalLayerResources)

         {

             if (globalLayerResource is PattResource)

             {

                  zasób = (PattResource)globalLayerResource;

                  zasób.PatternId = guid.ToString();

                  zasób.Name = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";        

                  zasób.SetPattern(nowyWzorzec, noweGraniceWzorca);               

             }

         }

         ((PatternFillSettings)wzorzecKreślenia.FillSettings).PatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";

         ((PatternFillSettings)wzorzecKreślenia.FillSettings).PatternId = guid.ToString() + "\0";

        im.Save(exportPath);

    }

    // Plik testowy po edycji

    using (var im = (PsdImage)Image.Load(nazwaPlikuZrodlowego, loadOptions))

    {

        var wzorzecKreślenia = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

        PattResource zasób = null;

        foreach (var globalLayerResource in im.GlobalLayerResources)

        {

            if (globalLayerResource is PattResource)

            {

                zasób = (PattResource)globalLayerResource;

            }

        }

        if (zasób == null)

        {

            throw new Exception("Nie znaleziono zasobu PattResource");

        }

        // Sprawdź dane wzorca

        Assert.AreEqual(nowyWzorzec, zasób.PatternData);

        Assert.AreEqual(noweGraniceWzorca, new Rectangle(0, 0, zasób.Width, zasób.Height));

        Assert.AreEqual(guid.ToString(), zasób.PatternId);

        Assert.AreEqual(BlendMode.Color, wzorzecKreślenia.BlendMode);

        Assert.AreEqual(127, wzorzecKreślenia.Opacity);

        Assert.AreEqual(true, wzorzecKreślenia.IsVisible);

        var fillSettings = (PatternFillSettings)wzorzecKreślenia.FillSettings;

        Assert.AreEqual(FillType.Pattern, fillSettings.FillType);

    }

{{< /highlight >}}

**Typ wypełnienia - Gradient**

{{< highlight java >}}

     // Efekt kreślenia. Typ wypełnienia - Gradient. Przykład

    string nazwaPlikuZrodlowego = "Stroke.psd";

    string exportPath = "StrokeGradientChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    using (var im = (PsdImage)Image.Load(nazwaPlikuZrodlowego, loadOptions))

    {

        var gradientKreślenia = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Normal, gradientKreślenia.BlendMode);

        Assert.AreEqual(255, gradientKreślenia.Opacity);

        Assert.AreEqual(true, gradientKreślenia.IsVisible);

        var fillSettings = (GradientFillSettings)gradientKreślenia.FillSettings;

        Assert.AreEqual(Color.Black, fillSettings.Color);

        Assert.AreEqual(FillType.Gradient, fillSettings.FillType);

        Assert.AreEqual(true, fillSettings.AlignWithLayer);

        Assert.AreEqual(GradientType.Linear, fillSettings.GradientType);

        Assert.IsTrue(Math.Abs(90 - fillSettings.Angle) < 0.001, "Zły kąt");

        Assert.AreEqual(false, fillSettings.Dither);

        Assert.IsTrue(Math.Abs(0 - fillSettings.HorizontalOffset) < 0.001, "Zły przesunięcie poziome");

        Assert.IsTrue(Math.Abs(0 - fillSettings.VerticalOffset) < 0.001, "Zły przesunicenie pionowe");

        Assert.AreEqual(false, fillSettings.Reverse);

        // Punkty kolorów

        var punktyKolorów = fillSettings.ColorPoints;

        Assert.AreEqual(2, punktyKolorów.Length);

        Assert.AreEqual(Color.Black, punktyKolorów[0].Color);

        Assert.AreEqual(0, punktyKolorów[0].Location);

        Assert.AreEqual(50, punktyKolorów[0].MedianPointLocation);

        Assert.AreEqual(Color.White, punktyKolorów[1].Color);

        Assert.AreEqual(4096, punktyKolorów[1].Location);

        Assert.AreEqual(50, punktyKolorów[1].MedianPointLocation);

        // Punkty przejrzystości

        var punktyPrzejrzystości = fillSettings.TransparencyPoints;

        Assert.AreEqual(2, punktyPrzejrzystości.Length);

        Assert.AreEqual(0, punktyPrzejrzystości[0].Location);

        Assert.AreEqual(50, punktyPrzejrzystości[0].MedianPointLocation);

        Assert.AreEqual(100, punktyPrzejrzystości[0].Opacity);

        Assert.AreEqual(4096, punktyPrzejrzystości[1].Location);

        Assert.AreEqual(50, punktyPrzejrzystości[1].MedianPointLocation);

        Assert.AreEqual(100, punktyPrzejrzystości[1].Opacity);

        // Test edycji

        fillSettings.Color = Color.Green;

        gradientKreślenia.Opacity = 127;

        gradientKreślenia.BlendMode = BlendMode.Color;

        fillSettings.AlignWithLayer = false;

        fillSettings.GradientType = GradientType.Radial;

        fillSettings.Angle = 45;

        fillSettings.Dither = true;

        fillSettings.HorizontalOffset = 15;

        fillSettings.VerticalOffset = 11;

        fillSettings.Reverse = true;

        // Dodanie nowego punktu koloru

        var punktKoloru = fillSettings.AddColorPoint();

        punktKoloru.Color = Color.Green;        

        punktKoloru.Location = 4096;

        punktKoloru.MedianPointLocation = 75;

        // Zmiana lokalizacji poprzedniego punktu

        fillSettings.ColorPoints[1].Location = 1899;

        // Dodanie nowego punktu przejrzystości

        var punktPrzejrzystości = fillSettings.AddTransparencyPoint();

        punktPrzejrzystości.Opacity = 25;

        punktPrzejrzystości.MedianPointLocation = 25;

        punktPrzejrzystości.Location = 4096;

        // Zmiana lokalizacji poprzedniego punktu przejrzystości

        fillSettings.TransparencyPoints[1].Location = 2411;

        im.Save(exportPath);

    }

    // Test pliku po edycji

    using (var im = (PsdImage)Image.Load(exportPath, loadOptions))

    {

        var gradientKreślenia = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Color, gradientKreślenia.BlendMode);

        Assert.AreEqual(127, gradientKreślenia.Opacity);

        Assert.AreEqual(true, gradientKreślenia.IsVisible);

        var fillSettings = (GradientFillSettings)gradientKreślenia.FillSettings;

        Assert.AreEqual(Color.Green, fillSettings.Color);

        Assert.AreEqual(FillType.Gradient, fillSettings.FillType);

        // Sprawdzenie punktów kolorów

        Assert.AreEqual(3, fillSettings.ColorPoints.Length);

        var punkt = fillSettings.ColorPoints[0];

        Assert.AreEqual(50, punkt.MedianPointLocation);

        Assert.AreEqual(Color.Black, punkt.Color);

        Assert.AreEqual(0, punkt.Location);

        punkt = fillSettings.ColorPoints[1];

        Assert.AreEqual(50, punkt.MedianPointLocation);

        Assert.AreEqual(Color.White, punkt.Color);

        Assert.AreEqual(1899, punkt.Location);

        punkt = fillSettings.ColorPoints[2];

        Assert.AreEqual(75, punkt.MedianPointLocation);

        Assert.AreEqual(Color.Green, punkt.Color);

        Assert.AreEqual(4096, punkt.Location);

        // Sprawdzenie punktów przejrzystości

        Assert.AreEqual(3, fillSettings.TransparencyPoints.Length);

        var punktPrzejrzystości = fillSettings.TransparencyPoints[0];

        Assert.AreEqual(50, punktPrzejrzystości.MedianPointLocation);

        Assert.AreEqual(100, punktPrzejrzystości.Opacity);

        Assert.AreEqual(0, punktPrzejrzystości.Location);

        punktPrzejrzystości = fillSettings.TransparencyPoints[1];

        Assert.AreEqual(50, punktPrzejrzystości.MedianPointLocation);

        Assert.AreEqual(100, punktPrzejrzystości.Opacity);

        Assert.AreEqual(2411, punktPrzejrzystości.Location);

        punktPrzejrzystości = fillSettings.TransparencyPoints[2];

        Assert.AreEqual(25, punktPrzejrzystości.MedianPointLocation);

        Assert.AreEqual(25, punktPrzejrzystości.Opacity);

        Assert.AreEqual(4096, punktPrzejrzystości.Location);

    }

{{< /highlight >}}

**PSDNET-84. Obsługa efektu wzoru.**

{{< highlight java >}}

    // Efekt nakładania wzoru. Przykład

    string nazwaPlikuZrodlowego = "PatternOverlay.psd";

    string exportPath = "PatternOverlayChanged.psd";

    var nowyWzorzec = new int[]

    {

        Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

        Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

    };

    var noweGraniceWzorca = new Rectangle(0, 0, 4, 2);

    var guid = Guid.NewGuid();

    var nowaNazwaWzorca = "$$$/Presets/Patterns/Pattern=Some new pattern name\0";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    using (var im = (PsdImage)Image.Load(nazwaPlikuZrodlowego, loadOptions))

    {

        var wzorzecNakładania = (PatternOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Normal, wzorzecNakładania.BlendMode);

        Assert.AreEqual(127, wzorzecNakładania.Opacity);

        Assert.AreEqual(true, wzorzecNakładania.IsVisible);

        var settings = wzorzecNakładania.Settings;

        Assert.AreEqual(Color.Empty, settings.Color);

        Assert.AreEqual(FillType.Pattern, settings.FillType);

        Assert.AreEqual("85163837-eb9e-5b43-86fb-e6d5963ea29a\0", settings.PatternId);

        Assert.AreEqual("$$$/Presets/Patterns/OpticalSquares=Optical Squares\0", settings.PatternName);

        Assert.AreEqual(null, settings.PointType);

        Assert.AreEqual(100, settings.Scale);

        Assert.AreEqual(false, settings.Linked);

        Assert.IsTrue(Math.Abs(0 - settings.HorizontalOffset) < 0.001, "Złe przesunięcie poziome");

        Assert.IsTrue(Math.Abs(0 - settings.VerticalOffset) < 0.001, "Złe przesunięcie pionowe");    

        // Test edycji

        settings.Color = Color.Green;

        wzorzecNakładania.Opacity = 193;

        wzorzecNakładania.BlendMode = BlendMode.Difference;        

        settings.HorizontalOffset = 15;

        settings.VerticalOffset = 11;

        PattResource zasób;

        foreach (var globalLayerResource in im.GlobalLayerResources)

        {

            if (globalLayerResource is PattResource)

            {

                zasób = (PattResource)globalLayerResource;

                zasób.PatternId = guid.ToString();

                zasób.Name = nowaNazwaWzorca;

                zasób.SetPattern(nowyWzorzec, noweGraniceWzorca);

            }

        }

        settings.PatternName = nowaNazwaWzorca;

        settings.PatternId = guid.ToString() + "\0";

        im.Save(exportPath);

    }

    // Test pliku po edycji

    using (var im = (PsdImage)Image.Load(nazwaPlikuZrodlowego, loadOptions))

    {

        var wzorzecNakładania = (PatternOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Difference, wzorzecNakładania.BlendMode);

        Assert.AreEqual(193, wzorzecNakładania.Opacity);

        Assert.AreEqual(true, wzorzecNakładania.IsVisible);

        var fillSettings = wzorzecNakładania.Settings;

        Assert.AreEqual(Color.Empty, fillSettings.Color);

        Assert.AreEqual(FillType.Pattern, fillSettings.FillType);

        PattResource zasób = null;

        foreach (var globalLayerResource in im.GlobalLayerResources)

        {

            if (globalLayerResource is PattResource)

            {

                 zasób = (PattResource)globalLayerResource;

            }

        }

        if (zasób == null)

        {

             throw new Exception("Nie znaleziono zasobu PattResource");

        }

        // Sprawdź dane wzorca

        Assert.AreEqual(nowyWzorzec, zasób.PatternData);

        Assert.AreEqual(noweGraniceWzorca, new Rectangle(0, 0, zasób.Width, zasób.Height));

        Assert.AreEqual(guid.ToString(), zasób.PatternId);

    }

{{< /highlight >}}

**PSDNET-89. Dodanie możliwości dodania nowej warstwy regularnej do obiektu PsdImage.**

{{< highlight java >}}

  // Dodanie możliwości dodania nowej warstwy regularnej do obiektu PsdImage

    string nazwaPlikuZrodlowego = "OneLayer.psd";

    string exportPath = "OneLayerEdited.psd";

    string exportPathPng = "OneLayerEdited.png";

    using (var im = (PsdImage)Image.Load(nazwaPlikuZrodlowego))

    {

       // Przygotowanie dwóch tablic int

       var data1 = new int[2500];

       var data2 = new int[2500];

       var rect1 = new Rectangle(0, 0, 50, 50);

       var rect2 = new Rectangle(0, 0, 100, 25);

       for (int i = 0; i < 2500; i++)

       {

           data1[i] = -10000000;

           data2[i] = -10000000;

       }

       var warstwa1 = im.AddRegularLayer();

       warstwa1.Left = 25;

       warstwa1.Top = 25;

       warstwa1.Right = 75;

       warstwa1.Bottom = 75;

       warstwa1.SaveArgb32Pixels(rect1, data1);

       var warstwa2 = im.AddRegularLayer();

       warstwa2.Left = 25;

       warstwa2.Top = 150;

       warstwa2.Right = 125;

       warstwa2.Bottom = 175;

       warstwa2.SaveArgb32Pixels(rect2, data2);

       // Zapisz psd

       im.Save(exportPath, new PsdOptions());

       // Zapisz png

       im.Save(exportPathPng, new PngOptions());

    }

{{< /highlight >}}

**PSDNET-93. Po aktualizacji zawartości warstwy tekstowej znakiem \ (backslash), plik wynikowy nie można otworzyć w programie Photoshop.**

{{< highlight java >}}

 using (

var obrazek = 

Image.Load(

"przykład.psd"))

{

if (!(obrazek is PsdImage)) return;

                var psdObrazek = (PsdImage)obrazek;

                var warstwy = psdObrazek.Layers;

                for (var indeks = warstwy.Length - 1; indeks >= 0; indeks--)

                {

                    var warstwa = warstwy[indeks];

                    if (!(warstwa is TextLayer)) continue;

                    var tekstowaWarstwa = (TextLayer)warstwa;

                    tekstowaWarstwa.UpdateText("展 就");

                }

                var opcjeObrazu = new PsdOptions(psdObrazek);

                psdObrazek.Save("wynik.psd", opcjeObrazu);

            }

{{< /highlight >}}