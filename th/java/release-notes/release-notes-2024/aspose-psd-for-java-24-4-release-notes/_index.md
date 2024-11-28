---
title: อสโปส.PSD สำหรับ Java 24.4 - บันทึกการอัปเดต
type: docs
weight: 40
url: /th/java/aspose-psd-for-java-24-4-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการอัปเดตสำหรับ [อสโปส.PSD สำหรับ Java 24.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.4/) {{% /alert %}}

| **หมายเลข** | **สรุป**                                                                                               | **ประเภท** |
|:------------|:------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-610 | การตั้งค่าใบอนุญาตสำหรับ Aspose.PSD สำหรับ Java ทำให้เกิดข้อยกเว้นหากมีการทำให้มากกว่าหนึ่งครั้ง | ข้อบกพร่อง          |
| PSDJAVA-611 | [รูปแบบ AI] เพิ่มการจัดการทรัพยากร XObjectForm                                                    | คุณลักษณะ      |
| PSDJAVA-612 | เพิ่มคอนสตรักเตอร์สำหรับ ShapeLayer                                                              | คุณลักษณะ      |
| PSDJAVA-613 | แก้ไขการแปลง Psd ไฟล์จากสี RGB เป็น CMYK                                                        | ข้อบกพร่อง          |
| PSDJAVA-614 | ไม่สามารถส่งออกไฟล์ PSD ที่ต้องการโดยใช้ Aspose.PSD                                           | ข้อบกพร่อง          |

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addShapeLayer

# **API ที่ถูกลบออก:**

- ไม่มี

## **ตัวอย่างการใช้:**

**PSDJAVA-610. การตั้งค่าใบอนุญาตสำหรับ Aspose.PSD สำหรับ Java ทำให้เกิดข้อยกเว้นหากมีการทำให้มากกว่าหนึ่งครั้ง**

{{< highlight java >}}

        License license = new License();
        String liccorrectJava = "Aspose.PSD.Java.lic";

        license.setLicense(liccorrectJava);
        license.setLicense(liccorrectJava);

{{< /highlight >}}

**PSDJAVA-611. [รูปแบบ AI] เพิ่มการจัดการทรัพยากร XObjectForm**

{{< highlight java >}}        

        String sourceFile = "src/main/resources/example.ai";
        String outputFilePath = "src/main/resources/example.png";

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            image.save(outputFilePath, new PngOptions());
        }

{{< /highlight >}}

**PSDJAVA-612. เพิ่มคอนสตรักเตอร์สำหรับ ShapeLayer**

{{< highlight java >}}

    private static final int IMG_TO_PSD_RATIO = 256 * 65535;

    public static void main(String[] args) {
        String outputFile = "src/main/resources/AddShapeLayer_output.psd";

        try (PsdImage newPsd = new PsdImage(600, 400)) {
            ShapeLayer layer = newPsd.addShapeLayer();

            PathShape newShape = generateNewShape(newPsd.getSize());
            List<IPathShape> newShapes = new List<>();
            newShapes.add(newShape);
            layer.getPath().setItems(newShapes.toArray(new IPathShape[0]));

            layer.update();

            newPsd.save(outputFile);
        }

        try (PsdImage image = (PsdImage) Image.load(outputFile)) {
            assertAreEqual(2, image.getLayers().length);

            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings internalFill = (ColorFillSettings) shapeLayer.getFill();
            IStrokeSettings strokeSettings = shapeLayer.getStroke();
            ColorFillSettings strokeFill = (ColorFillSettings) strokeSettings.getFill();

            assertAreEqual(1, shapeLayer.getPath().getItems().length); // 1 Shape
            assertAreEqual(3, shapeLayer.getPath().getItems()[0].getItems().length); // 3 knots in a shape

            assertAreEqual(-16127182, internalFill.getColor().toArgb()); // ff09eb32

            assertAreEqual(7.41, strokeSettings.getSize());
            assertAreEqual(false, strokeSettings.getEnabled());
            assertAreEqual(StrokePosition.Center, strokeSettings.getLineAlignment());
            assertAreEqual(LineCapType.ButtCap, strokeSettings.getLineCap());
            assertAreEqual(LineJoinType.MiterJoin, strokeSettings.getLineJoin());
            assertAreEqual(-16777216, strokeFill.getColor().toArgb()); // ff000000
        }
    }

    static PathShape generateNewShape(Size imageSize) {
        PathShape newShape = new PathShape();

        PointF point1 = new PointF(20, 100);
        PointF point2 = new PointF(200, 100);
        PointF point3 = new PointF(300, 10);

        BezierKnotRecord firstBezierKnotRecord = new BezierKnotRecord();
        firstBezierKnotRecord.setLinked(true);
        firstBezierKnotRecord.setPoints(new Point[]{
                pointFToResourcePoint(point1, imageSize),
                pointFToResourcePoint(point1, imageSize),
                pointFToResourcePoint(point1, imageSize)
        });

        // โค้ดอื่นๆ จะถูกข้ามเนื่องจากมันยาวเกินไป

{{< /highlight >}}

**PSDJAVA-613. แก้ไขการแปลง Psd ไฟล์จาก RGB เป็น CMYK**

{{< highlight java >}}

    public static void main(String[] args) {
        // โค้ดด้านล่างจะต้องข้ามเนื่องจากมันยาวเกินไป

{{< /highlight >}}

**PSDJAVA-614. ไฟล์ PSD ที่เฉพาะเจาะจงไม่สามารถส่งออกได้โดยใช้ Aspose.PSD**

{{< highlight java >}}

        String sourceFile = "src/main/resources/1966source.psd";
        String outputPng = "src/main/resources/output.png";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setLoadEffectsResource(true);

        try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
            psdImage.save(outputPng, new PngOptions());
        }

{{< /highlight >}}
