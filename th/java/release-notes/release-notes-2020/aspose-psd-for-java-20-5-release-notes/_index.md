---
title: Aspose.PSD for Java 20.5 - บันทึกการอัปเดต
type: docs
weight: 40
url: /th/java/aspose-psd-for-java-20-5-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD for Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) {{% /alert %}} 

|**คีย์**|**สรุป**|**ประเภท**|
| :- | :- | :- |
|PSDJAVA-188|Support for document conversion progress|คุณลักษณะ|
|PSDJAVA-197|Support of Grayscale ColorMode PSD Image saving with 16 bit per channel|คุณลักษณะ|
|PSDJAVA-198|Support of Nvrt Resource (Invert Adjustment Layer Resource)|คุณลักษณะ|
|PSDJAVA-200|` `Support of Layer Masks for Layer Groups|คุณลักษณะ|
|PSDJAVA-195|Fix saving PSD image with Grayscale ColorMode 16 bit per channel to 16bit per channel RGB PSD format|ปัญหา|
|PSDJAVA-196|Fix saving PSD image with Grayscale ColorMode 16 bit per channel to 8 bit per channel Grayscale PSD format|ปัญหา|
|PSDJAVA-199|การจัดวางข้อความผ่าน ITextPortion ไม่ทำงานสำหรับภาษาจากขวาไปซ้าย ไฟล์ผลลัพธ์เสียหาย|ปัญหา|
|PSDJAVA-201|ข้อยกเว้นเมื่อพยายามเปิดไฟล์ Psd ที่เฉพาะเจา Lab Color และ 8 bit/channel|ปัญหา|
# **การเปลี่ยนแปลงใน Public API**
# **API ที่เพิ่มเข้าไป:**
- ไม่มี
## **API ที่เอาออก:**
- ไม่มี
# **ตัวอย่างการใช้:**

**PSDJAVA-188. การสนับสนุนสำหรับความคืบหน้าของการแปลงเอกสาร**

{{< highlight java >}}

 // ตัวอย่างการใช้งานตัวจัดการความคืบหน้าสำหรับการโหลดและบันทึกข้อมูล

// โปรแกรมใช้ตัวเลือกการบันทึกที่แตกต่างกันเพื่อเรียกเหตุการณ์ความคืบหน้า

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// สร้างตัวจัดการความคืบหน้าที่เขียนข้อมูลความคืบหน้าไปยังคอนโซล

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s out of %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- กำลังโหลด Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Bind ตัวจัดการความคืบหน้าเพื่อแสดงความคืบหน้าการโหลด

loadOptions.setProgressEventHandler(localProgressEventHandler);

// โหลด PSD โดยใช้ตัวเลือกการโหลดเฉพาะ

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- กำลังบันทึก Apple.psd เป็นรูปแบบ PNG ----------");

    PngOptions pngOptions = new PngOptions();

    // ทำให้ภาพเป็นสีและไม่มีความโปร่งใส

    pngOptions.setColorType(PngColorType.Truecolor);

    // Bind ตัวจัดการความคืบหน้าเพื่อแสดงความคืบหน้าการบันทึก

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // แปลง PSD เป็น PNG ด้วยลักษณะที่เฉพาะเจา

    image.save(outputStream, pngOptions);

    System.out.println("---------- กำลังบันทึก Apple.psd เป็นรูปแบบ PSD ----------");

    PsdOptions psdOptions = new PsdOptions();

    // ทำให้ PSD สี

    psdOptions.setColorMode(ColorModes.Rgb);

    // กำหนดช่องสำหรับแต่ละสี (แดง เขียว และน้ำเงิน) รวมทั้งช่องผสม

    psdOptions.setChannelsCount((short)4);

    // Bind ตัวจัดการความคืบหน้าเพื่อแสดงความคืบหน้าการบันทึก

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // บันทึกสำเนาของ PSD ด้วยลักษณะที่เฉพาะเจา

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. การสนับสนุนการบันทึกภาพ PSD โหมดสี Grayscale 16 bit ต่อช่อง**

{{< highlight java >}}

 // ตัวอย่างการใช้งานการเปลี่ยนสีโหมด การแบ่งช่อง และการบีบอัดสำหรับเลเยอร์ที่ระบุไว้ล่่าสุดมาก

// ทำให้เมทอดสามารถเข้าถึงจากขอบเขตท้องเรื่อง

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String file,

            short colorMode,

            short channelBitsCount,

            short channelsCount,

            short compression,

            int layerNumber)

    {

        String filePath = file + ".psd";

        String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +

                channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);

        String exportPath = file + postfix + ".psd";

        String pngExportPath = file + postfix + ".png";

        // โหลด PSD ที่กำหนดไว้อัตโนมัติ 16 บิต

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // วาดเส้ในสีเทารอบรอบขอบของเลเยอร์

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // บันทึกสำเนาของ PSD ด้วยลักษณะที่เฉพาะเจา

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(colorMode);

            psdOptions.setChannelBitsCount(channelBitsCount);

            psdOptions.setChannelsCount(channelsCount);

            psdOptions.setCompressionMethod(compression);

            image.save(exportPath, psdOptions);

        }

        finally

        {

            image.dispose();

        }

        // โหลด PSD ที่บันทึกไว้

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            //convert  PSD ที่บันทึกไว้เป็น  PNG

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); 

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. Support of Nvrt Resource (Invert Adjustment Layer Resource)**

{{< highlight java >}}

 // ตัวอย่างการค้นหา NvrtResource ของชั้นการปรับแก้ไขการกลับสี

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// โหลด PSD ที่กำหนดไว้อัตโนมัติ 16 บิต

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // พยายามหาทรัพยากรของชั้นการปรับแก้ไขการกลับสี

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // พบ NvrtResource

                    nvrtResource = (NvrtResource)layerResource;

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-200. Support of Layer Masks for Layer Groups**

{{< highlight java >}}

 // ตัวอย่างการสนับสนุนการใช้งานแมสก์ชั้นสําหรับกลุ่มชั้น เปิดและบันทึก PSD ในรูปแบบที่แตกต่างๆโดยไม่เกิดข้อยกเว้น

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// โหลด PSD ที่กำหนดไว้

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // แปลง PSD ที่โหลดมาเป็น PNG

    input.save(outputPng, new PngOptions());

    // บันทึกสำเนาของ PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. แก้ไขปัญหาการบันทึกภาพ PSD โหมดสี Grayscale 16 bit ต่อช่องเป็นรูปแบบ 16bit ต่อช่องภาพ PSD แบบ RGB**

{{< highlight java >}}

 // ตัวอย่างการแปลง PSD 16-bit grayscale เป็น 16-bit RGB และกลับไปเป็น grayscale 16 bit แต่รูปภาพ

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// โหลด PSD ที่กำหนดไว้

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // วาดเส้ในสีเทารอบรอบขอบของเลเยอร์

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // บันทึกสำเนาของ PSD ด้วยการเปลี่ยนโหมดสีเป็น RBG

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Rgb);

    psdOptions.setChannelBitsCount((short)16);

    psdOptions.setChannelsCount((short)4);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// โอดยี่ห้ PSD ที่บันทึกไว้

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // แปลง PSD ที่บันทึกไว้เป็น PNG

    image1.save(pngExportPath, pngOptions); // ที่นี่ไม่ควรมีข้อยกเว้น

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. แก้ไขปัญหาการบันทึกภาพ PSD โหมดสี Grayscale 16 bit ต่อช่องเป็นรูปแบบ 8 bit ต่อช่องภาพ PSD แบบ Grayscale**

{{< highlight java >}}

 // ตัวอย่างการแปลง PSD 16-bit grayscale เป็น 8-bit grayscale และกลับเป็นภาพรวม

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// โหลด PSD ที่กำหนดไว้

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // วาดเส้ในสีเทารอบรอบขอบของเลเยอร์

    Graphics graphics = new Graphics(raster