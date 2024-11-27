---
title: Aspose.PSD за Java 20.4 - Бележки за изданието
type: docs
weight: 30
url: /bg/java/aspose-psd-za-java-20-4-release-notes/
---

{{% alert color="primary" %}} Тази страница съдържа бележки за изданието на [Aspose.PSD за Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) {{% /alert %}} 

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDJAVA-156|Поддръжка на ресурса 'Vector Origination Data'|Функционалност|
|PSDJAVA-171|Поддръжка на lclrResource (настройки на цветовете на листа)|Функционалност|
|PSDJAVA-157|Подръжка на свойствата от LengthRecord данните. (Операции с пътеки (логически операции), индекс на формата в слоя, брой на записите на бецеловия сгъв)|Функционалност|
|PSDJAVA-158|Поддръжка на Image Section Resource #1010 Заден фон|Функционалност|
|PSDJAVA-161|Добавяне на слоеве за попълване по време на изпълнение|Функционалност|
|PSDJAVA-168|Поддръжка на Image Section Resource #1009 Информация за граница|Функционалност|
|PSDJAVA-169|Поддръжка на слоевете в AI форматни файлове|Функционалност|
|PSDJAVA-163|Поддръжка за четене и редактиране на Gradient Overlay Layer Effect|Функционалност|
|PSDJAVA-164|Изчертаване на Gradient Overlay Layer Effect|Функционалност|
|PSDJAVA-149|Грешка в Aspose.PSD за Java, когато се извлича свойството textData.items на текстовия слой|Проблем|
|PSDJAVA-166|Оправяне на запис на PSD изображение с Градиращ цветен режим и 16 бита на канал към градиращ PSD формат|Проблем|
|PSDJAVA-167|Оправяне на запис на PSD изображение с Градиращ цветен режим и 16 бита на канал към PNG формат|Проблем|
|PSDJAVA-159|Промените в свойството GradientOverlayEffect.BlendMode не се показват в Photoshop|Проблем|
# Промени в публичния API
## Добавени API:
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
## Премахнати API:
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)
# Примери за използване:

**PSDJAVA-156. Поддръжка на ресурса 'Vector Origination Data'**

{{< highlight java >}}

 /*

Пример за четене и промяна на ресурс за начало на векторни данни.

*/

// Запазва методите в локалния обхват за удобство

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

            throw new Exception("VogkResource not found.");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// Зарежда PSD файл, съдържащ предварително зададен VOGK ресурс

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Намира първият VogkResource в ресурсите на предварително зададения слой

    VogkResource vogkResource = $.findFirstVogkResource( psdImage.getLayers()[1].getResources());

    // Проверява предварително зададените свойства на ресурса

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("VogkResource was misread.");

    }

    // Променя някои свойства на VogkResource

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // Запазва модифицирана копие на заредения PSD файл на пътеката

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. Поддръжка на lclrResource (настройки за цветовете на листа)**

{{< highlight java >}}

 /*

Пример за използване на Layer Sheet Color, за визуално означаване на слоевете. Например може

да актуализирате някои слоеве в PSD и след това да означите с цвят слоя, който искате да привлечете

вниманието.

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

                // Ресурсът lcrl винаги се представя в списъка с ресурси на файла PSD.

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("Sheet Color has been read wrong");

                }

                // Обърнете цветовете на платно. Задаване на цветния маркер на слоя.

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// Във файла цветовете на слоевете се записват в този ред

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

// Зарежда PSD файл, съдържащ предварително дефиниран LclrResource

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

// Зарежда само записания PSD файл

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // Обръща цветовете

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. Поддръжка на свойствата от LengthRecord данните. (Операции с пътеки (логически операции), индекс на формата в слоя, брой на записите на бецеловия сгъв)**

{{< highlight java >}}

 /*

Пример за изменение на пътните операции при работа с формите. Програмата чете

предефинирани записи за векторни пътеки (LengthRecord) и променя техните пътеви операции, след което записва

модифицирана копие на документа като нов PSD файл.

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// Зарежда PSD файл, съдържащ предефиниран vsms ресурс

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Намира първия VsmsResource в ресурсите на предефинирания слой

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

    // Променя начина, по който формите се комбинират

    lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);

    lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);

    lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);

    // Запазва модифицирана копие на заредения PSD файл на пътеката

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-158. Поддръжка на Image Section Resource #1010 Заден фон**

{{< highlight java >}}

 /*

Пример за четене и промяна на ресурс за фонов цвят.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// Зарежда PSD файл, съдържащ предефиниран ресурс за фонов цвят

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

        throw new Exception("BackgroundColorResource not found");

    }

    // Обновява цвета на ресура за фонов цвят

    backgroundColorResource.setColor(Color.getDarkRed());

    // Запазва модифицирано копие на заредения PSD файл на пътеката

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-161. Добавяне на слоеве за попълване по време на изпълнение**

{{< highlight java >}}

 /*

Пример за добавяне на слоеве за попълване от различни типове към документ в Photoshop.

*/

String outPsdFilePath = "output.psd";

// Създава документ в Photoshop с празно платно

PsdImage psdImage = new PsdImage(100,