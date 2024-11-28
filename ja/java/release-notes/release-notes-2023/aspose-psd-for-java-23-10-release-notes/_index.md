---
title: Aspose.PSD for Java 23.10 - リリースノート
type: ドキュメント
weight: 40
url: /ja/aspose-psd-for-java-23-10-release-notes/
---

{{% alert color="primary" %}} このページには、[Aspose.PSD for Java 23.10](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.10/) のリリースノートが含まれています {{% /alert %}}

| **キー**        | **サマリー**                                                                             | **カテゴリ** |
|:---------------|:----------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-538    | 垂直テキスト方向のサポート                                                      |    機能   |
| PSDJAVA-542    | Shapeストローク描画でvstkリソースからストローク設定を使用する                        |    機能   |
| PSDJAVA-540    | ストローク形状の内部領域のレンダリングを実装する                                   |    機能   |
| PSDJAVA-541    | Shapeレイヤーが変更されていない場合はShapeレイヤーを再描画しない                   |    機能   |
| PSDJAVA-545    | [AIフォーマット] PDFベースのAIファイルからヘッダーの読み取りサポートを追加する                   |    機能   |
| PSDJAVA-546    | Psdファイルの解像度を設定するさまざまな方法が機能しない                                      |      バグ     |
| PSDJAVA-547    | FontSettings.SetFontsFoldersが機能しないか、Aspose.PSDが誤ったフォントを使用している             |      バグ     |
| PSDJAVA-548    | Regression. Shapeレイヤーがある場合にPsdImage.SaveでNull参照例外が発生するのを修正             |      バグ     |

## **パブリックAPIの変更**
# **追加されたAPI:**

- M:com.aspose.psd.FontSettings.getGetSystemAlternativeFont
- M:com.aspose.psd.FontSettings.setGetSystemAlternativeFont(boolean)
- M:com.aspose.psd.Graphics.getPaintableImageOptions
- M:com.aspose.psd.Graphics.setPaintableImageOptions(com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.Image.getAutoAdjustPalette
- M:com.aspose.psd.Image.getFileFormat(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.extensions.RegionExtensions.#ctor
- M:com.aspose.psd.fileformats.psd.PsdImage.setResolution(double,double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.getStroke
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.setStroke(com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.getFillSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.JustificationMode.Center
- T:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getEnabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getFill
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineAlignment
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineCap
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineDashSet
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineJoin
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setFill(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineAlignment(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineCap(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineDashSet(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineJoin(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setSize(double)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getEnabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getFill
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineAlignment
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setFill(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineDashSet(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineCap
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineDashSet
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineJoin
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineAlignment(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineCap(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineJoin(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setSize(double)
- T:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String)
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)

# **削除されたAPI:**

- M:com.aspose.psd.Image.isAutoAdjustPalette
- M:com.aspose.psd.ImageOptionsBase.memberwiseClone
- M:com.aspose.psd.imageoptions.BmpOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.CmxRasterizationOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.GifOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.Jpeg2000Options.memberwiseClone
- M:com.aspose.psd.imageoptions.JpegOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PdfOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PngOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PsdOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.TiffOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.VectorRasterizationOptions.memberwiseClone
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.JustificationMode.Center

## **使用例:**

** PSDJAVA-538. 垂直テキスト方向のサポート**

{{< highlight java >}}
    
    String sourceFile = "src/main/resources/692_lt1.psd";
    String outputFile = "src/main/resources/692_output.png";
    String fontsFolder = "src/main/resources/692_Fonts";

        List<String> fontFolders = new List<>(FontSettings.getFontsFolders());
        fontFolders.add(fontsFolder);
        FontSettings.setFontsFolders(fontFolders.toArray(new String[0]), true);

        try(PsdImage psdImage = (PsdImage)Image.load(sourceFile)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            psdImage.save(outputFile, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-542. Shapeストローク描画でvstkリソースからストローク設定を使用する**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/StrokeShapeTest.psd";
        String outputFilePsd = "src/main/resources/StrokeShapeTest.out.psd";
        String outputFilePng = "src/main/resources/StrokeShapeTest.out.png";

        try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
            Layer layer = image.getLayers()[1];
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();
            fillSettings.setColor(Color.getGreenYellow());
            shapeLayer.update();

            ShapeLayer shapeLayer2 = (ShapeLayer) image.getLayers()[3];
            GradientFillSettings gradientSettings = (GradientFillSettings) shapeLayer2.getFill();
            gradientSettings.setDither(true);
            gradientSettings.setReverse(true);
            gradientSettings.setAlignWithLayer(false);
            gradientSettings.setAngle(20);
            gradientSettings.setScale(50);
            gradientSettings.getColorPoints()[0].setLocation(100);
            gradientSettings.getColorPoints()[1].setLocation(4000);
            gradientSettings.getTransparencyPoints()[0].setLocation(200);
            gradientSettings.getTransparencyPoints()[1].setLocation(3800);
            gradientSettings.getTransparencyPoints()[0].setOpacity(90);
            gradientSettings.getTransparencyPoints()[1].setOpacity(10);
            shapeLayer2.update();

            ShapeLayer shapeLayer3 = (ShapeLayer) image.getLayers()[5];
            StrokeSettings strokeSettings = (StrokeSettings) shapeLayer3.getStroke();
            strokeSettings.setSize(15);
            ColorFillSettings strokeFillSettings = (ColorFillSettings) strokeSettings.getFill();
            strokeFillSettings.setColor(Color.getGreenYellow());
            shapeLayer3.update();

            image.save(outputFilePsd);
            image.save(outputFilePng, new PngOptions());
        }

        // 変更されたデータを確認
        try (PsdImage image = (PsdImage) Image.load(outputFilePsd)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();
            assertAreEqual(Color.getGreenYellow(), fillSettings.getColor());

            ShapeLayer shapeLayer2 = (ShapeLayer) image.getLayers()[3];
            GradientFillSettings gradientSettings = (GradientFillSettings) shapeLayer2.getFill();
            assertAreEqual(true, gradientSettings.getDither());
            assertAreEqual(true, gradientSettings.getReverse());
            assertAreEqual(false, gradientSettings.getAlignWithLayer());
            assertAreEqual(20.0, gradientSettings.getAngle());
            assertAreEqual(50, gradientSettings.getScale());
            assertAreEqual(100, gradientSettings.getColorPoints()[0].getLocation());
            assertAreEqual(4000, gradientSettings.getColorPoints()[1].getLocation());
            assertAreEqual(200, gradientSettings.getTransparencyPoints()[0].getLocation());
            assertAreEqual(3800, gradientSettings.getTransparencyPoints()[1].getLocation());
            assertAreEqual(90.0, gradientSettings.getTransparencyPoints()[0].getOpacity());
            assertAreEqual(10.0, gradientSettings.getTransparencyPoints()[1].getOpacity());

            ShapeLayer shapeLayer3 = (ShapeLayer) image.getLayers()[5];
            StrokeSettings strokeSettings = (StrokeSettings) shapeLayer3.getStroke();
            ColorFillSettings strokeFillSettings = (ColorFillSettings) strokeSettings.getFill();
            assertAreEqual(15.0, strokeSettings.getSize());
            assertAreEqual(Color.getGreenYellow(), strokeFillSettings.getColor());
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

** PSDJAVA-540. ストローク形状の内部領域のレンダリングを実装する**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/StrokeShapeTest.psd";
        String outputFilePsd = "src/main/resources/StrokeShapeTest.out.psd";
        String outputFilePng = "src/main/resources/StrokeShapeTest.out.png";

        try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
            Layer layer = image.getLayers()[1];
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();
            fillSettings.setColor(Color.getGreenYellow());
            shapeLayer.update();

            ShapeLayer shapeLayer2 = (ShapeLayer) image.getLayers()[3];
            GradientFillSettings gradientSettings = (GradientFillSettings) shapeLayer2.getFill();
            gradientSettings.setDither(true);
            gradientSettings.setReverse(true);
            gradientSettings.setAlignWithLayer(false);
            gradientSettings.setAngle(20);
            gradientSettings.setScale(50);
            gradientSettings.getColorPoints()[0].setLocation(100);
            gradientSettings.getColorPoints()[1].setLocation(4000);
            gradientSettings.getTransparencyPoints()[0].setLocation(200);
            gradientSettings.getTransparencyPoints()[1].setLocation(3800);
            gradientSettings.getTransparencyPoints()[0].setOpacity(90);
            gradientSettings.getTransparencyPoints()[1].setOpacity(10);
            shapeLayer2.update();

            ShapeLayer shapeLayer3 = (ShapeLayer) image.getLayers()[5];
            StrokeSettings strokeSettings = (StrokeSettings) shapeLayer3.getStroke();
            strokeSettings.setSize(15);
            ColorFillSettings strokeFillSettings = (ColorFillSettings) strokeSettings.getFill();
            strokeFillSettings.setColor(Color.getGreenYellow());
            shapeLayer3.update();

            image.save(outputFilePsd);
            image.save(outputFilePng, new PngOptions());
        }

        // 変更されたデータを確認
        try (PsdImage image = (PsdImage) Image.load(outputFilePsd)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();
            assertAreEqual(Color.getGreenYellow(), fillSettings.getColor());

            ShapeLayer shapeLayer2 = (ShapeLayer) image.getLayers()[3];
            GradientFillSettings gradientSettings = (GradientFillSettings) shapeLayer2.getFill();
            assertAreEqual(true, gradientSettings.getDither());
            assertAreEqual(true, gradientSettings.getReverse());
            assertAreEqual(false, gradientSettings.getAlignWithLayer());
            assertAreEqual(20.0, gradientSettings.getAngle());
            assertAreEqual(50, gradientSettings.getScale());
            assertAreEqual(100, gradientSettings.getColorPoints()[0].getLocation());
            assertAreEqual(4000, gradientSettings.getColorPoints()[1].getLocation());
            assertAreEqual(200, gradientSettings.getTransparencyPoints()[0].getLocation());
            assertAreEqual(3800, gradientSettings.getTransparencyPoints()[1].getLocation());
            assertAreEqual(90.0, gradientSettings.getTransparencyPoints()[0].getOpacity());
            assertAreEqual(10.0, gradientSettings.getTransparencyPoints()[1].getOpacity());

            ShapeLayer shapeLayer3 = (ShapeLayer) image.getLayers()[5];
            StrokeSettings strokeSettings = (StrokeSettings) shapeLayer3.getStroke();
            ColorFillSettings strokeFillSettings = (ColorFillSettings) strokeSettings.getFill();
            assertAreEqual(15.0, strokeSettings.getSize());
            assertAreEqual(Color.getGreenYellow(), strokeFillSettings.getColor());
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

** PSDJAVA-541. Shapeレイヤーが変更されていない場合はShapeレイヤーを再描画しない**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/ShapeInternalSolid.psd";
        String outputFile = "src/main/resources/ShapeInternalSolid.out.psd";

        try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();
            fillSettings.setColor(Color.getRed());

            // 保存前にShapeレイヤーの更新を行わない

            image.save(outputFile);

            // 保存され