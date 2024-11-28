---
title: Примечания к выпуску Aspose.PSD для Java 20.4
type: документация
weight: 30
url: /ru/java/aspose-psd-for-java-20-4-release-notes/
---

{{% alert color="primary" %}} На этой странице содержатся примечания к выпуску [Aspose.PSD для Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) {{% /alert %}} 

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDJAVA-156|Поддержка ресурса «Исходные данные вектора»|Функция|
|PSDJAVA-171|Поддержка lclrResource (Настройка цвета листа)|Функция|
|PSDJAVA-157|Поддержка свойств данных LengthRecord. (Операции с путями (логические операции), индекс формы в слое, количество записей с кривыми Безье)|Функция|
|PSDJAVA-158|Поддержка ресурса раздела изображения №1010 Цвет фона|Функция|
|PSDJAVA-161|Добавление слоев заполнения во время выполнения|Функция|
|PSDJAVA-168|Поддержка ресурса раздела изображения №1009 Информация о границе.|Функция|
|PSDJAVA-169|Поддержка слоев в файлах формата AI|Функция|
|PSDJAVA-163|Поддержка чтения и редактирования наложения градиентной поверхности на слое|Функция|
|PSDJAVA-164|Визуализация эффекта градиентного наложения на слое|Функция|
|PSDJAVA-149|Ошибка Aspose.PSD для Java при получении свойства textData.items текстового слоя|Ошибка|
|PSDJAVA-166|Исправление сохранения изображения PSD с режимом цветности Grayscale и 16 бит на канал в формат PSD в оттенках серого|Ошибка|
|PSDJAVA-167|Исправление сохранения изображения PSD с режимом цветности Grayscale и 16 бит на канал в формат PNG|Ошибка|
|PSDJAVA-159|Изменения свойства GradientOverlayEffect.BlendMode не отображаются в Photoshop.|Ошибка|

# **Изменения в публичном API**
## **Добавленные API:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.text.IText.producePortions(java.lang.String[],com.aspose.psd.fileformats.psd.layers.text.ITextStyle,com.aspose.psd.fileformats.psd.layers.text.ITextParagraph)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getBaselineShift
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxBold
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxItalic
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontBaseline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontCaps
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getStrikethrough
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getUnderline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setBaselineShift(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxBold(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxItalic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontBaseline(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontCaps(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setStrikethrough(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setUnderline(boolean)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Subscript
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Superscript
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.AllCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.SmallCaps
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream)
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream,boolean)

## **Удаленные API:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)

# **Примеры использования:**

**PSDJAVA-156. Поддержка ресурса «Исходные данные вектора»**

{{< highlight java >}}

 /*

Пример чтения и изменения ресурса «Исходные данные вектора».

*/

// Поддержка методов в локальной области для упрощения

class LocalScopeExtension

{

    VogkResource findFirstVogkResource(LayerResource[] layerResources)

    {

        VogkResource vogkResource = null;

        for (LayerResource layerResource : layerResources)

        {

            if (layerResource instanceof VogkResource)

            {

                vogkResource = (VogkResource)layerResource;

                break;

            }

        }

        if (vogkResource == null)

        {

            throw new Exception("Ресурс VogkResource не найден.");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// Загрузка файла PSD, содержащего предопределенный ресурс VOGK

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Найти первый VogkResource в ресурсах предопределенного слоя

    VogkResource vogkResource = $.findFirstVogkResource(

            psdImage.getLayers()[1].getResources());

    // Подтвердить свойства предопределенного ресурса

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("Ресурс VogkResource был неправильно прочитан.");

    }

    // Изменить некоторые свойства ресурса Vogk

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // Сохранить измененную копию загруженного файла PSD по указанному пути

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. Поддержка lclrResource (Настройка цвета листа)**

{{< highlight java >}}

 /*

Пример использования цвета листа слоя для визуального выделения слоев. Например, можно

обновить некоторые слои в PSD, а затем выделить цветом слой, который требуется выделить

внимание.

*/

class LocalScopeExtension

{

    void checkSheetColorsAndRerverse(Short[] sheetColors, PsdImage psdImage)

    {

        int layersCount = psdImage.getLayers().length;

        for (int layerIndex = 0; layerIndex < layersCount; layerIndex++)

        {

            Layer layer = psdImage.getLayers()[layerIndex];

            for (LayerResource layerResource : layer.getResources())

            {

                if (!(layerResource instanceof LclrResource))

                {

                    continue;

                }

                // Ресурс lcrl всегда присутствует в списке ресурсов файла psd.

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("Цвет листа был неправильно прочитан");

                }

                // Инверсия цвета листа. Установка выделения цветом слоя.

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// В файле цвета выделения слоев расположены в следующем порядке

Short[] sheetColors = new Short[] {

        SheetColorHighlightEnum.Red,

        SheetColorHighlightEnum.Orange,

        SheetColorHighlightEnum.Yellow,

        SheetColorHighlightEnum.Green,

        SheetColorHighlightEnum.Blue,

        SheetColorHighlightEnum.Violet,

        SheetColorHighlightEnum.Gray,

        SheetColorHighlightEnum.NoColor

};

// Загрузка файла PSD, содержащего предопределенный ресурс LclrResource

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    $.checkSheetColorsAndRerverse(sheetColors, psdImage);

    psdImage.save(outPsdFilePath, new PsdOptions());

}

finally

{

    psdImage.dispose();

}

// Загрузка только что сохраненного файла PSD

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // Инверсия цветов

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. Поддержка свойств данных LengthRecord. (Операции с путями (логические операции), индекс формы в слое, количество записей с кривыми Безье)**

{{< highlight java >}}

 /*

Пример изменения операций с путями при работе с формами. Программа считывает

предопределенные записи векторных путей (LengthRecord) и изменяет их операции с путями, затем сохраняет

измененную копию документа в новый файл PSD.

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// Загрузка файла PSD, содержащего предопределенный ресурс Vsms

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Найти первый VsmsResource в ресурсах предопределенного слоя

    VsmsResource resource = null;

    for (LayerResource layerResource : psdImage.getLayers()[1].getResources())

    {

        if (layerResource instanceof VsmsResource)

        {

            resource = (VsmsResource)layerResource;

            break;

        }

    }

    LengthRecord lengthRecord0 = (LengthRecord)resource.getPaths()[2];

    LengthRecord lengthRecord1 = (LengthRecord)resource.getPaths()[7];

    LengthRecord lengthRecord2 = (LengthRecord)resource.getPaths()[11];

    // Изменение способа объединения форм

    lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);

    lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);

    lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);

    // Сохранить измененную копию загруженного файла PSD по указанному пути

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-158. Поддержка ресурса раздела изображения №1010 Цвет фона**

{{< highlight java >}}

 /*

Пример чтения и изменения цвета фона.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// Загрузка файла PSD, содержащего предопределенный ресурс цвета фона

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    BackgroundColorResource backgroundColorResource = null;

    for (ResourceBlock imageResource : psdImage.getImageResources())

    {

        if (imageResource instanceof BackgroundColorResource)

        {

            backgroundColorResource = (BackgroundColorResource)imageResource;

            break;

        }

    }

    if (backgroundColorResource == null)

    {

        throw new Exception("Ресурс BackgroundColorResource не найден");

    }

    // Обновление цвета ресурса цвета фона

    backgroundColorResource.setColor(Color.getDarkRed());

    // Сохранить измененную копию загруженного файла PSD по указанному пути

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-161. Добавление слоев заполнения во время выполнения**

{{< highlight java >}}

 /*

Пример добавления слоев заполнения различных типов в документ Photoshop.

*/

String outPsdFilePath = "output.psd";

// Создание документа Photoshop с пустым холстом

PsdImage psdImage = new PsdImage(100, 100);

try

{

    // Добавление слоев заполнения различных типов в PSD

    FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);

    colorFillLayer.setDisplayName("Слой заливки цветом");

    psdImage.addLayer(colorFillLayer);

    FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);

    gradientFillLayer.setDisplayName("Слой градиентной заливки");

    psdImage.addLayer(gradientFillLayer);

    FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);

    patternFillLayer.setDisplayName("Слой заливки узором");

    patternFillLayer.setOpacity((byte)50);

    psdImage.addLayer(patternFillLayer);

    // Сохранить измененную копию загруженного файла PSD по указ