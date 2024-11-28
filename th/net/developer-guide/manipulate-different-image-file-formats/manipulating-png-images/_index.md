---
title: การจัดการกับรูปภาพ PNG
type: docs
weight: 40
url: /th/net/manipulating-png-images/
---

## **ระบุความโปร่งใสสำหรับรูปภาพ PNG**
หนึ่งในข้อดีของการบันทึกรูปภาพในรูปแบบ PNG คือ PNG สามารถมีพื้นหลังโปร่งใสได้ Aspose.PSD สำหรับ .NET มีคุณสมบัติในการระบุความโปร่งใสสำหรับรูปภาพ PNG และรูปภาพแบบเรสเตอร์เช่นที่แสดงในส่วนด้านล่างนี้ Aspose.PSD สำหรับ .NET API สามารถใช้เพื่อตั้งค่าสีใดก็ได้ให้โปร่งใสขณะสร้างรูปภาพ PNG ใหม่หรือแปลงรูปภาพที่มีอยู่เป็นรูปแบบ PNG เพื่อวัตถุประสงค์เหล่านั้น Aspose.PSD สำหรับ .NET API ได้เปิดเผยคุณสมบัติ [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) และการจำแนกประเภทสีของ PngColorType ที่สามารถตั้งได้เพื่อระบุสีใดเป็นทรานสปาร์เรนต์ในภาพ PNG โค้ดย่อยที่ให้ไว้ด้านล่างแสดงตัวอย่างการแปลงภาพ PSD ที่มีอยู่เป็นภาพ PNG โดยระบุสีที่ต้องการให้โปร่งใส

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.cs" >}}
## **กำหนดความละเอียดสำหรับรูปภาพ PNG**
Aspose.PSD สำหรับ .NET เปิดเผยคลาส ResolutionSetting ซึ่งสามารถใช้เพื่อกำหนดความละเอียดสำหรับภาพทุกประเภทรวมทั้ง PNG บทความนี้สาธิตการใช้ Aspose.PSD สำหรับ .NET API เพื่อกำหนดพารามิเตอร์ความละเอียดแนวนอนและแนวตั้งสำหรับรูปภาพ PNG โค้ดย่อยด้านล่างโหลดภาพ PSD ที่มีอยู่และแปลงเป็นรูปแบบ PNG โดยเปลี่ยนความละเอียด

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.cs" >}}
## **บีบอัดไฟล์ PNG**
Portable Network Graphic (PNG) เป็นรูปแบบการบีบอัดที่ไม่สูญเสียสำหรับการส่งข้อมูลในรูปภาพบิทแมพผ่านเครือข่าย เมื่อคุณบันทึกรูปภาพเป็นไฟล์ PNG ในโปรแกรมใดๆ คุณอาจถูกถามให้เลือกระดับการบีบอัดในช่วงตั้งแต่ 0 ถึงระดับสูงสุด การกำหนดค่านี้จริงๆ แล้วจะบีบอัดขนาดไฟล์และไม่ลดคุณภาพของภาพบทความนี้อธิบายถึงว่า Aspose.PSD APIs ช่วยให้คุณควบคุมขนาดไฟล์ PNG ได้ Aspose.PSD APIs สามารถใช้เพื่อกำหนดระดับการบีบอัดสำหรับรูปแบบไฟล์ PNG โดยใช้คลาส PngOptions ที่มี [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel) อยู่ในรูปแบบ int property คุณสมบัตินี้ยอมรับค่าตั้งแต่ 0 ถึง 9 โดยที่ 9 คือการบีบอัดสูงสุด ตัวอย่างโค้ดย่อยที่ให้ด้านล่างDemo วิธีการตั้งค่าระดับการบีบอัดโดยใช้ Aspose.PSD สำหรับ .NET API

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.cs" >}}
## **ระบุความลึกของบิตสำหรับรูปภาพ PNG**
ความลึกของบิตในการภาพถ่ายคือจำนวนของบิตที่ใช้เพื่อแสดงสีของพิกเซลเดี่ยวในรูปภาพบิตแมพเหมือนกับรูปภาพ BMP ความลึกสี PNG ก็ถูกแทนด้วยบิต เช่น 1 บิต (2 สี) 2 บิต (4 สี) 4 บิต (16 สี) และ 8 บิต (256 สี) Aspose.PSD สำหรับ .NET API สามารถใช้กำหนดความลึกของบิตสำหรับรูปภาพ PNG โดยใช้ [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) property ที่เปิดเผยโดยคลาส PngOptions ในปัจจุบัน คุณสมบัติ BitDepth สามารถถูกตั้งค่าได้ที่ 1, 2, 4 หรือ 8 บิตสำหรับระดับสีเทาและสีดัชรี สำหรับสีชนิดอื่น ๆ เท่านั้นมีการสนับสนุน 8 บิตเท่านั้น ตัวอย่างโค้ดย่อยที่ให้ไว้ด้านล่างแสดงวิธีการตั้งค่าความลึกของบิตสำหรับภาพ PNG

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.cs" >}}
## **ปรับใช้วิธีกรองลำดับในรูปภาพ PNG**
ความลึกของบิตในการภาพถ่ายคือจำนวนของบิตที่ใช้เพื่อแสดงสีของพิกเซลเดี่ยวในรูปภาพบิตแมพเหมือนกับรูปภาพ BMP ความลึกสี PNG ก็ถูกแทนด้วยบิต เช่น 1 บิต (2 สี) 2 บิต (4 สี) 4 บิต (16 สี) และ 8 บิต (256 สี) Aspose.PSD สำหรับ .NET API สามารถใช้กำหนดความลึกของบิตสำหรับรูปภาพ PNG โดยใช้ BitDepth property ที่เปิดเผยโดยคลาส PngOptions ในปัจจุบัน คุณสมบัติ BitDepth สามารถถูกตั้งค่าได้ที่ 1, 2, 4 หรือ 8 บิตสำหรับระดับสีเทาและสีดัชรี สำหรับสีชนิดอื่น ๆ เท่านั้นมีการสนับสนุน 8 บิตเท่านั้น ตัวอย่างโค้ดย่อยที่ให้ไว้ด้านล่างแสดงวิธีการตั้งค่าความลึกของบิตสำหรับภาพ PNG

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.cs" >}}
## **เปลี่ยนสีพื้นหลังของภาพ PNG โปร่งใส**
ภาพในรูปแบบ PNG สามารถมีพื้นหลังโปร่งใส Aspose.PSD สำหรับ .NET มีคุณสมบัติในการเปลี่ยนสีพื้นหลังของภาพ PNG ที่มีพื้นหลังโปร่งใส Aspose.PSD สำหรับ .NET API สามารถใช้เพื่อตั้ง/เปลี่ยนสีของภาพ PNG ที่มีพื้นหลังโปร่งใสตัวอย่างโค้ดย่อยที่ให้ไว้ด้านล่างแสดงวิธีการตั้ง/เปลี่ยนสีพื้นหลังของภาพ PNG

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.cs" >}}
