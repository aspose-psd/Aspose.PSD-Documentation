---
title: Aspose.PSD for .NET 19.12 - บันทึกการอัปเดต
type: docs
weight: 10
url: /th/net/aspose-psd-for-net-19-12-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD for .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**รายงานสรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-11|[การรองรับเลเยอร์ที่เชื่อมโยง](/psd/th/net/working-with-layers/#workingwithlayers-supportoflinkedlayers)|คุณลักษณะ|
|PSDNET-131|[การรองรับ SoCoResource](/psd/th/net/support-of-socoresource/)|คุณลักษณะ|
|PSDNET-115|การเพิ่ม LineBreaks ไปยัง LineBreaks ที่มีอยู่หาก TextLayer ถูกอัพเดตด้วยสตริง|ข้อบกพร่อง|
|PSDNET-157|การบันทึก PSB เป็น PNG ทำให้แข็ง ไม่ตอบสนอง|ข้อบกพร่อง|
|PSDNET-250|ข้อยกเว้นในการโหลดไฟล์ PSD CMYK โดยไม่มีเลเยอร์ที่มีการบีบอัด RLE|ข้อบกพร่อง|
|PSDNET-161|ข้อยกเว้นในการอัปเดตเลเยอร์ข้อความ|ข้อบกพร่อง|
|PSDNET-222|การเปลี่ยนขนาดไฟล์ PSD บางรายการด้วยการมัสก์เลเยอร์ทำงานผิด|ข้อบกพร่อง|
|PSDNET-244|การบันทึก PSD ด้วย CultureInfo.CurrentCulture บางส่วนทำให้เกิดข้อยกเว้นในการโหลด|ข้อบกพร่อง|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **API ที่ถูกลบทิ้ง:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **ตัวอย่างการใช้:**
**PSDNET-11. การรองรับเลเยอร์ที่เชื่อมโยง**

{{< highlight java >}}

           using (var psd = (PsdImage)Image.Load("example.psd"))

            {

                Layer[] layers = psd.Layers;

                // link all layers in one linked group

                short layersLinkGroupId = psd.LinkedLayersManager.LinkLayers(layers);

                // gets id for one layer

                short linkGroupId = psd.LinkedLayersManager.GetLinkGroupId(layers[0]);

                if (layersLinkGroupId != linkGroupId)

                {

                    throw new Exception("layersLinkGroupId and linkGroupId are not equal.");

                }

                // gets all linked layers by link group id.

                Layer[] linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                // unlink each layer from group

                foreach (var linkedLayer in linkedLayers)

                {

                    psd.LinkedLayersManager.UnlinkLayer(linkedLayer);

                }

                // retrieves NULL for a link group ID that has no layers in the group.

                linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                if (linkedLayers != null)

                {

                    throw new Exception("The linkedLayers field is not NULL.");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}

**PSDNET-131. การรองรับ SoCoResource**

{{< highlight java >}}

      // การรองรับ SoCoResource

    string sourceFileName = "ColorFillLayer.psd";

    string exportPath = "SoCoResource_Edited.psd";

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

        foreach (var layer in im.Layers)

        {

            if (layer is FillLayer)

            {

                var fillLayer = (FillLayer)layer;

                foreach (var resource in fillLayer.Resources)

                {

                    if (resource is SoCoResource)

                    {

                        var socoResource = (SoCoResource)resource;

                        Assert.AreEqual(Color.FromArgb(63, 83, 141), socoResource.Color);

                        socoResource.Color = Color.Red;

                        break;

                    }

                 }

                 break;

             }

            im.Save(exportPath);

        }

    }

{{< /highlight >}}

**PSDNET-115. LineBreaks ถูกเพิ่มไปยัง LineBreaks ที่มีอยู่หาก TextLayer ถูกอัปเดตด้วยสตริง**

{{< highlight java >}}

           const string NewText = "abcdef\rzxcvbn";

        string sourceFilePath = "TestFileForAsianChars.psd");

        string outputFilePath = "result.psd";

        using (var image = (PsdImage)Image.Load(sourceFilePath))

        {

            var layer = (TextLayer)image.Layers[0];

            var imageOptions = new PsdOptions(image);

            layer.UpdateText(NewText);

            image.Save(outputFilePath, imageOptions);

        }

        using (var createdImage = (PsdImage)Image.Load(outputFilePath))

        {

            var createdLayer = (TextLayer)createdImage.Layers[0];

            if (NewText != createdLayer.Text)

            {

                throw new InvalidDataException("Updated text is invalid");

            }

        }

{{< /highlight >}}

**PSDNET-157. บันทึก PSB เป็น PNG ทำให้แข็ง**

{{< highlight java >}}

       // บันทึก PSB เป็น PNG 

    string sourceFileName = "sample.psb";

    string outFileName = "sample.png";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        PngOptions options = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

        image.Save(outFileName, options);

    }

{{< /highlight >}}



` `**PSDNET-250. ข้อยกเว้นในการโหลดไฟล์ PSD CMYK โดยไม่มีเลเยอร์ที่มีการบีบอัด RLE**

{{< highlight java >}}

     void LoadRawDataFromPsd()

        {

            string sourcePath = "CmykWithAlpha.psd";

            using (RasterImage image = (RasterImage)Image.Load(sourcePath))

            {

                var rawDataSettings = image.RawDataSettings;

                RawDataTester loader = new RawDataTester();

                image.LoadRawData(image.Bounds, rawDataSettings, loader);

            }

        }

        class RawDataTester : IPartialRawDataLoader

        {

            public void Process(Rectangle rectangle, byte[] pixels, Point start, Point end)

            {

            }

            public void Process(Rectangle rectangle, byte[] pixels, Point start, Point end, LoadOptions loadOptions)

            {

            }

        }

{{< /highlight >}}

` `**PSDNET-161. ข้อยกเว้นในการอัปเดตเลเยอร์ข้อความ**

{{< highlight java >}}

      // โหลดไฟล์ PSD เป็นภาพและแปลงเป็น PsdImage

    using (PsdImage psdImage = (PsdImage)Image.Load("example.psd"))

    {

        foreach (var layer in psdImage.Layers)

        {

            if (layer is TextLayer)

            {

                TextLayer textLayer = layer as TextLayer;

                textLayer.UpdateText("test update", new Point(0, 0), 15.0f, Color.Purple);

            }

        }

        psdImage.Save("UpdateTextLayerInPSDFile_out.psd");

    }

{{< /highlight >}}



**PSDNET-222. เปลี่ยนขนาดไฟล์ PSD บางรายการด้วยการมัสก์เลเยอร์ทำงานผิด**

{{< highlight java >}}

     int scale = 2;

        string[] names = {

                             "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

                             "LevelsLayerWithLayerMaskRgb",

                             "LevelsLayerWithLayerMaskCmyk",

                             "ColorBalanceAdjustmentLayer"

                         };

        for (int i = 0; i < names.Length; i++)

        {

            string sourceFilePath = names[i] + ".psd";

            string outputFilePath = "output_" + sourceFilePath;

            string outputPngFilePath = "output_" + names[i] + ".png";

            var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, psdLoadOptions))

            {

                image.Resize(image.Width * scale, image.Height * scale);

                image.Save(outputFilePath, new PsdOptions());

                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

        }

{{< /highlight >}}



**PSDNET-244. การบันทึก PSD ด้วย CultureInfo.CurrentCulture บางส่วนทำให้เกิดข้อยกเว้นในการโหลด**

{{< highlight java >}}

     for (int i = 0; i <= 6; i++)

        {

            string sourceFileName = string.Format("example-{0}.psd", i);

            var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

            var psdSaveOptions = new PsdOptions();

            var culture = new System.Globalization.CultureInfo("ru-RU");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentThread.CurrentUICulture = culture;

            string outputFileName = "output-" + sourceFileName;

            // Load a PSD file as an image and cast it into PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image.Resize(160, 120);

                image.Save(outputFileName, psdSaveOptions);

            }

            culture = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentThread.CurrentUICulture = culture;

            // Load a PSD file as an image and cast it into PsdImage

            using (PsdImage image2 = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image2.Resize(160, 120);

                image2.Save(outputFileName, psdSaveOptions);

            }

        }

{{< /highlight >}}