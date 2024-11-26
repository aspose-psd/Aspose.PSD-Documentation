---
title: Aspose.PSD cho .NET 21.6 - Ghi chú Phát hành
type: docs
weight: 70
url: /vi/net/aspose-psd-cho-net-21-6-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}} 

Trang này chứa các ghi chú phát hành cho [Aspose.PSD for .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-546|Мặt nạ cắt cho một nhóm không hiển thị đúng cách|Lỗi|
|PSDNET-547|Mặt nạ thường hoặc vector cho một nhóm lớp bị bỏ qua khi hiển thị|Lỗi|
|PSDNET-647|Hình ảnh PSD với mặt nạ lớp vector bị vô hiệu hóa khi lưu sẽ kích hoạt các mặt nạ vector|Lỗi|
|PSDNET-786|Ngoại lệ khi tạo một lớp TextLayer với văn bản dài hơn 255 ký tự|Lỗi|
|PSDNET-900|Văn bản của lớp Văn bản không thể hiển thị trên Linux|Cải tiến|

## **Thay đổi API công cộng**
# **API Thêm vào:**
- Không có

# **API Bị xóa:**
- Không có

## **Ví dụ về cách sử dụng:**

**PSDNET-546.	Mặt nạ cắt cho một nhóm không hiển thị đúng cách**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547.	Mặt nạ thường hoặc vector cho một nhóm lớp bị bỏ qua khi hiển thị**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647.	Hình ảnh PSD với các mặt nạ lớp vector bị vô hiệu hóa khi lưu sẽ kích hoạt các mặt nạ vector**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786.	Ngoại lệ khi tạo một lớp TextLayer với văn bản dài hơn 255 ký tự**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}
