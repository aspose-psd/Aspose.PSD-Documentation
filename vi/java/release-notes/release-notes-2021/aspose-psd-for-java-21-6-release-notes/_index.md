---
title: Aspose.PSD cho Java 21.6 - Ghi chú phát hành
type: docs
weight: 40
url: /vi/java/aspose-psd-cho-java-21-6-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}} Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) {{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDJAVA-351|Сlipping mask cho một nhóm không được render đúng cách|Lỗi|
|PSDJAVA-352|Masque thông thường hoặc masque vector cho một nhóm layer bị bỏ qua khi render|Lỗi|
|PSDJAVA-353|Hình ảnh PSD với masques lớp vector bị vô hiệu hóa khi lưu sẽ kích hoạt masques vector|Lỗi|
|PSDJAVA-354|Ngoại lệ khi tạo một TextLayer với văn bản dài hơn 255 ký tự|Lỗi|

# **Thay đổi API Công cộng**
# **APIs được thêm:**
- Không có

# **APIs bị gỡ bỏ:**
- Không có

# **Ví dụ về cách sử dụng:**

**PSDJAVA-351. Сlipping mask cho một nhóm không được render đúng cách**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. Masque thông thường hoặc masque vector cho một nhóm layer bị bỏ qua khi render**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. Hình ảnh PSD với masques lớp vector bị vô hiệu hóa khi lưu sẽ kích hoạt masques vector**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. Ngoại lệ khi tạo một TextLayer với văn bản dài hơn 255 ký tự**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}
