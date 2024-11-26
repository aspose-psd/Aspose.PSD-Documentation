---
title: Aspose.PSD for Java 20.6 - リリースノート
type: docs
weight: 50
url: /ja/java/aspose-psd-for-java-20-6-release-notes/
---

{{% alert color="primary" %}} このページには、[Aspose.PSD for Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) のリリースノートが含まれています。 {{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDJAVA-216|LnkEResource（スマートオブジェクトレイヤーのリソース）のサポート|機能|
|PSDJAVA-219|britResource（明るさ/コントラスト調整レイヤーのリソース）のサポート|機能|
|PSDJAVA-222|DefaultReplacementFont 設定を ImageOptionsBase クラスに移動|強化|
|PSDJAVA-217|調整レイヤーに空の境界を持つマスクがある場合、PSD ファイルのリサイズが正しく機能しない|バグ|
|PSDJAVA-218|RGB モード16ビット/チャンネルの Psd 画像はプレビューのレイヤーのみが更新される|バグ|
|PSDJAVA-220|PSD レイヤーマスクの変更が保存時に破棄される|バグ|
|PSDJAVA-221|空のレイヤーグループにレイヤーグループを追加するとレイヤー順序が正しくない|バグ|
|PSDJAVA-223|複合 LnkE リソースおよび adobeStockLicenseState プロパティを含む特定の PSD ファイルを読み込むと例外が発生する|バグ|
|PSDJAVA-224|AI ファイルを Jpeg2000 フォーマットに保存できない|バグ|
|PSDJAVA-225|PassThrough ブレンディングモードを持たないレイヤーグループはレンダリングされない|バグ|
|PSDJAVA-226|特定の Psd ファイルをイメージに変換しようとすると NullReference 例外が発生する|バグ|
|PSDJAVA-227|特定の Psd ファイルを開こうとして Overflow 例外が発生する|バグ|

# **パブリック API 変更**
# **追加された API:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFullPath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getRelativePath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setAdobeStockId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementRef(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileSize(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFullPath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setRelativePath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetLockedState
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetModTime
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getChildDocId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileCreator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.hasFileOpenDescriptor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.isLibraryLink
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetLockedState(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetModTime(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setChildDocId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileCreator(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileOpenDescriptor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileType(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setLibraryLink(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setUniqueId(java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getDataSourceCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.isEmpty
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.get_Item(int)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSourceType
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource
## **削除された API:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)
# **使用例:**

**PSDJAVA-216: LnkEResource（スマートオブジェクトレイヤーのリソース）のサポート**

{{< highlight java >}}

 // PSD にさまざまなタイプのアセット（ラスター画像、CC ライブラリ）をリンクする例です。

 // また、LnkeResource の API が考慮されています。

 // ローカルスコープ内にメソッドを保持するクラス

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("ExampleOfLnkEResourceSupport works incorrectly.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // Photoshop Psd LnkE のプロパティを取得および設定する例

    void exampleOfLnkEResourceSupport(

            String fileName,

            int length,

            int length2,

            int length3,

            int length4,

            String fullPath,

            String date,

            double assetModTime,

            String childDocId,

            boolean locked,

            String uid,

            String name,

            String originalFileName,

            String fileType,

            long size)

    {

        String outputPath = "out_" + fileName;

        // 事前に定義された PSD をロード

        PsdImage image = (PsdImage)Image.load(fileName);

        try

        {

            // グローバルアセットの中から LnkeResource を検索

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // LnkeResource プロパティを検証

                    assertAreEqual(lnkeResource.getLength(), length);

                    assertAreEqual(lnkeResource.get_Item(0).getUniqueId(), UUID.fromString(uid));

                    assertAreEqual(lnkeResource.get_Item(0).getFullPath(), fullPath);

                    assertAreEqual(new SimpleDateFormat("MM/dd/yyyy HH:mm:ss").format(lnkeResource.get_Item(0).getDate()), date);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetModTime(), assetModTime);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetLockedState(), locked);

                    assertAreEqual(lnkeResource.get_Item(0).getFileName(), name);

                    ...

                    assertAreEqual(lnkeResource.get_Item(0).getFileType().trim(), fileType);

                    assertAreEqual(lnkeResource.get_Item(0).getFileCreator().trim(), "");

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalFileName(), originalFileName);

                    ...

                    break;

                }

            }

            // LnkeResource がサポートされていることを確認

            assertIsTrue(lnkeResource != null);

            // 読み込んだ PSD のコピーを保存

            image.save(outputPath, new PsdOptions(image));

        }

        finally

        {

            image.dispose();

        }

        ...

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Photoshop Psd LnkE リソースに関するプロパティの取得および設定の例

$.exampleOfLnkEResourceSupport(...

// 別のリソースを含む画像を拡大する例

...

{{< /highlight >}}

...

**PSDJAVA-221: 空のレイヤーグループにレイヤーグループを追加するとレイヤー順序が正しくない**

{{< highlight java >}}

 // レイヤーグループを PSD にプログラムで追加する方法を示す例です。

String dstPsdPath = "output.psd";

// サイズが 1x1 ピクセルのイメージを作成

PsdImage psdImage = new PsdImage(1, 1);

try

{

    // 親のレイヤーグループを追加します（"true" は開始時にレイヤーグループを開くことを意味します）

    LayerGroup group1 = psdImage.addLayerGroup("Group 1", 0, true);

    // ネストされたレイヤーグループを追加

    LayerGroup group2 = group1.addLayerGroup("Group 2", 0);

    if (group1.getLayers().length != 2)

    {

        throw new RuntimeException("Group 1 must contain two layers of Group 2.");

    }

...

{{< /highlight >}}

...

**PSDJAVA-221: 空のレイヤーグループにレイヤーグループを追加するとレイヤー順序が正しくない**

{{< highlight java >}}

...

    // ネストされたレイヤーグループを追加

    LayerGroup group2 = group1.addLayerGroup("Group 2", 0);

    if (group1.getLayers().length != 2)

    {

        throw new RuntimeException("Group 1 must contain two layers of Group 2.");

    }

    // 作成したレイヤーグループを保存

    psdImage.save(dstPsdPath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-223: 複合 LnkE リソースおよび adobeStockLicenseState プロパティを含む特定の PSD ファイルを読み込むと例外が発生する**

{{< highlight java >}}

...

    // グローバルレイヤー リソースを持つ事前に定義された PSD をロード

    PsdImage image = (PsdImage)Image.load(srcPsdPath);

    try

    {

        // LnkeResource を検索

        LnkeResource lnkeResource = null;

        for (LayerResource resource : image.getGlobalLayerResources())

        {

            if (resource instanceof LnkeResource)

            {

                lnkeResource = (LnkeResource)resource;

                // プロパティが正しく読み取られていることを確認

                assertAreEqual(lnkeResource.getDataSourceCount(), 8);

                assertAreEqual(lnkeResource.getLength(), length);

                assertAreEqual(lnkeResource.isEmpty(), false);

                for (int i = 0; i < lnkeResource.getDataSourceCount(); i++)

                {

                    // データソースのプロパティを確認

                    LiFeDataSource liFeSource = lnkeResource.get_Item(i);

                    ...

                    assertAreEqual(liFeSource.getAdobeStockLicenseState(), expected[10]);

                    assertAreEqual(liFeSource.hasFileOpenDescriptor(), expected[11]);

                    ...

                    if (liFeSource.hasFileOpenDescriptor())

                    {

                        liFeSource.setCompId(Integer.MAX_VALUE);

                    }

                    liFeSource.setFullPath("file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png");

                    liFeSource.setFileName("rgb8_2x23.png");

                    ...

                }

                assertAreEqual(lnkeResource.getLength(), length2);

                break;

            }

        }

        // LnkeResource が見つかり、したがってサポートされていることを確認

        assertIsTrue(lnkeResource != null);

    }

    finally

    {

        image.dispose();

    }

...

{{< /highlight >}}