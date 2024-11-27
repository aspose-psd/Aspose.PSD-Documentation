---
title: Aspose.PSD за Java 20.5 - Бележки за версията
type: docs
weight: 40
url: /bg/aspose-psd-za-java-20-5-release-notes/
---

{{% alert color="primary" %}} Тази страница съдържа бележки за версията на [Aspose.PSD за Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) {{% /alert %}} 

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDJAVA-188|Поддръжка за напредъка на преобразуването на документ|Функционалност|
|PSDJAVA-197|Поддръжка на запазване на изображение в PSD формат със Цветови режим на Градацията на сивото с 16 бита на канал|Функционалност|
|PSDJAVA-198|Поддръжка на ресурс за Invert Настройка на слоя на Nvrt (Инверсно Настройка на слоя)|Функционалност|
|PSDJAVA-200|Поддръжка на слойни маски за групи от слоеве|Функционалност|
|PSDJAVA-195|Оправяне на запазването на PSD изображение с Цветови режим на Градацията на сивото с 16 бита на канал към PSD формат с 16 бита на канал RGB|Проблем|
|PSDJAVA-196|Оправяне на запазването на PSD изображение с Цветови режим на Градацията на сивото с 16 бита на канал към 8 бита на канал Цветови градации в PSD формат|Проблем|
|PSDJAVA-199|Позициониране на текста чрез ITextPortion не работи за дясно-наляво езици. Изходният файл е повреден.|Проблем|
|PSDJAVA-201|Изключение при опит за отваряне на конкретен PSD файл с цвят на Лаб и 8 бита/канал|Проблем|
# **Промени в обществените API**
# **Добавени API-та:**
- Никакви
## **Премахнати API-та:**
- Никакви
# **Примери за използване:**

**PSDJAVA-188. Поддръжка за напредъка на преобразуването на документ**

{{< highlight java >}}

 // Пример за използване на обработчика на напредъка за зареждане и запазване на операции.

// Програмата използва различни опции за запазване, за да активира събития за напредъка.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// Създайте обработчик на напредъка, който записва информация за напредъка в конзолата

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s out of %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Зареждане на Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Присъединете обработчика на напредъка, за да се покаже напредъка на зареждане

loadOptions.setProgressEventHandler(localProgressEventHandler);

// Заредете PSD с определени опции за зареждане

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Запазване на Apple.psd като PNG формат ----------");

    PngOptions pngOptions = new PngOptions();

    // Направете изображението цветно и не прозрачно

    pngOptions.setColorType(PngColorType.Truecolor);

    // Присъединете обработчика на напредъка, за да се покаже напредъка на запазване

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // Конвертирайте PSD в PNG с определени характеристики

    image.save(outputStream, pngOptions);

    System.out.println("---------- Запазване на Apple.psd като PSD формат ----------");

    PsdOptions psdOptions = new PsdOptions();

    // Направете изходното PSD цветно

    psdOptions.setColorMode(ColorModes.Rgb);

    // Задайте канал за всяка цветова гама (червено, зелено и синьо) плюс композитен канал

    psdOptions.setChannelsCount((short)4);

    // Присъединете обработчика на напредъка, за да се покаже напредъка при запазване

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // Запазете копие на PSD с определени характеристики

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Поддръжка на запазване на изображение в PSD формат с цветови режим на Градацията на сивото с 16 бита на канал**

{{< highlight java >}}

 // Пример за прилагане на различни комбинации от цветови режими, битове на канал, брой канали

// и компресии за специфични слоеве.

// Нека един метод бъде достъпен от локалния обхват

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String file,

            short цветовиРежим,

            short бройБитаНаКанал,

            short бройКанали,

            short компресия,

            int номерНаСлоя)

    {

        String filePath = file + ".psd";

        String postfix = Enum.getName(ColorModes.class, цветовиРежим) + бройБитаНаКанал + "_" +

                бройКанали + "_" + Enum.getName(CompressionMethod.class, компресия);

        String exportPath = file + postfix + ".psd";

        String pngExportPath = file + postfix + ".png";

        // Заредете предварително зададен 16-битов PSD с нива на сивота

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = номерНаСлоя >= 0 ? image.getLayers()[номерНаСлоя] : image;

            // Начертайте сив вътрешен контур около периметъра на слоя

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // Запазете копие на PSD с определени характеристики

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(цветовиРежим);

            psdOptions.setChannelBitsCount(бройБитаНаКанал);

            psdOptions.setChannelsCount(бройКанали);

            psdOptions.setCompressionMethod(компресия);

            image.save(exportPath, psdOptions);

        }

        finally

        {

            image.dispose();

        }

        // Заредете запазения PSD

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // Конвертирайте запазения PSD в сиво PNG изображение

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // тук не трябва да има изключение

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

**PSDJAVA-198. Поддръжка на ресурс за Invert Настройка на слоя**

{{< highlight java >}}

 // Пример за намиране на ресурс от инвертиран слой за настройка.

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// Зареждане на предварително зададен PSD с инверсен слой за настройка

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Опитайте се да намерите ресурс на инверсния слой за настройка

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // Намерен е ресурсът NvrtResource

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

**PSDJAVA-200. Поддръжка на слойни маски за групи от слоеве**

{{< highlight java >}}

 // Пример за поддръжка на слойни маски за групи от слоеве. Програмата зарежда и запазва PSD

// в различни изходни формати без изхвърляне на изключения.

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// Заредете предварително зададен PSD, съдържащ слойни маски за групи от слоеве

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // Конвертирайте заредения PSD в PNG

    input.save(outputPng, new PngOptions());

    // Запазете копие на PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. Оправяне на запазването на PSD изображение с Цветови режим на Градацията на сивото с 16 бита на канал към 16 бита на канал RGB PSD формат**

{{< highlight java >}}

 // Пример за преобразуване на 16-битов PSD с нива на сивота към 16-битов RGB и после обратно към

// 16-битово сиво изображение.

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// Заредете предварително зададен 16-битов PSD с нива на сивота

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Начертайте сив вътрешен контур около периметъра на слоя

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Запазете копие на PSD с променен цветови режим на RBG

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

// Заредете запазения PSD

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Конвертирайте запазения PSD в сиво PNG изображение

    image1.save(pngExportPath, pngOptions); // тук не трябва да има изключение

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. Оправяне на запазването на PSD изображение с Цветови режим на Градацията на сивото с 16 бита на канал към 8 бита на канал Цветови градации в PSD формат**

{{< highlight java >}}

 // Пример за преобразуване на 16-битов PSD с нива на сивота към 8-битово сиво и после към

// 8-битово сиво растерно изображение.

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// Заредете предварително зададен 16-битов PSD с нива на сивота

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Начертайте сив вътрешен контур около периметъра на слоя

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Запазете копие на PSD с променено брой канали на 8-битовата скала

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Grayscale);

    psdOptions.setChannelBitsCount((short)8);

    psdOptions.setChannelsCount((short)2);

    image.save(exportFilePath, ps