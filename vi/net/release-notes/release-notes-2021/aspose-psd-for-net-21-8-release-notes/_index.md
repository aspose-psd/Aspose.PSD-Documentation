---
title: Aspose.PSD cho .NET 21.8 - Ghi chú phát hành
type: docs
weight: 50
url: /vi/net/aspose-psd-cho-net-21-8-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}} 

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-698|Hỗ trợ phương pháp Nén ZipWithPrediction|Tính năng|
|PSDNET-663|Khoảng cách văn bản không chính xác trong tập tin PSD được tạo ra|Lỗi|
|PSDNET-685|Ngoại lệ khi lưu tập tin PSD|Lỗi|
|PSDNET-927|Khoảng cách không chính xác giữa dòng và ký tự trong Aspose.PSD khi sử dụng mà không có giấy phép|Lỗi|

## **Thay đổi trong API công cộng**
# **API đã thêm:**
- Không có

# **API đã loại bỏ:**
- Không có

## **Ví dụ về việc sử dụng:**

**PSDNET-663. Khoảng cách văn bản không chính xác trong tập tin PSD được tạo ra**

{{< highlight csharp >}}
            string sourceFileName = "source.psd";
            string outputFileName = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. Ngoại lệ khi lưu tập tin PSD**

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

**PSDNET-698. Hỗ trợ phương pháp Nén ZipWithPrediction**

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

**PSDNET-927. Khoảng cách không chính xác giữa dòng và ký tự trong Aspose.PSD khi sử dụng mà không có giấy phép**

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
