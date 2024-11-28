---
title: اطلاعات انتشار Aspose.PSD برای .NET 20.4
type: مستندات
weight: 90
url: /fa/net/aspose-psd-for-net-20-4-release-notes/
---

{{% alert color="primary" %}} 

صفحه حاضر شامل یادداشت‌های انتشار برای [Aspose.PSD برای .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-567|پشتیبانی از منبع 'داده برگ سازش وکتوری'   |ویژگی|
|PSDNET-373|پشتیبانی از lclrResource (تنظیم رنگ برگه)|ویژگی|
|PSDNET-563|پشتیبانی از خصوصیت‌های داده LengthRecord. (عملیات مسیر (عملیات بولینی)، شاخص اشکال در لایه، تعداد ریزرشتردهای بزرگراه)|ویژگی|
|PSDNET-425|پشتیبانی از اطلاعات بخش تصویر منبع #1010 رنگ پس‌زمینه|ویژگی|
|PSDNET-530|اضافه کردن لایه‌های پرشده به صورت زمان اجرا|ویژگی|
|PSDNET-424|پشتیبانی از اطلاعات بخش تصویر منبع #1009 اطلاعات حاشیه|ویژگی|
|PSDNET-592|پشتیبانی از لایه‌ها در فایل‌های قالب AI|ویژگی|
|PSDNET-256|پشتیبانی از خواندن و ویرایش اثر لایه افزایه گرادیان|ویژگی|
|PSDNET-257|تحلیل اثر لایه افزایه گرادیان|ویژگی|
|PSDNET-585|رفع اشکال درخصوص تغییر خصوصیت BlendMode در GradientOverlayEffect که در فتوشاپ نمایش داده نمی‌شود|اشکال|
|PSDNET-561|رفع مشکل در ذخیره‌سازی تصویر PSD با حالت رنگ Grayscale و 16 بیت در هر کانال به فرمت PSD خاکستری|اشکال|
|PSDNET-560|رفع مشکل در ذخیره‌سازی تصویر PSD با حالت رنگ Grayscale و 16 بیت در هر کانال به فرمت PNG|اشکال|

## **تغییرات در API عمومی**
# **API های اضافه شده:**
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
# **API های حذف شده:**
- هیچ

## **مثال‌های استفاده:**
**PSDNET-567. پشتیبانی از منبع 'داده برگ سازش وکتوری'**

{{< highlight java >}}

         // پشتیبانی VogkResource

        static void ExampleOfVogkResourceSupport()

        {

            string fileName = "VectorOriginationDataResource.psd";

            string outFileName = "out_VectorOriginationDataResource_.psd";

            using (var psdImage = (PsdImage)Image.Load(fileName))

            {

                var resource = GetVogkResource(psdImage);

                // خواندن

                if (resource.ShapeOriginSettings.Length != 1 ||

                    !resource.ShapeOriginSettings[0].IsShapeInvalidated ||

                    resource.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    throw new Exception("VogkResource were read wrong.");

                }

                // ویرایش

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

**PSDNET-373. پشتیبانی از lclrResource (تنظیم رنگ برگه)**

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

                    // منبع lcrl همیشه در لیست منابع فایل psd وجود دارد.

                    LclrResource resource = layerResource as LclrResource;

                    if (resource != null)

                    {

                        if (resource.Color != sheetColors[layerIndex])

                        {

                            throw new Exception("Sheet Color has been read wrong");

                        }

                        // معکوس رنگ برگه. تنظیم رنگ برجسته لایه.

                        resource.Color = sheetColors[layersCount - layerIndex - 1];

                        break;

                    }

                }

            }

        }

            string sourceFilePath = "AllLclrResourceColors.psd";

            string outputFilePath = "AllLclrResourceColorsReversed.psd";

            // در این فایل رنگ‌های برجسته لایه ها به این ترتیب هستند

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

            // رنگ برجسته لایه برای برجسته سازی بصری لایه ها استفاده می‌شود. 

            // به عنوان مثال می‌توانید برخی از لایه‌ها را در یک فایل PSD ویرایش کرده و سپس لایه ای را که می‌خواهید توجه کنید، با یک رنگ برجسته کنید.

            using (PsdImage img = (PsdImage)Image.Load(sourceFilePath))

            {

                CheckSheetColorsAndRerverse(sheetColors, img);

                img.Save(outputFilePath, new PsdOptions());

            }

            using (PsdImage img = (PsdImage)Image.Load(outputFilePath))

            {

                // رنگ‌ها باید معکوس شوند

                Array.Reverse(sheetColors);

                CheckSheetColorsAndRerverse(sheetColors, img);

            }

{{< /highlight >}}

**PSDNET-563. پشتیبانی از خصوصیت‌های داده LengthRecord. (عملیات مسیر (عملیات بولینی)، شاخص اشکال در لایه، تعداد ریزرشتردهای بزرگراه)**

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

                // در اینجا روش ترکیب شیوه‌های را تغییر می‌دهیم.

                lengthRecord0.PathOperations = PathOperations.ExcludeOverlappingShapes;

                lengthRecord1.PathOperations = PathOperations.IntersectShapeAreas;

                lengthRecord2.PathOperations = PathOperations.SubtractFrontShape;

                im.Save("out_" + fileName);

            }

{{< /highlight >}}

**PSDNET-425. پشتیبانی از اطلاعات بخش تصویر منبع #1010 رنگ پس‌زمینه**

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

                // به‌روزرسانی BackgroundColorResource

                backgroundColorResource .Color = Color.DarkRed;

                image.Save(outputFile);

            }

{{< /highlight >}}

**PSDNET-530. اضافه کردن لایه‌های پرشده به صورت زمان اجرا**

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

**PSDNET-424. پشتیبانی از اطلاعات بخش تصویر منبع #1009 اطلاعات حاشیه**

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

                // به‌روزرسانی BorderInformationResource

                borderInfoResource.Width = 0.1;

                borderInfoResource.Unit = PhysicalUnit.Inches;

                image.Save(outputFile);

            }

{{< /highlight >}}

**PSDNET-592. پشتیبانی از لایه‌ها در فایل‌های قالب AI**

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

        using (AiImage image = (AiImage)Image