---
title: یادداشت‌های انتشار Aspose.PSD برای .NET ۱۹.۱۰
type: مستندات
weight: 30
url: /fa/net/aspose-psd-for-net-19-10-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های انتشار Aspose.PSD برای .NET ۱۹.۱۰ می‌باشد.

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-207|[پشتیبانی از لایه تنظیم تعادل رنگ](psd/fa/net/modifying-images/#modifyingimages-colorbalanceadjustmentlayer)|ویژگی|
|PSDNET-145|[پشتیبانی از لایه تنظیم معکوس](psd/fa/net/modifying-images/#modifyingimages-invertadjustmentlayer)|ویژگی|
|PSDNET-139|[پیاده‌سازی بازنمونه‌گیر بیکیوبی](psd/fa/net/modifying-images/#modifyingimages-implementbicubicresampling)|ویژگی|
|PSDNET-169|[افزودن پشتیبانی از صدور PSD به PDF با Clipping Mask](psd/fa/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithclippingmask)|ویژگی|
|PSDNET-168|[افزودن پشتیبانی از صدور PSD به PDF با لایه‌های تنظیم](psd/fa/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithadjustmentlayer)|ویژگی|
|PSDNET-179|مشکل در دریافت اثر سایه لایه|بهبود|
|PSDNET-203|هنگام به‌روزرسانی متن با کاراکتر / (خط مستقیم)، فایل نمی‌تواند در فتوشاپ باز شود|اشکال|
|PSDNET-199|نمی‌توان فایل PSD را ذخیره کرد هنگامی که لایه متن تنها حاوی خط جداسازی است|اشکال|
|PSDNET-185|اندازه فونت اشتباه استخراج شده|اشکال|

## **تغییرات عمومی API**
# **API‌های اضافه شده:**
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.InvertAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.PsdImage.GlobalAngle
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddColorBalanceAdjustmentLayer
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddInvertAdjustmentLayer
- F:Aspose.PSD.ResizeType.CatmullRom
- F:Aspose.PSD.ResizeType.CubicConvolution
- F:Aspose.PSD.ResizeType.CubicBSpline
- F:Aspose.PSD.ResizeType.Mitchell
- F:Aspose.PSD.ResizeType.SinC
- F:Aspose.PSD.ResizeType.Bell
# **API‌های حذف شده:**
- هیچ‌کدام

## **نمونه‌های استفاده:**
**PSDNET-207. پشتیبانی از لایه تنظیم تعادل رنگ**

{{< highlight java >}}

            var filePath = "ColorBalance.psd";

            var outputPath = "ColorBalance_out.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                foreach (var layer in im.Layers)

                {

                    var cbLayer = layer as ColorBalanceAdjustmentLayer;

                    if (cbLayer != null)

                    {

                        cbLayer.ShadowsCyanRedBalance = 30;

                        cbLayer.ShadowsMagentaGreenBalance = -15;

                        cbLayer.ShadowsYellowBlueBalance = 40;

                        cbLayer.MidtonesCyanRedBalance = -90;

                        cbLayer.MidtonesMagentaGreenBalance = -25;

                        cbLayer.MidtonesYellowBlueBalance = 20;

                        cbLayer.HighlightsCyanRedBalance = -30;

                        cbLayer.HighlightsMagentaGreenBalance = 67;

                        cbLayer.HighlightsYellowBlueBalance = -95;

                        cbLayer.PreserveLuminosity = true;

                    }

                }

                im.Save(outputPath);

            }

{{< /highlight >}}

**PSDNET-145. پشتیبانی از لایه تنظیم معکوس**

{{< highlight java >}}

            var filePath = "InvertStripes_before.psd";

            var outputPath = "InvertStripes_after.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                im.AddInvertAdjustmentLayer();

                im.Save(outputPath);

            }

{{< /highlight >}}

**PSDNET-139. پیاده‌سازی بازنمونه‌گیر بیکیوبی**

{{< highlight java >}}

             string sourceFile = "sample.psd";

            string destName = "ResamplerCubicConvolutionStripes_after.psd";

            // Load an existing image into an instance of PsdImage class

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CubicConvolution);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerCatmullRomStripes_after.psd";

            // Load an existing image into an instance of PsdImage class

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CatmullRom);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerMitchellStripes_after.psd";

            // Load an existing image into an instance of PsdImage class

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.Mitchell);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerCubicBSplineStripes_after.psd";

            // Load an existing image into an instance of PsdImage class

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CubicBSpline);

                image.Save(destName, new PsdOptions(image));
                
            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerSinCStripes_after.psd";

            // Load an existing image into an instance of PsdImage class

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.SinC);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerBellStripes_after.psd";

            // Load an existing image into an instance of PsdImage class

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.Bell);

                image.Save(destName, new PsdOptions(image));

            }

{{< /highlight >}}

**PSDNET-169. افزودن پشتیبانی از صدور PSD به PDF با Clipping Mask**

{{< highlight java >}}

     using (PsdImage image = (PsdImage)Image.Load("clip.psd"))

    {

      image.Save("output.pdf", new PdfOptions());

    }

{{< /highlight >}}



**PSDNET-168. افزودن پشتیبانی از صدور PSD به PDF با لایه‌های تنظیم**

{{< highlight java >}}

      using (PsdImage image = (PsdImage)Image.Load("example.psd"))

    {

      image.Save("document.pdf", new PdfOptions());

    }

{{< /highlight >}}



**PSDNET-203. هنگام به‌روزرسانی متن با / (خط مستقیم)، فایل نمی‌تواند در فتوشاپ باز شود**

{{< highlight java >}}

         var psdImage = (PsdImage)image;

        var layers = psdImage.Layers;

        for (var index = layers.Length - 1; index >= 0; index--)

        {

            var layer = layers[index];

            if (!(layer is TextLayer)) continue;

            var textLayer = (TextLayer)layer;

            textLayer.UpdateText("/");

        }

        var imageOptions = new PsdOptions(psdImage);

        var fileName = Path.GetFileName(filePath);

        var outputFilePath = Path.GetDirectoryName(filePath) + "\\target_" + fileName;

        psdImage.Save(outputFilePath, imageOptions);



{{< /highlight >}}



**PSDNET-199. فایل PSD نمی‌تواند ذخیره شود هنگامی که لایه متن حاوی خط جداسازی باشد**

{{< highlight java >}}

 string filePath = "testLineBreaks2.psd";

string outputPath = "testLineBreaks2_changed.psd";

var newText = "\r";

        using (var image = Image.Load(filePath))

        {

            var psdImage = image as PsdImage;

            if (image == null)

            {

                return;

            }

            var layers = psdImage.Layers;

            for (var index = layers.Length - 1; index >= 0; index--)

            {

                var layer = layers[index] as TextLayer;

                if (layer == null)

                {

                    continue;

                }

                layer.UpdateText(newText);

            }

            var imageOptions = new PsdOptions(psdImage);

            psdImage.Save(outputPath, imageOptions);

        }

{{< /highlight >}}



**PSDNET-185. اندازه فونت اشتباه استخراج شده**

{{< highlight java >}}

             // استخراج اندازه فرمت اشتباه

            string filePath = "直播+电商.psd";

            var tolerance = 0.001;

            using (var image = Image.Load(filePath))

            {

                int layerIndex = 22;

                // پیش API (استفاده از اولین فونت پاراگراف)

                PsdImage psdImage = image as PsdImage;

                double[] matrix = ((TextLayer)psdImage.Layers[layerIndex]).TransformMatrix;

                double baseFontSize = ((TextLayer)psdImage.Layers[layerIndex]).Font.Size;

                double fontSize = matrix[0] * baseFontSize;

                // بررسی اندازه اصلی فونت

                if (Math.Abs(100.0 - baseFontSize) > tolerance)

                {

                    throw new Exception("اندازه فونت بطور نادرست خوانده شد");

                }

                // بررسی اندازه واقعی فونت

                if (Math.Abs(88.425 - fontSize) > tolerance)

                {

                    throw new Exception("TransformMatrix به صورت نادرست خوانده شد");

                }

                // API جدید (یک لایه متنی می‌تواند حاوی هر تعداد اندازه فونت باشد)

                ITextPortion[] portions = ((TextLayer)psdImage.Layers[layerIndex]).TextData.Items;

                ITextStyle style = portions[0].Style;

                double fontSizeOfPortion = matrix[0] * style.FontSize;

                // بررسی اندازه پایه بخش فونت

                if (Math.Abs(100.0 - style.FontSize) > tolerance)

                {

                    throw new Exception("اندازه فونت بطور نادرست خوانده شد");

                }

                // بررسی اندازه واقعی بخش فونت

                if (Math.Abs(88.425 - fontSizeOfPortion) > tolerance)

                {

                    throw new Exception("TransformMatrix به صورت نادرست خوانده شد");

                }

            }

{{< /highlight >}}



**PSDNET-179. مشکل در گرفتن لایه DropShadowEffect**

{{< highlight java >}}

       // زمانی که مشخصه UseGlobalLight اثر سایه به 'صحیح' باشد، آنگاه شیء DropShadowEffect از مقدار زاویه از مشخصه GlobalAngle شیء PsdImage استفاده می‌کند.

		using (PsdImage image = (PsdImage)Image