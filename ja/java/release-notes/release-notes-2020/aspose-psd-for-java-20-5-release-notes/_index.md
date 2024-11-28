---
title: Aspose.PSD for Java 20.5 - リリースノート
type: docs
weight: 40
url: /ja/java/aspose-psd-for-java-20-5-release-notes/
---

{{% alert color="primary" %}} このページには、[Aspose.PSD for Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) のリリースノートが含まれています。 {{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDJAVA-188|文書変換進行状況のサポート|機能|
|PSDJAVA-197|16ビットチャネルごとのグレースケールカラーモードPSDイメージの保存のサポート|機能|
|PSDJAVA-198|Nvrt リソース（反転調整レイヤー リソース）のサポート|機能|
|PSDJAVA-200|レイヤーグループ向けのレイヤーマスクのサポート|機能|
|PSDJAVA-195|グレースケールカラーモードのPSDイメージを16ビットチャネルから16ビットチャネルRGB PSD形式に保存する際のバグ修正|バグ|
|PSDJAVA-196|グレースケールカラーモードのPSDイメージを16ビットチャネルから8ビットチャネルグレースケールPSD形式に保存する際のバグ修正|バグ|
|PSDJAVA-199|右から左に向かう言語用の ITextPortion を介したテキストの配置が機能しない。出力ファイルが破損する.|バグ|
|PSDJAVA-201|LABカラーおよび8ビット/チャネルで特定のPsdファイルを開こうとする際の例外|バグ|
# **パブリック API 変更**
# **追加された API:**
- なし
## **削除された API:**
- なし
# **使用例:**

**PSDJAVA-188. 文書変換進行状況のサポート**

{{< highlight java >}}

 // ロードおよび保存操作の進行ハンドラの使用例。

// プログラムは進行イベントを発生させるためにさまざまな保存オプションを使用します。

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// 進行情報をコンソールに出力する進行ハンドラを作成

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s of %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Apple.psd の読み込み ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// ローディング進行状況を表示するために進行ハンドラをバインド

loadOptions.setProgressEventHandler(localProgressEventHandler);

// 特定のローディングオプションを使用してPSDをロード

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Apple.psd を PNG 形式で保存 ----------");

    PngOptions pngOptions = new PngOptions();

    // 出力イメージをカラー化し、透明度を持たないようにする

    pngOptions.setColorType(PngColorType.Truecolor);

    // 保存進行状況を表示するために進行ハンドラをバインド

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // 特定の特性でPSDをPNGに変換

    image.save(outputStream, pngOptions);

    System.out.println("---------- Apple.psd を PSD 形式で保存 ----------");

    PsdOptions psdOptions = new PsdOptions();

    // 出力PSDをカラー化する

    psdOptions.setColorMode(ColorModes.Rgb);

    // 各色（赤、緑、青）と合成チャネルに対してチャネルを設定

    psdOptions.setChannelsCount((short)4);

    // 保存進行状況を表示するために進行ハンドラをバインド

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // 特定の特性でPSDのコピーを保存

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. 16ビットチャネルごとのグレースケールカラーモードPSDイメージの保存のサポート**

{{< highlight java >}}

 // 特定のレイヤーに対して異なる色モード、チャネルビット数、チャネル数、圧縮の組み合わせを適用する例。

// メソッドをローカルスコープからアクセス可能にする

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String file,

            short colorMode,

            short channelBitsCount,

            short channelsCount,

            short compression,

            int layerNumber)

    {

        String filePath = file + ".psd";

        String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +

                channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);

        String exportPath = file + postfix + ".psd";

        String pngExportPath = file + postfix + ".png";

        // 16ビットグレースケールPSDを事前にロード

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // レイヤーの周囲に灰色の内側の境界線を描画 

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // 特定の特性でPSDのコピーを保存

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(colorMode);

            psdOptions.setChannelBitsCount(channelBitsCount);

            psdOptions.setChannelsCount(channelsCount);

            psdOptions.setCompressionMethod(compression);

            image.save(exportPath, psdOptions);

        }

        finally

        {

            image.dispose();

        }

        // 保存されたPSDをロード

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // 保存されたPSDをグレースケールPNGイメージに変換

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // ここでは例外が発生しないはず

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. Nvrt リソース（反転調整レイヤー リソース）のサポート**

{{< highlight java >}}

 // 反転調整レイヤーの NvrtResource を検索する例。

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// 反転調整レイヤーを含む事前定義のPSDをロード

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // 反転調整レイヤーのリソースを見つけようとする

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // NvrtResource を見つけた

                    nvrtResource = (NvrtResource)layerResource;

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-200. レイヤーグループ向けのレイヤーマスクのサポート**

{{< highlight java >}}

 // レイヤーグループのためのレイヤーマスクのサポートの例。プログラムは例外をスローせずにPSDを異なる出力形式にロードおよび保存します。

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// レイヤーグループを含む事前定義のPSDをロード

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // ロードされたPSDをPNGに変換

    input.save(outputPng, new PngOptions());

    // PSDのコピーを保存

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. グレースケールカラーモードのPSDイメージを16ビットチャネルから16ビットチャネルRGB PSD形式に保存する際のバグ修正**

{{< highlight java >}}

 // 16ビットグレースケールPSDを16ビットRGBに変換し、その後16ビットグレースケールに戻す例。

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// 16ビットグレースケールPSDをロード

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // レイヤーの周囲に灰色の内側の境界線を描画 

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // カラーモードをRGBに変更したPSDのコピーを保存

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Rgb);

    psdOptions.setChannelBitsCount((short)16);

    psdOptions.setChannelsCount((short)4);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// 保存されたPSDをロード

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // 保存されたPSDをグレースケールPNGイメージに変換

    image1.save(pngExportPath, pngOptions); // ここでは例外が発生しないはず

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. グレースケールカラーモードのPSDイメージを16ビットチャネルから8ビットチャネルグレースケールPSD形式に保存する際のバグ修正**

{{< highlight java >}}

 // 16ビットグレースケールPSDを8ビットグレースケールに変換し、その後8ビットグレースケールラスターイメージにします。

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// 16ビットグレースケールPSDをロード

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // レイヤーの周囲に灰色の内側の境界線を描画 

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // チャネルカウントを8ビットに変更したPSDのコピーを保存

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Grayscale);

    psdOptions.setChannelBitsCount((short)8);

    psdOptions.setChannelsCount((short)2);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// 保存されたPSDをロード

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // 保存されたPSDをグレースケールPNGイメージに変換

    image1.save(pngExportPath, pngOptions); // ここでは例外が発生しないはず

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. 右から左に進む言語の ITextPortion を介したテキスト配置が機能しない問題**

{{< highlight java >}}

 // ITextPortion を介してRTLテキストレイヤーを配置する例。 プログラムはロードされたPSD内の既存のRTLテキストレイヤーを変更し、変更されたドキュメントのコピーを保存します。

String sourceFileName = "bidi.psd";

String outputFileName = "bidiOutput.psd";

// RTLテキストレイヤーを含む事前定義のPSDをロード

PsdImage image = (PsdImage)Image.load(sourceFileName);

try

{

    // レイヤーからテキストポーションを取