---
title: Aspose.PSD for Java 21.7 - บันทึกการอัปเดต
type: docs
weight: 40
url: /th/java/aspose-psd-for-java-21-7-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD for Java 21.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.7/) {{% /alert %}}

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDJAVA-362|การสนับสนุนการแก้ไขฟอนต์โดยใช้ TextPortions|คุณลักษณะ|
|PSDJAVA-363|Aspose.PSD 21.6: ImageSaveException เมื่อพยายามแปลง PSD เป็น PNG|ข้อผิดพลาด|

# **การเปลี่ยนแปลง Public API**
# **API ที่เพิ่มเข้ามา:**
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontName
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontName(java.lang.String)
- M:com.aspose.psd.FontSettings.getAdobeFontName(java.lang.String)

# **API ที่ถูกลบ:**
- ไม่มี

# **ตัวอย่างการใช้:**

**PSDJAVA-362. การสนับสนุนการแก้ไขฟอนต์โดยใช้ TextPortions**

{{< highlight java >}}
        String outputFilePng = "result_fontEditTest.png";
        String outputFilePsd = "fontEditTest.psd";

        PsdImage image = new PsdImage(500, 500);
        try {
            FillLayer backgroundFillLayer = FillLayer.createInstance(FillType.Color);
            ((IColorFillSettings) backgroundFillLayer.getFillSettings()).setColor(Color.getWhite());
            image.addLayer(backgroundFillLayer);

            TextLayer textLayer = image.addTextLayer("Text 1", new Rectangle(10, 35, image.getWidth(), 35));

            ITextPortion firstPortion = textLayer.getTextData().getItems()[0];
            firstPortion.getStyle().setFontName(FontSettings.getAdobeFontName("Comic Sans MS"));

            ITextPortion secondPortion = textLayer.getTextData().producePortion();
            secondPortion.setText("Text 2");
            secondPortion.getParagraph().apply(firstPortion.getParagraph());
            secondPortion.getStyle().apply(firstPortion.getStyle());
            secondPortion.getStyle().setFontName(FontSettings.getAdobeFontName("Arial"));

            textLayer.getTextData().addPortion(secondPortion);
            textLayer.getTextData().updateLayerData();

            image.save(outputFilePng, new PngOptions());
            image.save(outputFilePsd);
        } finally {
            image.dispose();
        }

        PsdImage imageOutput = (PsdImage) Image.load(outputFilePsd);
        try {
            TextLayer textLayer = (TextLayer) imageOutput.getLayers()[2];

            String adobeFontName1 = FontSettings.getAdobeFontName("Comic Sans MS");
            String adobeFontName2 = FontSettings.getAdobeFontName("Arial");

            AssertAreEqual(adobeFontName1, textLayer.getTextData().getItems()[0].getStyle().getFontName());
            AssertAreEqual(adobeFontName2, textLayer.getTextData().getItems()[1].getStyle().getFontName());
        } finally {
            imageOutput.dispose();
        }
{{< /highlight >}}

**PSDJAVA-363. Aspose.PSD 21.6: ImageSaveException เมื่อพยายามแปลง PSD เป็น PNG**

{{< highlight java >}}
        String srcFile = "input.psd";
        String output = "output.png";
        Image image = Image.load(srcFile);
        try {
            image.save(output, new PngOptions());
        } finally {
            image.dispose();
        }
{{< /highlight >}}
