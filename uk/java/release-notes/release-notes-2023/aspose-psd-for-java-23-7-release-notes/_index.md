---
title: Примітки до випуску Aspose.PSD для Java 23.7
type: документація
weight: 40
url: /uk/java/aspose-psd-for-java-23-7-release-notes/
---

{{% alert color="primary" %}} Ця сторінка містить примітки до [Aspose.PSD для Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **Ключ**     | **Опис**                                                                                                                                      | **Категорія** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | Додано можливість експорту кожного шару файлу PSD до файлу Animated Gif                                       | Функція |
| PSDJAVA-503 | Призначення властивості Fill для шару форми від ресурсу vscg                                                       | Функція |
| PSDJAVA-504 | Додано нові типи warp (arc & arch)                                                                           | Функція |
| PSDJAVA-505 | Змінено програму, яка зберігає файл PSD на Aspose.PSD у разі встановлення властивості UpdateMetadata на true       | Функція |
| PSDJAVA-510 | Збільшено обчислювальну область зображення warp                                                              | Функція |
| PSDJAVA-511 | Корекція шару чорного та білого обробки оброблює напівпрозорості неправильно                                         | Помилка     |
| PSDJAVA-512 | SmartObject ReplaceContents (при активних параметрах AllowWarpRepaint) падає після 2 хвилин обчислення | Помилка     |
| PSDJAVA-513 | Додано можливість отримати реальне положення Ліворуч та Зверху для шару групи                                                 | Помилка     |
| PSDJAVA-514 | Зміна розміру шару працює неправильно, коли файл psd містить VogkResource зі структурами в точках                     | Помилка     |
| PSDJAVA-515 | TextBound не працює так, як очікувалося                                                                         | Помилка     |
| PSDJAVA-516 | Додавання шару, створеного конструктором за замовчуванням до зображення PSD не додає до нього ресурси за замовчуванням            | Помилка     |
| PSDJAVA-517 | Timeline.LoopesCount ігнорується при експорті в анімований GIF                                               | Помилка     |

## **Зміни у громадському API**
# **Додані API:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **Вилучені API:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **Приклади використання:**

**PSDJAVA-502. Додано можливість експорту кожного шару файлу PSD до файлу Animated Gif**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // Створення кадрів для кожного шару.
        int framesCount = psdImage.getLayers().length;
        Timeline timeline = psdImage.getTimeline();

        Frame[] frames = new Frame[framesCount];
        for (int i = 0; i < framesCount; i++) {
            frames[i] = new Frame();
            LayerState[] layerStates = new LayerState[framesCount];

            for (int j = 0; j < framesCount; j++) {
                layerStates[j] = new LayerState();
                layerStates[j].setEnabled(i == j);
            }

            frames[i].setLayerStates(layerStates);
        }

        timeline.setFrames(frames);

        // Оновлення поточних станів
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

**PSDJAVA-503. Призначення властивості Fill для шару форми від ресурсу vscg**

{{< highlight java >}}
        // Приклад заповнення коліром
        public static void main(String[] args) {
            String srcFile = "src/main/resources/ShapeInternalSolid.psd";
            String outFile = "src/main/resources/ShapeInternalSolid.psd.out.psd";

            PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
            psdLoadOptions.setLoadEffectsResource(true);

            try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
                 ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
                  ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();
                 fillSettings.setColor(Color.getRed());

                 shapeLayer.update();

                 image.save(outFile);
            }

            // Перевірка збережених змін
            try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();

            assertAreEqual(Color.getRed(), fillSettings.getColor());

            image.save(outFile);
        }

        static void assertAreEqual(Object expected, Object actual, String message) {
            if (!expected.equals(actual)) {
                throw new IllegalArgumentException(message);
            }
        }

        static void assertAreEqual(Object expected, Object actual) {
            assertAreEqual(expected, actual, "Об'єкти не рівні.");
        }
		
		// Приклад градієнтного заливання:

	public static void main(String[] args) {
    String srcFile = "src/main/resources/ShapeInternalGradient.psd";
    String outFile = "src/main/resources/ShapeInternalGradient.psd.out.psd";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
        GradientFillSettings fillSettings = (GradientFillSettings) shapeLayer.getFill();
        fillSettings.setDither(true);
        fillSettings.setReverse(true);
        fillSettings.setAlignWithLayer(false);
        fillSettings.setAngle(20);
        fillSettings.setScale(50);
        fillSettings.getColorPoints()[0].setLocation(100);
        fillSettings.getColorPoints()[1].setLocation(4000);
        fillSettings.getTransparencyPoints()[0].setLocation(200);
        fillSettings.getTransparencyPoints()[1].setLocation(3800);
        fillSettings.getTransparencyPoints()[0].setOpacity(90);
        fillSettings.getTransparencyPoints()[1].setOpacity(10);

        shapeLayer.update();

        image.save(outFile);
    }

    // Перевірка збережених змін
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
        GradientFillSettings fillSettings = (GradientFillSettings) shapeLayer.getFill();

        assertAreEqual(true, fillSettings.getDither());
        assertAreEqual(true, fillSettings.getReverse());
        assertAreEqual(false, fillSettings.getAlignWithLayer());
        assertAreEqual((double) 20, fillSettings.getAngle());
        assertAreEqual(50, fillSettings.getScale());
        assertAreEqual(100, fillSettings.getColorPoints()[0].getLocation());
        assertAreEqual(4000, fillSettings.getColorPoints()[1].getLocation());
        assertAreEqual(200, fillSettings.getTransparencyPoints()[0].getLocation());
        assertAreEqual(3800, fillSettings.getTransparencyPoints()[1].getLocation());
        assertAreEqual((double) 90, fillSettings.getTransparencyPoints()[0].getOpacity());
        assertAreEqual((double) 10, fillSettings.getTransparencyPoints()[1].getOpacity());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Об'єкти не рівні.");
}

{{< /highlight >}}

**PSDJAVA-504. Додано нові типи warp (arc & arch)**

{{< highlight java >}}
    String sourceArcFile = "src/main/resources/arc_warp.psd";
    String outputArcFile = "src/main/resources/arc_export.png";

    String sourceArchFile = "