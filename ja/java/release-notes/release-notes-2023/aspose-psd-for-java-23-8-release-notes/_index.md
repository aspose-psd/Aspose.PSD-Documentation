---
title: Aspose.PSD for Java 23.8 - リリースノート
type: docs
weight: 40
url: /ja/java/aspose-psd-for-java-23-8-release-notes/
---

{{% alert color="primary" %}} このページには、[Aspose.PSD for Java 23.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.8/) のリリースノートが含まれています。 {{% /alert %}}

| **キー**     | **概要**                                                                                                                                      | **カテゴリー** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-518 | 新しいタイプのワープ（フラグ）を追加                                                                                                                      |    機能   |
| PSDJAVA-519 | 新しいワープの種類を追加: 上向きアーク、下向きアーク、スフィア                                                                                                  |    機能   |
| PSDJAVA-520 | 新しいポスタリゼレイヤーを追加するための新しいメソッドPsdImage.AddPosterizeAdjustmentLayerを実装                                                         |    機能   |
| PSDJAVA-521 | 開いて保存するだけでPSD情報が失われる                                                                                                  |      バグ     |
| PSDJAVA-522 | 画像の読み込みに失敗                                                                                                                             |      バグ     |
| PSDJAVA-523 | 画像の読み込みに失敗: UnknownStructure型のオブジェクトをDescriptorStructure型にキャストできません                                                 |      バグ     |
| PSDJAVA-524 | 第三者ライブラリでファイルを変更するとPSDファイルが壊れますが、Photoshopで開くことができます                                                    |      バグ     |

## **公開APIの変更**
# **追加されたAPI:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **削除されたAPI:**

- なし

## **使用例:**

**PSDJAVA-518. 新しいワープの種類を追加します（フラグ）**

{{< highlight java >}}
    String sourceFile = "src/main/resources/flag_warp.psd";
    String outputFile = "src/main/resources/flag_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputFile, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-519. 新しいワープの種類を追加します: 上向きアーク、下向きアーク、スフィア**

{{< highlight java >}}
    String sourceFileArcUpper = "src/main/resources/arc_upper_warp.psd";
    String sourceFileArcLower = "src/main/resources/arc_lower_warp.psd";
    String sourceFileBulge = "src/main/resources/bulge_warp.psd";

    String outputFileArcUpper = "src/main/resources/ArcUpper_export.png";
    String outputFileArcLower = "src/main/resources/ArcLower_export.png";
    String outputFileBulge = "src/main/resources/Bulge_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileArcUpper, psdLoadOptions)) {
        psdImage.save(outputFileArcUpper, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileArcLower, psdLoadOptions)) {
        psdImage.save(outputFileArcLower, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileBulge, psdLoadOptions)) {
        psdImage.save(outputFileBulge, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-520. 新しいメソッドPsdImage.AddPosterizeAdjustmentLayerを実装します**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya.psd";
    String outFile = "src/main/resources/zendeya.psd.out.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile)) {
        psdImage.addPosterizeAdjustmentLayer();
        psdImage.save(outFile);
    }

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    // 保存された変更を確認
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        PosterizeLayer posterizeLayer = (PosterizeLayer) image.getLayers()[1];

        assertAreEqual(true, posterizeLayer instanceof PosterizeLayer);
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

**PSDJAVA-521. 開いて保存するだけでPSD情報が失われる**

{{< highlight java >}}
    String src = "src/main/resources/Original file.psd";
    String outputPsd = "src/main/resources/out_Original file.psd";
    String outputPng = "src/main/resources/out_Original file.png";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputPsd);
        psdImage.save(outputPng, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-522. 画像の読み込みに失敗**

{{< highlight java >}}
    String srcFile1 = "src/main/resources/test_text.psd";
    String srcFile2 = "src/main/resources/test_smart_object.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile1)) {
    }

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. 画像の読み込みに失敗: UnknownStructure型のオブジェクトをDescriptorStructure型にキャストできません**

{{< highlight java >}}
   try (PsdImage newPsd = new PsdImage(10, 10)) {
        newPsd.addLayer(FillLayer.createInstance(FillType.Gradient));

        final MemoryStream memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000);
        try {
            newPsd.save(memStream.toOutputStream());

            memStream.seek(DescriptorStructure.StructureKey, SeekOrigin.Current);
            memStream.write(new byte[1], 0, 0);
            memStream.setPosition(0);

            try (PsdImage psdImage = (PsdImage) Image.load(memStream.toInputStream())) {
                // 正しく読み込まれるはずです
            }
        } finally {
            memStream.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. 第三者ライブラリでファイルを変更するとPSDファイルが壊れますが、Photoshopで開くことができます**

{{< highlight java >}}
    String sourceFile = "src/main/resources/output.psd";
    String outputFile = "src/main/resources/export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage img = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setCompressionLevel(9);
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        img.save(outputFile, pngOptions);
    }
{{< /highlight >}}
