---
title: Aspose.PSD for Java 24.2 - リリースノート
type: docs
weight: 40
url: /ja/aspose-psd-for-java-24-2-release-notes/
---

{{% alert color="primary" %}} このページには、[Aspose.PSD for Java 24.2](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.2/) のリリースノートが含まれています。{{% /alert %}}

| **キー**     | **概要**                                                                   | **カテゴリ** |
|:------------|:------------------------------------------------------------------------------|:-------------|
| PSDJAVA-584 | パターンのすべての設定をハンドルする角度プロパティ。                         | 機能        |
| PSDJAVA-585 | テキストレイヤーの垂直および水平スケールのサポート。                       | 機能        |
| PSDJAVA-589 | [AI フォーマット] PDF ベースの AI フォーマットで背景の正しいレンダリングを実装。 | 機能      |
| PSDJAVA-590 | ワープ内の歪みメカニズムを変更。                                             | 強化       |
| PSDJAVA-591 | ワープのスピードアップ。                                                       | 強化       |
| PSDJAVA-592 | ドキュメントを開くと "画像の読み込みに失敗しました。" 例外が発生する。             | バグ        |
| PSDJAVA-593 | ストロークパターンを持つ psd ファイルの保存を修正。                            | バグ        |
| PSDJAVA-594 | ReplaceContents を使用したスマートオブジェクトのテキストスタイルが正しくありません。 | バグ      |
| PSDJAVA-595 | [AI フォーマット] AI ファイルでの Cubic Bezier のレンダリングを修正。           | バグ        |

## **公開 API 変更**
# **追加された API:**

- M:com.aspose.psd.fileformats.ai.AiImage.getActivePageIndex
- M:com.aspose.psd.fileformats.ai.AiImage.setActivePageIndex(int)
- T:com.aspose.psd.fileformats.psd.layers.FillLayer 
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.createInstance(int)
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.getFillSettings 
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.getFillType 
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.replaceNonTransparentColors(int)
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.update
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PtFlResource.getAngle
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PtFlResource.setAngle(double)

# **削除された API:**

- T:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer 
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.createInstance(int)
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.getFillSettings 
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.getFillType 
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.replaceNonTransparentColors(int)
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.update

## **使用例**

** PSDJAVA-584. パターンのすべての設定をハンドルする角度プロパティ**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/PatternFillLayerWide_0.psd";
        String outputFile = "src/main/resources/PatternFillLayerWide_0_output.psd";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setLoadEffectsResource(true);

        try (PsdImage image = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
            FillLayer fillLayer = (FillLayer) image.getLayers()[1];
            PatternFillSettings fillSettings = (PatternFillSettings) fillLayer.getFillSettings();
            fillSettings.setAngle(70.0);
            fillLayer.update();
            image.save(outputFile, new PsdOptions());
        }

        try (PsdImage image = (PsdImage) Image.load(outputFile, psdLoadOptions)) {
            FillLayer fillLayer = (FillLayer) image.getLayers()[1];
            PatternFillSettings fillSettings = (PatternFillSettings) fillLayer.getFillSettings();

            assertAreEqual(70.0, fillSettings.getAngle());
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "オブジェクトが等しくありません。");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

** PSDJAVA-585. テキストレイヤーの垂直および水平スケールのサポート**

{{< highlight java >}}

        String src = "src/main/resources/1719_src.psd";
        String output = "src/main/resources/out_1719.png";

        try (PsdImage psdImage = (PsdImage) Image.load(src)) {
            psdImage.save(output, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-589. [AI フォーマット] PDF ベースの AI フォーマットで背景の正しいレンダリングを実装**

{{< highlight java >}}

        String sourceFile = "src/main/resources/pineapples.ai";
        String outputFilePath = "src/main/resources/pineapples.png";

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            image.save(outputFilePath, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-590. ワープ内の歪みメカニズムを変更**

{{< highlight java >}}

        String sourceFile = "src/main/resources/crow_grid.psd";
        String outputFile = "src/main/resources/export.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);
        opt.setAllowWarpRepaint(true);

        try (PsdImage img = (PsdImage) Image.load(sourceFile, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(outputFile, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-591. ワープのスピードアップ**

{{< highlight java >}}

        String sourceFile = "src/main/resources/output.psd";
        String outputFile = "src/main/resources/export.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);
        opt.setAllowWarpRepaint(true);

        long startTime = System.currentTimeMillis();

        try (PsdImage img = (PsdImage) Image.load(sourceFile, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(outputFile, pngOptions);
        }

        long endTime = System.currentTimeMillis();
        int timeInSec = (int) (endTime - startTime);

        if (timeInSec > 100000) {
            throw new RuntimeException("プロセス時間が長すぎます");
        }

{{< /highlight >}}

** PSDJAVA-592. ドキュメントを開くと "画像の読み込みに失敗しました。" 例外が発生する**

{{< highlight java >}}

        String sourceFile1 = "src/main/resources/PRODUCT.ai";
        String outputFile1 = "src/main/resources/PRODUCT.png";

        try (AiImage image = (AiImage) Image.load(sourceFile1)) {
            image.save(outputFile1, new PngOptions());
        }

        String sourceFile2 = "src/main/resources/Dolota.ai";
        String outputFile2 = "src/main/resources/Dolota.png";

        try (AiImage image = (AiImage) Image.load(sourceFile2)) {
            image.save(outputFile2, new PngOptions());
        }

        String sourceFile3 = "src/main/resources/ARS_novelty_2108_out_01(1).ai";
        String outputFile3 = "src/main/resources/ARS_novelty_2108_out_01(1).png";

        try (AiImage image = (AiImage) Image.load(sourceFile3)) {
            image.save(outputFile3, new PngOptions());
        }

        String sourceFile4 = "src/main/resources/bit_gear.ai";
        String outputFile4 = "src/main/resources/bit_gear.png";

        try (AiImage image = (AiImage) Image.load(sourceFile4)) {
            image.save(outputFile4, new PngOptions());
        }

        String sourceFile5 = "src/main/resources/test.ai";
        String outputFile5 = "src/main/resources/test.png";

        try (AiImage image = (AiImage) Image.load(sourceFile5)) {
            image.save(outputFile5, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-593. ストロークパターンを持つ psd ファイルの保存を修正**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/StrokeShapePattern.psd";
        String outputFile = "src/main/resources/StrokeShapePattern_output.psd";

        Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
        UUID guid = UUID.randomUUID();
        String newPatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";
        int[] newPattern = new int[]
                {
                        Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
                };

        try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            PatternFillSettings strokeInternalFillSettings = (PatternFillSettings) shapeLayer.getFill();

            PattResource pattResource;
            for (LayerResource globalLayerResource : image.getGlobalLayerResources()) {
                if (globalLayerResource instanceof PattResource) {
                    pattResource = (PattResource) globalLayerResource;
                    PattResourceData patternItem = pattResource.getPatterns()[0]; // ストローク内部パターンデータ

                    patternItem.setPatternId(guid.toString());
                    patternItem.setName(newPatternName);
                    patternItem.setPattern(newPattern, newPatternBounds);

                    break;
                }
            }

            strokeInternalFillSettings.setPatternName(newPatternName);
            strokeInternalFillSettings.setPatternId(guid.toString() + "\0");

            shapeLayer.update();

            image.save(outputFile);
        }

        // 変更されたデータを確認。
        try (PsdImage image = (PsdImage) Image.load(outputFile)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            PatternFillSettings strokeInternalFillSettings = (PatternFillSettings) shapeLayer.getFill();

            assertAreEqual(guid.toString().toUpperCase(), strokeInternalFillSettings.getPatternId());
            assertAreEqual(newPatternName, strokeInternalFillSettings.getPatternName() + "\0");
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "オブジェクトが等しくありません。");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

** PSDJAVA-594. ReplaceContents を使用したスマートオブジェクトのテキストスタイルが正しくありません**

{{< highlight java >}}

        String inputFile = "src/main/resources/source.psd";
        String output2 = "src/main/resources/output.png";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setLoadEffectsResource(true);

        try (PsdImage psdImage = (PsdImage) Image.load(inputFile, psdLoadOptions)) {
            SmartObjectLayer smartObject = (SmartObjectLayer) psdImage.getLayers()[1];

            try (PsdImage smartObjectImage = (PsdImage) smartObject.loadContents(psdLoadOptions)) {
                smartObject.replaceContents(smartObjectImage);
            }

            PngOptions pngOptions = new PngOptions();
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            psdImage.save(output2, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-595. [AI フォーマット] AI ファイルでの Cubic Bezier のレンダリングを修正**

{{< highlight java >}}

        String sourceFile = "src/main/resources/Typography.ai";
        String outputFilePath = "src/main/resources/Typography.png";

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            image.save(outputFilePath, new PngOptions());
        }

{{< /highlight >}}