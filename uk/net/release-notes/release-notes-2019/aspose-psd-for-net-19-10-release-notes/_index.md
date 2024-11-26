---
title: Огляд Aspose.PSD для .NET 19.10 - Примітки до випуску
type: docs
weight: 30
url: /uk/net/aspose-psd-for-net-19-10-release-notes/
---

{{% alert color="primary" %}} 

Ця сторінка містить примітки до випуску Aspose.PSD для .NET 19.10

{{% /alert %}} 

|**Ключ**|**Короткий опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-207|[Підтримка шару коригування балансу кольору](/psd/uk/net/modifying-images/#modifyingimages-colorbalanceadjustmentlayer)|Функція|
|PSDNET-145|[Підтримка шару обернення](/psd/uk/net/modifying-images/#modifyingimages-invertadjustmentlayer)|Функція|
|PSDNET-139|[Реалізація бікубічного ресемплера](/psd/uk/net/modifying-images/#modifyingimages-implementbicubicresampling)|Функція|
|PSDNET-169|[Додана підтримка експорту PSD в PDF з обрізною маскою](/psd/uk/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithclippingmask)|Функція|
|PSDNET-168|[Додана підтримка експорту PSD в PDF з коригувальними шарами](/psd/uk/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithadjustmentlayer)|Функція|
|PSDNET-179|Проблема з отриманням зображення DropShadowEffect шару|Покращення|
|PSDNET-203|При оновленні тексту з символами / (косий слеш), файл не може бути відкритий у Photoshop|Помилка|
|PSDNET-199|Файл PSD не може бути збережений, коли шар тексту містить лише розрив рядка|Помилка|
|PSDNET-185|Вилучено неправильний розмір шрифту|Помилка|

## **Зміни у публічному API**
# **Додані API:**
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
# **Вилучені API:**
- Немає

## **Приклади використання:**
**PSDNET-207. Підтримка шару коригування балансу кольору**

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

**PSDNET-145. Підтримка шару обернення**

{{< highlight java >}}

            var filePath = "InvertStripes_before.psd";

            var outputPath = "InvertStripes_after.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                im.AddInvertAdjustmentLayer();

                im.Save(outputPath);

            }

{{< /highlight >}}

**PSDNET-139. Реалізація бікубічного ресемплера**

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

**PSDNET-169. Додана підтримка експорту PSD в PDF з обрізною маскою**

{{< highlight java >}}

     using (PsdImage image = (PsdImage)Image.Load("clip.psd"))

    {

      image.Save("output.pdf", new PdfOptions());

    }

{{< /highlight >}}



**PSDNET-168. Додана підтримка експорту PSD в PDF з коригувальними шарами**

{{< highlight java >}}

      using (PsdImage image = (PsdImage)Image.Load("example.psd"))

    {

      image.Save("document.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-203. При оновленні тексту з символами / (косий слеш), файл не може бути відкритий у Photoshop**

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

**PSDNET-199. Файл PSD не може бути збережений, коли шар тексту містить лише розрив рядка**

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

**PSDNET-185. Вилучено неправильний розмір шрифту**

{{< highlight java >}}

             // Вилучено неправильний розмір шрифту 

            string filePath = "直播+电商.psd";

            var tolerance = 0.001;

            using (var image = Image.Load(filePath))

            {

                int layerIndex = 22;

                // Старе API (З використанням розміру шрифту першого абзацу)

                PsdImage psdImage = image as PsdImage;

                double[] matrix = ((TextLayer)psdImage.Layers[layerIndex]).TransformMatrix;

                double baseFontSize = ((TextLayer)psdImage.Layers[layerIndex]).Font.Size;

                double fontSize = matrix[0] * baseFontSize;

                // Перевірка базового розміру шрифту

                if (Math.Abs(100.0 - baseFontSize) > tolerance)

                {

                    throw new Exception("Розмір шрифту був прочитаний некоректно");

                }

                // Перевірка реального розміру шрифту

                if (Math.Abs(88.425 - fontSize) > tolerance)

                {

                    throw new Exception("TransformMatrix було прочитано некоректно");

                }

                // Нове API (Один текстовий шар може містити будь-яку кількість розмірів шрифтів)

                ITextPortion[] portions = ((TextLayer)psdImage.Layers[layerIndex]).TextData.Items;

                ITextStyle style = portions[0].Style;

                double fontSizeOfPortion = matrix[0] * style.FontSize;

                // Перевірка базового розміру шрифту частини

                if (Math.Abs(100.0 - style.FontSize) > tolerance)

                {

                    throw new Exception("Розмір шрифту був прочитаний некоректно");

                }

                // Перевірка реального розміру шрифту частини

                if (Math.Abs(88.425 - fontSizeOfPortion) > tolerance)

                {

                    throw new Exception("TransformMatrix було прочитано некоректно");

                }

            }

{{< /highlight >}}

**PSDNET-179. Проблема у отриманні зображення DropShadowEffect шару**

{{< highlight java >}}

       // Коли властивість DropShadowEffect.UseGlobalLight встановлена на 'true', об'єкт DropShadowEffect використовує значення кута з властивості PsdImage.GlobalAngle.

		using (PsdImage image = (PsdImage)Image.Load("4.psd"))

		{

    		image.GlobalAngle = 30;

    		image.Save("output.psd");

		}

{{< /highlight >}}