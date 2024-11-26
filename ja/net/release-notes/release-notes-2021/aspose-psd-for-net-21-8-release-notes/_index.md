---
title: Aspose.PSD for .NET 21.8 - リリースノート
type: ドキュメント
weight: 50
url: /ja/net/aspose-psd-for-net-21-8-release-notes/
---

{{% alert color="primary" %}} 

このページには、[Aspose.PSD for .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-698|ZipWithPrediction の圧縮メソッドのサポート|機能|
|PSDNET-663|生成されたPSDのテキスト間のスペースが正しくない|バグ|
|PSDNET-685|PSDの保存時に例外が発生する|バグ|
|PSDNET-927|Aspose.PSDでライセンスなしで使用すると行とシンボル間の間隔が不正確|バグ|

## **公開APIの変更**
# **追加されたAPI:**
- なし

# **削除されたAPI:**
- なし

## **使用例:**

**PSDNET-663. 生成されたPSDのテキスト間のスペースが正しくない**

{{< highlight csharp >}}
            string sourceFileName = "source.psd";
            string outputFileName = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. PSDの保存時に例外が発生する**

{{< highlight csharp >}}
            string sourceFileName = "File.psd";
            string outputFileName = "File2.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                var layer1 = (TextLayer)image.Layers[1];
                layer1.TextData.UpdateLayerData();

                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-698. ZipWithPrediction の圧縮メソッドのサポート**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";

            string outputPng = "output.png";
            string outputRaw = "out_Raw.psd";
            string outputZip = "out_Zip.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(outputPng, new PngOptions());

                image.Save(outputRaw, new PsdOptions() { CompressionMethod = CompressionMethod.Raw });
                image.Save(outputZip, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. Aspose.PSDでライセンスなしで使用すると行とシンボル間の間隔が不正確**

{{< highlight csharp >}}
            bool[] licenseStates = new bool[] { false, true };
            for (int i = 0; i < licenseStates.Length; i++)
            {
                bool testLicense = licenseStates[i];
                if (testLicense)
                {
                    License license = new License();
                    license.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string sourceFile = "psdnetTest927.psd";
                string outputFile = "out_" + testLicense.ToString() + "_psdnetTest927.png";

                using (var image = (PsdImage)Image.Load(sourceFile))
                {
                    image.Save(outputFile, new PngOptions());
                }
            }
{{< /highlight >}}
