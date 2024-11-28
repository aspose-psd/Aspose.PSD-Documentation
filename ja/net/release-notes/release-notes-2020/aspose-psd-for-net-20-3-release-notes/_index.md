---
title: Aspose.PSD for .NET 20.3 - リリースノート
type: docs
weight: 100
url: /ja/net/aspose-psd-for-net-20-3-release-notes/
---

{{% alert color="primary" %}} 

このページには、[Aspose.PSD for .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}} 

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-188|.Net Core のサポート|Feature|
|PSDNET-523|Adobe Illustrator ファイルをPDFに変換する機能|Feature|
|PSDNET-212|1 つのテキストレイヤーで異なるスタイルをレンダリングする機能を追加|Feature|
|PSDNET-144|白黒調整レイヤーのサポート|Feature|
|PSDNET-233|AI 形式（バージョン 8）のエクスポートを他の形式にサポートする機能を追加|Feature|
|PSDNET-540|PassThroughブレンドモード処理のサポート（レイヤーグループ専用）|Feature|
|PSDNET-539|空のUnicode Alpha Namesリソースを持つ画像をロードしようとすると画像の読み込みに失敗する例外|Bug|
|PSDNET-541|レイヤーグループの可視性を変更した後の出力が正しくない|Bug|
|PSDNET-516|PSDイメージの読み込み時に例外が発生する: カラーセクション（DropShadowリソース）はRGB用に3つのカラーコンポーネント、CMYK用に4つのカラーコンポーネントを含める必要がある|Bug|
|PSDNET-536|シンプル版のコンストラクタを使用して新しく作成したレイヤーに描画しようとすると例外が発生する|Bug|

## **パブリック API 変更**
# **追加されたAPI:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Underline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Strikethrough
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **削除されたAPI:**
- なし

## **使用例:**
**PSDNET-523. Adobe Illustrator ファイルをPDFに変換**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. 1 つのテキストレイヤーで異なるスタイルをレンダリングする機能を追加**

{{< highlight java >}}

 string sourceFile = "text212.psd";

string ethalonFile = "Ethalon_text212.psd";

string outputFile = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(sourceFile))

{

    TextLayer textLayer = (TextLayer)img.Layers[1];

    IText textData = textLayer.TextData;

    ITextStyle defaultStyle = textData.ProducePortion().Style;

    ITextParagraph defaultParagraph = textData.ProducePortion().Paragraph;

    defaultStyle.FillColor = Color.DimGray;

    defaultStyle.FontSize = 51;

    textData.Items[1].Style.Strikethrough = true;

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Lowercasetext" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Underline = true; // テキストスタイルを編集 "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // テキストスタイルを編集 "2\r"

    newPortions[2].Style.FauxBold = true; // テキストスタイルを編集 "Bold"

    newPortions[3].Style.FauxItalic = true; // テキストスタイルを編集 "Italic\r"

    newPortions[3].Style.BaselineShift = -25; // テキストスタイルを編集 "Italic\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // テキストスタイルを編集 "Lowercasetext"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. AI形式（バージョン 8）のエクスポートをサポート**

{{< highlight java >}}

 // AIファイルをPSDとPNG形式にエクスポートする例

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. PassThroughブレンドモード処理のサポート（レイヤーグループ専用）**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Apple.psd";

string outputFileName = "Output" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "There is not 23rd layer.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "The 23rd layer is not a layer group.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "The 23rd layer name is not 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "AdjustmentGroup layer should have 'pass through' blend mode.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. テキストレイヤーのテキストを更新すると例外が発生する**

{{< highlight java >}}

 // テキストレイヤーのテキストを更新すると例外が発生する

string filePath = "FlipVertical.psd";

string outputPath = "FlipVertical_changed.psd";

var newText = "Test";

using (var image = Image.Load(filePath))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var layers = psdImage.Layers;

    for (var index = layers.Length - 1; index >= 0; index--)

    {

        var layer = layers[index] as TextLayer;

        if (layer == null)

        {

            continue;

        }

        layer.UpdateText(newText);

    }

    var imageOptions = new PsdOptions(psdImage);

    psdImage.Save(outputPath, imageOptions);

}

{{< /highlight >}}

**PSDNET-182. RotateFlip操作後にPSDイメージを保存すると読み込み不可能な破損ファイルが生成される**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// 例外なく実行されるべき

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // 何もしない

}

{{< /highlight >}}

**PSDNET-539. 空のUnicode Alpha Namesリソースを含む画像のロードに失敗する例外**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // ここで例外が発生しないはず

{

    // 何もしない

}

{{< /highlight >}}

**PSDNET-541. レイヤーグループの可視性を変更した後の出力が正しくない**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// レイヤー名を変更し、保存する

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // グループ内のすべてをオフにする

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. PSDイメージの読み込み時に例外が発生する: カラーセクション（DropShadowリソース）はRGB用に3つのカラーコンポーネント、CMYK用に4つのカラーコンポーネントを含める必要がある**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // ここで例外が発生しないはず

{

    // 何もしない

}

{{< /highlight >}}

**PSDNET-536. シンプル版のコンストラクタを使用して新しく作成したレイヤーに描画しようとすると例外が発生する**

{{< highlight java >}}

 string outputFile = "output.psd";

int width = 100;

int height = 100;

using (var image = new PsdImage(width, height))

{

    var layer = new Layer();

    layer.Bottom = height;

    layer.Right = width;

    image.AddLayer(layer);

    Graphics graphic = new Graphics(layer);

    graphic.Clear(Color.Yellow);

    // ペンツールを使用して四角形を描画

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // 青色の固体ブラシで別の四角形を描画

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}

