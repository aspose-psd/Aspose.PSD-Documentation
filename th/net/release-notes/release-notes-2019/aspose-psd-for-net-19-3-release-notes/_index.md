---
title: อ้างอิง Aspose.PSD สำหรับ .NET 19.3 - บันทึกการปล่อย
type: docs
weight: 100
url: /th/net/aspose-psd-for-net-19-3-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีบันทึกการปล่อยสำหรับ Aspose.PSD สำหรับ .NET 19.3

{{% /alert %}} 

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-104|การแสดงผลของเลเยอร์ข้อความที่หมุนด้วย TransformMatrix|คุณลักษณะ|
|PSDNET-96|การนำเข้าการแสดงผลของ Stroke effect พร้อมกับ Color Fill สำหรับการส่งออก|คุณลักษณะ|
|PSDNET-112|InnerData Transformers เสียหายบางเลเยอร์ที่มีการแมสก์เวกเตอร์|ข้อผิดพลาด|
|PSDNET-113|การอัพเดตเลเยอร์ข้อความสำหรับภาพ PSD ทำให้ข้อผิดพลาดเมื่อเปิดใน Photoshop|ข้อผิดพลาด|

## **การเปลี่ยนแปลงของ Public API**
# **API เพิ่มเติม:**
- ไม่มี
# **API ถูกลบ:**
- ไม่มี

## **ตัวอย่างการใช้งาน:**
**PSDNET-104. การแสดงผลของเลเยอร์ข้อความที่หมุนด้วย TransformMatrix**

{{< highlight java >}}

 string sourceFileName = "TransformedText.psd";

string exportPath = "TransformedTextExport.psd";

string exportPathPng = "TransformedTextExport.png";

var im = (PsdImage) Image.Load(sourceFileName);

using(im) {

 im.Save(exportPath);

 im.Save(exportPathPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

}      

{{< /highlight >}}

**PSDNET-96. การนำเข้าการแสดงผลของ Stroke effect พร้อมกับ Color Fill สำหรับการส่งออก**

{{< highlight java >}}

  // การดำเนินการแสดงผลของ Stroke effect พร้อมกับ Color Fill สำหรับการส่งออก

 string sourceFileName = "StrokeComplex.psd";

 string exportPath = "StrokeComplexRendering.psd";

 string exportPathPng = "StrokeComplexRendering.png";

 var loadOptions = new PsdLoadOptions() {

  LoadEffectsResource = true

 };

 using(var im = (PsdImage) Image.Load(sourceFileName, loadOptions)) {

  for (int i = 0; i < im.Layers.Length; i++) {

   var effect = (StrokeEffect) im.Layers[i].BlendingOptions.Effects[0];

   var settings = (ColorFillSettings) effect.FillSettings;

   settings.Color = Color.DeepPink;

  }

  // บันทึก psd

  im.Save(exportPath, new PsdOptions());

  // บันทึก png

  im.Save(exportPathPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. InnerData Transformers เสียหายบางเลเยอร์ที่มีการแมสก์เวกเตอร์**

{{< highlight java >}}

 // InnerData Transformers เสียหายบางเลเยอร์ที่มีการแมสก์เวกเตอร์

var sourceFile = "1.psd";

var pngPath = "RotateFlipTest2617.png";

var psdPath = "RotateFlipTest2617.psd";

var flipType = RotateFlipType.Rotate270FlipXY;

using(var im = (PsdImage)(Image.Load(sourceFile))) {

 im.RotateFlip(flipType);

 im.Save(pngPath, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

 im.Save(psdPath);

}

{{< /highlight >}}

**PSDNET-113. การอัพเดตเลเยอร์ข้อความสำหรับภาพ PSD ทำให้ข้อผิดพลาดเมื่อเปิดใน Photoshop**

{{< highlight java >}}

 string sourceFileName = "Test.psd";

string exportPath = "Result.psd";

using(Image image = Image.Load(sourceFileName)) {

 if (!(image is PsdImage)) {

  return;

 }

 PsdImage psdImage = (PsdImage) image;

 Layer[] layers = psdImage.Layers;

 for (int index = layers.Length - 1; index >= 0; index--) {

  Layer layer = layers[index];

  if (!(layer is TextLayer)) {

   continue;

  }

  TextLayer textLayer = (TextLayer) layer;

  textLayer.UpdateText("\\()");

 }

 PsdOptions imageOptions = new PsdOptions(psdImage);

 psdImage.Save(exportPath, imageOptions);

}

// ไฟล์ต้องเปิดโดยไม่มีข้อยกเว้นและต้องสามารถอ่านได้สำหรับ Photoshop

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
