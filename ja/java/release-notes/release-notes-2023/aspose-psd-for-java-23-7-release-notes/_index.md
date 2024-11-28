---
title: Aspose.PSD for Java 23.7 - リリースノート
type: docs
weight: 40
url: /ja/java/aspose-psd-for-java-23-7-release-notes/
---

{{% alert color="primary" %}} このページには、[Aspose.PSD for Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) のリリースノートが含まれています。{{% /alert %}}

| **キー**     | **概要**                                                                                                                                      | **カテゴリー** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | PSDファイルの各レイヤーをアニメーションGIFファイルにエクスポートする能力を追加                                       | 機能 |
| PSDJAVA-503 | ShapeレイヤーのFillプロパティをvscgリソースから割り当てる                                             | 機能 |
| PSDJAVA-504 | 新しいワープタイプ（arc & arch）を追加                                                                   | 機能 |
| PSDJAVA-505 | UpdateMetadataプロパティがtrueに設定されている場合、PSDファイルを保存するアプリケーションをAspose.PSDに変更する   | 機能 |
| PSDJAVA-510 | ワープ画像の計算領域を増やす                                                                             | 機能 |
| PSDJAVA-511 | モノクロ調整レイヤーが半透明を誤って処理する                                                             | バグ     |
| PSDJAVA-512 | SmartObjectのReplaceContents（AllowWarpRepaintオプションが有効な場合）が計算後2分で処理が落ちる              | バグ     |
| PSDJAVA-513 | 実際のLayerGroupの左上位置を取得する能力を追加                                                          | バグ     |
| PSDJAVA-514 | PSDファイルがポイントで構造化されたVogkResourceを持つ場合、レイヤーのリサイズが正常に機能しない           | バグ     |
| PSDJAVA-515 | TextBoundが期待どおりに機能しない                                                                         | バグ     |
| PSDJAVA-516 | デフォルトコンストラクタで作成したレイヤーをPSDイメージに追加すると、デフォルトのリソースが追加されない      | バグ     |
| PSDJAVA-517 | animated GIFにエクスポートする際にTimeline.LoopsCountが無視される                                       | バグ     |

## **Public API 変更**
# **追加されたAPI:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **削除されたAPI:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **使用例:**

**PSDJAVA-502. PSDファイルの各レイヤーをアニメーションGIFファイルにエクスポートする能力を追加**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // 各レイヤーのフレームを作成します
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

        // 現在の状態を更新します
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

**PSDJAVA-503. ShapeレイヤーのFillプロパティをvscgリソースから割り当てる**

{{< highlight java >}}
        // 一様な塗り例
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

            // 保存された変更を確認します
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
		
		//グラデーション塗り例

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

    // 保存された変更を確認します
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

{{< /highlight >}}

**PSDJAVA-504. 新しいワープタイプ（arc & arch）を追加**

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
