---
title: การจัดการกับรูปแบบ Adobe Photoshop Formats
type: docs
weight: 20
url: /th/net/manipulating-adobe-photoshop-formats/
---

## **ผสาน PSD layers เข้ากับอีก layers**

## **การส่งออกรูปภาพเป็น PSD**
PSD, เอกสารของ PhotoShop, เป็นรูปแบบไฟล์เริ่มต้นที่ใช้โดย Adobe Photoshop ในการทำงานกับภาพ. Aspose.PSD ช่วยให้คุณโหลด, แก้ไข, และบันทึกไฟล์เป็น PSD ให้สามารถเปิดและแก้ไขใน Photoshop. บทความนี้แสดงวิธีการบันทึกไฟล์เป็น PSD ด้วย Aspose.PSD, และอธิบายการตั้งค่าบางอย่างที่สามารถใช้เมื่อบันทึกในรูปแบบนี้. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) เป็นคลาสที่เฉพาะเจาะจงภายใน namespace [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) ที่ใช้ในการส่งออกรูปภาพเป็น PSD. เพื่อส่งออกเป็น PSD, สร้างอินสแตนซ์ของคลาส Image โดยโหลดจากไฟล์รูปภาพที่มีอยู่ (ตัวอย่างเช่นรูปภาพขนาดย่อ) หรือสร้างขึ้นมาด้วยตัวเอง. บทความนี้อธิบายวิธีการดังกล่าว ในตัวอย่างด้านล่าง รูปภาพถูกสร้างขึ้นด้วยตัวเองหลังจากสร้างและประชุมข้อมูลพิกเซล, บันทึกรูปภาพด้วยวิธี Save ของคลาส Image และกำหนดอ็อบเจกต์ PsdOptions เป็นอาร์กิวเมนต์ที่สอง. สามารถตั้งค่าคุณสมบัติของ PsdOptions ได้หลายอย่างสำหรับคอนเวอร์ชันขั้นสูง. บางคุณสมบัติได้แก่ ColorMode, [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) และ Version. Aspose.PSD รองรับวิธีการบีบอัดต่อได้ผ่านการเหมือนอีเมทชันคอมประซิอม:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

โหมดสีต่อไปนี้ได้รับการสนับสนุนผ่านอีเมทชัน [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes):

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB


สามารถเพิ่มทรัพยากรเสริมอื่น ๆ เช่น ทรัพยากรรูปตัวอย่างสำหรับ PSD v4.0, v5.0 และสูงกว่า หรือเส้นทางและแนวทำใจสำหรับ PSD v4.0 และสูงกว่า โค้ดด้านล่างสร้างไฟล์รูปภาพจากตั้งแต่ความสะดวก, ชุบเติมพิกเซลและบันทึกใน PSD ด้วยการบีบอัด RLE และโหมดสี Grayscale ด้วย โค้ดด้านล่างแสดงให้เห็นว่าการส่งออกรูปภาพไปยังไฟล์ PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}
## **นำเข้ารูปภาพเข้าเลเยอใน PSD layer**
บทความนี้แสดงการใช้ Aspose.PSD เพื่อเพิ่มหรือนำเข้ารูปภาพไปยัง PSD layer. Aspose.PSD APIs ได้เปิดเผยวิธีการใช้งานอย่างมีประสิทธิภาพและง่ายสำหรับบรรทัดนี้ Aspose.PSD ได้เปิดเผยวิธีการใช้งาน DrawImage ของคลาส Layer เพื่อเพิ่มหรือนำเข้ารูปภาพเข้าไปในไฟล์ PSD. วิธีการ DrawImage ต้องการตำแหน่งและค่ารูปภาพในการเพิ่มหรือนำเข้ารูปภาพไปยังไฟล์ PSD ขั้นตอนและง่ายเช่นด้านล่างคือ:

- โหลดไฟล์ PSD เป็นรูปภาพโดยใช้วิธีการไฟล์ที่ Load ที่เปิดเผยโดย Image class.
- สร้างอินสแตนซ์ของ Layer class จากไฟล์ด้วย