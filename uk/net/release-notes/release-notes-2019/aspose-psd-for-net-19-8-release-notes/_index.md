---
title: Опис версії Aspose.PSD для .NET 19.8
type: docs
weight: 50
url: /uk/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить опис версії Aspose.PSD для .NET 19.8

{{% /alert %}}

|**Ключ**|**Зміст**|**Категорія**|
| :- | :- | :- |
|PSDNET-184|Завантаження файлів зображень JPEG, PNG та інших до PsdImage з потоку|Функціонал|
|PSDNET-134|Реалізація рендерингу Fill Layer: Gradient|Функціонал|
|PSDNET-166|Збереження PSD у PDF не забезпечує вибіркового тексту|Функціонал|
|PSDNET-158|Підтримка збереження PSB у PDF|Функціонал|
|PSDNET-189|Високе використання пам'яті при завантаженні PSD з режимом "тільки для читання"|Покращення|
|PSDNET-171|Після створення нового TextLayer файл PSD стає нерозпізнаваним для PS|Помилка|
|PSDNET-156|Виняток під час завантаження PSD|Помилка|

## **Зміни в об'єктному API**
# **Додані API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **Вилучені API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Приклади використання:**
**PSDNET-184. Завантаження файлів зображень JPEG, PNG та інших до PsdImage з потоку**

{{< highlight java >}}

    // завантаження файлів зображень JPEG, PNG та інших до PsdImage з потоку

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

**PSDNET-134. Реалізація рендерингу Fill Layer: Gradient**

{{< highlight java >}}

             // Реалізація рендерингу Fill Layer: Gradient

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

**PSDNET-166. Збереження PSD у PDF не забезпечує вибіркового тексту**

{{< highlight java >}}

  // Збереження PSD у PDF не забезпечує вибіркового тексту

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. Після створення нового TextLayer файл PSD стає нерозпізнаваним для PS**

{{< highlight java >}}

 // Після створення нового TextLayer на Build Server, файл PSD стає нерозпізнаваним для PS

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Some text", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}



**PSDNET-156. Виняток під час завантаження PSD**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. Високе використання пам'яті при завантаженні PSD з режимом "тільки для читання"**

{{< highlight java >}}

 // Високе використання пам'яті Aspose.PSD при завантаженні PSD з режимом "тільки для читання"

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // Використання пам'яті повинно бути менше 100 MB для цих прикладів

            if (memoryUsed > 100)

            {

                throw new Exception("Використання пам'яті є занадто великим");

            }

{{< /highlight >}}

**PSDNET-158. Підтримка збереження PSB у PDF**

{{< highlight java >}}

 // Підтримка збереження PSB у PDF

    string sourceFileName = "sample.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "sample.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}
