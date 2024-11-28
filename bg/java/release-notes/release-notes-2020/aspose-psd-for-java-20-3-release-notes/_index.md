---
title: Aspose.PSD за Java 20.3 - Бележки за Изданието
type: docs
weight: 10
url: /bg/java/aspose-psd-za-java-20-3-belezhki-za-izdanieto/
---

{{% alert color="primary" %}} Тази страница съдържа бележки за изданието на [Aspose.PSD за Java 20.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.2/) {{% /alert %}} 

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDJAVA-133|Преобразуване на файлове от Adobe Illustrator в PDF|Функционалност|
|PSDJAVA-134|Добавяне на възможност за визуализиране на различни стилове в един текстов слой|Функционалност|
|PSDJAVA-135|Поддръжка на Слой за Регулиране на Черно и Бяло|Функционалност|
|PSDJAVA-137|Добавяне на поддръжка за извличане на AI формат (Версия 8) към други формати|Функционалност|
|PSDJAVA-138|Поддръжка на обработка на режим на смесване Пропускане (Използван за Група на Слоеве Само)|Функционалност|
|PSDJAVA-136|Изключение: Грешка при зареждане на изображение с празно Unicode Alpha Names Resource|Проблем|
|PSDJAVA-139|Некоректен изход след промяна на видимостта на Група на Слоеве|Проблем|
|PSDJAVA-140|Изключение при зареждане на PSD изображение: Секция за Цвят (DropShadow Resource) трябва да съдържа 3 цветови компонента за RGB или 4 цветови компонента за CMYK|Проблем|
|PSDJAVA-141|Изключение при опит за рисуване върху новосъздаден слой, ако се използва опростената версия на Конструктора|Проблем|
# **Променени Публични API**
# **Добавени API:**
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
## **Премахнати API:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.setVisibleInGroup(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(int)
# **Примери за Използване:**
**PSDJAVA-133. Преобразуване на файлове от Adobe Illustrator в PDF**

{{< highlight java >}}

 String inFile = "rect2_color.ai";

String outFile = "rect2_color.ai_output.pdf";

AiImage aiImage = (AiImage)Image.load(inFile);

try

{

    aiImage.save(outFile, new PdfOptions());

}

finally

{

    aiImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-134. Добавяне на възможност за визуализиране на различни стилове в един текстов слой**

{{< highlight java >}}

 String inFilePath = "text212.psd";

String outFilePath = "Output_text212.psd";

PsdImage image = (PsdImage)Image.load(inFilePath);

try

{

    TextLayer textLayer = (TextLayer)image.getLayers()[1];

    IText textData = textLayer.getTextData();

    ITextStyle defaultStyle = textData.producePortion().getStyle();

    ITextParagraph defaultParagraph = textData.producePortion().getParagraph();

    defaultStyle.setFillColor(Color.getDimGray());

    defaultStyle.setFontSize(51);

    textData.getItems()[1].getStyle().setStrikethrough(true);

    ITextPortion[] newPortions = textData.producePortions(new String[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Lowercasetext" }, defaultStyle, defaultParagraph);

    newPortions[0].getStyle().setUnderline(true); // edit text style "E=mc"

    newPortions[1].getStyle().setFontBaseline(FontBaseline.Superscript); // edit text style "2\r"

    newPortions[2].getStyle().setFauxBold(true); // edit text style "Bold"

    newPortions[3].getStyle().setFauxItalic(true); // edit text style "Italic\r"

    newPortions[3].getStyle().setBaselineShift(-25); // edit text style "Italic\r"

    newPortions[4].getStyle().setFontCaps(FontCaps.SmallCaps); // edit text style "Lowercasetext"

    for (ITextPortion newPortion : newPortions)

    {

        textData.addPortion(newPortion);

    }

    textData.updateLayerData();

    image.save(outFilePath);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-135. Поддръжка на Слой за Регулиране на Черно и Бяло**

{{< highlight java >}}

 // Пример за поддръжка на добавяне на слой за регулиране на черно и бяло по време на изпълнение.

String inFileName = "Stripes.psd";

String outFileName = "Output" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    BlackWhiteAdjustmentLayer newLayer = image.addBlackWhiteAdjustmentLayer();

    newLayer.setName("BlackWhiteAdjustmentLayer");

    newLayer.setReds(22);

    newLayer.setYellows(92);

    newLayer.setGreens(70);

    newLayer.setCyans(79);

    newLayer.setBlues(7);

    newLayer.setMagentas(28);

    image.save(outFileName, new PsdOptions());

}

finally

{

    image.dispose();

}

// Пример за поддръжка на слой за регулиране на черно и бяло.

inFileName = "BlackWhiteAdjustmentLayerStripesMask.psd";

outFileName = "Output" + inFileName;

PsdImage image1 = (PsdImage)Image.load(inFileName);

try

{

    BlackWhiteAdjustmentLayer blwhLayer = (BlackWhiteAdjustmentLayer)image1.getLayers()[1];

    blwhLayer.setReds(15);

    blwhLayer.setYellows(25);

    blwhLayer.setGreens(35);

    blwhLayer.setCyans(10);

    blwhLayer.setBlues(50);

    blwhLayer.setMagentas(105);

    blwhLayer.setUseTint(true);

    blwhLayer.setBwPresetKind(4);

    blwhLayer.setBlackAndWhitePresetFileName("bwPresetFileName");

    blwhLayer.setTintColorRed(60);

    blwhLayer.setTintColorGreen(80);

    blwhLayer.setTintColorBlue(200);

    image1.save(outFileName, new PsdOptions());

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-137. Добавяне на поддръжка за извличане на AI формат (Версия 8) към други формати**

{{< highlight java >}}

 // Пример за извличане на AI файл към PSD и PNG формат

String inFileName = "form_8.ai";

String outFileNamePrefix = "form_8_export";

AiImage image = (AiImage)Image.load(inFileName);

try

{

    image.save(outFileNamePrefix + ".psd", new PsdOptions());

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    image.save(outFileNamePrefix + ".png", pngOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-138. Поддръжка на обработка на режим на смесване Пропускане (Използван за Група на Слоеве Само).**

{{< highlight java >}}

 class LocalScope

{

    void assertIsTrue(boolean condition, String message)

    {

        if (!condition)

        {

            throw new FormatException(message);

        }

    }

}

LocalScope localScope = new LocalScope();

String inFileName = "Apple.psd";

String outFileName = "Output" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    localScope.assertIsTrue(image.getLayers().length >= 23, "There is not 23rd layer.");

    LayerGroup layer = (LayerGroup)image.getLayers()[23];

    localScope.assertIsTrue(layer != null, "The 23rd layer is not a layer group.");

    localScope.assertIsTrue(layer.getName().equals("AdjustmentGroup"), "The 23rd layer name is not 'AdjustmentGroup'.");

    localScope.assertIsTrue(layer.getBlendModeKey() == BlendMode.PassThrough, "AdjustmentGroup layer should have 'pass through' blend mode.");

    image.save(outFileName, new PsdOptions());

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("OutputApple.png", pngOptions);

    layer.setBlendModeKey(BlendMode.Normal);

    image.save("Normal" + outFileName, new PsdOptions());

    PngOptions pngOptions1 = new PngOptions();

    pngOptions1.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("NormalOutputApple.png", pngOptions1);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-136. Изключение: Грешка при зареждане на изображение с празно Unicode Alpha Names Resource**

{{< highlight java >}}

 String inFilePath = "apple.psd";

PsdImage psdImage = null;

try

{

    // Тук не трябва да получим изключения

    psdImage = (PsdImage)Image.load(inFilePath);

}

finally

{

    if (psdImage != null) psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-139. Некоректен изход след промяна на видимостта на Група на Слоеве**

{{< highlight java >}}

 String inFileName = "input.psd";

String outFileName = "output.psd";

// Извършете промени в имената на слоевете и го запазете

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    for (int i = 0; i < image.getLayers().length; i++)

    {

        Layer layer = image.getLayers()[i];

        // Изключете всичко вътре в група

        if (layer instanceof LayerGroup)

        {

            layer.setVisible(false);

        }

    }

    image.save(outFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-140. Изключение при зареждане на PSD изображение: Секция за Цвят (DropShadow Resource) трябва да съдържа 3 цветови компонента за RGB или 4 цветови компонента за CMYK**

{{< highlight java >}}

 String inFilePath = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

PsdImage image = null;

try

{

    image = (PsdImage)PsdImage.load(inFilePath);

}

finally

{

    if (image != null) image.dispose();

}       

{{< /highlight >}}

**PSDJAVA-141. Изключение при опит за рисуване върху новосъздаден слой, ако се използва опростената версия на Конструктора**

{{< highlight java >}}

 String outputFile = "output.psd";

int width = 100;

int height = 100;

PsdImage image = new PsdImage(width, height);

try

{

    Layer layer = new Layer();

    layer.setBottom(height);

    layer.setRight(width);

    image.addLayer(layer);

    Graphics graphic = new Graphics(layer);

    graphic.clear(Color.getYellow());

    // Нарисува четириъгълник с Перо инструмент

    graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

    // Нарисува друг четириъгълник с Пълно Четка в Син цвят

    graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));

    image.save(outputFile);

}

finally

{

    image.dispose();

}

{{< /highlight >}}