---
title: การสร้าง เปิด และบันทึกไฟล์ PSD
type: docs
weight: 10
url: /th/java/creating-opening-and-saving-psd-files/
---

## **ส่งออกภาพเป็น PSD**
PSD, หรือเอกสาร PhotoShop, เป็นรูปแบบไฟล์เริ่มต้นที่ใช้โดย Adobe PhotoShop สำหรับการทำงานกับภาพ  Aspose.PSD ช่วยให้คุณโหลด แก้ไข และบันทึกไฟล์เป็น PSD เพื่อให้มีการเปิดและแก้ไขใน PhotoShop บทความนี้แสดงวิธีการบันทึกไฟล์เป็น PSD ด้วย Aspose.PSD และยังหาระการตั้งค่าบางประการที่สามารถใช้เมื่อบันทึกในรูปแบบนี้ PsdOptions เป็นคลาสเชี้ยวชาญใน Nameสูงสุดของ  ImageOptions ที่ใช้เพื่อส่งออกภาพเป็น PSD เพื่อส่งออกไปยัง PSD สร้างตัวอย่างของคลาสรูปภาพทั้งใหม่จากตะกร้าจะอธิบายวิธีทำ ในตัวอย่างด้านล่าง รูปภาพถูกสร้างขึ้นจากเริ่มต้น หลังจากสร้างและข้อมูลพิกเซลถูกกระจายบรรจบ บันทึกภาพโดยใช้วิธีการ Save และให้วัตถุ PsdOptions เป็นอาร์กิวเมนต์ที่สอง สามารถตั้งค่าคุณสมบัติหลายอย่างให้กับคลาส PsdOptions สำหรับการแปลงรูปสำหรับการแปลงขั้นสูง PsdOptions คอมพิวเตอร์ ช่อง และเวอร์ชันรองรับยกเว้นCompressionMethod การเสริมเพื่อป้องกัน - CompressionMethod.Raw - CompressionMethod.RLE - 
CompressionMethod.ZipWithoutProtection - CompressionMethod.ZipWithProtection

โหมดสีต่อไปนี้สามารถให้การสูรครับเรยจ่คอย - ColorModes.Bitmap - ColorModes.Grayscale - ColorModes.RGB

สามารถเพิ่มทรัพยากรเพิ่มเติม เช่น ทรัพยากรตัวอย่างสัญลักษณ์สำหรับ PSD v4.0 v5.0และสูงกว่า หรือตารางแนะนำทรัพยากรสำหรับ PSD v4.0 และสูงกว่า โค้ดด้านล่างสร้าง BMP ไฟล์แบบใหม่จากต้นและกระจายพิกเซลและบันทึกเป็น PSD ด้วยการบีบอัด RLE และโหมดสีระดับเทา โค้ดตัวอย่างด้านล่างแสดงวิธีการส่งออกภาพเป็น PSD

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.java" >}}

## **นำเข้าภาพไปยัง PSD layer**
บทความนี้จะโปรแกรมเป็นของการใช้ Aspose.PSD เพื่อเพิ่มหรือนำเข้าภาพไปยัง PSD layer Aspose.PSD APIs ได้เปิดเผยวิธีการถูกและง่ายที่จะใช้สำหรับการประสบความสำเร็จ ตรงปลาย  'DrawImage' method ของคลาส  'Layer' เพื่อเพิ่ม/นำเข้ารูปภาพเข้าเข้าไฟล์ PSD  'DrawImage' method ต้องการตำแหน่งและค่ารูปภาพในการเพิ่ม/นำเข้ารูปภาพเข้าไฟล์ PSD ขั้นตอนในการนำเข้าไฟล์รูปภาพไปยัง PSD layer เป็นง่ายดังต่อไปนี้ etc.


- Load ไฟล์ PSD เป็นรูปภาพโดยใช้ factory method 'Load' เปิดเผยโดย Image class
- สร้างอินสแตนส์ของคลาส Layer และกำหนดให้แพ็คชั้นรูปภาพ PSD กับมัน
- Load รูปภาพที่ต้องการเพิ่มหรือสร้างหนึ่งใหม่จากเริ่มต้น
- เรียก  'DrawImage' method ของ  Layer กดระบุตำแหน่งภาพ
- บันทึกผลลัพธ์


โค้ดตัวอย่างด้านล่างแสดงวิธีการนำเข้าภาพไปยัง PSD layer

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ImportImageToPSDLayer-ImportImageToPSDLayer.java" >}}


## **สร้างภาพเป็นตัวอย่างจากไฟล์ PSD**
PSD เป็นรูปแบบสารส้นพันธุ์ของแอปพลิเคชัน Photoshop ของ Adobe Adobe Photoshop (รุ่น 5.0 และล่าสุด) เก็บข้อมูลรายละเอียดของภาพตัวอย่างสำหรับการแสดงผลตัวอย่างในพื้นที่ทรัพยากรภาพที่ประกอบไปด้วยหัวข้อ 28 ไบต์เริ่มต้น ตามด้วยรูปภาพตัวอย่าง JFIF ในลำดับสี RGB (สีแดง สีเขียว สีน้ำเงิน) Aspose.PSD API ให้กลไกการเข้าถึงทรัพยากรของไฟล์ PSD ที่ง่ายต่อการใช้งาน ทรัพยากรเหล่านี้รวมถึงทรัพยากรตัวอย่างภาพตัวอย่างที่สามารถดึงดึกและบันทึกลงดิสก์ตามความต้องการของแอปพลิเคชัน โค้ดตัวอย่างด้านล่างแสดงวิธีการสร้างภาพตัวอย่าง จากไฟล์ PSD

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.java" >}}


## **การสร้างไฟล์ PSD ดัชนี**
Aspose.PSD สำหรับ Java API สามารถสร้างไฟล์ PSD ดัชนีจากต้น บทความนี้โปรแกรมการใช้งาน PsdOptions และ PsdImage สำหรับการสร้าง PSD ดัชนีขณะวาดรูปร่างบางสิ่งที่สร้างภายบนแผนผ้าที่สร้างทีละ3กระโดดการสร้างไฟล์ PSD ดัชนีต้องการขั้นตอนง่ายๆดังนี้

- สร้างอินสแตนส์ของ PsdOptions และกำหนดความเข้าใจมาจากที่มา
- ตั้งคุณสมบัติ ColorMode ของ PsdOptions เป็น ColorModes.Indexed
- สร้างแถวใหม่ของสีจากช่องสี RGB และตั้งเป็นคุณสมบัติสีของ Palette ของ PsdOptions
- ตั้งคุณสมบัติ CompressionMethod ของนั้นเป็นอัลโกริทึมการบีบอัดที่ต้องการ
- สร้างภาพ PSD ใหม่โดยการเรียก PsdImage.Create method
- เรียก Layer.Save method เพื่อเขียนภาพทั้งหมด

โค้ดตัวอย่างด้านล่างแสดงวิธีการสร้างไฟล์ PSD ดัชนี

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.java" >}}

## **ส่งออก PSD Layer เป็นภาพแบบRaster**
Aspose.PSD สำหรับ Java ช่วยให้คุณส่งออกเลเยอร์ในไฟล์ PSD เป็นภาพเราสามารถใช้แม้วทดงคีวา  'Layer.Save' เพื่อส่งออกเลเยอร์ไปยสเยัรภาพ โค้ดตัวอย่างต่อไปนี้โหลดไฟล์ PSD และส่งออกแต่ละเลเยอร์ไปยสเยาพไปรใช้  'Layer.Save' ของ Aspose.PSD.FileFormats.Psd.Layers.Layer หลังจากที่ส่งออกเลเยอร์ทุกชั้นเป็นรูปภาพ PNG คุณสามารถเปิดด้วยโปรแกรมดูรูปภาพที่คุณชื่นชอบ เปิดด้วยโปรแกรมดูรูปภาพที่คุณชื่นชอบ โค้ดตัวอย่างต่อไปนี้แสดงให้เห็นวิธีการส่งออก PSD Layer เป็นภาพแบบRaster

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.java" >}}
