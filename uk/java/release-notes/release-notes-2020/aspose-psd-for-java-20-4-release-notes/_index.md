---
title: Aspose.PSD для Java 20.4 - Примітки до випуску
type: docs
weight: 30
url: /uk/java/aspose-psd-for-java-20-4-release-notes/
---

{{% alert color="primary" %}} Ця сторінка містить примітки до випуску для [Aspose.PSD для Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) {{% /alert %}} 

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDJAVA-156|Підтримка ресурсу 'Дані вихідного вектора'|Функція|
|PSDJAVA-171|Підтримка lclrResource (налаштування кольору аркуша)|Функція|
|PSDJAVA-157|Підтримка властивостей з даних LengthRecord. (Операції з шляхами (логічні операції), індекс форми в шарі, кількість записів бе́зьє наспівці)|Функція|
|PSDJAVA-158|Підтримка фонового кольору ресурсу Image Section #1010|Функція|
|PSDJAVA-161|Додавання заповнювачів шарів під час виконання|Функція|
|PSDJAVA-168|Підтримка інформації про рамку ресурсу Image Section #1009|Функція|
|PSDJAVA-169|Підтримка шарів у файлах формату AI|Функція|
|PSDJAVA-163|Підтримка читання та редагування ефекту "градієнтного наложення" на шарі|Функція|
|PSDJAVA-164|Відтворення ефекту "градієнтного наложення" на шарі|Функція|
|PSDJAVA-149|Помилка Aspose.PSD для Java при отриманні властивості textData.items текстового шару|Помилка|
|PSDJAVA-166|Виправлення збереження зображення PSD з колірним режимом відтінків сірого та 16 біт на канал у форматі PSD відтінків сірого|Помилка|
|PSDJAVA-167|Виправлення збереження зображення PSD з колірним режимом відтінків сірого та 16 біт на канал у форматі PNG|Помилка|
|PSDJAVA-159|Зміни властивості BlendMode для GradientOverlayEffect не відображаються в Photoshop|Помилка|

# **Зміни в загальнодоступному API**
# **Додані API:**
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
## **Вилучені API:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)

# **Приклади використання:**

**PSDJAVA-156. Підтримка ресурсу 'Дані вихідного вектора'**

{{< highlight java >}}

 /*

Приклад читання і зміни ресурсу вихідного вектора.

*/

// На прикладі зберігання методів у місцевому режимі для простоти

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

            throw new Exception("Ресурс VogkResource не знайдено.");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// Завантаження файлу PSD, який містить попередньо визначений ресурс VOGK

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Знаходимо перший VogkResource серед ресурсів попередньо визначеного шару

    VogkResource vogkResource = $.findFirstVogkResource(

            psdImage.getLayers()[1].getResources());

    // Перевірка попередньо визначених властивостей ресурсу

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("VogkResource був неправильно прочитаний.");

    }

    // Модифікація деяких властивостей ресурсу Vogk

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // Збереження модифікованої копії завантаженого файлу PSD за шляхом

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. Підтримка lclrResource(Sheet color setting)**

{{< highlight java >}}

 /*

Приклад використання кольору аркуша шару для візуального виділення шарів. Наприклад, ви можете

оновлювати деякі шари в PSD, а потім виділяти кольором той шар, на який ви хочете звернути

увагу.

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

                // Ресурс lcrl завжди присутній в  списку ресурсів psd файлу.

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("Колір аркуша було прочитано неправильно");

                }

                // Обернення кольору аркуша шару. Встановлення виділення кольору шару.

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// У файлі кольори шарів відзначені в цьому порядку

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

// Завантаження PSD файлу, що містить попередньо визначений LclrResource

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

// Завантаження щойно збереженого PSD файлу

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // Обернення кольорів

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. Підтримка властивостей з даних LengthRecord. (Операції зі шляхами (логічні операції), індекс форми в шарі, кількість записів бе́зьє наспівці)**

{{< highlight java >}}

 /*

Приклад зміни операцій шляхів при роботі з фігурами. Програма читає попередньовизначені записи векторного шляху (LengthRecord) та змінює їх операції шляхів, потім зберігає модифіковану копію документа як новий файл PSD.

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// Завантаження фаілу PSD, що містить попередньовизначений ресурс vsms

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Знаходимо перший VsmsResource серед ресурсів попередньо визначеного шару

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

    // Зміна способу комбінування форм

    lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);

    lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);

    lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);

    // Збереження модифікованої копії завантаженого файлу PSD за шляхом

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-158. Підтримка ресурсу Image Section #1010 Фоновий колір**

{{< highlight java >}}

 /*

Приклад читання та модифікації ресурсу фонового кольору.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// Завантаження PSD файла, що містить попередньо визначений ресурс фонового кольору

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

