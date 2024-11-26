---
title: เปิดไฟล์ PSD, PSB และ AI และส่งออกเป็น PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: ตัวอย่างการส่งออกรูปภาพ PSD, PSB และ AI เป็นรูปแบบอื่น ๆ
keywords: [เปิดไฟล์ PSD, เปิดไฟล์ AI, เปิดไฟล์ PSB, ส่งออกเป็น PNG, ส่งออกเป็น PDF, ส่งออกเป็น JPEG, ส่งออกเป็น TIFF, ไฟล์ PSD API, Java, ตัวอย่างโค้ด]
url: th/java/open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **ภาพรวม**
เพื่อแปลงไฟล์ PSD, PSB และ AI เป็นรูปแบบที่แตกต่างกันโดยใช้ Java, คุณสามารถใช้ไลบรารี Aspose.PSD ได้ นี่คือภาพรวมของขั้นตอนที่เกี่ยวข้อง:

- นำเข้าคลาสและโมดูลที่จำเป็นจากไลบรารี Aspose.PSD

- กำหนดตัวเลือกต่าง ๆ สำหรับรูปแบบต่าง ๆ เช่น PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB และ PSD

- สร้างพจนานุกรมที่จับคู่ไฟล์นามสกุลกับตัวเลือกการบันทึกที่เกี่ยวข้อง

- โหลดไฟล์ PSD โดยใช้ PsdImage.load() และคำนวณผ่านพจนานุกรมของรูปแบบเพื่อบันทึกรูปภาพในแต่ละรูปแบบที่ต้องการ

- ในทำเหมือนกัน, โหลดไฟล์ AI โดยใช้ AiImage.load() และคำนวณผ่านพจนานุกรมของรูปแบบเพื่อบันทึกรูปภาพในแต่ละรูปแบบที่ต้องการ

ระวังที่จะระบุเส้นทางไฟล์ที่ถูกต้องสำหรับไฟล์ PSD และ AI ต้นฉบับ
นั่นคือขั้นตอนทั่วไปสำหรับการแปลงไฟล์ PSD, PSB และ AI เป็นรูปแบบต่าง ๆ โดยใช้ Aspose.PSD สำหรับ Java

โปรดตรวจสอบตัวอย่างเต็ม

## **ตัวอย่าง**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.java" >}}
