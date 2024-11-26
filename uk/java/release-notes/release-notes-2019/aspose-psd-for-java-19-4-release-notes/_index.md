---
title: Примітки з випуску Aspose.PSD для Java 19.4
type: docs
weight: 20
url: /java/aspose-psd-for-java-19-4-release-notes/
---

{{% alert color="primary" %}} 

Ця сторінка містить примітки з випуску для Aspose.PSD для Java 19.4

{{% /alert %}} 

|**Ключ**|**Короткий опис**|**Категорія**|
| :- | :- | :- |
|PSDJAVA-1|Зробіть можливість завантажувати файли зображень JPEG/PNG/тощо до PsdImage без прямого завантаження (казка, яка не підтримується в Aspose.PSD)|Функціонал|
|PSDJAVA-2|Підтримка кольорового режиму RGB з 16 бітами на канал (64 біти на колір)|Функціонал|
|PSDJAVA-3|Підтримка векторних масок шарів та власного обертання/перевертання текстового шару|Функціонал|
|PSDJAVA-4|Усі азійські символи не відображаються належним чином|Помилка|
|PSDJAVA-5|Символи \r\n інтерпретуються як подвійний розрив рядка, що є неправильним|Помилка|
|PSDJAVA-6|Якщо TextLayer оновлено рядком з переносом рядка, файл PSD стає нерозпізнаваним|Помилка|
|PSDJAVA-7|Якщо TextLayer оновлено рядком, що містить символи табуляції, обробка завершиться із винятком|Помилка|

# **Зміни у загальнодоступному API**
# **Додані API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
## **Вилучені API:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.FileFormat
- P:Aspose.PSD.FileFormats.Gif.GifImage.XmpData
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasTrailer
- P:Aspose.PSD.FileFormats.Gif.GifImage.IsPaletteSorted
- P:Aspose.PSD.FileFormats.Gif.GifImage.PaletteColorResolutionBits
- P:Aspose.PSD.FileFormats.Gif.GifImage.Width
- P:Aspose.PSD.FileFormats.Gif.GifImage.Height
- P:Aspose.PSD.FileFormats.Gif.GifImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Gif.GifImage.Blocks
- P:Aspose.PSD.FileFormats.Gif.GifImage.ActiveFrame
- P:Aspose.PSD.FileFormats.Gif.GifImage.BackgroundColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.BackgroundColorIndex
- P:Aspose.PSD.FileFormats.Gif.GifImage.PixelAspectRatio
- P:Aspose.PSD.FileFormats.Gif.GifImage.IsCached
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasTransparentColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.TransparentColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasBackgroundColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.ImageOpacity
- M:Aspose.PSD.FileFormats.Gif.GifImage.Dither(Aspose.PSD.DitheringMethod,System.Int32,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.CacheData
- M:Aspose.PSD.FileFormats.Gif.GifImage.RotateFlipAll(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.OrderBlocks
- M:Aspose.PSD.FileFormats.Gif.GifImage.ClearBlocks
- M:Aspose.PSD.FileFormats.Gif.GifImage.InsertBlock(System.Int32,Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AddBlock(Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.RemoveBlock(Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Rotate(System.Single,System.Boolean,Aspose.PSD.Color)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Resize(System.Int32,System.Int32,Aspose.PSD.ImageResizeSettings)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ResizeProportional(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Crop(Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Grayscale
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeFixed(System.Byte)
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeOtsu
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeBradley(System.Double)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustBrightness(System.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustContrast(System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustGamma(System.Single,System.Single,System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustGamma(System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Filter(Aspose.PSD.Rectangle,Aspose.PSD.ImageFilters.FilterOptions.FilterOptionsBase)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ReplaceColor(System.Int32,System.Byte,System.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ReplaceNonTransparentColors(System.Int32)

# **Приклади використання:**

**PSDJAVA-1. Реалізуйте можливість завантажувати файли зображень JPEG/PNG/тощо до PsdImage без прямого завантаження (казка, яка не підтримується в Aspose.PSD)**

{{< highlight java >}}
 String filePath = "PsdExample.psd";

    String outputFilePath = "PsdResult.psd";

    PsdImage image = new PsdImage(200, 200);

    try 

    { 

         PsdImage im = Image.load(filePath);

         try 

         {

              Layer layer = null;

              try

              {

                  layer = new Layer((RasterImage)im);

                  image.addLayer(layer);

                  image.save(outputFilePath);

              }

              catch

              {

                  if (layer != null)

                  {

                       layer.dispose();

                  }

                  throw;

              }

         }    

         finally 
         {
              im.dispose(); 
         }
    }

    finally

    {

         image.dispose();

    }

{{< /highlight >}}

**PSDJAVA-2. Підтримка кольорового режиму RGB з 16 бітами на канал (64 біти на колір)**

{{< highlight java >}}

  // Підтримка кольорового режиму RGB з 16 бітами на канал (64 біти на колір)

        String sourceFileName = "inRgb16.psd.psd";

        String outputFilePathJpg = "outRgb16.jpg";

        String outputFilePathPsd = "outRgb16.psd";

        PsdLoadOptions options = new PsdLoadOptions();

        PsdImage image = (PsdImage)Image.load(sourceFileName, options);

        try

        {

            PsdOptions psdOpt = new PsdOptions(image);

            image.save(outputFilePathPsd, psdOpt);
            JpegOptions jpegOpt = new JpegOptions();

            jpegOpt.setQuality(100);

            image.save(outputFilePathJpg);

        }

        finally 

        {

             image.dispose();

        }

    // Файли повинні відкриватися без винятків і бути читабельними для Photoshop    

   image = Image.load(outputFilePathPsd);

   image.dispose(); 

{{< /highlight >}}

**PSDJAVA-3. Підтримка векторних масок шарів та власного обертання/повертання текстового шару**

{{< highlight java >}}

 // Операція RotateFlip працює, як очікувалося з форматом PSD

    String sourceFile = "1.psd";

    String pngPath = "RotateFlipTest2617.png";

    String psdPath = "RotateFlipTest2617.psd";

    int flipType = RotateFlipType.Rotate270FlipXY;

    PsdImage im = (PsdImage)(Image.load(sourceFile));
    try

    {

        im.rotateFlip(flipType);

        PngOptions options = new PngOptions();

        options.setColorType(PngColorType.TruecolorWithAlpha);

        im.save(pngPath, options);

        im.save(psdPath);

    }

    finally 

    {

        im.dispose();

    }

{{< /highlight >}}

**PSDJAVA-4. Усі азійські символи не відображаються належним чином**

[**Будь ласка, перевірте прикріплений приклад**](attachments/92602686/92766213.java)

**PSDJAVA-5. Символи \r\n інтерпретуються як подвійний розрив рядка, що є неправильним**

{{< highlight java >}}

 // Символи \r\n інтерпретуються як подвійний розрив рядка, що є неправильним

            String sourceFileName = "TextTest.psd";

            String exportPath = "Result.psd";

            PsdImage image = (PsdImage)Image.load(sourceFileName);

            TextLayer layer = (TextLayer)image.getLayers()[0];

            PsdOptions imageOptions = new PsdOptions(image);

            try

            {

                layer.updateText("First Paragraph\r\nSecond Paragraph\rThird paragraph\nFourth Paragraph");

                image.save(exportPath, imageOptions);

                // Створене зображення повинно бути читабельним для Aspose.PSD/Aspose.Imaging і Photoshop

                PsdImage createdImage = (PsdImage)Image.load(exportPath);

                createdImage.dispose();

            }

            finally

            {

                image.dispose();

            }

{{< /highlight >}}


**PSDJAVA-6. Якщо текстовий шар оновлено рядком з переносом рядка, файл PSD стає нерозпізнаваним**

{{< highlight java >}}

 // Якщо TextLayer оновлено рядком із переносом рядка, файл PSD стає нерозпізнаваним

            String sourceFileName = "TextTest.psd";

            String exportPath = "Result.psd";

            PsdImage image = (PsdImage)Image.load(sourceFileName);

            TextLayer layer = (TextLayer)image.getLayers()[0];

            PsdOptions imageOptions = new PsdOptions(image);

            try

            {

                layer.updateText("First Paragraph\r\nSecond Paragraph\r\nThird paragraph\r\nFourth Paragraph");

                image.save(exportPath, imageOptions);

                // Створене зображення повинно бути читабельним для Aspose.PSD/Aspose.Imaging та Photoshop

                PsdImage createdImage = (PsdImage)Image.load(exportPath);

                createdImage.dispose();

            }

            finally

            {

                image.dispose();

            }

{{< /highlight >}}


**PSDJAVA-7. Якщо TextLayer оновлено рядком, що містить символи табуляції, обробка завершиться із винятком**

{{< highlight java >}}

 // Якщо TextLayer оновлено рядком із символами табуляції, обробка завершиться із винятком

            String sourceFileName = "TextTest.psd";

            String exportPath = "Result.psd";

            PsdImage image = (PsdImage)Image.load(sourceFileName);

            TextLayer layer = (TextLayer)image.getLayers()[0];

            PsdOptions imageOptions = new PsdOptions(image);

            try

            {
                layer.UpdateText("Starting Text\tText After Tab");

                image.save(exportPath, imageOptions);

                // Створений зображення повинно бути читабельним для Aspose.PSD/Aspose.Imaging та в Photoshop

                PsdImage createdImage = (PsdImage)Image.load(exportPath);

                createdImage.dispose();
            }

            finally

            {

                image.dispose();

            }

{{< /highlight >}}