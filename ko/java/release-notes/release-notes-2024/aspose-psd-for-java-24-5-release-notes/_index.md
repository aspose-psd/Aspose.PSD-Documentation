---
title: Aspose.PSD for Java 24.5 - 릴리스 노트
type: docs
weight: 40
url: /ko/java/aspose-psd-for-java-24-5-release-notes/
---

{{% alert color="primary" %}} 이 페이지에는 [Aspose.PSD for Java 24.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.5/)에 대한 릴리스 노트가 포함되어 있습니다. {{% /alert %}}

| **키**        | **요약**                                                                                            | **카테고리** |
|:--------------|:---------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-617  | [AI 포맷] EPSF 헤더를 사용하는 AI 파일을 처리할 수 있는 지원 추가                                    | 기능         |
| PSDJAVA-620  | PSD 파일 미리보기에서 반투명이 잘못 처리됨                                                         | 버그         |
| PSDJAVA-621  | 모양 레이어 렌더링이 부분적으로 잘못됨                                                       | 버그         |
| PSDJAVA-622  | 큰 크기(200MB 이상 및 큰 차원)의 PSD 파일을 저장할 때 예외가 발생함(메모리 사용 문제)             | 버그         |
| PSDJAVA-623  | 23.7에서 24.3으로 업데이트 후 PDF로 저장할 때 이미지 저장에 실패하는 예외가 발생함               | 버그         |
| PSDJAVA-624  | 중국어 글꼴에 대한 GetFontInfoRecords 메서드의 문제 수정                                        | 버그         |

## **공개 API 변경**

# **추가된 API:**

- M:com.aspose.psd.fileformats.ai.AiLayerSection.getColorIndex
- M:com.aspose.psd.fileformats.ai.AiLayerSection.setColorIndex(int)
- M:com.aspose.psd.fileformats.ai.AiLayerSection.hasMultiLayerMasks
- M:com.aspose.psd.fileformats.ai.AiLayerSection.setMultiLayerMasks(boolean)
- M:com.aspose.psd.imageoptions.PsdOptions.getBackgroundContents
- M:com.aspose.psd.imageoptions.PsdOptions.setBackgroundContents(com.aspose.psd.fileformats.psd.rawcolor.RawColor)

# **제거된 API:**

- 없음

## **사용 예시:**

**PSDJAVA-617. [AI Format] EPSF 헤더가 있는 AI 파일 처리 지원 추가**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/example.ai";
        String outputFilePath = "src/main/resources/example.png";

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            assertAreEqual(image.getLayers().length, 2);
            assertAreEqual(image.getLayers()[0].hasMultiLayerMasks(), false);
            assertAreEqual(image.getLayers()[0].getColorIndex(), -1);
            assertAreEqual(image.getLayers()[1].hasMultiLayerMasks(), false);
            assertAreEqual(image.getLayers()[1].getColorIndex(), -1);

            image.save(outputFilePath, new PngOptions());
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Objects are not equal.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-620. PSD 파일 미리보기에서 반투명이 잘못 처리됨**

{{< highlight java >}}

        String sourceFile = "src/main/resources/frog_nosymb.psd";
        String outputFile = "src/main/resources/frog_nosymb_backgroundcontents_output.psd";

        try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
            RawColor backgroundColor = new RawColor(PixelDataFormat.getRgb32Bpp());
            int argbValue = 255 << 24 | 255 << 16 | 255 << 8 | 255;
            backgroundColor.setAsInt(argbValue); // 흰색

            PsdOptions psdOptions = new PsdOptions(psdImage);
            psdOptions.setColorMode(ColorModes.Rgb);
            psdOptions.setCompressionMethod(CompressionMethod.RLE);
            psdOptions.setChannelsCount((short) 4);
            psdOptions.setBackgroundContents(backgroundColor);

            psdImage.save(outputFile, psdOptions);
        }

{{< /highlight >}}

**PSDJAVA-621. 모양 레이어 렌더링이 부분적으로 잘못됨**

{{< highlight java >}}

    private static final int ImgToPsdRatio = 256 * 65535;

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/ShapeLayerTest.psd";
        String outputFile = "src/main/resources/ShapeLayerTest_output.psd";
        
        try (PsdImage im = (PsdImage) Image.load(sourceFile)) {
            ShapeLayer shapeLayer = (ShapeLayer) im.getLayers()[2];
            IPath path = shapeLayer.getPath();
            IPathShape[] pathShapes = path.getItems();
            List<BezierKnotRecord> knotsList = new ArrayList<>();
            for (IPathShape pathShape : pathShapes) {
                BezierKnotRecord[] knots = pathShape.getItems();
                Collections.addAll(knotsList, knots);
            }

            // 레이어 속성 변경
            PathShape newShape = new PathShape();

            BezierKnotRecord firstBezierKnotRecord = new BezierKnotRecord();
            firstBezierKnotRecord.setLinked(true);
            firstBezierKnotRecord.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            shapeLayer.getContainer().getSize())});

            BezierKnotRecord secondBezierKnotRecord = new BezierKnotRecord();
            secondBezierKnotRecord.setLinked(true);
            secondBezierKnotRecord.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(50, 490),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 490),
                            shapeLayer.getContainer().getSize()), // Anchor point
                    pointFToResourcePoint(
                            new PointF(150, 490),
                            shapeLayer.getContainer().getSize())
            });

            BezierKnotRecord thirdBezierKnotRecord = new BezierKnotRecord();
            thirdBezierKnotRecord.setLinked(true);
            thirdBezierKnotRecord.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(490, 150),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(490, 50),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(490, 20),
                            shapeLayer.getContainer().getSize()),
            });

            BezierKnotRecord[] bezierKnots = new BezierKnotRecord[]
                    {firstBezierKnotRecord, secondBezierKnotRecord, thirdBezierKnotRecord};

            newShape.setItems(bezierKnots);

            List<IPathShape> newShapes = new ArrayList<>(Arrays.asList(pathShapes));
            newShapes.add(newShape);

            IPathShape[] pathShapeNew = newShapes.toArray(new IPathShape[0]);
            path.setItems(pathShapeNew);

            shapeLayer.update();

            im.save(outputFile, new PsdOptions());
        }

        try (PsdImage im = (PsdImage) Image.load(outputFile)) {
            ShapeLayer shapeLayer = (ShapeLayer) im.getLayers()[2];
            IPath path = shapeLayer.getPath();
            IPathShape[] pathShapes = path.getItems();
            List<BezierKnotRecord> knotsList = new ArrayList<>();
            for (IPathShape pathShape : pathShapes) {
                BezierKnotRecord[] knots = pathShape.getItems();
                knotsList.addAll(Arrays.asList(knots));
            }

            assertAreEqual(3, pathShapes.length);
            assertAreEqual(42, shapeLayer.getLeft());
            assertAreEqual(14, shapeLayer.getTop());
            assertAreEqual(1600, shapeLayer.getBounds().getWidth());
            assertAreEqual(1086, shapeLayer.getBounds().getHeight());
        }
    }

    static Point pointFToResourcePoint(PointF point, Size imageSize) {
        return new Point(
                (int) Math.round(point.getY() * (ImgToPsdRatio / imageSize.getHeight())),
                (int) Math.round(point.getX() * (ImgToPsdRatio / imageSize.getWidth())));
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Objects are not equal.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-622. 큰 크기(200MB 이상 및 큰 차원)의 PSD 파일을 저장할 때 예외가 발생함(메모리 사용 문제)**

{{< highlight java >}}

    String sourceFile = "src/main/resources/bigfile.psd";
    String outputFile = "src/main/resources/output_raw.psd";

    PsdLoadOptions loadOptions = new PsdLoadOptions();
    loadOptions.setLoadEffectsResource(true);
    loadOptions.setUseDiskForLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, loadOptions)) {
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setCompressionMethod(CompressionMethod.RLE);

        // 여기서 오류가 발생하지 않아야 함
        psdImage.save(outputFile, psdOptions);
    }

{{< /highlight >}}

**PSDJAVA-623. 23.7에서 24.3으로 업데이트 후 PDF로 저장할 때 이미지 저장에 실패한 예외 발생**

{{< highlight java >}}

    String sourceFile = "src/main/resources/CVFlor.psd";
    String outputFile = "src/main/resources/_export.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(outputFile, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-624. 중국어 글꼴에 대한 GetFontInfoRecords 메서드의 문제 수정**

{{< highlight java >}}

    String fontFolder = "src/main/resources/Font";
    String sourceFile = "src/main/resources/bd-worlds-best-pink.psd";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    psdLoadOptions.setAllowWarpRepaint(true);

    try {
        FontSettings.setFontsFolders(new String[]{fontFolder}, true);

        try (PsdImage image = (PsdImage) PsdImage.load(sourceFile, psdLoadOptions)) {
            for (Layer layer : image.getLayers()) {
                if (layer instanceof TextLayer) {
                    TextLayer textLayer = (TextLayer) layer;

                    if ("best".equals(textLayer.getText())) {
                        // 중국어 글꼴로 인해 여기서 예외가 발생함으로 이 문제를 수정함.
                        textLayer.updateText("SUCCESS");
                    }
                }
            }
        }
    } finally {
        FontSettings.reset();
    }

{{< /highlight >}}