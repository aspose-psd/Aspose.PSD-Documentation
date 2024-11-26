---
title: Выпускные заметки Aspose.PSD для .NET 19.8
type: docs
weight: 50
url: /ru/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}} 

На этой странице содержатся выпускные заметки для Aspose.PSD для .NET 19.8.

{{% /alert %}} 

|**Ключ**|**Краткое описание**|**Категория**|
| :- | :- | :- |
|PSDNET-184|Загрузка JPEG, PNG и других изображений в PsdImage из потока|Функция|
|PSDNET-134|Реализация отображения слоя заполнения: Градиент|Функция|
|PSDNET-166|Сохранение PSD в PDF не обеспечивает выбор текста|Функция|
|PSDNET-158|Поддержка сохранения PSB как PDF|Функция|
|PSDNET-189|Высокое использование памяти при загрузке PSD в режиме "Только чтение"|Улучшение|
|PSDNET-171|После создания нового текстового слоя файл PSD становится недоступным для PS|Ошибка|
|PSDNET-156|Исключение при загрузке PSD|Ошибка|

## **Изменения в общедоступном API**
# **Добавленные API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **Удаленные API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Примеры использования:**
**PSDNET-184. Загрузка JPEG, PNG и других изображений в PsdImage из потока**

{{< highlight java >}}

    // загрузить JPEG, PNG и другие изображения в PsdImage из потока

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

**PSDNET-134. Реализация отображения слоя заполнения: Градиент**

{{< highlight java >}}

             // Реализация отображения слоя заполнения: Градиент

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

**PSDNET-166. Сохранение PSD в PDF не обеспечивает выбор текста**

{{< highlight java >}}

  // Сохранение PSD в PDF не обеспечивает выбор текста

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. После создания нового текстового слоя файл PSD становится недоступным для PS**

{{< highlight java >}}

 // После создания нового текстового слоя на сборочном сервере файл PSD становится недоступным для PS

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Некоторый текст", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}

**PSDNET-156. Исключение при загрузке PSD**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. Высокое использование памяти при загрузке PSD в режиме "Только чтение"**

{{< highlight java >}}

 // Высокое использование памяти Aspose.PSD при загрузке PSD в режиме "Только чтение"

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // Использование памяти должно быть менее 100 МБ для этих примеров

            if (memoryUsed > 100)

            {

                throw new Exception("Использование памяти слишком велико");

            }

{{< /highlight >}}

**PSDNET-158. Поддержка сохранения PSB как PDF**

{{< highlight java >}}

 // Поддержка сохранения PSB как PDF

    string sourceFileName = "sample.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "sample.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}
