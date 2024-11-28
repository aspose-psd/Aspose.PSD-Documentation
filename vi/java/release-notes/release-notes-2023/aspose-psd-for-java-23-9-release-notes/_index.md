---
title: Aspose.PSD cho Java 23.9 - Ghi chú Phát hành
type: docs
weight: 40
url: /vi/java/aspose-psd-cho-java-23-9-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}} Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/) {{% /alert %}}

| **Khóa**     | **Tóm tắt**                                                                                                                                      | **Danh mục** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | Thực hiện tạo mặt nạ cho các lớp điều chỉnh mới                                                                          |    Tính năng   |
| PSDJAVA-528 | Thêm hỗ trợ của Các lớp Clipped Layers như tùy chọn nhóm blending                                                                                  |    Tính năng   |
| PSDJAVA-529 | Tập tin PSD với chế độ màu 16 bit không áp dụng mặt nạ cho các lớp điều chỉnh                                                                        |      Lỗi     |
| PSDJAVA-530 | Hiển thị không chính xác dấu ngoặc trong lớp văn bản                                                                                                 |      Lỗi     |
| PSDJAVA-531 | Không thể cập nhật kiểu trong các lớp văn bản                                                                                                        |      Lỗi     |
| PSDJAVA-532 | Sau khi xuất tập tin PSD với CMYK, màu bị đổ vỡ trong tập tin PSD đã xuất                                                                              |      Lỗi     |
| PSDJAVA-533 | Tập tin cụ thể PSB ném ra ngoại lệ "Hình chữ nhật không có khu vực xử lý chung"                                                                       |      Lỗi     |
| PSDJAVA-534 | Tải hình ảnh thất bại. OverflowException: Phép tính số học dẫn đến tràn                                                          |      Lỗi     |

## **Thay đổi API công khai**
# **API Đã Thêm:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **API Đã Xóa:**

- Không có

## **Ví dụ về việc sử dụng:**

**PSDJAVA-527. Thực hiện tạo mặt nạ cho các lớp điều chỉnh mới**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya_BW.psd";
    String dstFile = "src/main/resources/zendeya_BW_out.psd";

    try (PsdImage im = (PsdImage) Image.load(srcFile)) {
        im.addBlackWhiteAdjustmentLayer();

        im.save(dstFile);
    }

    try (PsdImage im = (PsdImage) Image.load(dstFile)) {
        Layer layer = im.getLayers()[1];

        assertAreEqual(5, layer.getChannelsCount());
        assertAreEqual((short) -2, layer.getChannelInformation()[4].getChannelID());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Các đối tượng không bằng nhau.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-528. Thêm hỗ trợ của Các lớp Clipped Layers như tùy chọn nhóm blending**

{{< highlight java >}}
    String sourceFile = "src/main/resources/example_source.psd";
    String outputPsd = "src/main/resources/example_output.psd";
    String outputPng = "src/main/resources/example_output.png";

    try (PsdImage image = (PsdImage)Image.load(sourceFile)) {
        image.getLayers()[1].setBlendClippedElements(false);
        image.save(outputPsd);
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}

**PSDJAVA-529. Tập tin PSD với chế độ màu 16 bit không áp dụng mặt nạ cho các lớp điều chỉnh**

{{< highlight java >}}
	String sourceFile = "src/main/resources/source.psd";
    String outputPng = "src/main/resources/current.png";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}

**PSDJAVA-530. Hiển thị không chính xác dấu ngoặc trong lớp văn bản**

{{< highlight java >}}
    String file = "src/main/resources/file1.psd";
    String output = "src/main/resources/output_1235.png";

    try (PsdImage psdImage = (PsdImage) Image.load(file)) {
        for (Layer layer : psdImage.getLayers()) {
            if (layer instanceof TextLayer) {
                TextLayer textLayer = (TextLayer) layer;
                textLayer.getTextData().updateLayerData();

                PsdOptions imageOptions = new PsdOptions(psdImage);
                psdImage.save(output, imageOptions);
            }
        }
    }
{{< /highlight >}}

**PSDJAVA-531. Không thể cập nhật kiểu trong các lớp văn bản**

{{< highlight java >}}
    String sourceFile = "src/main/resources/Example_FontSize.psd";
    String outputFile = "src/main/resources/output_Example_FontSize.psd";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        TextLayer l1 = (TextLayer) psdImage.getLayers()[4];
        TextLayer l2 = (TextLayer) psdImage.getLayers()[5];

        ITextPortion[] textItems1 = l1.getTextData().producePortions(new String[]{"text1", "text2"},
                l1.getTextData().getItems()[0].getStyle(), l1.getTextData().getItems()[0].getParagraph());

        l1.getTextData().removePortion(0);
        for (ITextPortion item : textItems1) {
            l1.getTextData().addPortion(item);
        }

        ITextPortion[] textItems2 = l2.getTextData().producePortions(new String[]{"text layer 1", "text layer 22"},
                l2.getTextData().getItems()[0].getStyle(), l2.getTextData().getItems()[0].getParagraph());

        for (ITextPortion item : textItems2) {
            l2.getTextData().addPortion(item);
        }

        l1.getTextData().updateLayerData();
        l2.getTextData().updateLayerData();

        psdImage.save(outputFile);
    }
{{< /highlight >}}

**PSDJAVA-532. Sau khi xuất tập tin PSD với CMYK, màu bị đổ vỡ trong tập tin PSD đã xuất**

{{< highlight java >}}
    String sourceFile = "src/main/resources/canyon.psd";
    String outputFilePng = "src/main/resources/output_canyon.png";

    MemoryStream outputStream = new MemoryStream();

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        psdImage.save(outputStream.toOutputStream());
    }

    outputStream.setPosition(0);
    try (PsdImage psdImage = (PsdImage) Image.load(outputStream.toInputStream())) {
        psdImage.save(outputFilePng, new PngOptions());
    }

    outputStream.close();
{{< /highlight >}}

**PSDJAVA-533. Tập tin PSB cụ thể ném ra ngoại lệ "Hình chữ nhật không có khu vực xử lý chung"**

{{< highlight java >}}
    String input = "src/main/resources/1619_src.psb";
    String output = "src/main/resources/1619_output.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage img = (PsdImage) Image.load(input, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setCompressionLevel(9);
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
        img.save(output, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-534. Tải hình ảnh thất bại. OverflowException: Phép tính số học dẫn đến tràn**

{{< highlight java >}}
public static void main(String[] args) {
    String sourceFile = "src/main/resources/9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

    try (PsdImage im = (PsdImage)PsdImage.load(sourceFile))
    {
        Layer layer = im.getLayers()[28];
        GrdmResource grdmResource = (GrdmResource)layer.getResources()[0];

        assertAreEqual("自定", grdmResource.getGradientName());
    }

}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Các đối tượng không bằng nhau.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}
