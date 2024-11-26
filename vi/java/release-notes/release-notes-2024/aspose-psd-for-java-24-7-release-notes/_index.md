---
title: Aspose.PSD cho Java 24.7 - Ghi chú phát hành
type: docs
weight: 40
url: /vi/java/aspose-psd-cho-java-24-7-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}} Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}}

| **Khóa**    | **Tóm tắt**                                                                                      | **Danh mục** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | Ngoại lệ "Image loading failed." khi mở tài liệu AI                                              | Lỗi         |
| PSDJAVA-636 | Văn bản được hiển thị không chính xác trong các tệp PDF đầu ra                                    | Lỗi         |
| PSDJAVA-637 | Sửa lỗi ImageSaveException: Xuất hình ảnh thất bại cho tệp được cung cấp trên Linux             | Lỗi         |
| PSDJAVA-638 | Sửa lỗi tải phông chữ khi sử dụng Aspose.Drawing                                                 | Lỗi         |
| PSDJAVA-639 | 'Phép tính số học đã gây tràn' khi tạo lớp đối tượng thông minh bằng hình ảnh JPEG lớn          | Lỗi         |
| PSDJAVA-640 | Tệp AI không thể chuyển đổi thành tệp JPG                                                      | Lỗi         |

## **Thay đổi trong API công khai**
# **API Thêm vào:**

- Không có

# **API Loại bỏ:**

- Không có

## **Ví dụ sử dụng:**

**PSDJAVA-635. Ngoại lệ "Image loading failed." khi mở tài liệu AI**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. Văn bản được hiển thị không chính xác trong các tệp PDF đầu ra**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. Sửa lỗi ImageSaveException: Xuất hình ảnh thất bại cho tệp được cung cấp trên Linux**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Bed_Roll-Sticker4_1.psd";
    String outputFile = "src/main/resources/output.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        JpegOptions saveOptions = new JpegOptions();
        saveOptions.setQuality(70);
        psdImage.save(outputFile, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-638. Sửa lỗi tải phông chữ khi sử dụng Aspose.Drawing**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- Trước khi cập nhật. Số lượng phông chữ đã cài đặt: " + installedFonts.getFamilies().length);
        System.out.println("- Nền tảng: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- Làm mới bộ nhớ cache phông bằng cách thử lấy tên phông Adobe cho 'Arial': "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- Sau khi cập nhật. Số lượng phông chữ đã cài đặt: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'Phép tính số học đã gây tràn' khi tạo lớp đối tượng thông minh bằng hình ảnh JPEG lớn**

{{< highlight java >}}

    String srcFile = "src/main/resources/source.psd";
    String imageJpg = "src/main/resources/test.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setDataRecoveryMode(DataRecoveryMode.MaximalRecover);
    try (var image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        final FileStream stream = new FileStream(imageJpg, FileMode.Open);
        try {
            var addedLayer = new SmartObjectLayer(stream);
            addedLayer.setName("Test Layer");
            image.addLayer(addedLayer);
        } finally {
            stream.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. Tệp AI không thể chuyển đổi thành tệp JPG**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}
