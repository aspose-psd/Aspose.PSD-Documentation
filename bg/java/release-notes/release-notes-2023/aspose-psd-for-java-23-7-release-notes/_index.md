---
title: Aspose.PSD за Java 23.7 - Бележки за изданието
type: docs
weight: 40
url: /bg/java/aspose-psd-za-java-23-7-belejki-za-izdanieto/
---

{{% alert color="primary" %}} Тази страница съдържа бележки за изданието на [Aspose.PSD за Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **Ключ**     | **Резюме**                                                                                                                                      | **Категория** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | Добавяне на възможност за експортиране на всяко ниво на PSD файл към файл с анимиран GIF                                        | Функция |
| PSDJAVA-503 | Присвояване на свойство за попълване на форма от ресурс vscg на слой от формата                                       | Функция |
| PSDJAVA-504 | Добавяне на нови типове изкривяване (arc & arch)                                                                           | Функция |
| PSDJAVA-505 | Промяна на приложението, което запазва PSD файл към Aspose.PSD, ако свойството UpdateMetadata е зададено на true       | Функция |
| PSDJAVA-510 | Увеличаване на областта за изчисление на изкривяването на изображението                                                               | Функция |
| PSDJAVA-511 | Обработка на полу-прозрачността на слоя за корекция на черно и бяло неправилно                                          | Грешка     |
| PSDJAVA-512 | Заместване на SmartObject ReplaceContents (когато опциите AllowWarpRepaint са активирани) пада след 2 минути изчислително време | Грешка     |
| PSDJAVA-513 | Добавяне на възможност за получаване на реалната лява и горна позиция на LayerGroup                                      | Грешка     |
| PSDJAVA-514 | Преоразмеряването на слоя работи неправилно, когато PSD файла има VogkResource със структури в точки                       | Грешка     |
| PSDJAVA-515 | TextBound не функционира както се очаква                                                                         | Грешка     |
| PSDJAVA-516 | Добавяне на слой, създаден с конструктор по подразбиране към PSD изображение, не добавя подразбирателни ресурси към него           | Грешка     |
| PSDJAVA-517 | Timeline.LoopesCount се игнорира при експортиране към анимиран GIF                                          | Грешка     |

## **Промени в публичното API**
# **Добавени API:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **Премахнати API:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **Примери за използване:**

**PSDJAVA-502. Добавяне на възможност за експортиране на всяко ниво на PSD файл към файл с анимиран GIF**

```java
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // Create frames for each layer.
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

        // Update current states
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
```

**PSDJAVA-503. Присвояване на свойство за попълване на форма от ресурс vscg на слой от формата**

```java
        // Пример за пълноцветно попълване
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

            // Проверка на запазените промени
            try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();

            assertAreEqual(Color.getRed(), fillSettings.getColor());

            image.save(outFile);
        }

        // Пример за градиентно попълване:

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

        // Проверка на запазените промени
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
```