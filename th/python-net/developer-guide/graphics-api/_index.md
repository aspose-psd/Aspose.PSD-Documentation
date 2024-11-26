---
title: การใช้งาน Graphics API เพื่อแก้ไขเลเยอร์ในไฟล์ PSD
weight: 100
type: docs
description: ตัวอย่างการใช้ Graphics API ใน Aspose.PSD สำหรับ Python
keywords: [อัพเดทเลเยอร์, วาดวงกลม, วาดวงวง, วาดวงกลมเติม, กราฟิก, psd api, python, ตัวอย่างโค้ด]
url: th/python-net/graphics-api/
---

## **ภาพรวม**
ก่อนอื่นคุณต้องโหลดไฟล์ PSD โดยใช้เมธอด Image.load() หรือสร้าง Psd Image จากต้นฉบับ ในตัวอย่าง ตัวแปร inputFile แทนเส้นทางไปยังไฟล์ PSD ของคุณ และ loadOpt แทนตัวเลือกการโหลด (ถ้ามี)

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
ต่อไป คุณสามารถเข้าถึงเลเยอร์แรกของภาพ PSD โดยใช้ไวยากรณ์ psdImage.layers[0] นี้จะให้คุณอ้างอิงถึงอ็อปเจ็กต์เลเยอร์ที่คุณสามารถจัดการได้

```python 
layer = psdImage.layers[0]
```
เพื่อแก้ไขเลเยอร์คุณต้องสร้างอ็อปเจ็กต์ Graphics โดยการส่งเลเยอร์เป็นพารามิเตอร์ อ็อปเจ็กต์นี้ให้เมธอดต่าง ๆ สำหรับการวาดรูปร่างและใช้แปรง

```python 
graphics = Graphics(layer)
```
ในตัวอย่างของโค้ด สร้างอ็อปเจ็กต์ Pen เพื่อกำหนดสีและความหนาของเส้นขอบของรูปวงรี ค่าคงที่ Color.alice_blue แทนสี และคุณสามารถปรับความหนาตามต้องการ

```python 
pen = Pen(Color.alice_blue)
```
เช่นเดียวกัน สร้างอ็อปเจ็กต์ LinearGradientBrush เพื่อกำหนดสีเติมของรูปร่างวงรี Rectangle(250, 250, 150, 100) แทนตำแหน่งและขนาดของรูปร่างวงรี และ Color.red และ Color.aquamarine แทนสีเริ่มและสิ้นสุดของการหลายระดับ

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
เพื่อวาดรูปร่างวงรีบนเลเยอร์ คุณสามารถใช้เมธอด graphics.draw_ellipse()  Rectangle(100, 100, 200, 200) แทนตำแหน่งและขนาดของรูปร่างวงรี

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
เพื่อเติมสีรูปร่างวงรีด้วยแปรงเติม คุณสามารถใช้เมธอด graphics.fill_ellipse()  Rectangle(250, 250, 150, 100) แทนตำแหน่งและขนาดของรูปร่างวงรี

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
หลังจากการทำเปลี่ยนแปลงตามที่ต้องการบนเลเยอร์ คุณสามารถบันทึกภาพ PSD ที่แก้ไขแล้วโดยใช้เมธอด psdImage.save() ในตัวอย่าง ตัวแปร psdName แทนเส้นทางที่จะบันทึกไฟล์ PSD ที่แก้ไข

```python 
psdImage.save(psdName)
```
นอกจากนี้ คุณยังสามารถบันทึกภาพที่แก้ไขเป็นรูปแบบอื่น เช่น PNG โดยใช้คลาส PngOptions ตัวแปร pngName แทนเส้นทางที่จะบันทึกไฟล์ PNG

```python 
psdImage.save(pngName, PngOptions())
```
นั้นคือ! คุณได้ใช้งาน Graphics API ของ Aspose.PSD สำหรับ Python ในการแก้ไขเลเยอร์ในไฟล์ PSD อย่าลังเลเพื่อสำรวจคุณลักษณะและความสามารถเพิ่มเติมของไลบรารี Aspose.PSD เพื่อเสริมความสามารถในการแก้ไขรูปภาพของคุณ

โปรดตรวจสอบตัวอย่างแบบเต็ม.

## **ตัวอย่าง**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py " >}}
