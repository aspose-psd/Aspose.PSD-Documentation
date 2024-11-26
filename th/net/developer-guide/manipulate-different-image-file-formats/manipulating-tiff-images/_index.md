---
title: การจัดการภาพ TIFF
type: docs
weight: 50
url: /th/net/manipulating-tiff-images/
---

## **เพิ่มกรอบด้วยการตั้งค่าต่าง ๆ**
TIFF เป็นรูปแบบที่ยืดหยุ่นมาก และช่วยให้สามารถเพิ่มเฟรมต่าง ๆ ลงไปได้ โดยมีขนาดและการบีบอัดที่แตกต่างกันได้ Aspose.PSD APIs ช่วยให้คุณสามารถเพิ่มเฟรม TIFF ใดๆ ที่มีขนาดใดก็ได้ซึ่งจะช่วยในการสร้างเอกสารที่ซับซ้อน หากมีความต้องการที่จะปรับเฟรมระหว่างขั้นตอนเพื่อให้ทุกอย่างเท่ากัน คุณสามารถดำเนินการตามขั้นตอนดังต่อไปนี้:

- สร้างเฟรมใหม่โดยเปล่าหรือคัดลอกเฟรมต้นฉบับโดยระบุตัวเลือกผลลัพธ์ด้วยวิธี CreateFrameFrom
- เปลี่ยนขนาดเฟรม/รูปภาพต้นฉบับเป็นขนาดที่กำหนดด้วยวิธี Resize
- เพิ่มพิกเซลของเฟรม/รูปภาพต้นฉบับลงในเฟรมใหม่
- เพิ่มเฟรมใหม่ลงในภาพ TIFF ผลลัพธ์

## **ส่งออกเลเยอร์ของรูปภาพ PSD ไปยังรูปแบบไฟล์ Tiff หลายหน้า**
บางครั้งคุณอาจจำเป็นต้องส่งออกเลเยอร์รูปภาพ PSD ไปยังรูปแบบไฟล์ Tiff หลายหน้า บทความนี้จะสาธิตวิธีการดำเนินการนี้โดยใช้ Aspose.PSD for .NET API เริ่มต้นจากการโหลดรูปภาพ PSD จากดิสก์ จากนั้นเราจะไล่เลียนเลเยอร์รูปภาพ PSD และสร้าง TiffFrame จากเลเยอร์ที่เกี่ยวข้อง สุดท้ายเราจะบันทึกภาพ Tiff ผลลัพธ์ลงในไฟล์เดียวเท่านั้นบนดิสก์

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}

## **การกำหนด TiffOptions**
ผู้พัฒนาสามารถปรับแต่งคุณสมบัติต่าง ๆ ของคลาส [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) เพื่อให้ได้ผลลัพธ์ตามที่ต้องการ ในเอกสารนี้ เราจะให้ความสำคัญใน 4 คุณสมบัติหลักที่ควบคุมคุณลักษณะของภาพที่ผลลัพธ์ออกมา

คุณสมบัติเหล่านี้รายงานด้านล่าง

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

เมื่อเราเข้าหน้า TiffOptions โครงสร้างเปล่า จะถูกตั้งค่าในค่าเริ่มต้นของมัน เช่นการบีบอัดถูกตั้งค่าเป็น None BitsPerSample ถูกตั้งเป็น 1 และ Photometric เป็น MinIsWhite การบันทึกไปในรูปแบบนี้จะทำให้ภาพสุดท้ายเป็นขาวดำและนี่คือพฤติกรรมที่คาดหวังสำหรับส่วนผสานดังกล่าว เพื่อให้ได้ผลลัพธ์สี คุณต้องตั้งค่าทุกคุณสมบัติข้างต้นเป็นค่าที่สอดคล้องกับพื้นที่สีที่ต้องการหรือคุณสามารถเริ่มโครงสร้าง TiffOptions ด้วยการตั้งค่าที่กำหนดไว้ล่วงหน้าไว้ในบทความนี้ ด้านล่างจะมีตารางที่อธิบายค่าพารามิเตอร์ที่คุณควรตั้งเพื่อให้ได้ผลลัพธ์ตามที่ต้องการ โปรดทราบว่าคุณควรตั้งค่า 4 คอลัมน์ ผ่าน TiffOptions เพื่อบันทึกภาพใด ๆ ที่โหลด/สร้างในรูปแบบ TIFF

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/ไม่บีบอัด|1/4/8/16 (ตารางสี, โหมดสี) ช่องเดียวเท่านั้น|ไม่มี|
|MinIsWhite/MinIsBlack|LZW/ไม่บีบอัด|1/4/8/16 (โหมดพรางเกลียว) ช่องเดียวเท่านั้น|ไม่มี|
|Palette|LZW/ไม่บีบอัด|8 (ตารางสี, โหมดสี) ช่องเดียวเท่านั้น|แนวนอน (ได้รับการบีบอัดมากขึ้นสำหรับ LZW แบบเดียวกัน)|
|MinIsWhite/MinIsBlack|LZW/ไม่บีบอัด|8 (โหมดพรางเกลียว) ช่องเดียวเท่านั้น|แนวนอน (ได้รับการบีบอัดมากขึ้นสำหรับ LZW แบบเดียวกัน)|
|RGB|LZW/ไม่บีบอัด|[8,8,8] (3 ช่องสี RGB)|ไม่มี/แนวนอน|
|RGB|LZW/ไม่บีบอัด|[8,8,8,8] (3 ช่องสี RGB และช่อง alpha เพิ่มเติมสามารถตั้งค่าผ่าน TiffOptions.AlphaStorage) โดยที่การสนับสนุนจำนวนช่องเพิ่มเติมสามารถทำได้ แต่ในแต่ละช่องจะต้องมีขนาด 8 บิตเช่น [8,8,8,8,8,8]|ไม่มี/แนวนอน|
คุณต้องตั้งค่าทั้ง 4 คุณค่าผ่าน TiffOptions เพื่อบันทึกภาพใด ๆ ในรูปแบบ Tiff หากใช้ค่าผสมที่ต่างกัน บางซอฟต์แวร์แสดงภาพที่ได้ไม่ถูกต้อง (รวมถึง Windows Photo Viewer) เนื่องจากการสนับสนุนจำกัดที่พวกเขามี ในกรณีนี้ โปรดเลือกซอฟต์แวร์แสดงที่แตกต่างสำหรับการทดสอบของคุณ

### **ตั้งค่าที่กำหนดไว้ล่วงหน้าสำหรับคลาส TiffOptions**
เพื่อให้ผู้ใช้สะดวกและหลีกเลี่ยงการกำหนดค่า TiffOptions ผิด  Aspose.PSD for .NET API ได้เปิดเผยตัวกำหนดโครงสร้างใหม่ที่ยอมรับพารามิเตอร์ประเภท [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat) ที่เลือกจากอาร์เรย์ TiffExpectedFormat  ตามความเหมาะสม โครนเล็กจะกำหนดค่าโครงสร้างทุกคุณสมบัติที่จำเป็นสำหรับตัวอย่างการใช้งานที่ต้องการ ก่อนที่เราจะไปสู่รหัสตัวอย่าง นี่คือรายชื่อของฟิลด์ TiffExpectedFormat และรายละเอียดของมันสำหรับการเข้าใจวิธีการใช้อย่างดี

- TiffExpectedFormat.Default: การตั้งค่าฟิลด์เป็นค่าเริ่มต้นจะทำงานเหมือนกับคอนสตรัคเตอร์เริ่มต้นของคลาส TiffOptions โดยไม่มีการกำหนดการบีบอัดและ BitsPerPixel ที่กำหนดเป็น 1 เพื่อให้ได้ผลลัพธ์ขาวดำ แนะนำให้ใช้ฟิลด์นี้เมื่อคุณตั้งค่าคุณสมบัติที่เฉพาะเจาะจงตามที่ต้องการ
- TiffExpectedFormat.TiffCcitRle: พิเศษเฉพาะการเข้ารหัส RLE ขณะบันทึกผลลัพธ์ในรูปแบบ 1 BitsPerPixel (ขาวดำ) ของ TIFF
- TiffExpectedFormat.TiffCcittFax3: พิเศษเฉพาะการเข้ารหัส CCITT Fax3 ขณะบันทึกผลลัพธ์ในรูปแบบ 1 BitsPerPixel (ขาวดำ) ของ TIFF
- TiffExpectedFormat.TiffCcittFax4: พิเศษเฉพาะการเข้ารหัส CCITT Fax4 ขณะบันทึกผลลัพธ์ในรูปแบบ 1 BitsPerPixel (ขาวดำ) ของ TIFF
- TiffExpectedFormat.TiffDeflateBW: พิเศษเฉพาะการบีบอัด Deflate ขณะบันทึกผลลัพธ์ในรูปแบบ 1 BitsPerPixel (ขาวดำ) ของ TIFF
- TiffExpectedFormat.TiffDeflateRGB: พิเศษเฉพาะการบีบอัด Deflate ขณะบันทึกผลลัพธ์ในรูปแบบสี RGB ของ TIFF
- TiffExpectedFormat.TiffJpegRGB: พิเศษเฉพาะการบีบอัด Jpeg ขณะบันทึกผลลัพธ์ในรูปแบบสี RGB ของ TIFF
- TiffExpectedFormat.TiffJpegYCBCR: พิเศษเฉพาะการบีบอัด Deflate ขณะบันทึกผลลัพธ์ในรูปแบบสี YCBCR ของ TIFF
- TiffExpectedFormat.TiffLzwBW: พิเศษเฉพาะการบีบอัด LZW ขณะบันทึกผลลัพธ์ในรูปแบบ 1 BitsPerPixel (ขาวดำ) ของ TIFF
- TiffExpectedFormat.TiffLzwRGB: พิเศษเฉพาะการบีบอัด LZW ขณะบันทึกผลลัพธ์ในรูปแบบสี RGB ของ TIFF
- TiffExpectedFormat.TiffLzwRGBA: พิเศษเฉพาะการบีบอัด LZW ขณะบันทึกผลลัพธ์ในรูปแบบ RGBA (สีพร้อมความโปร่งแสง) ของ TIFF
- TiffExpectedFormat.TiffNoCompressionBW: พิเศษเฉพาะรูปแบบ TIFF ที่ไม่บีบอัดขณะบันทึกผลลัพธ์ใน 1 BitsPerPixel (ขาวดำ)
- TiffExpectedFormat.T
