---
title: Aspose.PSD cho .NET 21.5 - Ghi chú phát hành
type: docs
weight: 80
url: /vi/net/aspose-psd-cho-net-21-5-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}} 

Trang này chứa ghi chú phát hành cho [Aspose.PSD cho .NET 21.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-758|Hỗ trợ thay đổi kích thước của lớp hình dạng với đường dẫn vector|Tính năng|
|PSDNET-862|Hỗ trợ thay đổi kích thước của lớp hình dạng với đường dẫn vector khi chỉ có một lớp được thay đổi kích thước|Tính năng|
|PSDNET-578|Chuỗi văn bản bị cắt ngắn|Lỗi|

## **Thay đổi API công khai**
# **API Thêm vào:** 
- Không có

# **API Loại bỏ:** 
- Không có

## **Ví dụ sử dụng:**

**PSDNET-578. Chuỗi văn bản bị cắt ngắn**

{{< highlight csharp >}}
            string srcFile = "grinched-regular-font.psd";
            string output = "output_grinched-regular-font.psd.png";

            // Đặt đường dẫn font
            System.Collections.Generic.List<string> fonts = new System.Collections.Generic.List<string>();
            fonts.AddRange(FontSettings.GetDefaultFontsFolders());
            fonts.Add(@"Fonts\");
            FontSettings.SetFontsFolders(fonts.ToArray(), true);

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-758. Hỗ trợ thay đổi kích thước của lớp hình dạng với đường dẫn vector**

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

**PSDNET-862. Hỗ trợ thay đổi kích thước của lớp hình dạng với đường dẫn vector khi chỉ có một lớp được thay đổi kích thước**

{{< highlight csharp >}}
            // Ví dụ này cho thấy cách thay đổi kích thước các lớp với một Vogk và vector path tài nguyên trong hình ảnh PSD
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
