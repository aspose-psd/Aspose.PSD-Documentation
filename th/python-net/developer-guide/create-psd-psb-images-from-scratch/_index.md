---
title: สร้างภาพ PSD หรือ PSB จากต้นแบบโดยใช้ Python
weight: 100
type: docs
description: ตัวอย่างเช่นว่า Aspose.PSD สำหรับ Python สามารถสร้างภาพ Psd จากต้นแบบ
keywords: [สร้าง psd, สร้าง psb, สร้างใหม่, สร้างเลเยอร์, สร้างเลเยอร์ข้อความ, psd api, python, ตัวอย่างโค้ด]
url: th/python-net/create-psd-psb-images-from-scratch/
---

## **ภาพรวม**
เพื่อสร้างไฟล์ PSD หรือ PSB จากต้นแบบโดยใช้ Aspose.PSD สำหรับ Python คุณสามารถทำตามขั้นตอนด้านล่าง:

นำเข้าโมดูลและคลาสที่จำเป็นจากไลบรารี Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

ระบุชื่อและที่อยู่ไฟล์ผลลัพธ์:

```python 
outputFile = "CreateFileFromScratchExample.psd"
```

สร้างภาพ PSD ด้วยมิติที่ต้องการ:

```python 
with PsdImage(500, 500) as img:
```

เพิ่มเลเยอร์ PSD ปกติและอัปเดตด้วย Graphic API:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

สร้างเลเยอร์ข้อความ:
```python 
textLayer = img.add_text_layer("Sample Text", Rectangle(200, 200, 100, 100))
```

เพิ่มเอฟเฟ็กต์เงาลงเลเยอร์ข้อความ:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

บันทึกไฟล์ PSD:
```python 
img.save(outputFile)
```

โค้ดนี้สร้างภาพ PSD ขนาด 500x500 พิกเซล มันเพิ่มเลเยอร์ปกติและวาดวงรีบนนั้นโดยใช้ปากกาและแปรง จากนั้นเพิ่มเลเยอร์ข้อความด้วยข้อความ "Sample Text" และปรับใช้เอฟเฟ็กต์เงาลงไป ในที่สุดบันทึกไฟล์ PSD ด้วยชื่อไฟล์ผลลัพธ์ที่ระบุ

โปรดทราบว่าคุณต้องติดตั้งไลบรารี Aspose.PSD และตั้งค่าอย่างเหมาะสมในสภาพแวดล้อม Python เพื่อให้โค้ดนี้ทำงาน คุณสามารถอ่านเพิ่มเติมเกี่ยวกับ Aspose.PSD ในเอกสารอย่างเป็นทางการ

โปรดตรวจสอบตัวอย่างที่เต็ม

## **ตัวอย่าง**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}
