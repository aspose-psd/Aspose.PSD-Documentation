---
title: บันทึกการปล่อย Aspose.PSD for .NET 20.4
type: docs
weight: 90
url: /th/net/aspose-psd-for-net-20-4-release-notes/
---

{{% alert color="primary" %}}

หน้านี้ประกอบด้วยบันทึกการปล่อย [Aspose.PSD for .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-567|การสนับสนุน 'Vector Origination Data' resource|คุณลักษณะ|
|PSDNET-373|การสนับสนุน lclrResource (การตั้งค่าสีแผ่น)|คุณลักษณะ|
|PSDNET-563|การสนับสนุนคุณสมบัติจากข้อมูล LengthRecord (การดำเนินการเส้นทาง (การดำเนินการตรรกะ), ดัชนีของรูปร่างในเลเยอร์, จำนวนของบีเซียร์น็อตเรคคอร์ด)|คุณลักษณะ|
|PSDNET-425|การสนับสนุน Image Section Resource #1010 สีพื้นหลัง|คุณลักษณะ|
|PSDNET-530|การเพิ่ม Fill Layers ในระหว่างระบบการทำงาน|คุณลักษณะ|
|PSDNET-424|การสนับสนุน Image Section Resource #1009 ข้อมูลขอบเขตขอบ|คุณลักษณะ|
|PSDNET-592|การสนับสนุนเลเยอร์ในไฟล์รูปแบบ AI|คุณลักษณะ|
|PSDNET-256|การสนับการอ่านและแก้ไขเอฟเฟกต์เลเยอร์ฝาแผ่นสีเรียบ|คุณลักษณะ|
|PSDNET-257|การเรนเดอร์ของเอฟเฟกต์เลเยอร์ Gradient Overlay|คุณลักษณะ|
|PSDNET-585|การเปลี่ยนแปลงสมบัติยึดผสมของ GradientOverlayEffect.BlendMode ไม่แสดงใน Photoshop|ข้อบกพร่อง|
|PSDNET-561|แก้ไขการบันทึกรูปภาพ PSD ด้วย Grayscale ColorMode และ 16 บิตต่อช่องเป็นรูปแบบ PSD สีเทา|ข้อบกพร่อง|
|PSDNET-560|แก้ไขการบันทึกรูปภาพ PSD ด้วย Grayscale ColorMode และ 16 บิตต่อช่องเป็นรูปแบบ PNG|ข้อบกพร่อง|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Name
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsTemplate
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsLocked
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsShown
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPrinted
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPreview
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsImagesDimmed
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.DimValue
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorNumber
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Red
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Green
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Blue
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- T:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.Color
- T:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Width
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Unit
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.#ctor(System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.BezierKnotRecordsCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.ShapeIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.ShapeOriginSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.#ctor(System.Boolean,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidated
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.OriginIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.ExcludeOverlappingShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.CombineShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.SubtractFrontShape
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.IntersectShapeAreas
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.#ctor(Aspose.PSD.Color,System.Int32,System.Int32)
# **API ที่ถูกลบ:**
- ไม่มี

## **ตัวอย่างการใช้:**

**PSDNET-567. การสนับสนุน 'Vector Origination Data' resource**

{{< highlight java >}}

        // VogkResource Support

        static void ExampleOfVogkResourceSupport()

        {

            string fileName = "VectorOriginationDataResource.psd";

            string outFileName = "out_VectorOriginationDataResource_.psd";

            using (var psdImage = (PsdImage)Image.Load(fileName))

            {

                var resource = GetVogkResource(psdImage);

                // Reading

                if (resource.ShapeOriginSettings.Length != 1 ||

                    !resource.ShapeOriginSettings[0].IsShapeInvalidated ||

                    resource.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    throw new Exception("VogkResource were read wrong.");

                }

                // Editing

                resource.ShapeOriginSettings = new[]

                {

                    resource.ShapeOriginSettings[0],

                    new VectorShapeOriginSettings(true, 1)

                };

                psdImage.Save(outFileName);

            }

        }

        static VogkResource GetVogkResource(PsdImage image)

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

                throw new Exception("VogkResourcenot found.");

            }

            return resource;

        }

{{< /highlight >}}

**PSDNET-373. การสนับสนุน lclrResource (การตั้งค่าสีแผ่น)**

{{< highlight java >}}

        static void CheckSheetColorsAndRerverse(SheetColorHighlightEnum[] sheetColors, PsdImage img)

        {

            int layersCount = img.Layers.Length;

            for (int layerIndex = 0; layerIndex < layersCount; layerIndex++)

            {

                Layer layer = img.Layers[layerIndex];

                LayerResource[] resources = layer.Resources;

                foreach (LayerResource layerResource in resources)

                {

                    // The lcrl resource always presents in psd file resource list.

                    LclrResource resource = layerResource as LclrResource;

                    if (resource != null)

                    {

                        if (resource.Color != sheetColors[layerIndex])

                        {

                            throw new Exception("Sheet Color has been read wrong");

                        }

                        // Reverse of style sheet colors. Set up of Layer color highlight.

                        resource.Color = sheetColors[layersCount - layerIndex - 1];

                        break;

                    }

                }

            }

        }

            string sourceFilePath = "AllLclrResourceColors.psd";

            string outputFilePath = "AllLclrResourceColorsReversed.psd";

            // In the file colors of layers highlighting are in this order

            SheetColorHighlightEnum[] sheetColors = new SheetColorHighlightEnum[] {

                SheetColorHighlightEnum.Red,

                SheetColorHighlightEnum.Orange,

                SheetColorHighlightEnum.Yellow,

                SheetColorHighlightEnum.Green,

                SheetColorHighlightEnum.Blue,

                SheetColorHighlightEnum.Violet,

                SheetColorHighlightEnum.Gray,

                SheetColorHighlightEnum.NoColor

            };            

            // Layer Sheet Color is used to visually highlight layers. 

            // For example you can update some layers in PSD and then highlight by color the layer which you want to attract attention.

            using (PsdImage img = (PsdImage)Image.Load(sourceFilePath))

            {

                CheckSheetColorsAndRerverse(sheetColors, img);

                img.Save(outputFilePath, new PsdOptions());

            }

            using (PsdImage img = (PsdImage)Image.Load(outputFilePath))

            {

                // Colors should be reversed

                Array.Reverse(sheetColors);

                CheckSheetColorsAndRerverse(sheetColors, img);

            }

{{< /highlight >}}

**PSDNET-563. การสนับสนุนคุณสมบัติจากข้อมูล LengthRecord (การดำเนินการเส้นทาง (การดำเนินการตรรกะ), ดัชนีของรูปร่างในเลเยอร์, จำนวนของบีเซียร์น็อตเรคคอร์ด)**

{{< highlight java >}}

            string fileName = "PathOperationsShape.psd";

            using (var im = (PsdImage)Image.Load(fileName))

            {

                VsmsResource resource = null;

                foreach (var layerResource in im.Layers[1].Resources)

                {

                    if (layerResource is VsmsResource)

                    {

                        resource = (VsmsResource)layerResource;

                        break;

                    }

                }

                LengthRecord lengthRecord0 = (LengthRecord)resource.Paths[2];

                LengthRecord lengthRecord1 = (LengthRecord)resource.Paths[7];

                LengthRecord lengthRecord2 = (LengthRecord)resource.Paths[11];

                // Here we changin the way to combining betwen shapes.

                lengthRecord0.PathOperations = PathOperations.ExcludeOverlappingShapes;

                lengthRecord1.PathOperations = PathOperations.IntersectShapeAreas;

                lengthRecord2.PathOperations = PathOperations.SubtractFrontShape;

                im.Save("out_" + fileName);

            }

{{< /highlight >}}

**PSDNET-425. การสนับสนุน Image Section Resource #1010 สีพื้นหลัง**

{{< highlight java >}}

            string sourceFile = "input.psd";

            string outputFile = "output.psd";

            using (var image = (PsdImage)Image.Load(sourceFile))

            {

                ResourceBlock[] imageResources = image.ImageResources;

                BackgroundColorResource backgroundColorResource = null;

                foreach (var imageResource in imageResources)

                {

                    if (imageResource is BackgroundColorResource)

                    {

                        backgroundColorResource = (BackgroundColorResource)imageResource;

                        break;

                    }

                }

                // update BackgroundColorResource

                backgroundColorResource.Color = Color.DarkRed;

                image.Save(outputFile);

            }

{{< /highlight >}}

**PSDNET-530. การเพิ่ม Fill Layers ในระหว่างระบบการทำงาน**

{{< highlight java >}}

            string outputPsd = "output.psd";

            using (var image = new PsdImage(100, 100))

            {

                FillLayer colorFillLayer = FillLayer.CreateInstance(FillType.Color);

                colorFillLayer.DisplayName = "Color Fill Layer";

                image.AddLayer(colorFillLayer);

                FillLayer gradientFillLayer = FillLayer.CreateInstance(FillType.Gradient);

                gradientFillLayer.DisplayName = "Gradient Fill Layer";

                image.AddLayer(gradientFillLayer);

                FillLayer patternFillLayer = FillLayer.CreateInstance(FillType.Pattern);

                patternFillLayer.DisplayName = "Pattern Fill Layer";

                patternFillLayer.Opacity = 50;

                image.AddLayer(patternFillLayer);

                image.Save(outputPsd);

            }

{{< /highlight >}}

**PSDNET-424. การสนับสนุน Image Section Resource #1009 ข้อมูลขอบเขตขอบ**

{{< highlight java >}}

            string sourceFile = "input.psd";

            string outputFile = "output.psd";

            using (var image = (PsdImage)Image.Load(sourceFile))

            {

                ResourceBlock[] imageResources = image.ImageResources;

                BorderInformationResource borderInfoResource = null;

                foreach (var imageResource in imageResources)

                {

                    if (imageResource is BorderInformationResource)

                    {

                        borderInfoResource = (BorderInformationResource)imageResource;

                        break;

                    }

                }

                // update BorderInformationResource

                borderInfoResource.Width = 0.1;

                borderInfoResource.Unit = PhysicalUnit.Inches;

                image.Save(outputFile);

            }

{{< /highlight >}}

**PSDNET-592. การสนับสนุนเลเยอร์ในไฟล์รูปแบบ AI**

{{< highlight java >}}

        void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "form_8_2l3_7.ai";

        string outputFileName = "form_8_2l3_7_export";

        using (AiImage image = (AiImage)Image.Load(sourceFileName))

        {

            AiLayerSection layer0 = image.Layers[0];

            AssertIsTrue(layer0 != null, "Layer 0 should be not null.");

            AssertIsTrue(layer0.Name == "Layer 4", "The Name property of the layer 0 should be Layer 4");

            AssertIsTrue(!layer0.IsTemplate, "The IsTemplate property of the layer 0 should be false.");

            AssertIsTrue(layer0.IsLocked, "The IsLocked property of the layer 0 should be true.");

            AssertIsTrue(layer0.IsShown, "The IsShown property of the layer 0 should be true.");

            AssertIsTrue(layer0.IsPrinted, "The IsPrinted property of the layer 0 should be true.");

            AssertIsTrue(!layer