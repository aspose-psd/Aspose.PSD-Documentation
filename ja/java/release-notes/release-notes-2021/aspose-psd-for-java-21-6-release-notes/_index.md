---
title: Aspose.PSD for Java 21.6 - リリースノート
type: docs
weight: 40
url: /ja/java/aspose-psd-for-java-21-6-release-notes/
---

{{% alert color="primary" %}} このページには、[Aspose.PSD for Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) のリリースノートが含まれています。 {{% /alert %}}

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDJAVA-351|グループのクリッピングマスクが正しくレンダリングされない|バグ|
|PSDJAVA-352|レイヤーグループの通常またはベクターマスクがレンダリング時に無視される|バグ|
|PSDJAVA-353|無効になっているベクターレイヤーマスクを持つPSDイメージを保存すると、ベクターマスクが有効になる|バグ|
|PSDJAVA-354|255文字を超えるテキストを含むTextLayerを作成する際の例外|バグ|

# **公開APIの変更**
# **追加されたAPI:**
- なし

# **削除されたAPI:**
- なし

# **使用例:**

**PSDJAVA-351. グループのクリッピングマスクが正しくレンダリングされない**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. レイヤーグループの通常またはベクターマスクがレンダリング時に無視される**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. 無効になっているベクターレイヤーマスクを持つPSDイメージを保存すると、ベクターマスクが有効になる**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. 255文字を超えるテキストを含むTextLayerを作成する際の例外**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}
