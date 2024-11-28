---
title: การแปลงรูปภาพ
type: docs
weight: 20
url: /th/net/converting-images/
---

## **การแปลงรูปภาพเป็นขาวดำและระดับสีเทา**
บางครั้งคุณอาจต้องการที่จะแปลงรูปภาพสีเป็นขาวดำหรือระดับสีเทาสำหรับการพิมพ์หรือเก็บถาวรไว้ บทความนี้จะสาธิตการใช้ Aspose.PSD สำหรับ .NET API เพื่อบรรลุการนี้โดยใช้วิธีการสองตัวดังนี้

- การทำภาพกลม
- การทำสีเทา

### **การทำภาพกลม**
เพื่อเข้าใจแนวคิดของการทำภาพกลม สำคัญที่จะประกาศรูปภาพจากฐานสองที่เป็นรูปภาพดิจิตอลที่มีเพียงค่าสองค่าสำหรับแต่ละพิกเซล โดยปกติสีสองสีที่ใช้สำหรับรูปภาพกลมคือสีดำและสีขาวถึงท่านสองสีอื่น ๆ สามารถนำมาใช้ได้ การทำภาพกลมคือกระบวนการที่ทำให้รูปเป็นขั้นที่สองหมายความว่าแต่ละพิกเซลถูกเก็บในรูปแบบเดี่ยวเดียว (0 หรือ 1) ที่ 0 หมายถึงการขาดสีและ 1 หมายถึงสีมีอยู่ ในปัจจุบัน Aspose.PSD สำหรับ .NET API รองรับวิธีการทำภาพกลมสองวิธี
#### **การทำภาพกลมด้วยฟิกซ์ทรีเชิล**
โค้ดตัวอย่างต่อไปนี้จะแสดงถึงวิธีการใช้ฟิกซ์ทรีชิลให้นำไปใช้กับรูปภาพ


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **การทำภาพกลมด้วยฟิกซ์ออตซุ**
โค้ดตัวอย่างต่อไปนี้แสดงถึงวิธีการใช้การทำภาพกลมด้วยฟิกซ์ออตซุให้นำไปใช้กับรูปภาพ


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **การทำสีเทา**
การทำสีเทาคือกระบวนการที่ทำให้รูปภาพที่มีโทนสีต่อเนื่องเป็นรูปภาพที่มีโทนสีเทาไม่ต่อเนื่อง โค้ดตัวอย่างต่อไปนี้จะแสดงถึงวิธีการใช้การทำสีเทา


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}

## **แปลงเลเยอร์รูปภาพ GIF เป็นรูปภาพ TIFF**
บางครั้งจะต้องการสกัดและแปลงเลเยอร์ของรูปภาพ PSD เป็นรูปแบบภาพราสเตอร์อื่นเพื่อตอบโตกับความต้องการของแอปพลิเคชัน Aspose.PSD API สนับสนุนคุณสมบัติในการสกัดและแปลงเลเยอร์ของรูปภาพ PSD เป็นรูปแบบภาพราสเตอร์อื่นก่อนที่จะสร้างอินสแตนซ์ของรูปภาพและโหลดรูปภาพ PSD จากดิกส์ภาพภายใน จากนั้นเราจะวนรอบแต่ละเลเยอร์ในคุณสมบัติเลเยอร์ จากนั้นเราจะแปลงบล็อกเป็นรูปภาพ TIFF โค้ดตัวอย่างต่อไปนี้แสดงถึงวิธีการแปลงเลเยอร์รูปภาพ PSD เป็นรูปภาพ TIFF


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}

## **การแปลง CMYK PSD เป็น CMYK TIFF**
ใช้ Aspose.PSD สำหรับ .NET, นักพัฒนาสามารถแปลงไฟล์ CMYK PSD เป็นรูปแบบ tiff CMYK บทความนี้จะแสดงวิธีการส่งออก/แปลงไฟล์ CMYK PSD เป็นรูปแบบ tiff CMYK ด้วย Aspose.PSD สำหรับ .NET คุณสามารถโหลดรูปภาพ PSD และจากนั้นคุณสามารถกำหนดคุณสมบัติต่าง ๆ โดยใช้ [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) คลาส และบันทึกหรือส่งออกภาพ โค้ดตัวอย่างต่อไปนี้แสดงวิธีการบรรลุคุณสามารถทำเช่นนี้


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}

## **ส่งออกรูปภาพ**
นอกจากชุดคำสั่งประมวลรูปภาพที่หลากหลาย Aspose.PSD ยังมีคลาสที่พิเศษที่ให้การแปลงรูปภาพ PSD ไปยังรูปแบบอื่น ๆ การใช้ไลบรารี่นี้ การแปลงรูปภาพ PSD ง่ายและ intuitive ด้านล่างคือคลาสพิเศษสำหรับวัตถุนี้ใน [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) namespace.

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

การส่งออกรูปภาพ PSD ด้วย Aspose.PSD สำหรับ .NET API ง่ายมาก ทุกสิ่งที่คุณต้องการก็คืออ็อบเจกต์ของคลาสที่เหมาะสมจาก [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) namespace โดยใช้อ็อบเจกต์เหล่านี้ คุณสามารถส่งออกรูปภาพใด ๆ ที่สร้าง แก้ไข หรือเพียงแค่โหลดด้วย Aspose.PSD สำหรับ .NET ไปยังรูปแบบที่สนับสนุน
## **รวมรูปภาพ**
ตัวอย่างนี้ใช้คลาส Graphics และแสดงวิธีการรวมรูปภาพสองหรือมากกว่าในรูปภาพเดียวกัน โดยให้มองเห็นการดำเนินการตัวอย่างเช่นตัวอย่างสร้างภาพ PsdImage ใหม่และวาดรูปภาพบนพื้นผิวแคนวาดโดยใช้เมธอดวาดรูปภาพที่เปิดเผยโดยคลาส Graphics ด้วยการใช้ Graphics class รูปภาพสองอันหรือมากกว่าสามารถรวมกันในรูปภาพเดียวกันได้อย่างไรว่ารูปภาพที่ได้มาจะดูเหมือนเป็นรูปภาพเดียวกันกับไม่มีช่องว่างระหว่างส่วนของรูปภาพและไม่มีหน้า ขนาดแคนวาจะตรงกับขนาดของรูปภาพผลลัพธ์ ต่อไปคือการสาธิตการแสดงวิธีใช้ [วาดรูปภาพ](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) ของคลาส [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) เพื่อแสดงวิธีใช้รูปภาพหลายรูปภาพในรูปภาพเดียว


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}

## **ขยายและครอบรูปภาพ**
Aspose.PSD API ช่วยให้คุณสามารถขยายหรือครอบรูปภาพขณะกระบวนการแปลงรูปภาพ นักพัฒนาจำเป็นต้องสร้างสี่เหลี่ยมพื้นที่ด้วยตำแหน่งและความสูงขนาดสี่เหลี่ยม ตัวอย่าง X, Y และความกว้าง, ความสูงของสี่เหลี่ยมจะแสดงถึงการขยายหรือครอบภาพที่โหลดมาได้ หากต้องการขยายหรือครอบรูปภาพขณะกระบวนการแปลงรูปภาพ กระทำตามขั้นตอนต่อไปนี้:

1. สร้างอินสแตนซ์ของคลาส [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) และโหลดรูปภาพที่มีอยู่
1. สร้างอินสแตนซ์ของ ImageOption
1. สร้างอินสแตนซ์ของคลาส [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) และเริ่มต้นค่า X, Y และ Width, Height ของสี่เหลี่ยม
1. เรียกเมธอด [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) ของคลาส RasterImage พร้อมกับการส่งออกชื่อไฟล์, คำสั่งทางรูปภาพและอ็อบเจกต์สี่เหลี่ยมเป็นพารามิเตอร์


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}

## **อ่านและเขียนข้อมูล XMP กับรูปภาพ**
XMP (Extensible Metadata Platform) เป็นมาตราฐานของ ISO XMP มาตรจวรทางข้อมูล รูปแบบการเชิงลึก, รูปแบบการเซรีไลซ์กระทำและคุณสมบัติหลักสำหรับกำหนดและประมวลข้อมูลแบบเซรีไลซ์ มันยังมีข้อบังคับสำหรับการฝังข
