---
title: گزارش انتشار Aspose.PSD برای .NET 19.2
type: docs
weight: 110
url: /fa/net/aspose-psd-for-net-19-2-release-notes/
---

{{% alert color="primary" %}} 

این صفحه حاوی یادداشت‌های انتشار Aspose.PSD برای .NET 19.2 است.

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-97|افزودن پشتیبانی از لایه‌های پرکردن: پرکردن رنگ|ویژگی|
|PSDNET-98|افزودن پشتیبانی از لایه‌های پرکردن: پرکردن گرادیان|ویژگی|
|PSDNET-105|پشتیبانی از منبع GdFl|ویژگی|
|PSDNET-106|پشتیبانی از منبع Vmsk|ویژگی|
|PSDNET-109|انتقال منابع واقعی Aspose.Imaging به Aspose.PSD|افزایش کیفیت|
|PSDNET-92|افزودن پشتیبانی از بارگذاری جزئی برای برخی از متد‌ها|افزایش کیفیت|
|PSDNET-110|کاهش عملکرد PSD چندین بار|اشکال|

## **تغییرات در API عمومی**
# **API‌های اضافه شده:**
- T:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.FillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.FillType
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.GradientName
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Gradient
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Pattern
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IColorFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IColorFillSettings.Color
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IFillSettings.FillType
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.TransparencyPoints
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint.MedianPointLocation
- T:Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint.MedianPointLocation
- M:Aspose.PSD.Extensions.RectangleExtensions.UnionWith(Aspose.PSD.RectangleF,Aspose.PSD.RectangleF)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.Points
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.IsLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.IsOpen
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.ClipboardRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.ClipboardRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.ClipboardRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.IsFillStartsWithAllPixels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.IsOpen
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathFillRuleRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathFillRuleRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathFillRuleRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecord.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecordFactory
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecordFactory.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecordFactory.ProducePathRecord(System.Byte[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.ClosedSubpathLengthRecord
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.ClosedSubpathBezierKnotLinked
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.ClosedSubpathBezierKnotUnlinked
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.OpenSubpathLengthRecord
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.OpenSubpathBezierKnotLinked
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.OpenSubpathBezierKnotUnlinked
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.PathFillRuleRecord
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.ClipboardRecord
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.InitialFillRuleRecord
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FillLayerResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FillLayerResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FillLayerResource.Signature
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientInterval
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.AlignWithLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.VerticalOffset
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseFillSettings.FillType
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.FillType
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.MedianPointLocation
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.TransparencyPoints
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.AddColorPoint
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.AddTransparencyPoint
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint.MedianPointLocation
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Linked
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PointType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternId
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.VerticalOffset
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Linear
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Radial
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Angle
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Reflected
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Diamond
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.ShapeBurst
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint)
- M:Aspose.PSD.FileFormats.P### **SDNET-92. افزودن پشتیبانی از بارگذاری جزئی برای برخی متد‌ها**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.GenerateLfx2ResourceNodes

### **SDNET-110. کاهش عملکرد PSD چندین بار**
{{< highlight java >}}
  // PSD عملکرد چندین بار کاهش یافت
string نام_فایل_منبع = "1.psd";

string outFileNamePng = "imaging3203.png";

string outFileNamePsd = "imaging3203.psd";

var watch = new Stopwatch();

با استفاده از (PsdImage image = Image.Load(sourceFileName) as PsdImage) {

 watch.Start();

 image.Save(outFileNamePng, new PngOptions() {

  نوع_رنگ = PngColorType.TruecolorWithAlpha

 });

 image.Save(outFileNamePsd, new PsdOptions());

 watch.Stop();

}

Console.WriteLine("زمان گذشته: ", watch.Elapsed);
{{< /highlight >}}

## **نمونه‌های استفاده:**
**PSDNET-97. افزودن پشتیبانی از لایه‌های پرکردن: پرکردن رنگ**
{{< highlight java >}}
 // افزودن پشتیبانی از لایه‌های پرکردن: پرکردن رنگ

نام_فایل_منبع = "ColorFillLayer.psd";

exportPath = "ColorFillLayer_output.psd";

exportPathPng = "ColorFillLayer_output.png";

var im = (PsdImage) Image.Load(sourceFileName);

با استفاده از(im) {

 foreach(var layer in im.Layers) {

  if (layer is FillLayer) {

   var fillLayer = (FillLayer) layer;

   if (fillLayer.FillSettings.FillType != FillType.Color) {

    throw new Exception("لایه پرکردن نادرست است");

   }

   var settings = (IColorFillSettings) fillLayer.FillSettings;

   settings.Color = رنگ.قرمز;

   fillLayer.Update(); 

   im.Save(exportPath);  

   break;

  }

 }
}
{{< /highlight >}}

**PSDNET-98. افزودن پشتیبانی از لایه‌های پرکردن: پرکردن گرادیان**
{{< highlight java >}}
 // پشتیبانی از لایه پرکردن گرادیان

نام_فایل_منبع = "ComplexGradientFillLayer.psd";

outputFile = "ComplexGradientFillLayer_output.psd";

var im = (PsdImage) Image.Load(sourceFileName);

با استفاده از(im) {

 foreach(var layer in im.Layers) {

  if (layer is FillLayer) {

   var fillLayer = (FillLayer) layer;

   if (fillLayer.FillSettings.FillType != FillType.Gradient) {

    throw new Exception("لایه پرکردن نادرست است");

   }

   var settings = (IGradientFillSettings) fillLayer.FillSettings;

   if (

    Math.Abs(settings.Angle - 45) > 0.25 ||

    settings.Dither != true ||

    settings.AlignWithLayer != false ||

    settings.Reverse != false ||

    Math.Abs(settings.HorizontalOffset - (-39)) > 0.25 ||

    Math.Abs(settings.VerticalOffset - (-5)) > 0.25 ||

    settings.TransparencyPoints.Length != 3 ||

    settings.ColorPoints.Length != 2 ||

    Math.Abs(100.0 - settings.TransparencyPoints[0].Opacity) > 0.25 ||

    settings.TransparencyPoints[0].Location != 0 ||

    settings.TransparencyPoints[0].MedianPointLocation != 50 ||

    settings.ColorPoints[0].Color != رنگ.FromArgb(203, 64, 140) ||

    settings.ColorPoints[0].Location != 0 ||

    settings.ColorPoints[0].MedianPointLocation != 50) {

    throw new Exception("پرکردن گرادیان به درستی خوانده نشده است");

   }

   settings.Angle = 0.0;

   settings.Dither = false;

   settings.AlignWithLayer = true;

   settings.Reverse = true;

   settings.HorizontalOffset = 25;

   settings.VerticalOffset = -15;

   var colorPoints = new List < IGradientColorPoint > (settings.ColorPoints);

   var transparencyPoints = new List < IGradientTransparencyPoint > (settings.TransparencyPoints);

   colorPoints.Add(new GradientColorPoint() {

    Color = رنگ.بنفش,

     Location = 4096,

     MedianPointLocation = 75

   });

   colorPoints[1].Location = 3000;

   transparencyPoints.Add(new GradientTransparencyPoint() {

    Opacity = 80.0,

     Location = 4096,

     MedianPointLocation = 25

   });

   transparencyPoints[2].Location = 3000;

   settings.ColorPoints = colorPoints.ToArray();

   settings.TransparencyPoints = transparencyPoints.ToArray();

   fillLayer.Update();

   im.Save(outputFile, new PsdOptions(im));

   break;

  }

 }

}
{{< /highlight >}}