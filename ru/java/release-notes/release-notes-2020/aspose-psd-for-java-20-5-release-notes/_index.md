---
title: Заметки к выпуску Aspose.PSD для Java 20.5
type: docs
weight: 40
url: /ru/java/aspose-psd-for-java-20-5-release-notes/
---

{{% alert color="primary" %}} На этой странице содержатся заметки о выпуске [Aspose.PSD для Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) {{% /alert %}} 

|**Ключ**|**Сводка**|**Категория**|
| :- | :- | :- |
|PSDJAVA-188|Поддержка прогресса конвертации документа|Функция|
|PSDJAVA-197|Поддержка сохранения изображения PSD в цветовом режиме Grayscale ColorMode с 16 битами на канал|Функция|
|PSDJAVA-198|Поддержка ресурса Nvrt (ресурс слоя коррекции инверсии)|Функция|
|PSDJAVA-200|Поддержка масок слоев для групп слоев|Функция|
|PSDJAVA-195|Исправление сохранения изображения PSD в цветовом режиме Grayscale с 16 битами на канал в формат PSD RGB с 16 битами на канал|Ошибка|
|PSDJAVA-196|Исправление сохранения изображения PSD в цветовом режиме Grayscale с 16 битами на канал в формат PSD Grayscale с 8 битами на канал|Ошибка|
|PSDJAVA-199|Выравнивание текста через ITextPortion не работает для правосторонних языков. Выходной файл поврежден|Ошибка|
|PSDJAVA-201|Исключение при попытке открыть определенный файл Psd с цветом Лаборатории и 8 бит/канал|Ошибка|
# **Изменения в общедоступном API**
# **Добавленные API:**
- Нет
## **Удаленные API:**
- Нет
# **Примеры использования:**

**PSDJAVA-188. Поддержка прогресса конвертации документа**

{{< highlight java >}}

 // Пример использования обработчика прогресса для операций загрузки и сохранения.

// Программа использует различные варианты сохранения для вызова событий прогресса.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// Создаем обработчик прогресса, который записывает информацию о прогрессе в консоль

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s из %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Загрузка Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Привязываем обработчик прогресса для отображения прогресса загрузки

loadOptions.setProgressEventHandler(localProgressEventHandler);

// Загрузка PSD с использованием конкретных параметров загрузки

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Сохранение Apple.psd в формат PNG ----------");

    PngOptions pngOptions = new PngOptions();

    // Делаем выходное изображение цветным и непрозрачным

    pngOptions.setColorType(PngColorType.Truecolor);

    // Привязываем обработчик прогресса для отображения прогресса сохранения

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // Конвертируем PSD в PNG с конкретными характеристиками

    image.save(outputStream, pngOptions);

    System.out.println("---------- Сохранение Apple.psd в формат PSD ----------");

    PsdOptions psdOptions = new PsdOptions();

    // Делаем выходное PSD цветным

    psdOptions.setColorMode(ColorModes.Rgb);

    // Устанавливаем по каналу на каждый цвет (красный, зеленый и синий) плюс композитный канал

    psdOptions.setChannelsCount((short)4);

    // Привязываем обработчик прогресса для отображения прогресса сохранения

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // Сохраняем копию PSD с конкретными характеристиками

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Поддержка сохранения изображения PSD в цветовом режиме Grayscale с 16 битами на канал**

{{< highlight java >}}

 // Пример применения различных комбинаций цветовых режимов, бит на канал, количества

// каналов и сжатий для определенных слоев.

// Делаем метод доступным из локальной области видимости

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String file,

            short colorMode,

            short channelBitsCount,

            short channelsCount,

            short compression,

            int layerNumber)

    {

        String filePath = file + ".psd";

        String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +

                channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);

        String exportPath = file + postfix + ".psd";

        String pngExportPath = file + postfix + ".png";

        // Загружаем предопределенный 16-битный PSD в оттенках серого

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // Рисуем серую внутреннюю границу вокруг периметра слоя

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // Сохраняем копию PSD с конкретными характеристиками

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(colorMode);

            psdOptions.setChannelBitsCount(channelBitsCount);

            psdOptions.setChannelsCount(channelsCount);

            psdOptions.setCompressionMethod(compression);

            image.save(exportPath, psdOptions);

        }

        finally

        {

            image.dispose();

        }

        // Загружаем сохраненный PSD

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // Конвертируем сохраненный PSD в оттенок серого изображение PNG

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // здесь не должно быть исключения

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. Поддержка ресурса Nvrt (ресурс слоя коррекции инверсии)**

{{< highlight java >}}

 // Пример поиска ресурса NvrtResource слоя коррекции инверсии.

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// Загружаем предопределенный PSD, содержащий слой коррекции инверсии

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Пытаемся найти ресурс слоя коррекции инверсии

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // Найден ресурс NvrtResource

                    nvrtResource = (NvrtResource)layerResource;

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-200. Поддержка масок слоев для групп слоев**

{{< highlight java >}}

 // Пример поддержки масок слоев для групп слоев. Программа загружает и сохраняет PSD

// в различных выходных форматах без выбрасывания исключений.

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// Загружаем предопределенный PSD, содержащий маски слоев для групп слоев

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // Конвертируем загруженный PSD в PNG

    input.save(outputPng, new PngOptions());

    // Сохраняем копию PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. Исправление сохранения изображения PSD в цветовом режиме Grayscale с 16 битами на канал в формат PSD RGB с 16 битами на канал**

{{< highlight java >}}

 // Пример преобразования 16-битного PSD в оттенках серого в 16-битный RGB и обратно

// к 16-битному оттенку серого, но с растром.

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// Загружаем предопределенный 16-битный PSD в оттенках серого

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Рисуем серую внутреннюю границу вокруг периметра слоя

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Сохраняем копию PSD с измененным цветовым режимом на RBG

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Rgb);

    psdOptions.setChannelBitsCount((short)16);

    psdOptions.setChannelsCount((short)4);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// Загружаем сохраненный PSD

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Конвертируем сохраненный PSD в оттенок серого изображение PNG

    image1.save(pngExportPath, pngOptions); // здесь не должно быть исключения

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. Исправление сохранения изображения PSD в цветовом режиме Grayscale с 16 битами на канал в формат PSD Grayscale с 8 битами на канал**

{{< highlight java >}}

 // Пример преобразования 16-битного PSD в оттенках серого в 8-битный оттенок серого и затем

// в 8-битное серое растровое изображение.

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// Загружаем предопределенный 16-битный PSD в оттенках серого

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Рисуем серую внутреннюю границу вокруг периметра слоя

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Сохраняем копию PSD с измененным количество каналов на 8-битный

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Grayscale);

    psdOptions.setChannelBitsCount((short)8);

    psdOptions.setChannelsCount((short)2);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// Загружаем сохраненный PSD

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Конвертируем сохраненный PSD в оттенок серого изображение PNG

    image1.save(pngExportPath, pngOptions); // здесь не должно быть исключения

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. Выравнивание текста через ITextPortion не работает для правосторонних языков. Выходной файл поврежден.**

{{< highlight java >}}

 // Пример выравнивания текстового слоя справа налево через ITextPortion. Программа модифицирует

// существующий текстовый слой RTL в загруженном PSD и сохраняет копию измененного документа.

String sourceFileName = "bidi.psd";

String outputFileName = "bidiOutput.psd";

// Загружаем предопределенный PSD, содержащий RTL текстовый слой

PsdImage image = (PsdImage)Image.load(sourceFileName);

try

{

    // Получаем части текста из слоя

    TextLayer layer = (TextLayer)image.getLayers()[2];

    ITextPortion[] portions = layer.getTextData().getItems();

    // Изменяем выравнивание текста

    portions[0].getParagraph().setJustification(2);

