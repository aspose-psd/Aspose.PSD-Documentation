---
title: Aspose.PSD cho .NET 21.9 - Ghi chú phiên bản
type: docs
weight: 40
url: /vi/net/aspose-psd-cho-net-21-9-release-notes/
---

{{% alert color="primary" %}} 

Trang này chứa các ghi chú phiên bản cho [Aspose.PSD cho .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-574|Làm cho nén RLE mặc định cho việc lưu trữ PSD để tránh kích thước PSD đầu ra lớn|Tính năng|
|PSDNET-747|Hỗ trợ Overlay Pattern Layer Effects với chế độ màu multichannel trong tập tin PSD|Tính năng|
|PSDNET-951|Sau khi tạo nên lớp mới, thuộc tính Resources của nó là null, ngăn cản các thao tác (Thay đổi kích thước ví dụ)|Lỗi|
|PSDNET-955|Không hỗ trợ phương pháp nén ZipWithPrediction cho 8 bit|Lỗi|

## **Thay đổi API Công khai**
# **APIs Đã Thêm:**
- Không có

# **APIs Đã Xóa:**
- Không có

## **Ví dụ về cách sử dụng:**

**PSDNET-574. Làm cho nén RLE mặc định cho việc lưu trữ PSD để tránh kích thước PSD đầu ra lớn**

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

**PSDNET-747. Hỗ trợ Overlay Pattern Layer Effects với chế độ màu multichannel trong tập tin PSD**

{{< highlight csharp >}}
            var fileName = "AllEffects.psd";
            var outputFile = "AllEffects_out.psd";
            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // Không nên ném ngoại lệ
            using (var im = Image.Load(fileName, loadOptions))
            {
                // Không nên ném ngoại lệ
                im.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-951. Sau khi tạo nên lớp mới, thuộc tính Resources của nó là null, ngăn cản các thao tác (Thay đổi kích thước ví dụ)**

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
                    // Màu Đỏ
                    var r = (byte)((pixels[i] >> 16) & 0xff);
                    // Màu Xanh lá
                    var g = (byte)((pixels[i] >> 8) & 0xff);
                    // Màu Xanh dương
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
                #region Thêm Lớp 1

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
                    // Thay đổi màu Trắng thành Trong suốt
                    ReplaceColor(Layer3, Color.White, 256, Color.Transparent);
                    Layer2.DrawImage(new Point(0, 0), Layer3);
                }

                image.Save(outFileName, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. Không hỗ trợ phương pháp nén ZipWithPrediction cho 8 bit**

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
