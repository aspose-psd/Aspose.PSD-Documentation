---
title: การจัดการกับรูปแบบ Adobe Illustrator
type: docs
weight: 10
url: /th/net/manipulating-adobe-illustrator-formats/
---

## **ส่งออกไฟล์ AI เป็น PSD**
ด้วย Aspose.PSD for .NET, นักพัฒนาสามารถแปลงไฟล์ Adobe Illustrator เป็นรูปแบบ PSD ได้ หัวข้อนี้อธิบายวิธีการโหลดไฟล์ AI ที่มีอยู่และแปลงเป็น PSD โดยใช้คลาส [PsdOptions](https://reference.aspose.com/net/psd/aspose.psd.imageoptions/psdoptions) 

ขั้นตอนในการแปลงไฟล์ AI เป็น PSD ง่ายมากดังนี้:

- สร้างอินสแตนซ์ของ AiImage และโหลดภาพโดยใช้วิธีการ Load ของ Image class
- สร้างอินสแตนซ์ของ [PsdOptions](https://reference.aspose.com/net/psd/aspose.psd.imageoptions/psdoptions) คลาส
- เรียกใช้เมธอด AiImage.Save พร้อมที่อยู่ปลายทางและอินสแตนซ์ของ PsdOptions 

ด้านล่างเช่นตัวอย่างรหัสที่ให้เห็นวิธีการส่งออก AI เป็น PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-AI-AIToPSD-AIToPSD.cs" >}}
## **ส่งออกไฟล์ AI เป็น JPEG**
ด้วย Aspose.PSD for .NET, นักพัฒนาสามารถแปลงไฟล์ Adobe Illustrator เป็นรูปแบบ JPEG ได้ หัวข้อนี้อธิบายวิธีการโหลดไฟล์ AI ที่มีอยู่และแปลงเป็น JPEG โดยใช้คลาส [JpegOptions](https://reference.aspose.com/net/psd/aspose.psd.imageoptions/jpegoptions) 

ขั้นตอนในการแปลงไฟล์ AI เป็น JPEG ง่ายมากดังนี้:

- สร้างอินสแตนซ์ของ AiImage และโหลดภาพโดยใช้วิธีการ Load ของ Image class
- สร้างอินสแตนซ์ของ [JpegOptions](https://reference.aspose.com/net/psd/aspose.psd.imageoptions/jpegoptions) คลาส
- ตั้งคุณสมบัติของภาพ [คุณภาพ](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/quality)
- เรียกเมธอด [AiImage](https://reference.aspose.com/psd/net/aspose.psd/fileformats.ai/aiimage).[Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save) พร้อมที่อยู่ปลายทางและอินสแตนซ์ของ JpegOptions 

ด้านล่างเช่นตัวอย่างรหัสที่ให้เห็นวิธีการส่งออก AI เป็น JPEG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-AI-AIToJPG-AIToJPG.cs" >}}
## **ส่งออกไฟล์ AI เป็น GIF**
Aspose.PSD for .NET มีคลาส **AiImage** เพื่อโหลดไฟล์ Adobe Illustrator และสามารถใช้ไฟล์ดังกล่าวเพื่อส่งออกไฟล์ AI เป็นรูปแบบ GIF ตัวอย่างนี้แสดงการใช้ Aspose.PSD for .NET API เพื่อส่งออกไฟล์ AI เป็นรูปภาพ GIF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-AI-AIToGIF-AIToGIF.cs" >}}
## **ส่งออกไฟล์ AI เป็น PNG**
ด้วย Aspose.PSD for .NET, นักพัฒนาสามารถแปลงไฟล์ Adobe Illustrator เป็นรูปแบบ PNG ได้ หัวข้อนี้อธิบายวิธีการโหลดไฟล์ AI ที่มีอยู่และแปลงเป็น PNG โดยใช้คลาส [PngOptions](https://reference.aspose.com/net/psd/aspose.psd.imageoptions/pngoptions) 

ขั้นตอนในการแปลงไฟล์ AI เป็น PNG ง่ายมากดังนี้:

- สร้างอินสแตนซ์ของ AiImage และโหลดภาพโดยใช้วิธีการ Load ของ Image class
- สร้างอินสแตนซ์ของ [PngOptions](https://reference.aspose.com/net/psd/aspose.psd.imageoptions/pngoptions) คลาส
- ตั้งคุณสมบัติ [ประเภทของสี](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/colortype)
- เรียกเมธอด AiImage.Save พร้อมที่อยู่ปลายทางและอินสแตนซ์ของ PngOptions 

ด้านล่างเช่นตัวอย่างรหัสที่ให้เห็นวิธีการส่งออก AI เป็น PNG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-AI-AIToPNG-AIToPNG.cs" >}}
## **ส่งออกไฟล์ AI เป็น TIFF**
Aspose.PSD for .NET มีคลาส **AiImage** เพื่อโหลดไฟล์ Adobe Illustrator และสามารถใช้ไฟล์ดังกล่าวเพื่อส่งออกไฟล์ AI เป็นรูปแบบ TIFF ตัวอย่างนี้แสดงการใช้ Aspose.PSD for .NET API เพื่อส่งออกไฟล์ AI เป็นรูปภาพ TIFF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-AI-AIToTIFF-AIToTIFF.cs" >}}
## **รูปภาพแบบราสเตอร์ใน Illustrator**
[Aspose.PSD for .NET](https://products.aspose.com/psd/net) ตอนนี้สนับสนุนรูปภาพแบบราสเตอร์ในไฟล์รูปภาพรูปแบบ Adobe Illustrator ต่อไปนี้คือรหัสที่สาธิตวิธีการโหลดการตั้งค่าของรูปภาพแบบราสเตอร์ในไฟล์รูปภาพรูปแบบ Adobe Illustrator.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-AI-SupportOfRasterImagesInAI-SupportOfRasterImagesInAI.cs" >}}
