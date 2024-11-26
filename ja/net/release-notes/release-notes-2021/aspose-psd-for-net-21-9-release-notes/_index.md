---
title: Aspose.PSD for .NET 21.9 - リリースノート
type: docs
weight: 40
url: /ja/net/aspose-psd-for-net-21-9-release-notes/
---

{{% alert color="primary" %}} 

このページには、[Aspose.PSD for .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが記載されています。

{{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-574|PSD 保存のために RLE 圧縮をデフォルトに設定して、出力 PSD を大幅に削減する|機能|
|PSDNET-747|PSD ファイル内の多チャンネルカラーモードでオーバーレイパターンレイヤーエフェクトをサポートする|機能|
|PSDNET-951|新しいレイヤーを作成した後、そのリソースプロパティが null であるため、操作を防ぐ（例：リサイズ）|バグ|
|PSDNET-955|8ビットに対する ZipWithPrediction 圧縮メソッドのサポートがされていない|バグ|

## **パブリック API の変更**
# **追加された API:**
- なし

# **削除された API:**
- なし

## **使用例:**

**PSDNET-574. PSD 保存のために RLE 圧縮をデフォルトに設定して、出力 PSD を大幅に削減する**

{{< highlight csharp >}}
            string inputFilePath = "file.psd";
            string output1 = "output_original.psd";
            string output2 = "output_psdOptions.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(output1);
                image.Save(output2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. PSD ファイル内の多チャンネルカラーモードでオーバーレイパターンレイヤーエフェクトをサポートする**

{{< highlight csharp >}}
            var fileName = "AllEffects.psd";
            var outputFile = "AllEffects_out.psd";
            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // 例外がスローされないはず
            using (var im = Image.Load(fileName, loadOptions))
            {
                // 例外がスローされないはず
                im.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-951. 新しいレイヤーを作成した後、そのリソースプロパティが null であるため、操作を防ぐ（例：リサイズ）**

{{< highlight csharp >}}
            string PSDFile = "Layer1.psd";
            string layer1File = "Layer2.png";
            string layer2File = "Layer3.png";
            string outFileName = "finaloutput.psd";

            void ReplaceColor(RasterImage image, Color oldColor, int diff, Color newColor)
            {
                var pixels = image.LoadArgb32Pixels(image.Bounds);
                var length = pixels.Length;

                var oldR = oldColor.R;
                var oldG = oldColor.G;
                var oldB = oldColor.B;
                var newColorValue = newColor.ToArgb();

                for (int i = 0; i < length; i++)
                {
                    // 赤
                    var r = (byte)((pixels[i] >> 16) & 0xff);
                    // 緑
                    var g = (byte)((pixels[i] >> 8) & 0xff);
                    // 青
                    var b = (byte)(pixels[i] & 0xff);

                    int actualDiff = Math.Abs(r - oldR) + Math.Abs(g - oldG) + Math.Abs(b - oldB);

                    if (actualDiff <= diff)
                    {
                        pixels[i] = newColorValue;
                    }
                }

                image.SaveArgb32Pixels(image.Bounds, pixels);
            }

            Layer Layer2 = null;
            Layer Layer3 = null;
            using (PsdImage image = (PsdImage)Image.Load(PSDFile))
            {
                #region レイヤー 1 の追加

                using (var stream = new FileStream(layer1File, FileMode.Open))
                {
                    Layer2 = new Layer(stream);

                    Layer2.Resize(image.Width, image.Height);
                    var width = Layer2.Width;
                    var height = Layer2.Height;

                    Layer2.Left = 675;
                    Layer2.Top = 0;

                    Layer2.Right = Layer2.Left + width;
                    Layer2.Bottom = Layer2.Top + height;

                    image.AddLayer(Layer2);
                }

                #endregion

                using (var stream = new FileStream(layer2File, FileMode.Open))
                {
                    Layer3 = new Layer(stream);
                    // 白色を透明に置換
                    ReplaceColor(Layer3, Color.White, 256, Color.Transparent);
                    Layer2.DrawImage(new Point(0, 0), Layer3);
                }

                image.Save(outFileName, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. 8ビット用の Compression methods ZipWithPrediction がサポートされていない**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";
            string outputZip8 = "out_Zip8bit.psd";
            string outputZip16 = "out_Zip16bit.psd";

            using (PsdImage image = (PsdImage)Image.Load(inputFilePath))
            {
                image.Save(outputZip8, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 8 });
                image.Save(outputZip16, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 16 });
            }
{{< /highlight >}}
