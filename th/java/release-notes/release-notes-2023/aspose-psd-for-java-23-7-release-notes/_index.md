---
title: คำอธิบายการเปิด Aspose.PSD สำหรับ Java 23.7
type: docs
weight: 40
url: /th/java/aspose-psd-for-java-23-7-release-notes/
---

{{% alert color="primary" %}} หน้านี้ประกอบด้วยโน้ตการอัพเดทสำหรับ [Aspose.PSD สำหรับ Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **Key**     | **สรุป**                                                                                                                                      | **หมวดหมู่** |
|:------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDJAVA-502 | เพิ่มความสามารถในการส่งออกแต่ละเลเยอร์ของไฟล์ PSD เป็นไฟล์ Animated Gif                                        | คุณลักษณะ |
| PSDJAVA-503 | กำหนดคุณสมบัติการเติม Fill ของชั้นรูปร่างจากทรัพยากร vscg                                 | คุณลักษณะ |
| PSDJAVA-504 | เพิ่มประเภทของการเคลียร์ใหม่ (arc และ arch)                                                   | คุณลักษณะ |
| PSDJAVA-505 | เปลี่ยนแอปพลิเคชันที่บันทึกไฟล์ PSD เป็น Aspose.PSD หากคุณสมบัติ UpdateMetadata ถูกตั้งเป็น true      | คุณลักษณะ |
| PSDJAVA-510 | เพิ่มพื้นที่คำนวณของภาพกายภาพการกัด                          | คุณลักษณะ |
| PSDJAVA-511 | การประมวลผลชั้นปรับสีขาวดำที่มีความโปร่งใสไม่ถูกต้อง                                    | ข้อผิดพลาด     |
| PSDJAVA-512 | SmartObject ReplaceContents (เมื่อตัวเลือก AllowWarpRepaint เปิดใช้งาน) ล้มหาล้างหลังจาก 2 นาทีของการคำนวณ | ข้อผิดพลาด     |
| PSDJAVA-513 | เพิ่มความสามารถในการรับตำแหน่งของเลเยอร์กลุ่มจริงด้านซ้ายและด้านบน                         | ข้อผิดพลาด     |
| PSDJAVA-514 | การปรับขนาดของเลเยอร์ผิดเมื่อไฟล์ psd มี VogkResource ด้วยโครงสร้างในจุด           | ข้อผิดพลาด     |
| PSDJAVA-515 |  TextBound ไม่ทำงานอย่างที่คาดหวัง                                                                                | ข้อผิดพลาด     |
| PSDJAVA-516 | เพิ่มเลเยอร์ที่สร้างด้วยสร้างตัวกระซิบเข้าภาพ PSD ไม่เพิ่มทรัพยากรเริ่มต้นหาก | ข้อผิดพลาด     |
| PSDJAVA-517 | การปรับเปลี่ยนเวลาหน้าต่าง LoopesCount ถูกละเลยเมื่อส่งออกเป็น GIF แอนิเมชัน                    | ข้อผิดพลาด     |

## **การเปลี่ยนแปลง API สาธารณะ**
# **API เพิ่มเติม:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **API ที่ถูกลบ:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **ตัวอย่างการใช้:**

**PSDJAVA-502. เพิ่มความสามารถในการส่งออกแต่ละเลเยอร์ของไฟล์ PSD เป็นไฟล์ Animated Gif**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // Create frames for each layer.
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

        // Update current states
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

**PSDJAVA-503. กำหนดคุณสมบัติการเติม Fill ของชั้นรูปร่างจากทรัพยากร vscg**

{{< highlight java >}}
        // ตัวอย่างเติมสี
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

            // ตรวจสอบการเปลี่ยนแปลง
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
            assertAreEqual(expected, actual, "Objects are not equal.");
        }
		
		// ตัวอย่างการเติมกระดาษรูปแบบธง:

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

    // ตรวจสอบการเปลี่ยนแปลง
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

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Objects are not equal.");
}

{{< /highlight >}}

**PSDJAVA-504. เพิ่มประเภทใหม่ของการเคลียร์ (arc และ arch)**

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


    try (PsdImage psdImage = (PsdImage) Image.load(sourceArchFile, psdLoadOptions)) {
        psdImage.save(outputArchFile, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-505. เปลี่ยนแอปพลิเคชันที่บันทึกไฟล์ PSD เป็น Aspose.PSD หากคุณสมบัติ UpdateMetadata ถูกตั้งเป็น true**

{{< highlight java >}}
    String path = "src/main/resources/output.psd";
    try (PsdImage image = new PsdImage(100, 100)) {
        // หากคุณต้องการให้เครื่องสร้างเปลี่ยนไป ตรวจสอบให้แน่ใจว่า "UpdateMetadata" ถูกตั้งเป็น true มันถูกตั้งเป็น true โดยค่าเริ่มต้น
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setUpdateMetadata(true);

        // กำลังบันทึกรูปภาพ
        image.save(path, psdOptions);

        // ตรวจสอบเครื่องมือสร้างในโค้ด
        XmpPacketWrapper xmpData = image.getXmpData();
        XmpPackage basicPackage = image.getXmpData().getPackage(Namespaces.XmpBasic);

        // ที่นี่จะมีข้อมูลเครื่องมือสร้างที่อัปเดต
        String currentCreatorTool = (String) basicPackage.get_Item(":CreatorTool");
{{< /highlight >}}

**PSDJAVA-510. เพิ่มพื้นที่คำนวณของภาพกายภาพการกัด**

{{< highlight java >}}
    String sourceFile = "src/main/resources/mug4_warp.psd";
    String outputFile = "src/main/resources/mug4_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputFile, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-511. การประมวลปรับสีดำขาวดำย่อยผิด**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/frog_nosymb.psd";
    String outFile = "src/main/resources/frog_nosymb.psd.out.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile)) {
        psdImage.addBlackWhiteAdjustmentLayer();
        psdImage.save(outFile);
    }

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    // ตรวจสอบการเปลี่ยนแปลง
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer) image.getLayers()[1];

        if (blackWhiteAdjustmentLayer == null) {
            throw new Exception("ชั้นที่ 2 ควรเป็น BlackWhiteAdjustmentLayer");
        }

        image.save(outFile);
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Objects are not equal.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
       throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-512. SmartObject ReplaceContents (เมื่อตัวตัวเลือก AllowWarpRepaint เปิดใช้งาน) ล่มหลังจาก 2 นาทีของการคำนวณ**

{{< highlight java >}}
    String sourceFile = "src/main/resources/mug 4.psd";
    String changeFile = "src/main/resources/artwork for replace.png";
    String outputFile = "src