---
title: Aspose.PSD for .NET 21.12 - リリースノート
type: docs
weight: 10
url: /ja/net/aspose-psd-for-net-21-12-release-notes/
---

{{% alert color="primary" %}} 

このページには、[Aspose.PSD for .NET 21.12](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-997|フォントをプログラムで制限する機能を追加|機能|
|PSDNET-785|Aspose.PSD 20.10: PSD の読み込みに失敗|不具合|
|PSDNET-812|PSD の読み込み時の ImageLoad 例外|不具合|
|PSDNET-870|サポートされていない CompressionMethod を持つ PSD レイヤーを読み込む際の ImageLoad 例外|不具合|
|PSDNET-918|Aspose.PSD 21.6: PSD ファイルに対してサポートされていない圧縮メソッド|不具合|
|PSDNET-984|マスクを持つベクターパスの正しくない保存|不具合|
|PSDNET-1001|特定のファイルの TextPortion における不正なフォント|不具合|
|PSDNET-1031|画像の読み込み時にサポートされていない圧縮メソッドの例外|不具合|
|PSDNET-1033|特定のファイルの保存時に範囲外エラー|不具合|
|PSDNET-1036|ファイル読み込みエラーを回避するための PathStructure のサポートを追加|不具合|

## **パブリック API 変更**
# **追加された API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Prefix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Path
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.StructureKey
- M:Aspose.PSD.FontSettings.SetAllowedFonts(System.String[])
- M:Aspose.PSD.FontSettings.IsFontAllowed(System.String)
- M:Aspose.PSD.FontSettings.GetReplacementFont(System.String)
- M:Aspose.PSD.FontSettings.GetFontReplacements(System.String)
- M:Aspose.PSD.FontSettings.SetFontReplacements(System.String,System.String[])
- M:Aspose.PSD.FontSettings.ClearFontReplacements

# **削除された API:**
- なし

## **使用例:**

**PSDNET-785. Aspose.PSD 20.10: PSD の読み込みに失敗**

{{< highlight csharp >}}
            string src = "ShimadzuLetterhead100.psd";
            string output = "output.psd";
            using (var img = (PsdImage)Image.Load(src, new PsdLoadOptions() { ReadOnlyMode = true }))
            {
                img.Save(output);
            }
{{< /highlight >}}

**PSDNET-812. PSD の読み込み時の ImageLoad 例外**

{{< highlight csharp >}}
            string src = "5-MX10600_Amazon_DEVICES_2_1000x1000.psd";
            string output = "output.psd";
            using (var img = (PsdImage)Image.Load(src))
            {
                img.Save(output);
            }
{{< /highlight >}}

**PSDNET-870. サポートされていない CompressionMethod を持つ PSD レイヤーを読み込む際の ImageLoad 例外**

{{< highlight csharp >}}
            string srcFile = "sourceFile.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-918. Aspose.PSD 21.6: PSD ファイルに対してサポートされていない圧縮メソッド**

{{< highlight csharp >}}
            string srcFile = "Fb-blue-jury (1).psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-984. マスクを持つベクターパスの正しくない保存**

{{< highlight csharp >}}
            string srcFile = "PsdConvertToPngExample.psd";
            string outputFilePng = "output.png";

            using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                psdImage.Save(
                    outputFilePng,
                    new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha, Progressive = true, CompressionLevel = 9 });
            }
{{< /highlight >}}

**PSDNET-997. フォントをプログラムで制限する機能を追加**

{{< highlight csharp >}}
            string srcFile = "fonts_com_updated.psd";
            string output = "etalon_fonts_com_updated.psd.png";

            try
            {
                var fontList = new string[] { "Courier New", "Webdings", "Bookman Old Style" };
                FontSettings.SetAllowedFonts(fontList);

                var myriadReplacement = new string[] { "Courier New", "Webdings", "Bookman Old Style" };
                var calibriReplacement = new string[] { "Webdings", "Courier New", "Bookman Old Style" };
                var arialReplacement = new string[] { "Bookman Old Style", "Courier New", "Webdings" };
                var timesReplacement = new string[] { "Arial", "NotExistedFont", "Courier New" };

                FontSettings.SetFontReplacements("MyriadPro-Regular", myriadReplacement);
                FontSettings.SetFontReplacements("Calibri", calibriReplacement);
                FontSettings.SetFontReplacements("Arial", arialReplacement);
                FontSettings.SetFontReplacements("Times New Roman", timesReplacement);

                using (PsdImage image = (PsdImage)Image.Load(srcFile))
                {
                    image.Save(output, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            } 
            finally
            {
                FontSettings.SetAllowedFonts(null);
                FontSettings.ClearFontReplacements();
            }
{{< /highlight >}}

**PSDNET-1001. 特定のファイルの TextPortion における不正なフォント**

{{< highlight csharp >}}
            string srcFile = "fonts_com.psd";
            string output = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                var tl = (TextLayer)image.Layers[1];
                var fontName = tl.TextData.Items[0].Style.FontName;
                if (fontName != "MyriadPro-Regular")
                {
                    throw new Exception("不正なフォント");
                }

                // Myriad Pro を取得するはずですが、AdobeInvisFont が見えます
                image.Save(output, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-1031. 画像の読み込み時にサポートされていない圧縮メソッドの例外**

{{< highlight csharp >}}
            string srcFile = "shirt-error.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-1033. 特定のファイルの保存時に範囲外エラー**

{{< highlight csharp >}}
            string srcFile = "237708.psd";
            string output = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1036. ファイル読み込みエラーを回避するための PathStructure のサポートを追加**

{{< highlight csharp >}}
            string srcFile = "shirt-color.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}
