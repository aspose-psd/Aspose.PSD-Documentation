---
title: บันทึกการอัพเดท Aspose.PSD สำหรับ .NET 21.2
type: docs
weight: 110
url: /th/net/aspose-psd-for-net-21-2-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้ประกอบด้วยบันทึกการอัพเดทสำหรับ [Aspose.PSD สำหรับ .NET 21.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**สรุป**|**ประเภท**|
| :- | :- | :- |
|PSDNET-404|รองรับ vogkResource|คุณลักษณะ|
|PSDNET-809|ขอบเขตเรกของเสมาร์ตออบเจกต์ที่ไม่ถูกต้องเมื่อเราแทนที่เนื้อหาอสมาร์ตออบเจกต์ด้วยไฟล์ที่มีขนาดและความละเอียดต่างกัน|คุณลักษณะ|
|PSDNET-752|ข้อผิดพลาดไม่สามารถแปลง FillLayer เป็น SmartObjectLayer|ข้อบกพร่อง|
|PSDNET-778|LayerGroup เพิ่มเลเยอร์ใหม่ในลำดับที่กลับด้าน|ข้อบกพร่อง|
|PSDNET-790|การนำเข้าภาพในชั้น SmartObject ทำให้เกิดความเสียหายในไฟล์ PSD|ข้อบกพร่อง|
|PSDNET-810|ข้อยกเว้นในการโหลดไฟล์|ข้อบกพร่อง|
|PSDNET-824|ขอบเขต vogk ไม่ถูกต้องหลังจากโหลดและบันทึกรูปภาพ PSD ด้วยชั้นรูปและเส้นทางเวกเตอร์|ข้อบกพร่อง|
|PSDNET-827|ข้อยกเว้นในการโหลดโครงสร้าง ReferenceStructure และ EnumeratedReferenceStructure|ข้อบกพร่อง|

## **การเปลี่ยนแปลงใน Public API**
# **APIs ที่เพิ่มเข้ามา:**
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginType
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginResolution
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginShapeBox
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginRadiiRectangle
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidatedPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginIndexPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginTypePresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginResolutionPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginRadiiRectanglePresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginShapeBBoxPresent
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Left
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Top
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Right
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Bottom
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.QuadVersion
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Bounds
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.TopLeft
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.TopRight
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.BottomRight
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.BottomLeft
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.QuadVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID.#ctor(System.String,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ReplaceContents(Aspose.PSD.Image,Aspose.PSD.ResolutionSetting)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ReplaceContents(System.String,Aspose.PSD.ResolutionSetting)

# **APIs ที่ถูกลบ:**
- None

## **ตัวอย่างการใช้:**

**PSDNET-404. สนับสนุน vogkResource**

{{< highlight csharp >}}
            // ตัวอย่างนี้แสดงให้เห็นว่าการโหลดและบันทึกรูปภาพ PSD ด้วยชั้นรูปและเส้นทางเวกเตอร์ทำงานได้อย่างถูกต้อง
            string dataDir = "PSDNET404_1";
            string sourcePath = Path.Combine(dataDir, "vectorShapes.psd");
            string outputFilePath = Path.Combine(dataDir, "output_vectorShapes.psd");
            using (PsdImage image = (PsdImage)Image.Load(sourcePath))
            {
                var resource = GetVogkResource(image);
                AssertAreEqual(1, resource.ShapeOriginSettings.Length);
                var setting = resource.ShapeOriginSettings[0];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(false, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(true, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(0, setting.OriginIndex);
                var originalSetting = resource.ShapeOriginSettings[0];
                originalSetting.IsShapeInvalidated = true;
                resource.ShapeOriginSettings = new[]
                {
                    originalSetting,
                    new VectorShapeOriginSettings()
                    {
                        OriginIndex = 1,
                        OriginResolution = 144,
                        OriginType = 4,
                        OriginShapeBox = new VectorShapeBoundingBox()
                        {
                            Bounds = Rectangle.FromLeftTopRightBottom(10, 15, 40, 70)
                        }
                    },
                    new VectorShapeOriginSettings()
                    {
                        OriginIndex = 2,
                        OriginResolution = 301,
                        OriginType = 5,
                        OriginRadiiRectangle = new VectorShapeRadiiRectangle()
                        {
                            TopLeft = 2,
                            TopRight = 6,
                            BottomLeft = 23,
                            BottomRight = 42,
                            QuadVersion = 1
                        }
                    }
                };

                image.Save(outputFilePath, new PsdOptions());
            }

            using (PsdImage image = (PsdImage)Image.Load(outputFilePath))
            {
                var resource = GetVogkResource(image);
                AssertAreEqual(3, resource.ShapeOriginSettings.Length);

                var setting = resource.ShapeOriginSettings[0];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(true, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(true, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(0, setting.OriginIndex);
                AssertAreEqual(true, setting.IsShapeInvalidated);

                setting = resource.ShapeOriginSettings[1];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(false, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(true, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(1, setting.OriginIndex);
                AssertAreEqual(144.0, setting.OriginResolution);
                AssertAreEqual(4, setting.OriginType);
                AssertAreEqual(Rectangle.FromLeftTopRightBottom(10, 15, 40, 70), setting.OriginShapeBox.Bounds);

                setting = resource.ShapeOriginSettings[2];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(false, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(false, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(true, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(2, setting.OriginIndex);
                AssertAreEqual(301.0, setting.OriginResolution);
                AssertAreEqual(5, setting.OriginType);
                AssertAreEqual(2.0, setting.OriginRadiiRectangle.TopLeft);
                AssertAreEqual(6.0, setting.OriginRadiiRectangle.TopRight);
                AssertAreEqual(23.0, setting.OriginRadiiRectangle.BottomLeft);
                AssertAreEqual(42.0, setting.OriginRadiiRectangle.BottomRight);
                AssertAreEqual(1, setting.OriginRadiiRectangle.QuadVersion);
            }

            VogkResource GetVogkResource(PsdImage image)
            {
                var layer = image.Layers[1];

                VogkResource resource = null;
                var resources = layer.Resources;
                for (int i = 0; i < resources.Length; i++)
                {
                    if (resources[i] is VogkResource)
                    {
                        resource = (VogkResource)resources[i];
                        break;
                    }
                }

                if (resource == null)
                {
                    throw new Exception("VogkResource not found.");
                }

                return resource;
            }

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Objects are not equal.");
                }
            }
{{< /highlight >}}

**PSDNET-752. ข้อผิดพลาดที่ไม่สามารถแปลง FillLayer เป็น SmartObjectLayer**

{{< highlight csharp >}}
            string sourceFilePath = "effectlost.psd";
            string outputFilePath = "output.psd";

            using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFilePath))
            {
                SmartObjectLayer smartObject = psdImage.SmartObjectProvider.ConvertToSmartObject(0);

                psdImage.Save(outputFilePath);
            }
{{< /highlight >}}

**PSDNET-778. LayerGroup เพิ่มเลเยอร์ใหม่ในลำดับที่กลับด้าน**

{{< highlight csharp >}}
            void AreEqual(string expected, string actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Values are not equal.");
                }
            }

            string outputFile = "output.psd";

            PsdOptions psdOptions = new PsdOptions();
            psdOptions.Source = new StreamSource(new MemoryStream());
            using (PsdImage psdImage = (PsdImage)Image.Create(psdOptions, 100, 100))
            {
                LayerGroup layerGroup = psdImage.AddLayerGroup("Folder", 0, true);
                layerGroup.AddLayer(new Layer() { DisplayName = "Layer 1" });
                layerGroup.AddLayer(new Layer() { DisplayName = "Layer 2" });

                AreEqual("Layer 1", layerGroup.Layers[0].DisplayName);
                AreEqual("Layer 2", layerGroup.Layers[1].DisplayName);

                psdImage.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-790. Importing image in SmartObject layer results in PSD corruption**

{{< highlight csharp >}}
            const string baseFolder = "PSDNET790_1\\";
            const string outputFolder = baseFolder + "output\\";

            // ทดสอบว่าชั้นที่นำเข้าจากรูปภาพถูกแปลงเป็นชั้น SmartObject และไฟล์ PSD ที่ถูกบันทึกเป็นไฟล์ที่ถูกต้อง
            using (PsdImage image = (PsdImage)Image.Load(baseFolder + @"layerTest1.psd"))
            {

                string layerFilePath = baseFolder + @"picture.jpg";
                string outputFilePath = outputFolder + "layerTest2.psd";
                string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
                using (var stream = new FileStream(layerFilePath, FileMode.Open))
                {
                    Layer layer = null;
                    try
                    {
                        layer = new Layer(stream);
                        image.AddLayer(layer);
                    }
                    catch (Exception)
                    {
                        if (layer != null)
                        {
                            layer.Dispose();
                        }

                        throw;
                    }

                    var layer2 = image.Layers[2];
                    var layer3 = image.SmartObjectProvider.ConvertToSmartObject(image.Layers.Length - 1);
                    var bounds = layer3.Bounds;
                    layer3.Left = (image.Width - layer3.Width) / 2;
                    layer3.Top = layer2.Top;
                    layer3.Right = layer3.Left + bounds.Width;
                    layer3.Bottom = layer3.Top + bounds.Height;

                    image.Save(outputFilePath);
                    image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}

**PSDNET-809. ขอบเขตของ smart object layer ไม่ถูกต้องเมื่อเราแทนที่เนื้อหา smart object ด้วยไฟล์ที่มีขนาดและความละเอียดต่างกัน**

{{< highlight csharp >}}
            // ตัวอย่างนี้แสดงให้เห็นว่าวิธีการแทนที่เนื้อหาทำงานได้อย่างถูกต้องเมื่อไฟล์เนื้อหาใหม่มีความละเอียดแตกต่าง
            const string baseFolder = "PSDNET809_1\\";
            const string outputFolder = baseFolder + "output\\";
            const string fileName = "CommonPsb.psd";
            const string filePath = baseFolder + fileName; // original PSD image
            const string newContentPath = baseFolder + "image.jpg"; // the new content file for the smart object
            const string outputFilePath = outputFolder + "ChangedPsd";
            const string pngOutputPath = outputFilePath + ".png"; // the output PNG file
            const string psdOutputPath = outputFilePath + ".psd"; // the output PSD file
            using (PsdImage psd = (PsdImage)Image.Load(filePath))
            {
                for (int i = 0; i < psd.Layers.Length; i++)
                {
                    var layer = psd.Layers[i];
                    SmartObjectLayer smartObjectLayer = layer as SmartObjectLayer;
                    if (smartObjectLayer != null)
                    {
                        smartObjectLayer.ReplaceContents(newContentPath);

                        psd.Save(psdOutputPath);
                        psd.Save(pngOutputPath, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
                    }
                }
            }
{{< /highlight >}}

**PSDNET-810. Exception on loading the files**

{{< highlight csharp >}}
            string testFile1 = "face.psd";
            string testFile2 = "BigFile2.psd";

            using (var psdImage = (PsdImage)Image.Load(testFile1))
            {
                // โหลดไฟล์สำเร็จ
            }

            using (var psdImage = (PsdImage)Image.Load(testFile2))
            {
                // โหลดไฟล์สำเร็จ
            }
{{< /highlight >}}

**PSDNET-824. ขอบเขต vogk ไม่ถูกต้องหลังจากโหลดแและบันทึกรูปภาพ PSD ด้วยชั้นรูปเแและเส้นทางเวกเตอร์**

{{< highlight csharp >}}
            // ตัวอย่างนี้แสดงให้เห็นว่าโหลดและบันทึกรูปภาพ PSD 