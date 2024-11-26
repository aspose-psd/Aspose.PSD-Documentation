---
title: Примітки щодо випуску Aspose.PSD для .NET 18.8
type: docs
weight: 50
url: /uk/net/aspose-psd-for-net-18-8-release-notes/
---

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-68|Підтримка властивості LayerCreationDateTime.|Функціонал|
|PSDNET-67|Підтримка підсвітки SheetColor.|Функціонал|
|PSDNET-66|Можливість об'єднати шари один з одним.|Функціонал|
|PSDNET-65|Додана часткова підтримка властивості Text Layer BoundBox.|Функціонал|
|PSDNET-64|Додана підтримка IopaResource.|Функціонал|
|PSDNET-56|Підтримка ефектів шару для формату PSD.|Функціонал|
|PSDNET-55|Підтримка InterruptMonitor для .Net.|Функціонал|
|PSDNET-50|Можливість злиття шарів.|Функціонал|
|PSDNET-49|Додано відтворення властивості прозорості заливки на шарах.|Функціонал|
|PSDNET-43|Здійснення рендерингу шара коригування кривих.|Функціонал|
|PSDNET-42|Додана підтримка шара коригування кривих.|Функціонал|
|PSDNET-41|Здійснення рендерингу шара коригування рівнів.|Функціонал|
|PSDNET-40|Додана підтримка шара коригування рівнів.|Функціонал|
|PSDNET-37|Додана підтримка шара коригування каналів Channel Mixer.|Функціонал|
|PSDNET-35|Додана підтримка шара коригування відтінків/насиченості Hue/Saturation.|Функціонал|
|PSDNET-34|Здійснення рендерингу шара коригування експозиції для експорту.|Функціонал|
|PSDNET-31|Додана підтримка рендерингу для експорту шара коригування Channel Mixer.|Функціонал|
|PSDNET-26|Додана підтримка обрізного маскування.|Функціонал|
|PSDNET-13|Додана підтримка маски шара.|Функціонал|
|PSDNET-9|Додана підтримка шара коригування фільтрації фотографій Photo Filter.|Функціонал|
|PSDNET-8|Додана підтримка шара коригування каналів Channel mixer.|Функціонал|
|PSDNET-7|Додана підтримка шара коригування експозиції Exposure.|Функціонал|
|PSDNET-6|Додана підтримка шара коригування яскравості/контрастності Brightness/Contrast.|Функціонал|
|PSDNET-5|Додана часткова підтримка шарів коригування.|Функціонал|
|PSDNET-3|Додана підтримка параметра тексту PSD без розбивки.|Функціонал|
|PSDNET-2|Можливість додавання шару тексту під час роботи.|Функціонал|
|PSDNET-62|TIFF Кодек не може зберегти зображення з 16-бітним каналом.|Покращення|
|PSDNET-61|Збереження зображення PSD призводить до невірних кольорів зображення.|Покращення|
|PSDNET-60|Координати верхнього лівого кута неправильні під час оновлення.|Покращення|
|PSDNET-59|Виникнення помилки під час оновлення текстових шарів.|Покращення|
|PSDNET-58|Публічно викласти властивість Codec зображення JPEG2000.|Покращення|
|PSDNET-57|Виправлення налаштувань 24 біт на побітову глибину для експорту в BMP.|Покращення|
|PSDNET-46|Шар коригування ігнорується під час конвертації PSD CMYK в TIFF або JPG.|Покращення|

## **Приклади використання:**

**PSDNET-68 Підтримка властивості LayerCreationDateTime**

{{< highlight java >}}

 // Приклад використання властивості LayerCreationDateTime

string sourceFileName = "OneLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // Перевірте, чи Дата створення Час оновлюється на новостворених шарах

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 Підтримка підсвітки SheetColor**

{{< highlight java >}}

 // Приклад використання властивості SheetColorHighlight

string sourceFileName = "SheetColorHighlightExample.psd";

string exportPath = "SheetColorHighlightExampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer1 = im.Layers[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, layer1.SheetColorHighlight);

    var layer2 = im.Layers[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, layer2.SheetColorHighlight);

    layer1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-66 Можливість об'єднати шари один з одним**

{{< highlight java >}}

 // Приклад об'єднання двох шарів

var sourceFile1 = "FillOpacitySample.psd";

var sourceFile2 = "ThreeRegularLayersSemiTransparent.psd";

var exportPath = "MergedLayersFromTwoDifferentPsd.psd" 

using (var im1 = (PsdImage)(Image.Load(sourceFile1)))

{

    var layer1 = im1.Layers[1];

    using (var im2 = (PsdImage)(Image.Load(sourceFile2)))

    {

        var layer2 = im2.Layers[0];

        layer1.MergeLayerTo(layer2);

        im2.Save(exportPath);	

    }

}

{{< /highlight >}}**PSDNET-65 Додана часткова підтримка властивості Text Layer BoundBox**

{{< highlight java >}}

 // Приклад використання властивості TextBoundBox

string sourceFileName = "LayerWithText.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 Додана підтримка IopaResource**

{{< highlight java >}}

 // Зміна властивості Fill Opacity за допомогою IopaResource

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];

    var resources = layer.Resources;

    foreach (var resource in resources)

    {

        if (resource is IopaResource)

        {

            var iopaResource = (IopaResource)resource;

            iopaResource.FillOpacity = 200;

        }

    }

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-56 Підтримка ефектів шару для формату PSD**

{{< highlight java >}}

 using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFileName, new Aspose.PSD.ImageLoadOptions.PsdLoadOptions() { LoadEffectsResource = true, UseDiskForLoadEffectsResource = true }))
{
    image.Save(output, new Aspose.PSD.ImageOptions.PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}

{{< /highlight >}}

**PSDNET-55 Підтримка InterruptMonitor для .Net**

{{< highlight java >}}

public void InterruptMonitorTest(string dir, string ouputDir)
{
    ImageOptionsBase saveOptions = new ImageOptions.PngOptions();
    Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();
    SaveImageWorker worker = new SaveImageWorker(dir + "big.psb", dir + "big_out.png", saveOptions, monitor);
    System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(worker.ThreadProc));
    try
    {
        thread.Start();
        // Тайм-аут повинен бути менше часу, потрібного для повного конвертування зображення (без переривання).
        System.Threading.Thread.Sleep(3000);
        // Перервати процес
        monitor.Interrupt();
        System.Console.WriteLine("Переривання потоку зберігання #{0} at {1}", thread.ManagedThreadId, System.DateTime.Now);
        // Чекаємо на переривання...
        thread.Join();
    }
    finally
    {
        // Якщо файл для видалення не існує, виняток не виникає
        System.IO.File.Delete(dir + "big_out.png");
    }
}

private class SaveImageWorker
{
    private readonly string inputPath;

    private readonly string outputPath;

    private readonly Multithreading.InterruptMonitor monitor;

    private readonly ImageOptionsBase saveOptions;

    public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)
    {
        this.inputPath = inputPath;
        this.outputPath = outputPath;
        this.saveOptions = saveOptions;
        this.monitor = monitor;
    }

    public void ThreadProc()
    {
        using (Image image = Image.Load(this.inputPath))
        {
            Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;
            try
            {
                image.Save(this.outputPath, this.saveOptions);
                Assert.Fail("Очікуване переривання.");
            }
            catch (CoreExceptions.OperationInterruptedException e)
            {
                System.Console.WriteLine("Потік зберігання #{0} завершується at {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);
                System.Console.WriteLine(e);
            }
            catch (System.Exception e)
            {
                System.Console.WriteLine(e);
            }
            finally
            {
                Multithreading.InterruptMonitor.ThreadLocalInstance = null;
            }
        }
    }
}

{{< /highlight >}}