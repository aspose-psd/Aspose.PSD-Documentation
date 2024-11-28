---
title: Aspose.PSD for Java 20.8 - บันทึกการปล่อย
type: docs
weight: 50
url: /th/java/aspose-psd-for-java-20-8-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการปล่อยของ [Aspose.PSD for Java 20.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.8/) {{% /alert %}} 

|**คีย์**|**สรุป**|**ประเภท**|
| :- | :- | :- |
|PSDJAVA-264|Support of SoLdResource (Smart Object Layer Data resource)|คุณลักษณะ|
|PSDJAVA-263|Support of PlLdResource (placed layer resource for Smart Object Layer)|คุณลักษณะ|
|PSDJAVA-262|Add Object Array and Unit Array structures support: ObAr / UnFl signatures|คุณลักษณะ|
|PSDJAVA-265|Underline and strikethrough lost after focusing on the text in file saved with Aspose.|ข้อผิดพลาด|
|PSDJAVA-257|Fix saving modified PSD image with CMYK ColorMode 16 bit per channel|ข้อผิดพลาด|
|PSDJAVA-268|Regression: Aspose.PSD 20.7.0 breaks font sizes for older files|ข้อผิดพลาด|

# **การเปลี่ยนแปลงของ API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- F:com.aspose.psd.fileformats.psd.layers...
- M:com.aspose.psd.fileformats.psd.layers...
- T:com.aspose.psd.fileformats.psd.layers...

# **ตัวอย่างการใช้:**  

**PSDJAVA-264. การสนับสนุน SoLdResource (Smart Object Layer Data resource)**
{{< highlight java >}}
// ตัวอย่างนี้แสดงถึงวิธีการรับหรือกำหนดค่าสมบัติของข้อมูลเลเยอร์การใช้เฉพาะของไฟล์ PSD
...
{{< /highlight >}}

**PSDJAVA-263. การสนับสนุน PlLdResource (เชิงบรรทัดที่จัดไว้เป็นชั้นของ Smart Object Layer)**
{{< highlight java >}}
// ตัวอย่างนี้แสดงถึงวิธีการหรือจัดค่าสมบัติของเลเยอร์ของไฟล์ PSD
...
{{< /highlight >}}

**PSDJAVA-262. การเพิ่มการสนับสนุนโครงสร้าง Object Array และ Unit Array: ลายเซนต์ ObAr / UnFl**
{{< highlight java >}}
// ตัวอย่างนี้พิสูจน์ว่า ObjectArrayStructure และ UnitArrayStructure ถูกสนับสนุนโดยไลบรารีเพื่อให้สามารถอ่านและเขียนมัน
...
{{< /highlight >}}

**PSDJAVA-265. Underline and strikethrough หายไปหลังจากโฟกัสที่ข้อความในไฟล์ที่บันทึกไว้ด้วย Aspose.PSD**
{{< highlight java >}}
// ตัวอย่างนี้พิสูจน์ว่ารูปแบบ underline และ strikethrough ไม่หายไปเมื่อเลือกข้อความโดยใช้เครื่องมือชื่อเรื่องแนวนอนใน Photoshop หลังจากไฟล์ PSD ได้รับการบันทึกโดยไลบรารี
...
{{< /highlight >}}

**PSDJAVA-257. การแก้ไขการบันทึกรูปภาพ PSD ที่ปรับเปลี่ยนด้วย CMYK ColorMode 16 บิตต่อช่อง**
{{< highlight java >}}
// ตัวอย่างนี้พิสูจน์ว่าไม่มีข้อผิดพลาดในการบันทึกรูปภาพ PSD 16 บิตในโหมดสี CMYK โปรแกรม๓โหลดภาพ 16 บิตในโหมดสี CMYK จากนั้นโมดิไฟเยนดิ่ไที่ดีเล็กน้อยและบันทึกเป็นเอกสารฟอโตรเช็ปอื่นๆ
...
{{< /highlight >}}

**PSDJAVA-268. การถอดกลับ: Aspose.PSD 20.7.0 ทำให้ขนาดตัวอักษรเสียสำหรับไฟล์เก่า**
{{< highlight java >}}
// ตัวอย่างนี้ทำให้ขนาดตัวอักษรของไฟล์ PSD เก่าเสียหาย
...
{{< /highlight >}}**PSDJAVA-264. Support of SoLdResource (Smart Object Layer Data resource)**
{{< highlight java >}}
// This example shows how to get or set the smart object layer data properties of the PSD file.
...
{{< /highlight >}}

**PSDJAVA-263. Support of PlLdResource (placed layer resource for Smart Object Layer)**
{{< highlight java >}}
// This example shows how to get or set the Placed layer resource properties of the PSD file.
...
{{< /highlight >}}

**PSDJAVA-262. Add Object Array and Unit Array structures support: ObAr / UnFl signatures**
{{< highlight java >}}
// This example proves that ObjectArrayStructure and UnitArrayStructure are supported by
// the library so that we can read and write them. The program walks through the hierarchy
// of resource structures in search of the valid UnitArrayStructure.
...
{{< /highlight >}}

**PSDJAVA-265. Underline and strikethrough lost after focusing on the text in file saved with Aspose.PSD**
{{< highlight java >}}
// This example proves that underline and strikethrough formatting does not disappear on
// selecting text using Horizontal Type Tool in Photoshop after the PSD file was saved
// by the library.
...
{{< /highlight >}}

**PSDJAVA-257. Fix saving modified PSD image with CMYK ColorMode 16 bit per channel**
{{< highlight java >}}
// This example proves that there is no error on saving a 16-bit PSD image in the CMYK
// color mode. The program loads a 16-bit image in the CMYK color mode than modifies it
// slightly and saves it as another Photoshop document.
...
{{< /highlight >}}

**PSDJAVA-268. Regression: Aspose.PSD 20.7.0 breaks font sizes for older files**
{{< highlight java >}}
// This example reproduces the bug that breaks font sizes for older PSD files.
...
{{< /highlight >}}