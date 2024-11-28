```md
---
title: Aspose.PSD для Java 23.7 - Примечания к выпуску
type: docs
weight: 40
url: /ru/java/aspose-psd-for-java-23-7-release-notes/
---

{{% alert color="primary" %}} На этой странице содержатся примечания к выпуску [Aspose.PSD для Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **Ключ**     | **Сводка**                                                                                                                                      | **Категория** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | Добавить возможность экспортировать каждый слой файла PSD в файл Animated Gif             | Функция |
| PSDJAVA-503 | Назначить свойство заполнения слоя формы из ресурса vscg                                  | Функция |
| PSDJAVA-504 | Добавить новые типы искажения (дугу и арку)                                               | Функция |
| PSDJAVA-505 | Изменить приложение, которое сохраняет файл PSD в Aspose.PSD, если свойство UpdateMetadata установлено в true       | Функция |
| PSDJAVA-510 | Увеличить область расчета изображения искажения                                            | Функция |
| PSDJAVA-511 | Черно-белая коррекция слоя на полупрозрачность обрабатывается неправильно                | Ошибка     |
| PSDJAVA-512 | Замена содержимого SmartObject (когда активна опция AllowWarpRepaint) падает после 2 минут вычислений | Ошибка     |
| PSDJAVA-513 | Добавить возможность получить реальное положение слева и сверху группы слоев             | Ошибка     |
| PSDJAVA-514 | Изменение размера слоя работает неправильно, когда файл PSD содержит VogkResource со структурами в точках     | Ошибка     |
| PSDJAVA-515 | Текстовая область не работает как ожидалось                                                  | Ошибка     |
| PSDJAVA-516 | Добавление слоя, созданного конструктором по умолчанию, к изображению PSD не добавляет к нему стандартные ресурсы | Ошибка     |
| PSDJAVA-517 | Количество петель Timeline.LoopesCount игнорируется при экспорте в анимированный GIF       | Ошибка     |

## **Изменения в общедоступном API**
# **Добавленные API:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **Удаленные API:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **Примеры использования:**

**PSDJAVA-502. Добавить возможность экспортировать каждый слой файла PSD в файл Animated Gif**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // Создание кадров для каждого слоя.
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

        // Обновление текущих состояний
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

**PSDJAVA-503. Назначить свойство заполнения слоя формы из ресурса vscg**

{{< highlight java >}}
        // Пример заполнения сплошным цветом
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

            // Проверка сохраненных изменений
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
            assertAreEqual(expected, actual, "Objects are not equal.");
        }
		
		// Пример градиентного заполнения:

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

    // Проверка сохраненных изменений
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
    assertAreEqual(expected, actual, "Objects are not equal.");
}

{{< /highlight >}}

**PSDJAVA-504. Добавить новые типы искажения (дугу и арку)**

{{< highlight java >}}
    String sourceArcFile = "src/main/resources/arc_warp.psd";
    String outputArcFile = "src/main/resources/arc_export.png";

    String sourceArchFile = "src/main/resources/arch_warp.psd";
    String outputArchFile = "src/main/resources/arch_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceArcFile, psdLoadOptions)) {
        psdImage.save(outputArcFile, pngOptions);
    }


    try (PsdImage psdImage = (PsdImage) Image.load(sourceArchFile, psdLoadOptions)) {
        psdImage.save(outputArchFile, pngOptions);
    }
