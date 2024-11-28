---
title: Aspose.PSD for .NET 19.4 - บันทึกการอัปเดต
type: สารบัญ
weight: 90
url: /th/net/aspose-psd-for-net-19-4-release-notes/
---

{{% alert color="primary" %}}

หน้านี้ประกอบด้วยบันทึกการอัปเดตสำหรับ Aspose.PSD for .NET 19.4

{{% /alert %}}

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-87|สร้างคุณสมบัติในการโหลดไฟล์รูปภาพ JPEG/PNG/etc เข้ามาใน PsdImage โดยไม่ต้องโหลดโดยตรง(ซึ่งไม่ได้รับการสนับสนุนใน Aspose.PSD)|คุณสมบัติ|
|PSDNET-120|สนับสนุน RGB Color mode ด้วย 16 bits/channel (64 bits ต่อสี)|คุณสมบัติ|
|PSDNET-108|สนับสนุน Layer Vector Masks และ Text Layer Custom FlipRotate|คุณสมบัติ|
|PSDNET-99|ตัวละครภาษาเอเชียทั้งหมดไม่ถูกเรนเดอร์อย่างถูกต้อง|ข้อบกพร่อง|
|PSDNET-116|สัญลักษณ์ \r\n ถูกตีความเป็นการขึ้นบรรทัดสองซึ่งผิด|ข้อบกพร่อง|
|PSDNET-117|หาก TextLayer ถูกอัปเดตด้วยสตริงที่ประกอบด้วย LineBreaks แล้วไฟล์ PSD กลายเป็นไม่อ่านได้|ข้อบกพร่อง|
|PSDNET-118|หาก TextLayer ถูกอัปเดตด้วยสตริงที่ประกอบด้วยสัญลักษณ์แท็บ การประมวลผลล้มเหลวพรัองกระตุ้นข้อยกเว้น|ข้อบกพร่อง|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
# **API ที่ถูกลบ:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- ...

## **ตัวอย่างการใช้:**
**PSDNET-87. สร้างคุณสมบัติในการโหลดไฟล์รูปภาพ JPEG/PNG/etc เข้ามาใน PsdImage โดยไม่ต้องโหลดโดยตรง(ซึ่งไม่ได้รับการสนับสนุนใน Aspose.PSD)**

{{< highlight java >}}

 string filePath = "PsdExample.psd";

string outputFilePath = "PsdResult.psd";

using(var image = new PsdImage(200, 200)) {

 using(var im = Image.Load(filePath)) {

  Layer layer = null;

  try {

   layer = new Layer((RasterImage) im);

   image.AddLayer(layer);

  } catch (Exception e) {

   if (layer != null) {

    layer.Dispose();

   }

   throw;

  }

 }

 image.Save(outputFilePath);

}  

{{< /highlight >}}

**PSDNET-120. สนับสนุน RGB Color mode ด้วย 16 bits/channel (64 bits ต่อสี)**

{{< highlight java >}}

  // สนับสนุน RGB Color mode ด้วย 16 bits/channel (64 bits ต่อสี)

string sourceFileName = "inRgb16.psd.psd";

string outputFilePathJpg = "outRgb16.jpg";

string outputFilePathPsd = "outRgb16.psd";

var options = new PsdLoadOptions();

using(PsdImage image = (PsdImage) Image.Load(sourceFileName, options)) {

 image.Save(outputFilePathPsd, new PsdOptions(image));

 image.Save(outputFilePathJpg, new JpegOptions() {

  Quality = 100

 });

}

// ไฟล์ต้องเปิดโดยไม่มีข้อยกเว้นและต้องสามารถอ่านได้สำหรับ Photoshop    

using(Image image = Image.Load(outputFilePathPsd)) {}  

{{< /highlight >}}

**PSDNET-108. สนับสนุน Layer Vector Masks และ Text Layer Custom FlipRotate**

{{< highlight java >}}

 // การดำเนินการ RotateFlip ไม่ทำงานตามที่คาดหวังกับ PSD

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

**PSDNET-99. ตัวละครภาษาเอเชียทั้งหมดไม่ถูกเรนเดอร์อย่างถูกต้อง**

[**กรุณาตรวจสอบไฟล์ตัวอย่างที่แนบ**](attachments/86278147/86343681.cs)

**PSDNET-116. สัญลักษณ์ \r\n ถูกตีความเป็นการขึ้นบรรทัดสองซึ่งผิด**

{{< highlight java >}}

 // สัญลักษณ์ \r\n ถูกตีความเป็นการขึ้นบรรทัดสองซึ่งผิด

string sourceFileName = "TextTest.psd";

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

  textLayer.UpdateText("First Paragraph\r\nSecond Paragraph\rThird paragraph\nFourth Paragraph");

 }

 PsdOptions imageOptions = new PsdOptions(psdImage);

 psdImage.Save(exportPath, imageOptions);

}

// ไฟล์ต้องเปิดโดยไม่มีข้อยกเว้นและต้องสามารถอ่านได้สำหรับ Photoshop ต้องมี 3 การขึ้นบรรทัดหนึ่งระหว่างทุกแถว

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}



**PSDNET-117. หาก TextLayer ถูกอัปเดตด้วยสตริงที่ประกอบด้วย LineBreaks แล้วไฟล์ PSD กลายเป็นไม่อ่านได้**

{{< highlight java >}}

 // หาก TextLayer ถูกอัปเดตด้วยสตริงที่ประกอบด้วย LineBreaks แล้วไฟล์ PSD กลายเป็นไม่อ่านได้.

string sourceFileName = "TextTest.psd";

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

  textLayer.UpdateText("First Paragraph\r\nSecond Paragraph\r\nThird paragraph\r\nFourth Paragraph");

 }

 PsdOptions imageOptions = new PsdOptions(psdImage);

 psdImage.Save(exportPath, imageOptions);

}

// ไฟล์ต้องเปิดโดยไม่มีข้อยกเว้นและต้องสามารถอ่านได้สำหรับ Photoshop

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}



**PSDNET-118. หาก TextLayer ถูกอัปเดตด้วยสตริงที่ประกอบด้วยสัญลักษณ์แท็บ การประมวลผลล้มเหลวพรัองกระยัร้กเว้น**

{{< highlight java >}}

 // หาก TextLayer ถูกอัปเดตด้วยสตริงที่ประกอบด้วยสัญลักษณ์แท็บ การประมวลผลล้มเหลวพรัองกระยัร้กเว้น

string sourceFileName = "TextTest.psd";

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

  textLayer.UpdateText("Starting Text\tText After Tab");

 }

 PsdOptions imageOptions = new PsdOptions(psdImage);

 psdImage.Save(exportPath, imageOptions);

}

// ไฟล์ต้องเปิดโดยไม่มีข้อยกเว้นและต้องสามารถอ่านได้สำหรับ Photoshop

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}