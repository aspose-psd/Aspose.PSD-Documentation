---
title: Catatan Rilis Aspose.PSD for .NET 18.12
type: docs
weight: 10
url: /id/net/aspose-psd-for-net-18-12-release-notes/
---

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-76|Dukungan untuk Layer Stroke|Fitur|
|PSDNET-83|Dukungan untuk Efek Gradien|Fitur|
|PSDNET-84|Dukungan untuk Efek Pola|Fitur|
|PSDNET-89|Membuat kemampuan untuk menambahkan layer reguler yang baru ke PsdImage|Fitur|
|PSDNET-93|Setelah memperbarui konten layer teks dengan karakter \ (backslash), file hasilnya tidak dapat dibuka di Photoshop|Bug|
|PSDNET-39|Gambar rusak setelah diekspor dengan data gambar yang terlalu besar dalam Mode Warna CMYK|Bug|
|PSDNET-52|Mungkin: Rotasi dalam PSD tidak berfungsi|Bug|
|PSDNET-88|Mungkin: Metode Cropping di Aspose.Psd tidak berfungsi|Bug|
|PSDNET-91|Terapkan perubahan Aspose.Imaging ke Aspose.PSD|Peningkatan|

## **Perubahan API Publik**
Metode    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

Kelas    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Metode    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Metode    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Kelas    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Kelas    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Kelas    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Kelas    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

Kelas    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Kelas    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

Kelas    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

Kelas    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

Kelas    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Kelas    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

Kelas    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

Kelas    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddGradientOverlay

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddPatternOverlay

Metode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

Kelas    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Settings

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.BlendMode

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.IsVisible

Properti    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Opacity


## **Contoh Penggunaan:**
**PSDNET-76. Dukungan untuk Layer Stroke**

**1) Jenis Isian - Pola**

{{< highlight java >}}

     // Efek stroke. Jenis Isian - Pola. Contoh

    string sourceFileName = "Stroke.psd";

    string exportPath = "StrokePatternChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    // Menyiapkan data baru

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

    // File uji setelah diedit

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

            throw new Exception("PattResource not found");

        }

        // Periksa data pola

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

**Jenis Isian - Gradien**

{{< highlight java >}}

     // Efek stroke. Jenis Isian - Gradien. Contoh

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

        Assert.AreEqual(true, Math.Abs(90 - fillSettings.Angle) < 0.001, "Sudut tidak benar");

        Assert.AreEqual(false, fillSettings.Dither);

        Assert.AreEqual(true, Math.Abs(0 - fillSettings.HorizontalOffset) < 0.001, "Penggeseran horizontal tidak benar");

        Assert.AreEqual(true, Math.Abs(0 - fillSettings.VerticalOffset) < 0.001, "Penggeseran vertikal tidak benar");

        Assert.AreEqual(false, fillSettings.Reverse);

        // Titik Warna

        var colorPoints = fillSettings.ColorPoints;

        Assert.AreEqual(2, colorPoints.Length);

        Assert.AreEqual(Color.Black, colorPoints[0].Color);

        Assert.AreEqual(0, colorPoints[0].Location);

        Assert.AreEqual(50, colorPoints[0].MedianPointLocation);

        Assert.AreEqual(Color.White, colorPoints[1].Color);

        Assert.AreEqual(4096, colorPoints[1].Location);

        Assert.AreEqual(50, colorPoints[1].MedianPointLocation);

        // Titik Transparansi

        var transparencyPoints = fillSettings.TransparencyPoints;

        Assert.AreEqual(2, transparencyPoints.Length);

        Assert.AreEqual(0, transparencyPoints[0].Location);

        Assert.AreEqual(50, transparencyPoints[0].MedianPointLocation);

        Assert.AreEqual(100, transparencyPoints[0].Opacity);

        Assert.AreEqual(4096, transparencyPoints[1].Location);

        Assert.AreEqual(50, transparencyPoints[1].MedianPointLocation);

        Assert.AreEqual(100, transparencyPoints[1].Opacity);

        // Uji pengeditan

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

        // Tambahkan titik warna baru

        var colorPoint = fillSettings.AddColorPoint();

        colorPoint.Color = Color.Green;        

        colorPoint.Location = 4096;

        colorPoint.MedianPointLocation = 75;

        // Ubah lokasi titik sebelumnya

        fillSettings.ColorPoints[1].Location = 1899;

        // Tambahkan titik transparansi baru

        var transparencyPoint = fill```java
        transparencyPoint.Opacity = 25;

        transparencyPoint.MedianPointLocation = 25;

        transparencyPoint.Location = 4096;

        // Ubah lokasi titik transparansi sebelumnya

        fillSettings.TransparencyPoints[1].Location = 2411;

        im.Save(exportPath);

    }

    // File uji setelah diedit

    using (var im = (PsdImage)Image.Load(exportPath, loadOptions))

    {

        var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Color, gradientStroke.BlendMode);

        Assert.AreEqual(127, gradientStroke.Opacity);

        Assert.AreEqual(true, gradientStroke.IsVisible);

        var fillSettings = (GradientFillSettings)gradientStroke.FillSettings;

        Assert.AreEqual(Color.Green, fillSettings.Color);

        Assert.AreEqual(FillType.Gradient, fillSettings.FillType);

        // Periksa titik warna

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

        // Periksa titik transparansi

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

**Jenis Isian - Warna**

{{< highlight java >}}

    // Efek stroke. Jenis Isian - Warna. Contoh

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

    // File uji setelah diedit

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

**PSDNET-83. Dukungan untuk Efek Gradien.**

{{< highlight java >}}

 // Efek gradien overlay. Contoh

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

         Assert.