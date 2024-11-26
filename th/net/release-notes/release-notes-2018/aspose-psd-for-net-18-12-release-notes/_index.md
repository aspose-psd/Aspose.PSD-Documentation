---
title: บันทึกการปล่อย Aspose.PSD สำหรับ .NET 18.12
type: เอกสาร
weight: 10
url: /th/net/aspose-psd-for-net-18-12-release-notes/
---

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-76|การรองรับของเส้น Stroke|คุณลักษณะ|
|PSDNET-83|การรองรับอินดี้เกรเดียนท์ Effect|คุณลักษณะ|
|PSDNET-84|การรองรับพอตเทิร์น Effect|คุณลักษณะ|
|PSDNET-89|ทำให้สามารถเพิ่มเลเยอร์ทั่วไปที่สร้างขึ้นใหม่ลงใน PsdImage|คุณลักษณะ|
|PSDNET-93|หลังจากอัปเดตเนื้อหาเลเยอร์ข้อความด้วยเครื่องหมาย \ (เครื่องล่าง) ไฟล์ผลลัพธ์ไม่สามารถเปิดใน Photoshop|ข้อผิดพลาด|
|PSDNET-39|รูปถ่ายเสียหลังจากส่งออกกับข้อมูลรูปภาพที่ใหญ่เกินไปในโหมดสี CMYK|ข้อผิดพลาด|
|PSDNET-52|เป็นไปได้: การหมุนใน PSD ไม่ทำงาน|ข้อผิดพลาด|
|PSDNET-88|เป็นไปได้: เมธอดการครอบใน Aspose.Psd ไม่ทำงาน|ข้อปรับปรุง|

## **การเปลี่ยนแปลง API สาธารณะ**

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

## **ตัวอย่างการใช้:**
**PSDNET-76. การรองรับของเส้น Stroke**

**1) ชนิดการเติม - พอตเทิร์น**

{{< highlight java >}}

     // ผลกระทบของเส้น Stroke. ชนิดการเติม - พอตเทิร์น. ตัวอย่าง

    string sourceFileName = "Stroke.psd";

    string exportPath = "StrokePatternChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    // เตรียมข้อมูลใหม่

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

         Assert. 

..Continued..
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
                resource = (PattResource)