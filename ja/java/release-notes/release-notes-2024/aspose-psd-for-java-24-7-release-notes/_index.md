---
title: Aspose.PSD for Java 24.7 - リリースノート
type: docs
weight: 40
url: /ja/java/aspose-psd-for-java-24-7-release-notes/
---

{{% alert color="primary" %}} このページには、[Aspose.PSD for Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) のリリースノートが含まれています。 {{% /alert %}}

| **キー**     | **概要**                                                                                          | **カテゴリ** |
|:------------|:----------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | AI ドキュメントを開くときに "Image loading failed." 例外が発生する                                 | バグ         |
| PSDJAVA-636 | テキストが出力された PDF ファイルで正しくレンダリングされない                                    | バグ         |
| PSDJAVA-637 | Linux 上のファイルで画像エクスポートに失敗する ImageSaveException を修正                         | バグ         |
| PSDJAVA-638 | Aspose.Drawing を使用する際のフォントの読み込みを修正                                             | バグ         |
| PSDJAVA-639 | 大きな JPEG を使用してスマートオブジェクトレイヤを作成する際に 'Arithmetic operation resulted in an overflow' が発生する | バグ         |
| PSDJAVA-640 | AI ファイルを JPG ファイルに変換できない                                                         | バグ         |

## **パブリック API 変更**
# **追加された API:**

- なし

# **削除された API:**

- なし 

## **使用例:**

**PSDJAVA-635. AI ドキュメントを開くときに "Image loading failed." 例外が発生する**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. テキストが出力された PDF ファイルで正しくレンダリングされない**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. Linux 上のファイルで画像エクスポートに失敗する ImageSaveException を修正**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Bed_Roll-Sticker4_1.psd";
    String outputFile = "src/main/resources/output.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        JpegOptions saveOptions = new JpegOptions();
        saveOptions.setQuality(70);
        psdImage.save(outputFile, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-638. Aspose.Drawing を使用する際のフォントの読み込みを修正**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- 更新前。インストールされているフォントの数: " + installedFonts.getFamilies().length);
        System.out.println("- プラットフォーム: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- 'Arial' の Adobe フォント名を取得してフォントキャッシュを更新: "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- 更新後。インストールされているフォントの数: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 大きな JPEG を使用してスマートオブジェクトレイヤを作成する際に 'Arithmetic operation resulted in an overflow' が発生する**

{{< highlight java >}}

    String srcFile = "src/main/resources/source.psd";
    String imageJpg = "src/main/resources/test.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setDataRecoveryMode(DataRecoveryMode.MaximalRecover);
    try (var image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        final FileStream stream = new FileStream(imageJpg, FileMode.Open);
        try {
            var addedLayer = new SmartObjectLayer(stream);
            addedLayer.setName("Test Layer");
            image.addLayer(addedLayer);
        } finally {
            stream.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. AI ファイルを JPG ファイルに変換できない**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}
