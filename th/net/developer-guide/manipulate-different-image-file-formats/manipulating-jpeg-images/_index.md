---
title: การจัดการรูปภาพ JPEG
type: docs
weight: 30
url: /th/net/manipulating-jpeg-images/
---

## **การใช้คลาส ExifData เพื่ออ่านและแก้ไขแท็ก JPEG EXIF**
เกือบทุกกล้องดิจิทัล (รวมถึงสมาร์ทโฟน) สแกนเนอร์ และระบบอื่น ๆ ที่ประมวลผลรูปภาพบันทึกภาพพร้อมกับข้อมูล EXIF (Exchangeable Image File) ข้อมูลการตั้งค่ากล้องและข้อมูลประสิทธิภาพถูกบันทึกโดยกล้องลงในไฟล์รูปภาพ ข้อมูล EXIF รวมถึงความเร็วในการคอก, วันที่และเวลาที่ถ่ายภาพ, ความยาวโฟกัส, การปรับค่าไดออฟ, รูปแบบการวัดแสงและว่ามีการใช้แฟลชหรือไม่ Aspose.Imaging APIs ทำให้สามารถดึงข้อมูล EXIF ออกจากรูปภาพที่กำหนดไว้ได้อย่างง่ายดายและเรียบง่าย ผู้พัฒนาก็สามารถเขียนข้อมูล EXIF ลงในรูปภาพหรือแก้ไขข้อมูลที่มีอยู่ตามต้องการของตน Aspose.PSD ได้ให้ [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) คลาสสำหรับการอ่าน, เขียน และแก้ไขข้อมูล EXIF, ในขณะที่ [Aspose.PSD.Exif.Enums](
https://reference.aspose.com/psd/net/aspose.psd.exif.enums) นามเสมอฉบับที่ใช้ในกระบวนการ
### **การอ่านข้อมูล EXIF**
Aspose.PSD APIs มีวิธีการอ่านข้อมูล EXIF จากรูปภาพที่กำหนดไว้ด้านล่างเสดงตัวอย่างการใช้คลาส ExifData เพื่ออ่านข้อมูล EXIF จากภาพ
- โหลดรูปภาพ PSD โดยใช้วิธีการโรงงานโหลด
- ค้นหา Jpeg รูปย่อใน PSD ทรัพยากร
- ส่งออกอินสแตนซ์ของคลาส ExifData

ดึงข้อมูลที่ต้องการแล้วเขียนไปยังคอนโซล

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


เพิ่มเติม, ผู้พัฒนาสามารถได้รับข้อมูลเฉพาะโดยใช้โค้ดสุรทัศน์ต่อไปนี้

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **การเขียนและแก้ไขข้อมูล EXIF**
โดยใช้ Aspose.PSD APIs, ผู้พัฒนาสามารถเขียนข้อมูล EXIF ใหม่และแก้ไขข้อมูล EXIF ที่มีอยู่ของรูปภาพ กระบวนการทั้งสอง (การเขียนและการแก้ไข) ต้องการโหลดรูปภาพและดึงข้อมูล EXIF ไปยังอินสแตนซ์ของคลาส ExifData จากนั้นสามารถเข้าถึงคุณสมบัติที่เปิดเผยโดยคลาส ExifData เพื่อตั้งค่าตามความต้องการของตนโปรดทราบว่ารูปภาพที่ต้องการจัดการควรเป็นรูปภาพ Jpeg หรือรูปภาพไทฟฟ์ธัมน์ สรุปโค้ดที่แสดงการใช้งานดังนี้:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **สร้างรูปย่อจากรายการทรัพยากร PSD**
รูปย่อเป็นโหมดขนาดเล็กของรูปภาพ ใช้เพื่อแสดงส่วนสำคัญของรูปภาพแทนกรอบเต็ม เรื่องชื่อไฟลเอกสเป็ลชี (โดยเฉพาะรูปถ่ายด้วยกล้องดิจิทัล) มีรูปย่อฝังอยู่ในไฟลหรือไม่ Aspose.PSD API ช่วยให้คุณสามารถสร้างรูปย่อของทรัพยากร PSD และเก็บไว้อย่างแยกต่างหาก ทรัพยากรรูปย่อมีสมบัติ ExifData.[Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) สามารถดึงข้อมูลรูปย่อได้ โค้ดตัวอย่างที่ให้ด้านล่างสาธิตวิธีการใช้


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


ใช้วิธีการด้านบนเพื่อเก็บรูปย่อไปยังรูปแบบไฟลอื่นที่รองรับหากคุณต้องการส่งออกข้อมูลรูปย่อไปยังรูปแบบไฟลอื่น เช่น BMP & PNG โปรดใช้ตัวเลือกส่งภาพอื่น
### **สร้างรูปย่อจากส่วนตอบความ JFIF**
เป็นไปได้ที่จะสร้างรูปย่อจากส่วน ExifData หรือส่วน JFIF ของทรัพยากรรูปย่อ PSD โค้ดต่อไปนำเสนอวิธีการดำเนินการของการสกัดข้อมูลรูปย่อจาก JFIF หรือส่วน ExifData


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


ใชวิธีการดีขึ้นเพื่อเก็บรูปย่อไปยังรูปแบบไฟลที่รองรับดน่าว่าคุณต้องการส่งออรูปย่อไปยังรูปแบบไฟลอื่น เช่น BMP & PNG โปรดใช้ตัวเลือส่งภาพอืน
### **เพ่มรูปย่อไปยังส่วนตอบความ JFIF**
โค้ดตัวอย่างด้านล่างสาธิตวิธีใช้คุณสมบัติ JFIF. รูปย่อ เพื่ส่มรูปย่อไปยังส่วน JFIF ของรูป PSD ที่โหลด


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}


รูปย่อตัวอื่นที่มีข้อมูลส่วนไม่สามารถใช้พื้นที่มากกว่า 65,545 ไบต น่าว่างินรูปรูาเนื่องจากการมาตรการของรูปของ JPEG
### **เพ่มรูปย่อไปยังส่วนตอบความ EXIF**
โค้ดตัวอย่างด้านล่างสาธิตวิธีใช้คงสมบัติ ExifData. รูปย่อเพื่ทาได้รับร่าเรายย่ ไปย 62โหลดกิพ PSD ข ืน์ ย่อไปย การใช้ตัวเลือกส่งภาพอื่น


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


ในกรณีนี้, Aspose.PSD API ไม่สามารถประมาณขนาดรูปย่อ, แต็มาเป็นขนาดของชุดข้อมูล EXIF โปรดระมวงว่ามันไม่สามารถมากกว่า 65,535 ไบต
## **การใช้คลาส JpegExifData เพื่ออ่านและแทข EXIF Tags ของ Jpeg**
Aspose.PSD APIs ให้เป็น [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) คลาสที่เฉพาะเจา Jpeg รูปภาพเพื่อดึง & อัพเดตขขลEXIF รายละเอียด บทความนี้สาธิตที่ใช้ JpegExifData คลาสเพื่อทำเช่นเดียวกับนั้น คลาส Aspose.PSD.Exif.JpegExifData บรษ มท่อนโค้ดที่เปิดชวกดูต่องการทหติน์หและหาดวีดีดูได้ดังในต่องการต่อไป: 
 





{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **รานการเต็มขข EXIF Tags**
ท่อนโค้ดด้านบนอ่านหใบขEXIF Tags ใช้คุณสมบัติที่ให้โดยคลass JpegExifData เติมขอบ ก่ายลลจีกินิ ถ็น๋ 5์ [System.Reflection.PropertyInfo
(https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0) เพื่ออ่าน โหลดรกม่ต่องัทั้งหมดTagsตอนตาิห้าิ็


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **การปรับปรุงการหันกลิตมขขท JEPG Images**
รูปภาพสมมคดำตรกิชงณีหร้าะ่ต ถ้าดม้่สงอิห ดใจิญดไมีก มุแคืดำถ์็ทัน่ึารสกภั่  IF ด้ จขไมีปด้่คุูกุทิปมิำีทแสดอํัจ๊ิฐฮทุัธบไันใึก็ดิ. ID UF ทิปุปตีี่ เป็แด์ี้ิงำยีัน่าดีทงด้าใ..ด..ศแง้ดดตไม.แนด้า.ช้ิ่าด่มบีไม... ี่ย


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **สนับรotas55-JC9 ด้za255**


F. UF ีสี.ii่ีี็ี.it.coี่ิา่า.์พ็.าดีตด็.บ.ด่.ี็.ี้์I.uf ียS F ทเ้้UF 59.i.coี่ิ์พือN... f.ีุี.งี์บา.B.ดี   


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **จสzunggur 482าC**


Q. WkW.คG.3..4.n.์ห.กตีUI.U.MainJ.3..S..4....ktีเ.บ..ีิ...ี.ว
