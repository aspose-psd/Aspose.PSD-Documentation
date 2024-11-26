---
title: Aspose.PSD for .NET 21.5 - リリースノート
type: docs
weight: 80
url: /ja/net/aspose-psd-for-net-21-5-release-notes/
---

{{% alert color="primary" %}} 

このページには、[Aspose.PSD for .NET 21.5](https://www.nuget.org/packages/Aspose.PSD/)のリリースノートが含まれています。

{{% /alert %}} 

|**キー**|**概要**|カテゴリ|
| :- | :- | :- |
|PSDNET-758|ベクトルパスを持つ形状レイヤーのリサイズサポート|機能|
|PSDNET-862|レイヤーがリサイズされたときにのみ、ベクトルパスを持つ形状レイヤーのリサイズをサポート|機能|
|PSDNET-578|切り捨てられたテキスト文字列|バグ|

## **パブリック API 変更**
# **追加された API:**
- なし

# **削除された API:**
- なし

## **使用例:**

**PSDNET-578. 切り捨てられたテキスト文字列**

{{< highlight csharp >}}
            string srcFile = "grinched-regular-font.psd";
            string output = "output_grinched-regular-font.psd.png";

            // フォントパスを設定
            System.Collections.Generic.List<string> fonts = new System.Collections.Generic.List<string>();
            fonts.AddRange(FontSettings.GetDefaultFontsFolders());
            fonts.Add(@"Fonts\");
            FontSettings.SetFontsFolders(fonts.ToArray(), true);

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-758. ベクトルパスを持つ形状レイヤーのリサイズサポート**

{{< highlight csharp >}}
            string sourceFileName = "vectorShapes.psd";
            string outputFileName = "out_vectorShapes.psd";
            string dataDir = "PSDNET758_1";
            string sourcePath = Path.Combine(dataDir, sourceFileName);
            string outputPath = Path.Combine(dataDir, outputFileName);
            using (var psdImage = (PsdImage)Image.Load(sourcePath))
            {
                foreach (var layer in psdImage.Layers)
                {
                    layer.Resize(layer.Width * 5 / 4, layer.Height / 2);
                }

                psdImage.Save(outputPath);
                psdImage.Save(Path.ChangeExtension(outputPath, ".png"), new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-862. レイヤーがリサイズされたときにのみ、ベクトルパスを持つ形状レイヤーのリサイズをサポート**

{{< highlight csharp >}}
            // この例では、PSD イメージ内の図形とベクトルパスリソースをリサイズする方法を示しています
            float scaleX = 0.45f;
            float scaleY = 1.60f;
            string dataDir = "PSDNET862_1";
            string sourceFileName = Path.Combine(dataDir, "vectorShapes.psd");
            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                for (int layerIndex = 1; layerIndex < image.Layers.Length; layerIndex++, scaleX += 0.25f, scaleY -= 0.25f)
                {
                    var layer = image.Layers[layerIndex];
                    var newWidth = (int)Math.Round(layer.Width * scaleX);
                    var newHeight = (int)Math.Round(layer.Height * scaleY);
                    layer.Resize(newWidth, newHeight);

                    Thread.CurrentThread.CurrentCulture = CultureInfo.CreateSpecificCulture("en-GB");
                    string outputName = string.Format("resized_{0}_{1}_{2}", layerIndex, scaleX, scaleY);
                    string outputPath = Path.Combine(dataDir, outputName + ".psd");
                    string outputPngPath = Path.Combine(dataDir, outputName + ".png");
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}
