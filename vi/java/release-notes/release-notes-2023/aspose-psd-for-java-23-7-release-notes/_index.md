---
title: Aspose.PSD cho Java 23.7 - Ghi chú phát hành
type: docs
weight: 40
url: /vi/java/aspose-psd-cho-java-23-7-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}} Trang này chứa ghi chú phát hành cho [Aspose.PSD cho Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **Khóa**     | **Tóm tắt**                                                                                                                                      | **Danh mục** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | Thêm khả năng xuất mỗi lớp của Tệp PSD sang Tệp Gif hoạt hình                                        | Tính năng |
| PSDJAVA-503 | Gán thuộc tính Fill của lớp Hình dạng từ nguồn tài nguyên vscg                                                       | Tính năng |
| PSDJAVA-504 | Thêm các loại warp mới (arc & arch)                                                                           | Tính năng |
| PSDJAVA-505 | Thay đổi ứng dụng lưu Tệp PSD thành Aspose.PSD nếu thuộc tính UpdateMetadata được đặt là true       | Tính năng |
| PSDJAVA-510 | Tăng diện tích tính toán của hình ảnh warp                                                                    | Tính năng |
| PSDJAVA-511 | Lớp điều chỉnh đen và trắng xử lý độ trong suốt không chính xác                                           | Lỗi     |
| PSDJAVA-512 | SmartObject ReplaceContents (khi tùy chọn AllowWarpRepaint được kích hoạt) bị lỗi sau 2 phút tính toán | Lỗi     |
| PSDJAVA-513 | Thêm khả năng lấy vị trí Thực sự Bên trái và Bên trên của LayerGroup                                    | Lỗi     |
| PSDJAVA-514 | Thay đổi kích thước của lớp hoạt động không chính xác khi tệp psd có VogkResource với cấu trúc theo điểm     | Lỗi     |
| PSDJAVA-515 | TextBound không hoạt động như mong đợi                                                                           | Lỗi     |
| PSDJAVA-516 | Thêm một lớp được tạo bằng constructor mặc định vào hình ảnh PSD không thêm nguồn tài nguyên mặc định   | Lỗi     |
| PSDJAVA-517 | Timeline.LoopesCount bị bỏ qua khi xuất sang GIF hoạt hình                                                | Lỗi     |

## **Thay đổi API công cộng**
# **API Thêm mới:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **API Đã Xóa:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **Ví dụ sử dụng:**

**PSDJAVA-502. Thêm khả năng xuất mỗi lớp của Tệp PSD sang Tệp Gif hoạt hình** 

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // Tạo frames cho mỗi lớp.
        int framesCount = psdImage.getLayers().length;
        Timeline timeline = psdImage.getTimeline();

        Frame[] frames = new Frame[framesCount];
        for (int i = 0; i < framesCount; i++) {
            frames[i] = new Frame();
            LayerState[] layerStates = new LayerState[framesCount];

            for (int j = 0; j < framesCount; j++) {
                layerStates[j] = new LayerState();
                layerStates[j].setEnabled(i == j);
            }

            frames[i].setLayerStates(layerStates);
        }

        timeline.setFrames(frames);

        // Cập nhật states hiện tại
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

**PSDJAVA-503. Gán thuộc tính Fill của lớp Hình dạng từ tài nguyên vscg**

{{< highlight java >}}
        // Ví dụ fill rắn
        public static void main(String[] args) {
            String srcFile = "src/main/resources/ShapeInternalSolid.psd";
            String outFile = "src/main/resources/ShapeInternalSolid.psd.out.psd";

            PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
            psdLoadOptions.setLoadEffectsResource(true);

            try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
                 ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
                  ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();
                 fillSettings.setColor(Color.getRed());

                 shapeLayer.update();

                 image.save(outFile);
            }

            // Kiểm tra các thay đổi đã lưu
            try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();

            assertAreEqual(Color.getRed(), fillSettings.getColor());

            image.save(outFile);
        }

        static void assertAreEqual(Object expected, Object actual, String message) {
            if (!expected.equals(actual)) {
                throw new IllegalArgumentException(message);
            }
        }

        static void assertAreEqual(Object expected, Object actual) {
            assertAreEqual(expected, actual, "Các đối tượng không bằng nhau.");
        }
		
		// Ví dụ fill chéo:

	public static void main(String[] args) {
    String srcFile = "src/main/resources/ShapeInternalGradient.psd";
    String outFile = "src/main/resources/ShapeInternalGradient.psd.out.psd";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
        GradientFillSettings fillSettings = (GradientFillSettings) shapeLayer.getFill();
        fillSettings.setDither(true);
        fillSettings.setReverse(true);
        fillSettings.setAlignWithLayer(false);
        fillSettings.setAngle(20);
        fillSettings.setScale(50);
        fillSettings.getColorPoints()[0].setLocation(100);
        fillSettings.getColorPoints()[1].setLocation(4000);
        fillSettings.getTransparencyPoints()[0].setLocation(200);
        fillSettings.getTransparencyPoints()[1].setLocation(3800);
        fillSettings.getTransparencyPoints()[0].setOpacity(90);
        fillSettings.getTransparencyPoints()[1].setOpacity(10);

        shapeLayer.update();

        image.save(outFile);
    }

    // Kiểm tra các thay đổi đã lưu
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
        GradientFillSettings fillSettings = (GradientFillSettings) shapeLayer.getFill();

        assertAreEqual(true, fillSettings.getDither());
        assertAreEqual(true, fillSettings.getReverse());
        assertAreEqual(false, fillSettings.getAlignWithLayer());
        assertAreEqual((double) 20, fillSettings.getAngle());
        assertAreEqual(50, fillSettings.getScale());
        assertAreEqual(100, fillSettings.getColorPoints()[0].getLocation());
        assertAreEqual(4000, fillSettings.getColorPoints()[1].getLocation());
        assertAreEqual(200, fillSettings.getTransparencyPoints()[0].getLocation());
        assertAreEqual(3800, fillSettings.getTransparencyPoints()[1].getLocation());
        assertAreEqual((double) 90, fillSettings.getTransparencyPoints()[0].getOpacity());
        assertAreEqual((double) 10, fillSettings.getTransparencyPoints()[1].getOpacity());
    }
}

{{< /highlight >}}

**PSDJAVA-504. Thêm các loại warp mới (arc & arch)**

{{< highlight java >}}
     String sourceArcFile = "src/main/resources/arc_warp.psd";
     String outputArcFile = "src/main/resources/arc_export.png";
     
     String sourceArchFile = "src/main/resources/arch_warp.psd";
     String outputArchFile = "src/main/resources/arch_export.png";
     
     PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
     psdLoadOptions.setAllowWarpRepaint(true);
     psdLoadOptions.setLoadEffectsResource(true);
     
     PngOptions pngOptions = new PngOptions();
     pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
     
     try (PsdImage psdImage = (PsdImage) Image.load(sourceArcFile, psdLoadOptions)) {
         psdImage.save(outputArcFile, pngOptions);
     }
     
     
     try (PsdImage psdImage = (PsdImage) Image.load(sourceArchFile,