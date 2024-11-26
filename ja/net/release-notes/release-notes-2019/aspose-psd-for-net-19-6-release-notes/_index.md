---
title: Aspose.PSD for .NET 19.6 - リリースノート
type: ドキュメント
weight: 70
url: /ja/net/aspose-psd-for-net-19-6-release-notes/
---

{{% alert color="primary" %}} 

このページには、[Aspose.PSD for .NET 19.6](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-127|PSDファイルをPSBに変換およびその逆変換する機能|機能|
|PSDNET-154|Aspose.Imaging 19.5のソースをAspose.PSDに移植|強化|
|PSDNET-155|Aspose.PSDに関連するパブリックAPIのクリーンアップ|強化|
|PSDNET-159|IsLicensedプロパティを削除|強化|
|PSDNET-102|PSBをJPGに変換するとハングが発生|バグ|
|PSDNET-150|Photoshopで編集すると、新しく追加されたテキストレイヤーの位置がシフトされる|バグ|

## **パブリックAPIの変更**
# **追加されたAPI:**
- T:Aspose.PSD.FileFormats.Psd.FileFormatVersion
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.FileFormatVersion
- F:Aspose.PSD.FileFormat.Cdr
- F:Aspose.PSD.FileFormat.Cmx
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResource.PsbResourceSignature
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LayerLockType.LockAll
- P:Aspose.PSD.Image.BufferSizeHint
- P:Aspose.PSD.ImageOptions.JpegOptions.ResolutionUnit
- P:Aspose.PSD.ImageOptions.VectorRasterizationOptions.TextRenderingHint
- M:Aspose.PSD.ImageOptions.VectorRasterizationOptions.CopyTo(Aspose.PSD.ImageOptions.VectorRasterizationOptions)
- P:Aspose.PSD.LoadOptions.BufferSizeHint
- T:Aspose.PSD.MemoryManagement.Configuration
- P:Aspose.PSD.MemoryManagement.Configuration.BufferSizeHint
- T:Aspose.PSD.ResolutionUnit
- F:Aspose.PSD.ResolutionUnit.None
- F:Aspose.PSD.ResolutionUnit.Inch
- F:Aspose.PSD.ResolutionUnit.Cm
# **削除されたAPI:**
- M:Aspose.PSD.Blend.op_Equality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.Blend.op_Inequality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.ColorBlend.op_Equality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- M:Aspose.PSD.ColorBlend.op_Inequality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- T:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader
- M:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.#ctor
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.HeaderSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapWidth
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapHeight
(以下省略)```java
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapCoreHeaderSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.Os22XBitmapHeaderSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.Os22XBitmapHeaderFullSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV2
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV3
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV4
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV5
(Tiff関連APIの削除と追加されたAPIの一部は省略)

## **使用例:**
**PSDNET-127. PSDファイルをPSBに変換およびその逆変換する機能**

{{< highlight java >}}

 // PSDファイルをPSBに変換およびその逆変換する機能

            string sourceFilePathPsb = "2layers.psb";

            string outputFilePathPsd = "ConvertFromPsb.psd";

            using (Image img = Image.Load(sourceFilePathPsb))

            {

                var options = new PsdOptions((PsdImage)img) { FileFormatVersion = FileFormatVersion.Psd };

                img.Save(outputFilePathPsd, options);

            }

            string sourceFilePathPsd = "2layers.psd";

            string outputFilePathPsb = "ConvertFromPsd.psb";

            using (Image img = Image.Load(sourceFilePathPsd))

            {

                var options = new PsdOptions((PsdImage)img) { FileFormatVersion = FileFormatVersion.Psb };

                img.Save(outputFilePathPsb, options);

            }

{{< /highlight >}}

**PSDNET-102. PSBをJPGに変換するとハングが発生**

{{< highlight java >}}

  // PSBをJPGに変換するとハングが発生          

            string[] sourceFileNames = new string[] { 

                // レイヤーを持つテストファイル

                "Little",

                "Simple",

                // レイヤーを持たないテストファイル

                "psb",

                "psb3"

            };

            var options = new PsdLoadOptions();

            foreach (var fileName in sourceFileNames)

            {

                var sourceFileName = fileName + ".psb";

                using (PsdImage image = (PsdImage)Image.Load(sourceFileName, options))

                {

                    // すべてのjpegファイルとpsdファイルは読み込み可能である必要があります

                    image.Save(fileName + "_output.jpg", new JpegOptions() { Quality = 95 });

                    image.Save(fileName + "_output.psb");

                }

            }             

{{< /highlight >}}

**PSDNET-150: Photoshopで編集すると、新しく追加されたテキストレイヤーの位置がシフトされる**

{{< highlight java >}}

             // Photoshopで編集すると、新しく追加されたテキストレイヤーの位置がシフトされる

    string sourceFileName = "OneLayer.psd";

    string exportPath = "OneLayer_Edited.psd";

    int leftPos = 99;

    int topPos = 47;

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

        im.AddTextLayer("Some text", new Rectangle(leftPos, topPos, 99, 47));

        TextLayer textLayer = (TextLayer)im.Layers[1];

        if (textLayer.Left != leftPos || textLayer.Top != topPos) 

        {

            throw new Exception("Was created incorrect Text Layer");

        }

        // パブリックAPIでTransform Matrixをテストすることはできませんが、

        // Photoshopでテキストレイヤーを編集すると、作成した境界線を受け取るはずです。

        im.Save(exportPath);

    }

{{< /highlight >}}
```