---
title: تحديثات إصدار Aspose.PSD لـ Java 24.8
type: docs
weight: 40
url: /ar/java/aspose-psd-for-java-24-8-release-notes/
---

{{% alert color="primary" %}} تحتوي هذه الصفحة على تحديثات الإصدار لـ [Aspose.PSD لـ Java 24.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.8/) {{% /alert %}}

| **Key**     | **Summary**                                                                                        | **Category** |
|:------------|:---------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-642 | [نسق AI] إضافة التعامل لمجموعات الأجسام XObject                                                    | تحسين      |
| PSDJAVA-645 | تحسين قدرات تحويل المنحنى عن طريق إضافة إعدادات الانحناء لـ TextLayer و SmartObjectLayer      | ميزة        |
| PSDJAVA-646 | [نسق AI] الحسابات لطبقات في عمليات التيارات القابلة للتنفيذ                                      | ميزة        |
| PSDJAVA-647 | نتيجة العرض لملف AI مختلفة جدًا مقارنة بنتائج Illustrator                                         | خلل         |
| PSDJAVA-648 | إعادة ربط العنصر الذكي لا ينطبق على جميع العناصر الذكية في ملف PSD                                | خلل         |

## **تغييرات واجهة برمجة التطبيقات العامة**
# **تمت إضافة واجهات برمجة تطبيقات:**

- M: com.aspose.psd.fileformats.psd.layers.TextLayer.getWarpSettings
- M: com.aspose.psd.fileformats.psd.layers.TextLayer.setWarpSettings(com.aspose.psd.fileformats.psd.layers.warp.WarpSettings)
- M: com.aspose.psd.fileformats.psd.layers.smartobjects.SmartObjectLayer.getWarpSettings
- M: com.aspose.psd.fileformats.psd.layers.smartobjects.SmartObjectLayer.setWarpSettings(com.aspose.psd.fileformats.psd.layers.warp.WarpSettings)
- T: com.aspose.psd.fileformats.psd.layers.warp.WarpSettings 
- M: com.aspose.psd.fileformats.psd.layers.warp.WarpSettings.# ctor(com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure[],com.aspose.psd.Rectangle)
- M: com.aspose.psd.fileformats.psd.layers.warp.WarpSettings.# ctor(com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedResource)
- M: com.aspose.psd.fileformats.psd.layers.warp.WarpSettings.getBounds
- M: com.aspose.psd.fileformats.psd.layers.warp.WarpSettings.getMeshPoints
- M: com.aspose.psd.fileformats.psd.layers.warp.WarpSettings.getRotate
- M: com.aspose.psd.fileformats.psd.layers.warp.WarpSettings.getStyle
- M: com.aspose.psd.fileformats.psd.layers.warp.WarpSettings.getValue
- M: com.aspose.psd.fileformats.psd.layers.warp.WarpSettings.setBounds(com.aspose.psd.Rectangle)
- M: com.aspose.psd.fileformats.psd.layers.warp.WarpSettings.setMeshPoints(com.aspose.psd.Point[])
- M: com.aspose.psd.fileformats.psd.layers.warp.WarpSettings.setRotate(int)
- M: com.aspose.psd.fileformats.psd.layers.warp.WarpSettings.setStyle(int)
- M: com.aspose.psd.fileformats.psd.layers.warp.WarpSettings.setValue(double)
- T: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.Inflate
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.Arc
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.Wave
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.Squeeze
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.Flag
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.Twist
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.Arch
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.ArcLower
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.Rise
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.Custom
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.ArcUpper
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.Bulge
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.Fish
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpStyles.None
- T: com.aspose.psd.fileformats.psd.layers.warp.WarpRotates
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpRotates.Horizontal
- F: com.aspose.psd.fileformats.psd.layers.warp.WarpRotates.Vertical

# **تمت إزالة واجهات برمجة التطبيقات:**

- لا شيء

## **أمثلة على الاستخدام:**

**PSDJAVA-645. تحسين قدرات تحويل المنحنى عن طريق إضافة إعدادات الانحناء لـ TextLayer و SmartObjectLayer**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/smart_without_warp.psd";

        var opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);
        opt.setAllowWarpRepaint(true);

        String[] outputImageFile = new String[4];
        String[] outputPsdFile = new String[4];

        for (int caseIndex = 0; caseIndex < outputImageFile.length; caseIndex++) {
            outputImageFile[caseIndex] = "src/main/resources/export_" + caseIndex + ".png";
            outputPsdFile[caseIndex] = "src/main/resources/export_" + caseIndex + ".psd";

            try (PsdImage img = (PsdImage) Image.load(sourceFile, opt)) {
                for (Layer layer : img.getLayers()) {
                    if (layer instanceof SmartObjectLayer) {
                        var smartLayer = (SmartObjectLayer) layer;
                        smartLayer.setWarpSettings(getWarpSettingsByIndex(smartLayer.getWarpSettings(), caseIndex));
                    }

                    if (layer instanceof TextLayer) {
                        var textLayer = (TextLayer) layer;

                        if (caseIndex != 3) {
                            textLayer.setWarpSettings(getWarpSettingsByIndex(textLayer.getWarpSettings(), caseIndex));
                        }
                    }
                }

                img.save(outputPsdFile[caseIndex], new PsdOptions());
            }

            try (PsdImage img1 = (PsdImage) Image.load(outputPsdFile[caseIndex], opt)) {
                var pngOptions = new PngOptions();
                pngOptions.setCompressionLevel(9);
                pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

                img1.save(outputImageFile[caseIndex], pngOptions);
            }
        }
    }

    static WarpSettings getWarpSettingsByIndex(WarpSettings warpParams, int caseIndex) {
        switch (caseIndex) {
            case 0:
                warpParams.setStyle(WarpStyles.Rise);
                warpParams.setRotate(WarpRotates.Horizontal);
                warpParams.setValue(20);
                break;
            case 1:
                warpParams.setStyle(WarpStyles.Rise);
                warpParams.setRotate(WarpRotates.Vertical);
                warpParams.setValue(10);
                break;
            case 2:
                warpParams.setStyle(WarpStyles.Flag);
                warpParams.setRotate(WarpRotates.Horizontal);
                warpParams.setValue(30);
                break;
            case 3:
                warpParams.setStyle(WarpStyles.Custom);
                warpParams.getMeshPoints()[2].setY(warpParams.getMeshPoints()[2].getY() + 70);
                break;
        }

        return warpParams;
    }

{{< /highlight >}}

**PSDJAVA-646. [نسق AI] الحسابات لطبقات في عمليات التيارات القابلة للتنفيذ**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Layers-NoPen.ai";
    String outputFile = "src/main/resources/Layers-NoPen.output.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-647. نتيجة العرض لملف AI مختلفة جدًا مقارنة بنتائج Illustrator**

{{< highlight java >}}

    String sourceFile = "src/main/resources/4.ai";
    String outputFilePath = "src/main/resources/4.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFilePath, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-648. إعادة ربط العنصر الذكي لا ينطبق على جميع العناصر الذكية في ملف PSD**

{{< highlight java >}}

    String[] files = {"simple_test", "w22"};
    String changeFile = "src/main/resources/image(19).png";

    String[] sourceFile = new String[files.length];
    String[] outputFiles = new String[files.length];

    for (int i = 0; i < files.length; i++) {
        sourceFile[i] = "src/main/resources/" + files[i] + ".psd";
        outputFiles[i] = "src/main/resources/" + files[i] + "_output.psd";

        try (var image = (PsdImage) Image.load(sourceFile[i])) {
            for (Layer layer : image.getLayers()) {
                if (layer instanceof SmartObjectLayer) {
                    SmartObjectLayer smart = (SmartObjectLayer) layer;

                    // For the second smart layer here was error
                    smart.replaceContents(changeFile);
                }
            }

            image.save(outputFiles[i]);
        }
    }

{{< /highlight >}}