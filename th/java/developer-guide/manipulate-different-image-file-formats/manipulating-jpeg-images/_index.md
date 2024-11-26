---
title: การจัดการภาพ JPEG
type: docs
weight: 20
url: /java/manipulating-jpeg-images/
---

## **ใช้ ExifData Class เพื่ออ่านและแก้ไข JPEG EXIF Tags**


เกือบทุกกล้องดิจิทัล (รวมถึงสมาร์ทโฟน) และสแกนเนออื่อระบบอื่ภิสการบันทึภาพ Save ภาพพร้อมข้อมูล EXIF (Exchangeable Image File) ข้อมูลการตั้งค่ากล้องและฉากภาพถูกบันทึโดยกล้องลงในไฟล์ภาพ ข้อมูล EXIF รวมถึ ความเร็วตั้งผ้ากล้อง วันที่และเวลาที่ถ่ายภาพ ความยาวโฟกัส การปรับค่าเอ็กซ์โปเจอร์ รูปแบบการวัดแสง และการใช้แฟลช Aspose.Imaging APIs ทำให้สามารถสร้างข้อมูล EXIF จากภาพที่กำหนดได้อย่างง่ายและกระชับ ผู้พัฒนาสามารถเขียนข้อมูล EXIF ลงในภาพหรือแก้ไขข้อมูลที่มีอยู่ตามต้องการ Aspose.Imaging ได้ให้ ExifData class สำหรับการอ่าน เขียนและปรับเปลี่ยนข้อมูล EXIF, ในที่นี้ Aspose.PSD.Exif.Enums namespace มีรายการสมาชิกที่เกี่ยวข้องที่ใช้ในกระบวนการ
### **อ่านข้อมูล EXIF**
Aspose.PSD APIs ให้วิธีการอ่านข้อมูล EXIF จากภาพที่กำหนด ด้านล่างเป็นขั้นตอนให้อัน illustration การใช้งานของ ExifData class เพื่ออ่านข้อมูล EXIF จากภาพ.

- โหลด PSD Image โดยใช้ factory method Load.
- ค้นหาภาพตัวย่อ JPEG ในทรัศมี PSD.
- แยกอินสแตนซ์ของ ExifData class.

ดึงข้อมูลที่ต้องการและเขียนไปยังคอนโซล

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}



แทนที่นี้ ผู้พัฒนาสามารถหาข้อมูลเฉพาะโดยใช้โค้ดต่อไปนี้


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **เขียนและปรับเปลี่ยนข้อมูล EXIF**
โดยใช้ Aspose.PSD APIs, ผู้พัฒนาสามารถเขียนข้อมูล EXIF ใหม่และแก้ไขข้อมูล EXIF ที่มีในภาพได้ ทั้งกระบวนการ (เขียนและปรับเปลี่ยน) ต้องการโหลดภาพและเข้าถึงข้อมูล EXIF เข้าไปในอินสแตนซ์ของ ExifData class จากนั้นสามารถเข้าถึงคุณสมบัติที่ ExifData class เปิดเผยเพื่อตั้งค่าตามที่เหมาะสม โปรดทราบว่าภาพสำหรับการแก้ไขควรเป็นภาพ JPEG หรือ TIFF ซึ่งโดยทั่มี PSD thumbnails ชุดของรหัสเพื่อสอดคล้องกับห้องปฎิบัติการ Sample ในการสื่งเสด ดังนี้:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **สกัดไธม์เนลเนลย์จากทรัศมี PSD**
ภาพตัวย่อ (Thumbnail) คือรุ่นลดขนาดของรุปภาพที่ใช้แสดงสวนหนึ่งของรูปภาพแทนการแสดงทั้งรูป Prelime(้Whichin하SanallheakesRpredifferitereQ).หภพlays มีรูปย่อถูกประกาศอยู่ในไฟล์  Aspose.CAP ให้การสด้ารบข้อมูลใหเน
PdtoP.A.is8ess..iesPdataed.TheOmrapti.RetvegLable.adsTr.tifAAS..ThareGE(resourcesD.A.IPYThurtyrpesLAYり汁メント.TunHAD.Aperty,Cたのlow0.adanテーア.ShowIOD



pro
