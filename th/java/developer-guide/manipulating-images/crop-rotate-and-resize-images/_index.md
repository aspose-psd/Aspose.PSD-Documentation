---
title: ตัดภาพ หมุนและปรับขนาดภาพ
type: docs
weight: 40
url: /th/java/crop-rotate-and-resize-images/
---

## **การตัดภาพ**
การตัดภาพ通常หมายถึงการลบส่วนด้านนอกของภาพเพื่อช่วยปรับปรุงกรอบภาพได้ การตัดภาพอาจใช้เพื่อตัดออกบางส่วนของภาพเพื่อเพิ่มการโฟกัสในพื้นที่เฉพาะบางส่วนเช่นกัน  API Aspose.PSD รองรับวิธีการตัดภาพให้กับภาพได้อย่างสองวิธีคือ โดยการเลื่อนและโดยรูปสี่เหลี่ยม
### **การตัดโดยการเลื่อน**
คลาส RasterImage มีเวอร์ชันอัพโหลดของเมธอด Crop ที่ใช้ 4 ค่าจำนวนเต็มที่บ่งบอก แถบซ้าย แถบขวา ด้านบนและด้านล่าง ขึ้นอยู่กับการค่าที่สี่นี้เมธอด Crop จะย้ายขอบภาพไปทางกลางของภาพในขณะที่ทิ้งส่วนด้านนอกไป Code snippet ด้านล่างแสดงตัวอย่างการตัดภาพโดยการเลื่อน

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **การตัดโดยรูปสี่เหลี่ยม**
คลาส RasterImage มีเวอร์ชันอัพโหลดอีกตัวของเมธอด Crop ที่ใช้ตัวอย่างของคลาส Rectangle คุณสามารถตัดส่วนใดๆของภาพโดยการให้ขอบที่ต้องการให้กับออบเจกต์ Rectangle โค้ดสำเร็จรูปด้านล่างแสดงตัวอย่างการตัดภาพใดๆด้วยรูปสี่เหลี่ยม

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **หมุนและพลิกภาพ**
Aspose.PSD for Java เป็นไลบรารีที่ใช้ง่ายเพราะมีเมทอดง่ายๆ ในการทำการดำเนินการที่ซับซ้อน เช่น Aspose.PSD for Java ได้ให้เมทอด RotateFlip สำหรับคลาสหลักของมันคือ Image หากประยุกต์ใช้งานต้องการหมุนภาพ โดยไม่คำนึงถึงรูปแบบภาพไลบรารีสามารถแสดงกระบวนการหมุนและพลิกที่เฉพาะเป็นไปตามนั้น
### **การหมุนภาพ**
Mแมธอด Image.RotateFlip สามารถใช้หมุนภาพได้ 90/180/270 องศาและพลิกภาพแนวนอนหรือแนวตั้ง Image.RotateFlip ยอมรับพารามิเตอร์ของ RotateFlipType ซึ่งระบุประเภทการหมุนและพลิกที่จะใช้กับภาพ ขั้นตอนในการทำการหมุนและพลิกง่ายมากดังต่อไปนี้

1. โหลดภาพโดยใช้วิธีการโหลดที่เปิดเผยโดยคลาส Image
1. เรียกใช้ Image.RotateFlip พร้อมกับการระบุ RotateFlipType ที่เหมาะสม
1. บันทึกผลลัพธ์

ตัวอย่างโค้ดด้านล่างแสดงวิธีการตั้งค่า RotateFlip ของอิมเมจและการนับถอยหลัก

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **หมุนภาพในมุมที่ระบุ**
อิมพลีเมนท์ Aspose.PSD for Java API การหมุนหมุน RasterImage. Rotate เพื่อให้ความสะดวกสำหรับผู้ใช้ที่ต้องการหมุนภาพในมุมที่ระบุ ไม่เหมือนกับเมธอด RasterImage.RotateFlip เมธอด RasterImage.Rotate ยอมรับพารามิเตอร์สามตัว:

1. มุมการหมุน: พารามิเตอร์ชนิด float ระบุมุมการหมุนภาพที่หารต้องการหมุน ค่าบวกจะหมุนภาพตามเข็มนาฬิกา; ค่าลบจะทำการหมุนทวนเข็มนาฬิกา
1. ขยายอัตราส่วน: พารามิเตอร์ประเภทบูลีนระบุว่าขนาดภาพจะเปลี่ยนตามการโครงอัฟของเหลี่ยมที่หมุนไป หากตั้งค่าเป็นเท็จ มิติของภาพจะไม่เปลี่ยนและเฉพาะเนื้อหาภาพภายในที่หมุน
1. สีพื้นหลัง: พารามิเตอร์ประเภทสีระบุสีที่จะเติมในพื้นหลังของภาพที่หมุน

ตัวอย่างโค้ดด้านล่างแสดงการใช้งานของ RasterImage.Rotate เมธอด

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **ปรับขนาดภาพ**
บทความนี้จะสาธิตการใช้ Aspose.PSD for Java เพื่อทำการปรับขนาดภาพ API Aspose.PSD ได้เปิดหลักการที่ใช้งานได้ง่ายและมีประสิทธิภาพเพื่อไปสู่จุดหมายนี้ Aspose.PSD for Java ได้เปิดเมธอดปรับขนาดสำหรับคลาส Image ซึ่งสามารถใช้ปรับขนาดภาพที่มีอยู่บนที่สด There are two overloads of the Resize method to suit the application needs.
### **การปรับขนาดแบบง่าย**
ขั้นตอนในการทำการปรับขนาดง่ายดังต่อไปนี้

1. Load in image using the factory method Load exposed by Image class.
1. Call the Image.Resize method while specifying new Height & Width.
1. บันทึกผลลัพธ์.

ที่ตัวอย่างโค้ดด้านล่างแสดงวิธีการปรับขนาดภาพ

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **ปรับขนาดด้วย ResizeType Enumeration**
API Aspose.PSD ได้เปิดขึ้นใช้ว่า ResizeType enumeration ที่สามารถใช้กับ Image.Resize เพื่อให้ความสมบูรณ์ โค้ดถี่ที่โดยต้องการให้ค่า ResizeType enumeration ในขณะที่รายละเอียดของ จะมองเห็นที่ด้านล่างของหน้านี้

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}



หากคุณตั้งใจที่จะได้ผลลัพธ์ที่ดีหลังจากการปรับขนาดให้ใช้ ResizeType.LanczosResample เพราะมันจะให้ผลลัพธ์ที่มีคุณภาพสูง แต่อาจจะทำงานช้ากว่า ResizeType.NearestNeighbourResample อีกทั้ง ResizeType.NearestNeighbourResample ถูกใช้เพื่อปรับขนาดอย่างรวดเร็วในขณะที่คุณภาพของภาพย่อ วิธีนี้อาจมีประโยชน์สำหรับการสร้างตัวอย่างย่อในเวลาจริงหรือกระบวนการที่คล้ายกันซึ่งต้องการประสิทธิภาพ
## **ปรับขนาดภาพอย่างสัมพันธ์**
คุณสามารถปรับขนาดภาพโดยการส่งค่าความสูงและความกว้างใหม่เป็นพารามิเตอร์ไปยังเมธอด Image.Resize แต่ในกรณีนี้คุณต้องคำนวณอัตราส่วนด้วยตัวเอง เนี่ยเพราะเมื่อความกว้างหรือความสูงของภาพถูกเปลี่ยนแปลงภาพจะถูกขยายหรือย่ำเพื่อเติมขนาดใหม่ . หากมีการเปลี่ยนแปลงทวารหน้าและความสูงของภาพไม่สัมพันธ์นี้อาจทำให้ได้ผลลัพธ์ที่ถูกยืดและเบิดหยาง บทความนี้สาธิตการใช้งาน Aspose.PSD สำหรับ API Java เพื่อปรับขนาดภาพโดยการส่งค่าความสูงหรือความกว้างใหม่ในขณะที่อนุญาตให้ API คำนวณค่าอัตราส่วนอื่นอย่างอัติโธยค้า

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **ResizeType Enumeration**
ResizeType ระบุประเภทของการปรับขนาดภาพที่จะนำมาใช ตามตัวกรองที่เลือก

สมาชิกของ ResizeType Enumeration

|**ชื่อสมาชิก**|**ค่า**|**รายละเอียด**|
| :- | :- | :- |
|LeftTopToLeftTop|0|จุดนำด้ามซ้ายของภาพใหม่จะตรงกับจุดด้ามซ้ายของภาพดั้มเดิย การตัดภาพจะเกิดขึ้นหากจำเป็นแล้ว|
|RightTopToRightTop|1|จุดด้ามด้านขวาของภาพใหม่จะตรงกับจุดด้ามด้านขวาของภาพดั้มเดิย การตัดภาพจะเกิดขึ้นหากจำเป็นแล้ว|
|RightBottomToRightBottom|2|จุดด้ามด้านขวาล่างของภาพใหม่จะตรงกับจุดด้ามด้านขวาล่างของภาพดั้มเดิย การตัดภาพจะเกิดขึ้นหากจำเป็นแล้ว|
|LeftBottomToLeftBottom|3|จุดด้ามด้านล่างซ้ายของภาพใหม่จะตรงกับจุดด้ามด้านล่างซ้ายของภาพดั้มเดิย การตัดภาพจะเกิดขึ้นหากจำเป็นแล้ว|
|CenterToCenter|4|จุดกลาง
