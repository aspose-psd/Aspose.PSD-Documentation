---
title: Aspose.PSD for .NET 19.2 - บันทึกการอัปเดต
type: docs
weight: 110
url: /th/net/aspose-psd-for-net-19-2-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีเอกสารการอัปเดตสำหรับ Aspose.PSD สำหรับ .NET 19.2

{{% /alert %}} 

| **Key**   | **สรุป**    | **ประเภท**    |
| :- | :- | :- |
| PSDNET-97  | เพิ่มการสนับสนุนฟิลเลเยอร์: การเติมสี      | คุณลักษณะ    |
| PSDNET-98  | เพิ่มการสนับสนุนฟิลเลเยอร์: การเติมแบบไหล     | คุณลักษณะ    |
| PSDNET-105 | การสนับสนุน GdFlResource     | คุณลักษณะ    |
| PSDNET-106 | การสนับสนุน VmskResource     | คุณลักษณะ    |
| PSDNET-109 | การโอนย้ายข้อมูลที่เป็นความจำจริงจาก Aspose.Imaging ไป Aspose.PSD | การปรับปรุง    |
| PSDNET-92  | เพิ่มการสนับสนุนการโหลดบางส่วนสำหรับบางวิธี | การปรับปรุง    |
| PSDNET-110 | ความสามารถในการทำงานของ PSD ลดลงหลายครั้ง | ข้อผิดพลาด    |

## **การเปลี่ยนแปลงทาง API สาธารณะ**
# **เพิ่ม API:**
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
- ...

## **ตัวอย่างการใช้:**
**PSDNET-97. เพิ่มการสนับสนุนฟิลเลเยอร์: การเติมสี**

{{< highlight java >}}

 // Add support of Fill layers: Color fill

string sourceFileName = "ColorFillLayer.psd";

string exportPath = "ColorFillLayer_output.psd";

string exportPathPng = "ColorFillLayer_output.png";

var im = (PsdImage) Image.Load(sourceFileName);

using(im) {

 foreach(var layer in im.Layers) {

  if (layer is FillLayer) {

   var fillLayer = (FillLayer) layer;

   if (fillLayer.FillSettings.FillType != FillType.Color) {

    throw new Exception("Wrong Fill Layer");

   }

   var settings = (IColorFillSettings) fillLayer.FillSettings;

   settings.Color = Color.Red;

   fillLayer.Update(); 

   im.Save(exportPath);   

   break;

  }

 }

}

{{< /highlight >}}

**PSDNET-98. เพิ่มการสนับสนุนฟิลเลเยอร์: การเติมแบบไหล**

{{< highlight java >}}

 // Support of Gradient Fill Layer

string sourceFileName = "ComplexGradientFillLayer.psd";

string outputFile = "ComplexGradientFillLayer_output.psd";

var im = (PsdImage) Image.Load(sourceFileName);

using(im) {

 foreach(var layer in im.Layers) {

  if (layer is FillLayer) {

   var fillLayer = (FillLayer) layer;

   if (fillLayer.FillSettings.FillType != FillType.Gradient) {

    throw new Exception("Wrong Fill Layer");

   }

   var settings = (IGradientFillSettings) fillLayer.FillSettings;

   if (...

...

{{< /highlight >}}
**PSDNET-98. เพิ่มการสนับสนุนฟิลเลเยอร์: การเติมแบบไหล**

{{< highlight java >}}

 // Support of Gradient Fill Layer

string sourceFileName = "ComplexGradientFillLayer.psd";

string outputFile = "ComplexGradientFillLayer_output.psd";

var im = (PsdImage) Image.Load(sourceFileName);

using(im) {

 foreach(var layer in im.Layers) {

  if (layer is FillLayer) {

   var fillLayer = (FillLayer) layer;

   if (fillLayer.FillSettings.FillType != FillType.Gradient) {

    throw new Exception("Wrong Fill Layer");

   }

   var settings = (IGradientFillSettings) fillLayer.FillSettings;

   if (...

...

{{< /highlight >}}

 **PSDNET-105. การสนับสนุน GdFlResource**

 {{< highlight java >}}

  // การสนับสนุน GdFlResource

string sourceFileName = "ComplexGradientFillLayer.psd";

string exportPath = "ComplexGradientFillLayer_after.psd";

var im = (PsdImage) Image.Load(sourceFileName);

using(im) {

 foreach(var layer in im.Layers) {

  if (layer is FillLayer) {

   var fillLayer = (FillLayer) layer;

   var resources = fillLayer.Resources;

   foreach(var res in resources) {

    if (res is GdFlResource) {

     // การอ่าน

     var resource = (GdFlResource) res;

     if (...

...

{{< /highlight >}}

 **PSDNET-106. การสนับสนุน VmskResource**

 {{< highlight java >}}

  // การสนับสนุน VmskResource

static void ExampleOfVmskResourceSupport() {

 string sourceFileName = "Rectangle.psd";

 string exportPath = "Rectangle_changed.psd";

 var im = (PsdImage) Image.Load(sourceFileName);

 using(im) {

  var resource = GetVmskResource(im);

  // การอ่าน

  if (...

...

{{< /highlight >}}

 **PSDNET-110. ความสามารถในการทำงานของ PSD ลดลงหลายครั้ง**

 {{< highlight java >}}

  // ความสามารถในการทำงานของ PSD ลดลงหลายครั้ง

string sourceFileName = "1.psd";

string outFileNamePng = "imaging3203.png";

string outFileNamePsd = "imaging3203.psd";

var watch = new Stopwatch();

using(PsdImage image = Image.Load(sourceFileName) as PsdImage) {

 watch.Start();

 image.Save(outFileNamePng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

 image.Save(outFileNamePsd, new PsdOptions());

 watch.Stop();

}

Console.WriteLine("ELAPSED: ", watch.Elapsed);

{{< /highlight >}}