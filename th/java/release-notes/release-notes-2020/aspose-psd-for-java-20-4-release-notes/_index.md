---
title: บันทึกการปล่อย Aspose.PSD for Java 20.4
type: งาน
weight: 30
url: /th/java/aspose-psd-for-java-20-4-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการปล่อยสำหรับ [Aspose.PSD for Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) {{% /alert %}} 

|**Key**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDJAVA-156|รองรับ 'ข้อมูลต้นทางเวกเตอร์' resource|คุณสมบัติ|
|PSDJAVA-171|รองรับ lclrResource (การตั้งค่าสีชีท)|คุณสมบัติ|
|PSDJAVA-157|รองรับคุณสมบัติจากข้อมูล LengthRecord (การดำเนินการเพิ่มเติม (การดำเนินการบูลีเลียน), ดัชนีของรูปร่างในเลเยอร์, จำนวนของบีเซียร์คอตรอล์เรคคอต)|คุณสมบัติ|
|PSDJAVA-158|รองรับ Image Section Resource #1010 สีพื้นหลัง|คุณสมบัติ|
|PSDJAVA-161|การเพิ่ม Fill Layers เมื่อใช้งาน|คุณสมบัติ|
|PSDJAVA-168|รองรับ Image Section Resource #1009 ข้อมูลขอบเขต|คุณสมบัติ|
|PSDJAVA-169|รองรับเลเยอร์ในไฟล์รูปแบบ AI|คุณสมบัติ|
|PSDJAVA-163|รองรับการอ่านและแก้ไข Gradient Overlay Layer Effect|คุณสมบัติ|
|PSDJAVA-164|การเรนเดอริ่งของ Gradient Overlay Layer Effect|คุณสมบัติ|
|PSDJAVA-149|Aspose.PSD for java error เมื่อได้รับคุณสมบัติ textData.items ของ text layer|แก้ปัญหา|
|PSDJAVA-166|แก้ไขปัญหาการบันทึกรูปภาพ PSD ที่มี Grayscale ColorMode และ 16 bit ต่อช่องเป็นรูปแบบ PSD สีเทา|แก้ปัญหา|
|PSDJAVA-167|แก้ไขปัญหาการบันทึกรูปภาพ PSD ที่มี Grayscale ColorMode และ 16 bit ต่อช่องเป็นรูปแบบ PNG|แก้ปัญหา|
|PSDJAVA-159|การเปลี่ยนแปลงคุณสมบัติของ GradientOverlayEffect.BlendMode ไม่ถูกแสดงใน Photoshop|แก้ปัญหา|
# **การเปลี่ยนแปลง API สาธารณะ**
# **API เพิ่มเข้ามา:**
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
## **API ที่ถูกนำออก:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)
# **Ex การใช้:**

**PSDJAVA-156. รองรับ 'ข้อมูลต้นทางเวกเตอร์' resource**

{{< highlight java >}}

 /*

ตัวอย่างการอ่านและปรับเปลี่ยนข้อมูลของ Vector Origination Data resource.

*/

// ยังคงวิธีการในขอบเขตของพื้นที่ท้องที่สำหรับความง่าย

// here

{{< /highlight >}}

**PSDJAVA-171. รองรับ lclrResource (การตั้งค่าสีชีท)**

{{< highlight java >}}

 /*

ตัวอย่างการใช้ Layer Sheet Color เพื่อเน้นชั้น. ตัวอย่างเช่นคุณสามารถ

อัปเดตบางชั้นใน Photoshop แล้วเน้นด้วยสีชั้นที่ต้องการเพื่อดึงดูด

ความสนใจ.

*/

// ยังคงวิธีการในขอบเขตของพื้นที่ท้องที่สำหรับความง่าย

// here

{{< /highlight >}}

**PSDJAVA-157. รองรับคุณสมบัติจากข้อมูล LengthRecord (การดำเนินการเพิ่มเติม (การดำเนินการบูลีเลียน), ดัชนีของรูปร่างในเลเยอร์, จำนวนของบีเซียร์คอตรอล์เรคคอต)**

{{< highlight java >}}

 /*

ตัวอย่างการเปลี่ยนการดำเนินการเพิ่มเติมเมื่อทำงานกับรูปร่าง. โปรแกรมอ่าน

เทนเนอร์เวกเตอร์ที่กำหนดไว้ (LengthRecord) และเปลี่ยนการดำเนินการเของพวกเขา

จากนั้นบันทึกสำเนาที่มีการปรับเปลี่ยนเอกสารเป็นภาพใหม่เป็นไฟล์ PSD.

*/

// ยังคงวิธีการในขอบเขตของพื้นที่ท้องที่สำหรับความง่าย

// here

{{< /highlight >}}

**PSDJAVA-158. รองรับ Image Section Resource #1010 สีพื้นหลัง**

{{< highlight java >}}

 /*

ตัวอย่างการอ่านและปรับเปลี่ยนข้อมูลสีพื้นหลัง.

*/

// ยังคงวิธีการในขอบเขตของพื้นที่ท้องที่สำหรับความง่าย

// here

{{< /highlight >}}

**PSDJAVA-161. การเพิ่ม Fill Layers เมื่อใช้งาน**

{{< highlight java >}}

 /*

ตัวอย่างการเพิ่มชั้นเติมของชนิดต่าง ๆ ลงในเอกสาร Photoshop.

*/

// ยังคงวิธีการในขอบเขตของพื้นที่ท้องที่สำหรับความง่าย

// here

{{< /highlight >}}

**PSDJAVA-168. รองรับ Image Section Resource #1009 ข้อมูลขอบเขต**

{{< highlight java >}}

 /*

ตัวอย่างการอ่าน, ปรับเปลี่ยนและบันทึกไฟล์ PSD ที่มีข้อมูลขอบของ

เขตความจุงาน.

*/

// ยังคงวิธีการในขอบเขตของพื้นที่ท้องที่สำหรับความง่าย

// here

{{< /highlight >}}

**PSDJAVA-169. รองรับเลเยอร์ในไฟล์รูปแบบ AI**

{{< highlight java >}}

 /*

ตัวอย่างการส่งออกไฟล์ AI ที่มีเลเยอร์ไปยังรูปแบบไฟล์อื่น ๆ. โปรแกรม

โหลดไฟล์ AI ที่กำหนดไว้ล่วงหน้าและตรวจสอบก่อนการส่งออกต่อไป.

*/

// ยังคงวิธีการในขอบเขตของพื้นที่ท้องที่สำหรับความง่าย

// here

{{< /highlight >}}

**PSDJAVA-163. รองรับการอ่านและแก้ไข Gradient Overlay Layer Effect**

{{< highlight java >}}

 /*

ตัวอย่างการนำเอฟเฟคการยึดขอบเขตสีไปใช้กับชั้นรูป.

*/

// ยังคงวิธีการในขอบเขตของพื้นที่ท้องที่สำหรับความง่าย

// here

{{< /highlight >}}

**PSDJAVA-164. เรนเดอริ่งของเอฟเฟค Gradient Ovelay Layer Effect**

{{< highlight java >}}

 /*

ตัวอย่างการโหลดและบันทึกไฟล์ PSD ที่มีชั้นที่มีเอฟเฟกทับบนเอกสาร.

*/

// ยังคงวิธีการในขอบเขตของพื้นที่ท้องที่สำหรับความง่าย

// here

{{< /highlight >}}

**PSDJAVA-149. ความคลาดเคลื่อนของ Aspose.PSD สำหรับข้อผิดพลาดที่ได้รับจาก textData.items property ของ text layer**

{{< highlight java >}}

 /*

ตัวอย่างการสร้างรูปภาพ PNG หลาย ๆ รูปจากไฟล์เทมเพลต PSD. โปรแกรมเพียง

วนลูปสำหรับแต่ละชั้นและแทนที่อาร์กิวเม้นที่ต้องการด้วยข้อมูลจริง. เมื่อ

แล้วและสร้างรูป PN

*/

// ห่องสำหรับเก็บข้อมูลชั้นที่จะถูกตั้ง

{{< /highlight >}}

**PSDJAVA-166. แก้ไขปัญหาการบันทึกภาพ PSD ที่มี Grayscale ColorMode และ 16 bit ต่อช่องเป็นรูปแบบ PSD สีเทา**

{{< highlight java >}}

 /*

ตัวอย่าง