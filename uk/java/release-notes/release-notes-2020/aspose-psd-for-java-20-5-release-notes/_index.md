---
title: Aspose.PSD для Java 20.5 - Примітки до випуску
type: docs
weight: 40
url: /uk/java/aspose-psd-dlya-java-20-5-release-notes/
---

{{% alert color="primary" %}} Ця сторінка містить примітки до випуску [Aspose.PSD для Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) {{% /alert %}} 

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDJAVA-188|Підтримка показу прогресу конвертації документа|Функціонал|
|PSDJAVA-197|Підтримка збереження монохромного зображення у режимі кольору Grayscale PSD з 16 біт на канал|Функціонал|
|PSDJAVA-198|Підтримка ресурсу Nvrt (ресурс налаштування обернення)|Функціонал|
|PSDJAVA-200|Підтримка масок шарів для груп шарів|Функціонал|
|PSDJAVA-195|Виправлення збереження PSD-зображення у режимі кольору Grayscale з 16 біт на канал у форматі RGB PSD з 16 біт на канал|Помилка|
|PSDJAVA-196|Виправлення збереження PSD-зображення у режимі кольору Grayscale з 16 біт на канал у форматі Grayscale PSD з 8 біт на канал|Помилка|
|PSDJAVA-199|Вирівнювання тексту через ITextPortion не працює для праворуч говорячих мов. Вихідний файл пошкоджено|Помилка|
|PSDJAVA-201|Виняток при спробі відкрити певний файл Psd у кольорі Lab та 8 біт / канал|Помилка|
# **Зміни в публічному API**
# **Додані API:**
- Немає
## **Вилучені API:**
- Немає
# **Приклади використання:**

**PSDJAVA-188. Підтримка показу прогресу конвертації документа**

{{< highlight java >}}

 // Приклад використання обробника прогресу для операцій завантаження та збереження.

// Програма використовує різні параметри збереження для виклику подій прогресу.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// Створення обробника прогресу, який записує інформацію про прогрес у консоль

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s із %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Завантаження Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Прив'язати обробника прогресу для показу прогресу завантаження

loadOptions.setProgressEventHandler(localProgressEventHandler);

// Завантажити PSD зі специфічними параметрами завантаження

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Збереження Apple.psd у форматі PNG ----------");

    PngOptions pngOptions = new PngOptions();

    // Зробити выхідне зображення кольоровим і непрозорим

    pngOptions.setColorType(PngColorType.Truecolor);

    // Прив'язати обробника прогресу для показу прогресу збереження

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // Конвертувати PSD в PNG зі специфічними характеристиками

    image.save(outputStream, pngOptions);

    System.out.println("---------- Збереження Apple.psd у форматі PSD ----------");

    PsdOptions psdOptions = new PsdOptions();

    // Здійснює вихідний PSD кольоровим

    psdOptions.setColorMode(ColorModes.Rgb);

    // Встановити канал для кожного кольору (червоний, зелений і синій) плюс комбінований канал

    psdOptions.setChannelsCount((short)4);

    // Прив'язати обробника прогресу для показу прогресу збереження

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // Зберегти копію PSD зі специфічними характеристиками

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Підтримка збереження монохромного зображення у режимі кольору Grayscale PSD з 16 біт на канал**

{{< highlight java >}}

 // Приклад застосування різних комбінацій кольорових режимів, бітів на канал, кількості каналів

// та стиснень для конкретних шарів.

// Зробити метод доступним у локальному контексті

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

        // Завантажити попередньо визначений 16-бітний монохромний PSD

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // Намалювати сірий внутрішній бордюр навколо периметра шару

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // Зберегти копію PSD зі специфічними характеристиками

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

        // Завантажити збережений PSD

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // Конвертувати збережений PSD у монохромне PNG-зображення

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // тут не повинно бути винятку

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

**PSDJAVA-198. Підтримка ресурсу Nvrt (ресурс налаштування обернення випрямування)**

{{< highlight java >}}

 // Приклад пошуку ресурсу NvrtResource оберненої коригуючої шаруватості.

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// Завантажити попередньо визначений PSD, що містить обернений коригуючий шар

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Спробувати знайти ресурс оберненої коригуючої шару

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // Знайдено NvrtResource

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

**PSDJAVA-200. Підтримка масок шарів для груп шарів**

{{< highlight java >}}

 // Приклад підтримки масок шарів для груп шарів. Програма завантажує та зберігає PSD

// в різні формати виводу без викидання винятків.

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// Завантажити попередньо визначений PSD, що містить маски для груп шарів

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // Конвертувати завантажений PSD у PNG

    input.save(outputPng, new PngOptions());

    // Зберегти копію PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. Виправлення збереження PSD-зображення у режимі кольору Grayscale з 16 біт на канал у форматі RGB PSD з 16 біт на канал**

{{< highlight java >}}

 // Приклад конвертування 16-бітового монохромного PSD в 16-бітовий RGB та назад до

// 16-бітового монохромного растрового зображення.

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// Завантажити попередньо визначений 16-бітовий монохромний PSD

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Намалювати сірий внутрішній бордюр навколо периметра шару

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Зберегти копію PSD зі зміненим режимом кольору на RBG

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

// Завантажити збережений PSD

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Конвертувати збережений PSD у монохромне PNG-зображення

    image1.save(pngExportPath, pngOptions); // тут не повинно бути винятку

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. Виправлення збереження PSD-зображення у режимі кольору Grayscale з 16 біт на канал у форматі Grayscale PSD з 8 біт на канал**

{{< highlight java >}}

 // Приклад конвертування 16-бітового монохромного PSD в 8-бітовий монохромний та назад до

// монохромного растрового зображення з 8 бітами на канал.

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// Завантажити попередньо визначений 16-бітовий монохромний PSD

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Намалювати сірий внутрішній бордюр навколо периметра шару

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Зберегти копію PSD зі зміною кількост