---
title: Aspose.PSD for Java 20.3 - Release Notes
type: docs
weight: 10
url: /java/aspose-psd-for-java-20-3-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการปล่อย [Aspose.PSD for Java 20.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.2/) {{% /alert %}} 

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDJAVA-133|แปลงไฟล์ Adobe Illustrator เป็น PDF|Feature|
|PSDJAVA-134|เพิ่มความสามารถในการแสดงสไตล์ต่าง ๆ ในหนึ่งชั้นข้อความ|Feature|
|PSDJAVA-135|รองรับชั้นการปรับสีดำขาว|Feature|
|PSDJAVA-137|เพิ่มการสนับสนุนการส่งออกรูปแบบ AI (เวอร์ชัน 8) เป็นรูปแบบอื่น|Feature|
|PSDJAVA-138|รองรับการประมวลผลโหมดผสมของ PassThrough (ใช้สำหรับกลุ่มเลเยอร์เท่านั้น)|Feature|
|PSDJAVA-136|Exception: ล้มเหลวในการโหลดภาพเมื่อโหลดภาพที่มีชื่อ Unicode Alpha Names Resource ว่างเปล่า|Bug|
|PSDJAVA-139|ผลลัพธ์ไม่ถูกหลังจากเปลี่ยนการมองเห็นของ LayerGroup|Bug|
|PSDJAVA-140|Exception ในการโหลดภาพ PSD: ส่วนสี (DropShadow Resource) ต้องมีส่วนประกอบสี 3 ส่วนสำหรับ RGB หรือ 4 ส่วนสำหรับ CMYK|Bug|
|PSDJAVA-141|Exception หากพยายามวาดบนเลเยอร์ที่สร้างใหม่หากใช้อินสแตนเวอร์ชันง่าย|Bug|

# **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.text.IText.producePortions(java.lang.String[],com.aspose.psd.fileformats.psd.layers.text.ITextStyle,com.aspose.psd.fileformats.psd.layers.text.ITextParagraph)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getBaselineShift
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxBold
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxItalic
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontBaseline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontCaps
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getStrikethrough
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getUnderline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setBaselineShift(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxBold(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxItalic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontBaseline(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontCaps(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setStrikethrough(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setUnderline(boolean)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Subscript
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Superscript
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.AllCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.SmallCaps
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream)
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream,boolean)

## **API ที่ถูกลบ:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.setVisibleInGroup(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(int)

# **ตัวอย่างการใช้:**
**PSDJAVA-133. แปลงไฟล์ Adobe Illustrator เป็น PDFs**

{{< highlight java >}}
  String inFile = "rect2_color.ai";
  String outFile = "rect2_color.ai_output.pdf";
  AiImage aiImage = (AiImage)Image.load(inFile);

  try {
      aiImage.save(outFile, new PdfOptions());
  } finally {
      aiImage.dispose();
  }
{{< /highlight >}}

**PSDJAVA-134. เพิ่มความสามารถในการแสดงสไตล์ต่าง ๆ ในหนึ่งชั้นข้อความ**

{{< highlight java >}}
  String inFilePath = "text212.psd";
  String outFilePath = "Output_text212.psd";
  PsdImage image = (PsdImage)Image.load(inFilePath);
  
  try {
      TextLayer textLayer = (TextLayer)image.getLayers()[1];
      IText textData = textLayer.getTextData();
      ITextStyle defaultStyle = textData.producePortion().getStyle();
      // Remaining code here...
  } finally {
      image.dispose();
  }
{{< /highlight >}}

**PSDJAVA-135. รองรับชั้นการปรับสีดำขาว**

{{< highlight java >}}
 // ตัวอย่างการรองรับการเพิ่มชั้นการปรับสีดำขาวในระหว่างการทำงาน
  // Remaining code here...
{{< /highlight >}}

**PSDJAVA-137. เพิ่มการสนับสนุนการส่งออกรูปแบบ AI (เวอร์ชัน 8) เป็นรูปแบบอื่น**

{{< highlight java >}}
 // ตัวอย่างการส่งออกไฟล์ AI เป็นรูปแบบ PSD และ PNG
  // Remaining code here...
{{< /highlight >}}

**PSDJAVA-138. รองรับการประมวลผลโหมดผสมของ PassThrough (ใช้สำหรับกลุ่มเลเยอร์เท่านั้น)**

{{< highlight java >}}
  // Remaining code here...
{{< /highlight >}}

**PSDJAVA-139. ผลลัพธ์ไม่ถูกหลังจากเปลี่ยนการมองเห็นของ LayerGroup**

{{< highlight java >}}
  // Remaining code here...
{{< /highlight >}}

**PSDJAVA-140. Exception ในการโหลดภาพ PSD: ส่วนสี (DropShadow Resource) ต้องมีส่วนประกอบสี 3 ส่วนสำหรับ RGB หรือ 4 ส่วนสำหรับ CMYK**

{{< highlight java >}}
  // Remaining code here...
{{< /highlight >}}

**PSDJAVA-141. Exception หากพยายามวาดบนเลเยอร์ที่สร้างใหม่หากใช้รุ่นง่ายของ Constructor**

{{< highlight java >}}
  // Remaining code here...
{{< /highlight >}}