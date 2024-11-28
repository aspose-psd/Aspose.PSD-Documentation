---
title: Aspose.PSD за .NET 19.8 - Бележки за версията
type: docs
weight: 50
url: /bg/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}} 

Тази страница съдържа бележки за версията на Aspose.PSD за .NET 19.8

{{% /alert %}} 

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-184|Зареждане на JPEG, PNG и други изображения в PsdImage от поток|Функционалност|
|PSDNET-134|Изпълнение на изпълнението на Запълващ щит: Градиент|Функционалност|
|PSDNET-166|Запазването на PSD в PDF не осигурява избираем текст|Функционалност|
|PSDNET-158|Поддръжка на запазване на PSB като PDF|Функционалност|
|PSDNET-189|Висока употреба на памет при зареждането на PSD с режим "Само за четене"|Подобрение|
|PSDNET-171|След създаването на нов TextLayer, PSD файлът стана неразличим за PS|Проблем|
|PSDNET-156|Изключение при зареждане на PSD|Проблем|

## **Промени в публичния API**
# **Добавени API-та:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **Премахнати API-та:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Примери за използване:**
**PSDNET-184. Зареждане на JPEG, PNG и други изображения в PsdImage от поток**

{{< highlight java >}}

    // зареждане на JPEG, PNG и други изображения в PsdImage от поток

    string outputFilePath = "PsdResult.psd";

    var filesList = new string[]

    {

        "PsdExample.psd",

        "BmpExample.bmp",

        "GifExample.gif",

        "Jpeg2000Example.jpf",

        "JpegExample.jpg",

        "PngExample.png",

        "TiffExample.tif",

    };

    using (var image = new PsdImage(200, 200))

    {

        foreach (var fileName in filesList)

        {

            string filePath = fileName;

            using (var stream = new FileStream(filePath, FileMode.Open))

            {

                Layer layer = null;

                try

                {

                     layer = new Layer(stream);

                     image.AddLayer(layer);

                }

                catch (Exception e)

                {

                    if (layer != null)

                    {

                        layer.Dispose();

                    }

                    throw e;

                }

            }

        }

        image.Save(outputFilePath);

    }

{{< /highlight >}}

**PSDNET-134. Изпълнение на изпълнението на Запълващ щит: Градиент**

{{< highlight java >}}

             // Изпълнение на изпълнението на Запълващ щит: Градиент

            string fileName = "FillLayerGradient.psd";

            GradientType[] gradientTypes = new[]

            {

                GradientType.Linear, GradientType.Radial, GradientType.Angle, GradientType.Reflected, GradientType.Diamond

            };

            using (var image = Image.Load(fileName))

            {

                PsdImage psdImage = (PsdImage)image;

                FillLayer fillLayer = (FillLayer)psdImage.Layers[0];

                GradientFillSettings fillSettings = (GradientFillSettings)fillLayer.FillSettings;

                foreach (var gradientType in gradientTypes)

                {

                    fillSettings.GradientType = gradientType;

                    fillLayer.Update();

                    psdImage.Save(fileName + "_" + gradientType.ToString() + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

                }

            }

{{< /highlight >}}

**PSDNET-166. Запазването на PSD в PDF не осигурява избираем текст**

{{< highlight java >}}

  // Запазването на PSD в PDF не осигурява избираем текст

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. След създаването на нов TextLayer, PSD файлът стана неразличим за PS**

{{< highlight java >}}

 // След създаването на нов TextLayer на Сървър за създаване, PSD файлът стана неразличим за PS

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Някой текст", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}

**PSDNET-156. Изключение при зареждане на PSD**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. Висока употреба на памет при зареждането на PSD с режим "Само за четене"**

{{< highlight java >}}

 // Висока употреба на памет от Aspose.PSD при зареждането на PSD с режим "Само за четене"

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // Използването на памет трябва да е по-малко от 100 MB за тези примери

            if (memoryUsed > 100)

            {

                throw new Exception("Употребата на паметта е твърде голяма");

            }

{{< /highlight >}}

**PSDNET-158. Поддръжка на запазване на PSB като PDF**

{{< highlight java >}}

 // Поддръжка на запазване на PSB като PDF

    string sourceFileName = "sample.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "sample.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}
