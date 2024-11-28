---
title: Aspose.PSD для Java 23.4 - Примітки до випуску
type: docs
weight: 40
url: /uk/java/aspose-psd-for-java-23-4-release-notes/
---

{{% alert color="primary" %}} Ця сторінка містить примітки до випуску для [Aspose.PSD для Java 23.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.4/) {{% /alert %}}

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDJAVA-446|Перенесення пропущеної функціональності з Aspose.PSD для .Net до Aspose.PSD для Java|Покращення|
|PSDJAVA-441|Створення класу RawColor для використання його у громадському API в PSD API замість застарілої структури Color|Покращення|
|PSDJAVA-418|Інтеграція сучасної ліцензії Aspose для Aspose.PSD|Покращення|
|PSDJAVA-445|Форматування зміщується під час редагування у програмі Photoshop|Помилка|
|PSDJAVA-443|Редагування тексту за допомогою частин тексту не зберігає правильний результат|Помилка|
|PSDJAVA-444|Початок і кінець стилів або абзаців виявляються в неправильному місці під час редагування текстового шару за допомогою ITextPortion|Помилка|

# **Зміни у громадському API**
# **Додані API:**
- M:com.aspose.psd.FontSettings.getFontReplacements(java.lang.String)
- M:com.aspose.psd.FontSettings.getReplacementFont(java.lang.String)
- ...
- M:com.aspose.psd.fileformats.psd.layers.LayerHashCalculator.getContentHash

# **Вилучені API:**
- M:com.aspose.psd.FontSettings.addFontsFolder(java.lang.String)
- M:com.aspose.psd.FontSettings.removeFontsFolder(java.lang.String)
- ...
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResource.setWidth(short)

# **Приклади використання:**

**PSDJAVA-446. Перенесення пропущеної функціональності з Aspose.PSD для .Net до Aspose.PSD для Java**

Будь ласка, перевірте <a href="https://reference.aspose.com/psd/java/">API Reference для Aspose.PSD для Java </a>. Не всі приклади використання нового API були скопійовані та протестовані.

{{< highlight java >}}        
        // Приклади будуть надані пізніше.
{{< /highlight >}}

**PSDJAVA-441. Створення класу RawColor для використання його в громадському API в PSD API замість застарілої структури Color**

{{< highlight java >}}
		PixelDataFormat rgb32Bpp = PixelDataFormat.getRgb32Bpp();
		RawColor color = new RawColor(rgb32Bpp);
		Color oldColor = Color.fromArgb(5, 1, 2, 3);

		int argbValue = oldColor.toArgb();
		color.setAsInt(argbValue);

		Assertions.assertEquals("ARGB", color.getColorModeName());
		Assertions.assertEquals(32, color.getBitDepth());
		Assertions.assertEquals("A Alpha", color.getComponents()[0].getFullName());
		Assertions.assertEquals(5, (int)color.getComponents()[0].getValue());
		...
{{< /highlight >}}

**PSDJAVA-445. Форматування зміщується під час редагування у програмі Photoshop**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-443. Редагування тексту за допомогою частин тексту не зберігає правильний результат**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-444. Початок і кінець стилів або абзаців виявляються в неправильному місці під час редагування текстового шару за допомогою ITextPortion**

{{< highlight java >}}
...
{{< /highlight >}}**PSDJAVA-444. Початок і кінець стилів або абзаців виявляються в неправильному місці під час редагування текстового шару за допомогою ITextPortion**

{{< highlight java >}}
public static void main(String[] args) {
    String sourceFilePSDEmail = Directory.getCurrentDirectory() + "/inputv2.psd";
    String outputFile = Directory.getCurrentDirectory() + "/export.psd";

    PsdImage imageTestEmail = (PsdImage) Image.load(sourceFilePSDEmail);

    Layer[] layers = imageTestEmail.getLayers();

    for (Layer layerItem : layers) {
        boolean isTextLayer = layerItem instanceof TextLayer;

        if (isTextLayer) {
            var layerTLToUpdateText = (TextLayer) layerItem;

            //Buscar lsak text
            if (layerTLToUpdateText.getText().contains("lsak")) {

                var textDataTL = layerTLToUpdateText.getTextData();

                if (textDataTL.getText().contains("lsak")) {

                    //Step: Replace text
                    replaceLsakFourthMethod(textDataTL);

                    System.out.println("Replaced text " + textDataTL.getText());

                    //Step: Format text
                    formatLsakFourthMethod(textDataTL);

                    System.out.println("Formated text " + textDataTL.getText());

                    //Step: Center textlayer
                    if (layerTLToUpdateText.getDisplayName().equals("cc")
                            || layerTLToUpdateText.getDisplayName().equals("tl")
                            || layerTLToUpdateText.getDisplayName().equals("cl")) {

                        //old Values
                        var boundBoxOld = layerTLToUpdateText.getTextBoundBox();

                        var wordSizeOld = layerTLToUpdateText.getSize();

                        var OldY = layerTLToUpdateText.getTop();

                        textDataTL.updateLayerData();

                        // new values
                        var wordSize = layerTLToUpdateText.getSize();

                        var boundBox = layerTLToUpdateText.getTextBoundBox();

                        var newSize = new Size((int) Math.ceil(boundBoxOld.getWidth()), wordSize.getHeight());

                        var beforePoint = centerInRectangle(wordSize, new RectangleF(layerTLToUpdateText.getLeft(),
                                layerTLToUpdateText.getTop(), layerTLToUpdateText.getWidth(), boundBoxOld.getHeight()));

                        layerTLToUpdateText.setTextBoundBox(
                                new RectangleF(new PointF(0, beforePoint.getY() - OldY), Size.to_SizeF(newSize)));

                        var newPoint = centerInRectangle(wordSize, new RectangleF(layerTLToUpdateText.getLeft(),
                                layerTLToUpdateText.getTop(), layerTLToUpdateText.getWidth(), boundBoxOld.getHeight()));

                        layerTLToUpdateText.setLeft((int) newPoint.getX());

                        layerTLToUpdateText.setTop((int) newPoint.getY());

                        textDataTL.updateLayerData();

                        System.out.println("Center text");
                    }
                }
            }
        }
    }

    imageTestEmail.save(outputFile);
}

static String replaceText(String lsak) {
    StringBuilder sb = new StringBuilder(lsak);
    sb = new StringBuilder(sb.toString().replace("#lsak_011#", "[1] Terms and exclusions apply. Game catalog varies over time, by region, and by device. Requires Windows 11 (with updates); excludes S mode and ARM devices. See <font:Segoe UI Semibold>xbox.com/pcgamepass</font> and <font:Segoe UI Semibold>https://www.ea.com/ea-play/terms</font> and <font:Segoe UI Semibold>https://www.ea.com/ea-play</font> for details. <br/>[2] See https://www.ea.com/ea-play/terms and https://www.ea.com/ea-play for details. The EA logo and Battlefield are trademarks of Electronic Arts Inc. © FIFA is a copyright and/or trademark of FIFA. All rights reserved. Manufactured under license by Electronic Arts Inc. STAR WARS © & TM 2019 Lucasfilm Ltd. All rights reserved. "));
    ...

{{< /highlight >}}