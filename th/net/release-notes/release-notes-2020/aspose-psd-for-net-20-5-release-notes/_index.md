---
title: บันทึกการปล่อย Aspose.PSD สำหรับ .NET 20.5
type: การเอกสาร
weight: 80
url: /th/net/aspose-psd-for-net-20-5-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีบันทึกการปล่อยสำหรับ [Aspose.PSD for .NET 20.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-595|การสนับสนุนของ Layer Masks สำหรับ Layer Groups|คุณลักษณะ|
|PSDNET-201|การสนับสนุนสำหรับความคืบหน้าในการแปลงเอกสาร|คุณลักษณะ|
|PSDNET-275|การสนับสนุนของ Nvrt Resource (Invert Adjustment Layer Resource)|คุณลักษณะ|
|PSDNET-124|การสนับสนุนสำหรับการบันทึกรูปแบบ Grayscale ColorMode PSD ด้วย 16 บิตต่อช่อง|คุณลักษณะ|
|PSDNET-589|การปรับปรุงตัวอย่างบน GitHub|การปรับปรุง|
|PSDNET-587|การจัดแนวข้อความผ่าน ITextPortion ไม่ทำงานสำหรับภาษาที่เขียนไปทางขวา ไฟล์ผลลัพธ์เสียหาย|ข้อบกพร่อง|
|PSDNET-604|ข้อยกเว้นเมื่อพยายามเปิดไฟล์ Psd โดยเฉพาะด้วยสี Lab และ 8 บิตต่อช่อง|ข้อบกพร่อง|
|PSDNET-598|การแก้ไขการบันทึกรูปภาพ PSD ด้วยโหมด Grayscale 16 บิตต่อช่องเป็นรูปแบบ PSD Grayscale 8 บิตต่อช่อง|ข้อบกพร่อง|
|PSDNET-599|การแก้ไขการบันทึกรูปภาพ PSD ด้วย Grayscale ColorMode 16 บิตต่อช่องเป็นรูปแบบ RGB PSD 16 บิตต่อช่อง|ข้อบกพร่อง|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API เพิ่มเติม:**
- ไม่มี
# **API ที่ถูกลบ:**
- ไม่มี

## **ตัวอย่างการใช้:**
**PSDNET-595. การสนับสนุนของ Layer Masks สำหรับ Layer Groups**

{{< highlight java >}}

 string srcFile = "psdnet595.psd";

string outputPng = "output.png";

string outputPsd = "output.psd";

using (var input = (PsdImage)Image.Load(srcFile))

{

     input.Save(outputPng, new PngOptions());

     input.Save(outputPsd);

}

{{< /highlight >}}

**PSDNET-201. การสนับสนุนสำหรับความคืบหน้าในการแปลงเอกสาร**

{{< highlight java >}}

 string sourceFilePath = "Apple.psd";

Stream outputStream = new MemoryStream();

ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)

{

      string message = string.Format(

           "{0} {1}: {2} out of {3}",

           progressInfo.Description,

           progressInfo.EventType,

           progressInfo.Value,

           progressInfo.MaxValue);

      Console.WriteLine(message);

};

Console.WriteLine("---------- Loading Apple.psd ----------");

var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };

using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))

{

      Console.WriteLine("---------- Saving Apple.psd to PNG format ----------");

      image.Save(

           outputStream,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler

           });

      Console.WriteLine("---------- Saving Apple.psd to PSD format ----------");

      image.Save(

           outputStream,

           new PsdOptions()

           {

                 ColorMode = ColorModes.Rgb,

                 ChannelsCount = 4,

                 ProgressEventHandler = localProgressEventHandler

           });

}

{{< /highlight >}}

**PSDNET-275. การสนับสนุนของ Nvrt Resource (Invert Adjustment Layer Resource)**

{{< highlight java >}}

 using (var psdImage = (PsdImage)Image.Load("InvertAdjustmentLayer.psd"))

{

      foreach (var layer in psdImage.Layers)

      {

           if (layer is InvertAdjustmentLayer)

           {

                 foreach (var layerResource in layer.Resources)

                 {

                      if (layerResource is NvrtResource)

                      {

                           // ทรัพยากร NvrtResource ได้รับการสนับสนุน

                           var resource = (NvrtResource)layerResource;

                           break;

                      }

                 }

           }

      }

}

{{< /highlight >}}

**PSDNET-124. การแก้ไขการบันทึกรูปภาพ PSD ด้วย Grayscale ColorMode 16 บิตต่อช่องเป็นรูปแบบ Grayscale PSD 8 บิตต่อช่อง**

{{< highlight java >}}

 void SaveToPsdThenLoadAndSaveToPng(

    string file,

    ColorModes colorMode,

    short channelBitsCount,

    short channelsCount,

    CompressionMethod compression,

    int layerNumber)

{

    string filePath = file + ".psd";

    string postfix = colorMode.ToString() + channelBitsCount + "_" + channelsCount + "_" + compression;

    string exportPath = @"Output\" + file + postfix + ".psd";

    PsdOptions psdOptions = new PsdOptions()

    {

        ColorMode = colorMode,

        ChannelBitsCount = channelBitsCount,

        ChannelsCount = channelsCount,

        CompressionMethod = compression

    };

    using (PsdImage image = (PsdImage)Image.Load(filePath))

    {

        RasterCachedImage raster = layerNumber >= 0 ? (RasterCachedImage)image.Layers[layerNumber] : image;

        Aspose.PSD.Graphics graphics = new Graphics(raster);

        int width = raster.Width;

        int height = raster.Height;

        Rectangle rect = new Rectangle(

            width / 3,

            height / 3,

            width - (2 * (width / 3)) - 1,

            height - (2 * (height / 3)) - 1);

        graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), rect);

        image.Save(exportPath, psdOptions);

    }

    string pngExportPath = Path.ChangeExtension(exportPath, "png");

    using (PsdImage image = (PsdImage)Image.Load(exportPath))

    {

        // ที่นี่ไม่ควรมีข้อยกเว้น

        image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

    }

}

SaveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, 16, 5, CompressionMethod.RLE, 0);

SaveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, 0);

SaveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

SaveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, 0);

SaveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

SaveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

SaveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDNET-587. การจัดแนวข้อความผ่าน ITextPortion ไม่ทำงานสำหรับภาษาที่เขียนไปทางขวา ไฟล์ผลลัพธ์เสียหาย.**

{{< highlight java >}}

 string sourceFileName = "bidi.psd";

string outputFileName = "bidiOutput.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    var layer = (TextLayer)image.Layers[2];

    var portions = layer.TextData.Items;

    portions[0].Paragraph.Justification = 2;

    layer.TextData.UpdateLayerData();

    image.Save(outputFileName);

}

{{< /highlight >}}

` `**PSDNET-604. ข้อยกเว้นเมื่อพยายามเปิดไฟล์ Psd โดยเฉพาะด้วยสี Lab และ 8 บิตต่อช่อง**

{{< highlight java >}}

 string srcFile = "Untitled-1.psd";

string outputFilePsd = "output.psd";

using (var psdImage = (PsdImage)Image.Load(srcFile))

{

    psdImage.Save(outputFilePsd);

}

// ไฟล์ LAB ถูกโหลดและบันทึกโดยไม่ทิ้งข้อยกเว้น

{{< /highlight >}}

**PSDNET-598. การแก้ไขการบันทึกรูปภาพ PSD ด้วย Grayscale ColorMode 16 บิตต่อช่องเป็นรูปแบบ PSD Grayscale 8 บิตต่อช่อง**

{{< highlight java >}}

 string sourceFileName = "grayscale16bit.psd";

string exportFileName = "grayscale16bit_output.psd";

PsdOptions psdOptions = new PsdOptions()

{

    ColorMode = ColorModes.Grayscale,

    ChannelBitsCount = 8,

    ChannelsCount = 2

};

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    RasterCachedImage raster = image.Layers[0];

    Aspose.PSD.Graphics graphics = new Graphics(raster);

    int width = raster.Width;

    int height = raster.Height;

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), rect);

    image.Save(exportFileName, psdOptions);

}

string pngExportPath = Path.ChangeExtension(exportFileName, "png");

using (PsdImage image = (PsdImage)Image.Load(exportFileName))

{

    // ที่นี่ไม่ควรมีข้อยกเว้น

    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}

**PSDNET-599. การแก้ไขการบันทึกรูปภาพ PSD ด้วย Grayscale ColorMode 16 บิตต่อช่องเป็นรูปแบบ RGB PSD 16 บิตต่อช่อง**

{{< highlight java >}}

 string sourceFileName = "grayscale16bit.psd";

string exportFileName = "grayscale16bit_output.psd";

PsdOptions psdOptions = new PsdOptions()

{

    ColorMode = ColorModes.Rgb,

    ChannelBitsCount = 8,

    ChannelsCount = 4

};

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    RasterCachedImage raster = image.Layers[0];

    Aspose.PSD.Graphics graphics = new Graphics(raster);

    int width = raster.Width;

    int height = raster.Height;

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), rect);

    image.Save(exportFileName, psdOptions);

}

string pngExportPath = Path.ChangeExtension(exportFileName, "png");

using (PsdImage image = (PsdImage)Image.Load(exportFileName))

{

    // ที่นี่ไม่ควรมีข้อยกเว้น

    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}
