--- 
title: Забележки към версия 20.5 на Aspose.PSD за .NET
type: docs
weight: 80
url: /bg/net/aspose-psd-za-net-20-5-zabelezhki-kam-izdavaneto/
---

{{% alert color="primary" %}}

Тази страница съдържа забележки към [Aspose.PSD за .NET 20.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Обобщение**|**Категория**|
| :- | :- | :- |
|PSDNET-595|Поддръжка на слойни маски за групи на слоеве|Функционалност|
|PSDNET-201|Поддръжка на прогрес при конвертиране на документи|Функционалност|
|PSDNET-275|Поддръжка на Nvrt ресурс (ресурс за корекция на инверсия на слой)|Функционалност|
|PSDNET-124|Поддръжка на запазване на PSD изображение с цветови режим на сиво с 16 бита на канал|Функционалност|
|PSDNET-589|Рефакториране на примерите в GitHub|Подобрение|
|PSDNET-587|Подравняване на текст чрез ITextPortion не работи за дясно-наляви езици. Изходният файл е повреден.|Проблем|
|PSDNET-604|Изключение при опит за отваряне на конкретен Psd файл с Lab цвят и 8 бита/канал|Проблем|
|PSDNET-598|Оправяне на запазване на PSD изображение с цветови режим на сиво с 16 бита на канал до 8 бита на канал формат на сиво-картинен PSD|Проблем|
|PSDNET-599|Оправяне на запазване на PSD изображение с цветови режим на сиво с 16 бита на канал до 16 бита на канал RGB формат PSD|Проблем|

## **Промени в общественото API**
# **Добавени APIs:**
- Няма
# **Премахнати APIs:**
- Няма

## **Примери за използване:**
**PSDNET-595. Поддръжка на слойни маски за групи на слоеве**

{{< highlight java >}}

 string srcFile = "psdnet595.psd";

string outputPng = "output.png";

string outputPsd = "output.psd";

using (var input = (PsdImage)Image.Load(srcFile))

{

     input.Save(outputPng, new PngOptions());

     input.Save(outputPsd);

}

{{< /highlight >}}

**PSDNET-201. Поддръжка на прогрес при конвертиране на документи**

{{< highlight java >}}

 string sourceFilePath = "Apple.psd";

Stream outputStream = new MemoryStream();

ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)

{

      string message = string.Format(

           "{0} {1}: {2} от {3}",

           progressInfo.Description,

           progressInfo.EventType,

           progressInfo.Value,

           progressInfo.MaxValue);

      Console.WriteLine(message);

};

Console.WriteLine("---------- Зареждане на Apple.psd ----------");

var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };

using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))

{

      Console.WriteLine("---------- Запазване на Apple.psd в PNG формат ----------");

      image.Save(

           outputStream,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler

           });

      Console.WriteLine("---------- Запазване на Apple.psd в PSD формат ----------");

      image.Save(

           outputStream,

           new PsdOptions()

           {

                 ColorMode = ColorModes.Rgb,

                 ChannelsCount = 4,

                 ProgressEventHandler = localProgressEventHandler

           });

}

{{< /highlight >}}

**PSDNET-275. Поддръжка на Nvrt ресурс (ресурс за корекция на инверсия на слой)**

{{< highlight java >}}

 using (var psdImage = (PsdImage)Image.Load("InvertAdjustmentLayer.psd"))

{

      foreach (var layer in psdImage.Layers)

      {

           if (layer is InvertAdjustmentLayer)

           {

                 foreach (var layerResource in layer.Resources)

                 {

                      if (layerResource is NvrtResource)

                      {

                           // Ресурсът NvrtResource е поддържан.

                           var resource = (NvrtResource)layerResource;

                           break;

                      }

                 }

           }

      }

}

{{< /highlight >}}

**PSDNET-124. Оправяне на запазване на PSD изображение с цветови режим на сиво с 16 бита на канал до формат на сиво-картинен PSD с 8 бита на канал**

{{< highlight java >}}

 void SaveToPsdThenLoadAndSaveToPng(

    string file,

    ColorModes colorMode,

    short channelBitsCount,

    short channelsCount,

    CompressionMethod compression,

    int layerNumber)

{

    string filePath = file + ".psd";

    string postfix = colorMode.ToString() + channelBitsCount + "_" + channelsCount + "_" + compression;

    string exportPath = @"Output\" + file + postfix + ".psd";

    PsdOptions psdOptions = new PsdOptions()

    {

        ColorMode = colorMode,

        ChannelBitsCount = channelBitsCount,

        ChannelsCount = channelsCount,

        CompressionMethod = compression

    };

    using (PsdImage image = (PsdImage)Image.Load(filePath))

    {

        RasterCachedImage raster = layerNumber >= 0 ? (RasterCachedImage)image.Layers[layerNumber] : image;

        Aspose.PSD.Graphics graphics = new Graphics(raster);

        int width = raster.Width;

        int height = raster.Height;

        Rectangle rect = new Rectangle(

            width / 3,

            height / 3,

            width - (2 * (width / 3)) - 1,

            height - (2 * (height / 3)) - 1);

        graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), rect);

        image.Save(exportPath, psdOptions);

    }

    string pngExportPath = Path.ChangeExtension(exportPath, "png");

    using (PsdImage image = (PsdImage)Image.Load(exportPath))

    {

        // Тук не би трябвало да има изключение.

        image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

    }

}

SaveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, 16, 5, CompressionMethod.RLE, 0);

SaveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, 0);

SaveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

SaveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, 0);

SaveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

SaveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

SaveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDNET-587. Подравняване на текст чрез ITextPortion не работи за дясно-наляви езици. Изходният файл е повреден.**

{{< highlight java >}}

 string sourceFileName = "bidi.psd";

string outputFileName = "bidiOutput.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    var layer = (TextLayer)image.Layers[2];

    var portions = layer.TextData.Items;

    portions[0].Paragraph.Justification = 2;

    layer.TextData.UpdateLayerData();

    image.Save(outputFileName);

}

{{< /highlight >}}

` `**PSDNET-604. Изключение при опит за отваряне на конкретен Psd файл с Lab цвят и 8 бита/канал**

{{< highlight java >}}

 string srcFile = "Untitled-1.psd";

string outputFilePsd = "output.psd";

using (var psdImage = (PsdImage)Image.Load(srcFile))

{

    psdImage.Save(outputFilePsd);

}

// Файлът LAB е зареден и записан без хвърляне на изключения.

{{< /highlight >}}

**PSDNET-598. Оправяне на запазване на PSD изображение с цветови режим на сиво с 16 бита на канал до 8 бита на канал формат на сиво-картинен PSD**

{{< highlight java >}}

 string sourceFileName = "grayscale16bit.psd";

string exportFileName = "grayscale16bit_output.psd";

PsdOptions psdOptions = new PsdOptions()

{

    ColorMode = ColorModes.Grayscale,

    ChannelBitsCount = 8,

    ChannelsCount = 2

};

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    RasterCachedImage raster = image.Layers[0];

    Aspose.PSD.Graphics graphics = new Graphics(raster);

    int width = raster.Width;

    int height = raster.Height;

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), rect);

    image.Save(exportFileName, psdOptions);

}

string pngExportPath = Path.ChangeExtension(exportFileName, "png");

using (PsdImage image = (PsdImage)Image.Load(exportFileName))

{

    // Тук не би трябвало да има изключение.

    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}

**PSDNET-599. Оправяне на запазване на PSD изображение с цветови режим на сиво с 16 бита на канал до 16бита на канал RGB формат PSD**

{{< highlight java >}}

 string sourceFileName = "grayscale16bit.psd";

string exportFileName = "grayscale16bit_output.psd";

PsdOptions psdOptions = new PsdOptions()

{

    ColorMode = ColorModes.Rgb,

    ChannelBitsCount = 8,

    ChannelsCount = 4

};

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    RasterCachedImage raster = image.Layers[0];

    Aspose.PSD.Graphics graphics = new Graphics(raster);

    int width = raster.Width;

    int height = raster.Height;

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), rect);

    image.Save(exportFileName, psdOptions);

}

string pngExportPath = Path.ChangeExtension(exportFileName, "png");

using (PsdImage image = (PsdImage)Image.Load(exportFileName))

{

    // Тук не би трябвало да има изключение.

    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}
