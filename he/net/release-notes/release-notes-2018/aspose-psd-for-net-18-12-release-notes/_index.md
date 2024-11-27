---
title: Aspose.PSD עבור .NET 18.12 - הערות לגרסה
type: docs
weight: 10
url: /he/net/aspose-psd-for-net-18-12-release-notes/
---

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-76|תמיכה בשכבת הקווים הנקיפה|תכונה|
|PSDNET-83|תמיכה באפקט הגרדיאנט|תכונה|
|PSDNET-84|תמיכה באפקט התבנית|תכונה|
|PSDNET-89|לאפשרות להוסיף את השכבה הרגילה המיוצרת ל-PsdImage|תכונה|
|PSDNET-93|לאחר עדכון של תוכן שכבת הטקסט עם תו \ (קו נטוי), הקובץ התוצאה לא יכול להיפתח בפוטושופ|באג|
|PSDNET-39|תמונות שבורות אחרי ייצוא עם נתוני תמונה גדולה מידי במצב הצבע CMYK|באג|
|PSDNET-52|אפשרי: הסיבוב ב-PSD אינו עובד|באג|
|PSDNET-88|אפשרי: שיטות חיתוך ב-Aspose.Psd לא עובדות|באג|
|PSDNET-91|ליישם שינויים של Aspose.Imaging ל-Aspose.PSD|שדרוג|

## **שינויים ב- API הציבורי**
Method    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

Class    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Method    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Method    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddGradientOverlay

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddPatternOverlay

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Settings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.BlendMode

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.IsVisible

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Opacity

## **דוגמאות שימוש:**
**PSDNET-76. תמיכה בשכבת הקווים הנקיפה**

**1) סוג מילאה - תבנית**

{{< highlight java >}}

     // אפקט שכבת הקו. מילאה - תבנית. דוגמה

    string sourceFileName = "Stroke.psd";

    string exportPath = "StrokePatternChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    // הכנת נתונים חדשים

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

    // קובץ בדיקה לאחר עריכה

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

        // בדיקת נתונים התבנית

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

**סוג מילאה - גרדיאנט**

{{< highlight java >}}

     // אפקט שכבת הקו. מילאה - גרדיאנט. דוגמה

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

        Assert.IsTrue(Math.Abs(90 - fillSettings.Angle) < 0.001, "זווית שגויה");

        Assert.AreEqual(false, fillSettings.Dither);

        Assert.IsTrue(Math.Abs(0 - fillSettings.HorizontalOffset) < 0.001, "אופסט אופקי שגוי");

        Assert.IsTrue(Math.Abs(0 - fillSettings.VerticalOffset) < 0.001, "אופסט אנכי שגוי");

        Assert.AreEqual(false, fillSettings.Reverse);

        // נקודות צבע

        var colorPoints = fillSettings.ColorPoints;

        Assert.AreEqual(2, colorPoints.Length);

        Assert.AreEqual(Color.Black, colorPoints[0].Color);

        Assert.AreEqual(0, colorPoints[0].Location);

        Assert.AreEqual(50, colorPoints[0].MedianPointLocation);

        Assert.AreEqual(Color.White, colorPoints[1].Color);

        Assert.AreEqual(4096, colorPoints[1].Location);

        Assert.AreEqual(50, colorPoints[1].MedianPointLocation);

        // נקודות שקופות

        var transparencyPoints = fillSettings.TransparencyPoints;

        Assert.AreEqual(2, transparencyPoints.Length);

        Assert.AreEqual(0, transparencyPoints[0].Location);

        Assert.AreEqual(50, transparencyPoints[0].MedianPointLocation);

        Assert.AreEqual(100, transparencyPoints[0].Opacity);

        Assert.AreEqual(4096, transparencyPoints[1].Location);

        Assert.AreEqual(50, transparencyPoints[1].MedianPointLocation);

        Assert.assertEquals(100, transparencyPoints[1].Opacity);

        // בדיקת עריכה

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

        // הוספת נקודת צבע חדשה

        var colorPoint = fillSettings.AddColorPoint();

        colorPoint.Color = Color.Green;

        colorPoint.Location = 4096;

        colorPoint.MedianPointLocation = 75;

        // שינוי מיקום של הנקודה הקודמת

        fillSettings.ColorPoints[1].Location = 1899;

        // הוספת נקודת שקיפות חדשה

        var transparencyPoint = fillSettings.AddTransparencyPoint();

        transparencyPoint.Opacity = 25;

        transparencyPoint.MedianPointLocation = 25;

        transparencyPoint.Location = 4096;

        // שינוי מיקום של הנקודת השקיפות הקודמת

        fillSettings.TransparencyPoints[1].Location = 2411;

        im.Save(exportPath);

    }

    // קובץ בדיקה לאחר עריכה

    using (var im = (PsdImage)Image.Load(exportPath, loadOptions))

    {

        var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Color, gradientStroke.BlendMode);

        Assert.AreEqual(127, gradientStroke.Opacity);

        Assert.AreEqual(true, gradientStroke.IsVisible);

        var fillSettings = (GradientFillSettings)gradientStroke.FillSettings;

        Assert.AreEqual(Color.Green, fillSettings.Color);

        Assert.AreEqual(FillType.Gradient, fillSettings.FillType);

        // בדיקת נקודות צבע

        Assert.AreEqual(3, fillSettings.ColorPoints.Length);

        var point = fillSettings.ColorPoints[0];

        Assert.AreEqual(50, point.MedianPointLocation);

        Assert.AreEqual(Color.Black, point.Color);

        Assert.assertEqual(0, point.Location);

        point = fillSettings.ColorPoints[1];

        Assert.AreEqual(50, point.MedianPointLocation);

        Assert.AreEqual(Color.White, point.Color);

        Assert.assertEquals(1899, point.Location);

        point = fillSettings.ColorPoints[2];

        Assert.AreEqual(75, point.MedianPointLocation);

        Assert.assertEquals(Color.Green, point.Color);

        Assert.assertEqual(4096, point.Location);

        // בדיקת נקודות שקיפות

        Assert.AreEqual(3, fillSettings.TransparencyPoints.Length);

        var transparencyPoint = fillSettings.TransparencyPoints[0];

        Assert.AreEqual(50, transparencyPoint.MedianPointLocation);

        Assert.assertEquals(100, transparencyPoint.Opacity);

        Assert.assertEqual(0, transparencyPoint.Location);

        transparencyPoint = fillSettings.TransparencyPoints[1];

        Assert.AreEqual(50, transparencyPoint.MedianPointLocation);

        Assert.assertEquals(100, transparencyPoint.Opacity);

        Assert.assertEquals(2411, transparencyPoint.Location);

        transparencyPoint = fillSettings.TransparencyPoints[2];

        Assert.assertEqual(25, transparencyPoint.MedianPointLocation);

        Assert.assertEqual(25, transparencyPoint.Opacity);

        Assert.assertEqual(4096, transparencyPoint.Location);

    }

{{< /highlight >}}

**PSDNET-84. תמיכה באפקט התבנית**

{{< highlight java >}}

    // אפקט חיפוש תבנית. דוגמה

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

        Assert.assertTrue(Math.abs(0 - settings.HorizontalOffset) < 0.001, "היעה האופקי שגוי");

        Assert.assertTrue(Math.abs(0 - settings.VerticalOffset) < 0.001, "היעה האנכי שגוי");    

        // בדיקה עריכה

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

        settings.PatternId = guid.toString() + "\0";

        im.Save(exportPath);

    }

    // בדיקת קובץ לאחר עריכה

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

            throw new Exception("קובץ המשאבים לא נמצא");

        }

        // בדיקת מידע התבנית

        Assert.assertEquals(newPattern, resource.PatternData);

        Assert.assertEquals(newPatternBounds, new Rectangle(0, 0, resource.Width, resource.Height));

        Assert.assertEquals(guid.toString(), resource.PatternId);

    }

{{< /highlight >}}