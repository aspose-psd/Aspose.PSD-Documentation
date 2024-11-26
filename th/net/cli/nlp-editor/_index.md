---
title: แอปพลิเคชัน Aspose.PSD CLI NLP Editor สำหรับ .NET
type: สารบัญ
weight: 10
url: /th/net/cli/nlp-editor/
is_root: false
keywords: CLI Photoshop Tool NLP Natural-Language-Processing PSD Console C# Library PSD API
description: แอปพลิเคชัน Aspose.PSD CLI NLP Editor ที่ใช้ Aspose.PSD เพื่อแก้ไขไฟล์ PSD, PSB, และ AI โดยไม่ต้องการโค้ด CI/CD Automation รองรับการประมวลผลภาษาธรรมชาติสำหรับการแก้ไขไฟล์ PSD ให้เขียนคำขอของคุณเป็นภาษาธรรมชาติเพื่อดำเนินการต่าง ๆ เช่น การแปลง, การปรับขนาด, และอื่น ๆ ไม่ต้องการติดตั้ง Adobe Photoshop หรือ Adobe Illustrator และสามารถใช้งานได้จากคอนโซลโดยไม่ต้องการโค้ดเพิ่มเติม
---

**![Aspose.PSD for .NET โลโก้ผลิตภัณฑ์](home_1.png)**

**ยินดีต้อนรับสู่ Aspose.PSD NLP Editor CLI Application สำหรับ .NET**

Aspose.PSD CLI NLP Editor Application เป็นเครื่องมือคอนโซลเบาสำหรับแก้ไขไฟล์ PSD ด้วยคำสั่งในภาษาธรรมชาติ ผ่านการรวดเร็วใน CI/CD Pipelines.

**คำชี้แจง**

นี่เป็นแอปพลิเคชันทดลอง กรุณาลองใช้และให้คำติชม คำติชมใด ๆ จะได้รับการต้อนรับอย่างสูง พวกเราต้องการพัฒนาแอปพลิเคชัน No-Code ไปสู่ระดับถัดไป การรวมเข้ากับไทม์ไลน์สำหรับการสร้างหรือกระบวนธุรกิจทุกประการเป็นเป้าหมายของเรา

**ฟังก์ชันหลักของ Aspose.PSD NLP Editor CLI Application สำหรับ .NET**

1. ดำเนินการบนไฟล์ PSD, PSB, AI โดยใช้คำสั่งภาษาธรรมชาติ
2. รองรับการดำเนินการต่าง ๆ เช่น การแปลง, การปรับขนาด, และอื่น ๆ
3. การออโตเมชัน CI/CD โดยไม่ต้องเขียนโค้ด
4. รองรับการเขียนคำขอในภาษาธรรมชาติสำหรับการแก้ไขไฟล์ PSD

## **การใช้งานจากบรรทัดคำสั่ง:**

{{% alert color="primary" %}}
ก่อนทุกอย่างครั้งแรกให้ติดตั้งเครื่องมือ dotnet นี้:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

เราขอแนะนำก่อนการใช้งานครั้งแรกให้เปิดใช้งานคำสั่งต่อไปนี้:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
หลังจากทำคำสั่งนี้คุณจะสามารถใช้แอปพลิเคชันนี้ด้วยชื่อสั้น nlp.cli แทนที่ Aspose.PSD.CLI.NLP.Editor คุณสามารถระบุชื่อสั้นของคุณเองได้
{{% /alert %}}

**พารามิเตอร์ที่สามารถใช้ได้สำหรับ Aspose.PSD.CLI.Crop Application** 

| **อาร์กิวเมนต์** | **คำอธิบาย**                         |
|:-------------|:----------------------------------------|
| any text     | จำเป็นต้องใช้ คำสั่งของคุณในภาษาธรรมชาติเพื่ออัพเดตไฟล์ PSD หรือ PSB      |
| license      | พาธไปยังใบอนุญาต                |
| verbose      | แสดงข้อมูลเพิ่มเติมเกี่ยวกับคำสั่งที่ระบุ |
| setup        | สร้างไฟล์ Bat ในโฟลเดอร์เครื่องมือเพื่อใช้เรียกด่วนจากโคนโซล. ตัวอย่าง: --setup psd.nlp. จากนั้นคุณสามารถเรียกเครื่องมือด้วยคำสั่ง psd.nlp |


**ตัวอย่างการใช้**

1. คำสั่งนี้จะแปลงไฟล์ของคุณที่พบเป็นตัวแรก (ที่สามารถเปิดด้วย Aspose.PSD) จากโฟลเดอร์ปัจจุบันและจะบันทึกเป็นรูปแบบ png พร้อมความ๏โปร่งใส และรายการใบอนุญาตจะต้องถูกตั้งค่าคุณจะต้องระบุใบอนุญาตเพียงครั้งเดียวเท่านั้น ในการรันครั้งถัดไปใบอนุญาตจะถูกใช้จากพาทที่ระบุ คำสั่งนี้จะแสดงบันทึกละเอียดของการประมวลผล NLP ถ้ามี
{{< highlight bash >}}
  nlp.cli Convert file from this folder to png format with alpha --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. คำสั่งนี้จะค้นหาไฟล์ที่มีชื่อที่คล้ายกันที่สุดกับ "smth.psd" จากนั้นจะปรับความคมชัดซึ่งและจะบันทึกเป็น jpeg ด้วยคุณภาพที่ดีที่สุด ชื่อของไฟล์ผลลัพธ์จะถูกพิมพ์ จะเป็น smth.jpg
{{< highlight bash >}}
Adjust contrast on 10 of layer with name ellipse in file smth.psd and save it to output.jpg with best quality
{{< /highlight >}}

3. คำสั่งนี้จะหาไฟล์บนพาทที่กำหนด และจะลดขนาดลง 25% ไฟล์ผลลัพธ์จะถูกพิมพ์ จะถูกบันทึกในโฟลเดอร์ปัจจุบันของคอนโซล
{{< highlight bash >}}
Resize file C:\Users\someuser\Desktop\input.psd to 25%
{{< /highlight >}}

4. คำสั่งนี้จะค้นหาไฟล์ input.psd ในพาท C:\Users\someuser\Desktop จากนั้นจะค้นหาเลเยอร์ด้วยดัชนี 3 และจะปรับขนาดเป็น width 50px และ height 100px จากนั้นเลเยอร์นี้จะถูกบันทึกเป็น PDF ใน C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}
 Resize layer with index 3 of C:\Users\someuser\Desktop\input.psd to width 50 and height 100 and save it to C:\Users\someuser\Desktop\output.pdf
 {{< /highlight >}}

 5. คำสั่งนี้จะเปิด smth.psd ในโฟลเดอร์ปัจจุบัน แต่ทุกระบบจะถูกปิด และจากนั้นไฟล์นี้จะถูกแปลงเป็น BMP และเป็น output.bmp ในโฟลเดอร์ปัจจุบัน
 {{< highlight bash >}}
 Open smth.psd without effects and save it to output.bmp
  {{< /highlight >}}

**กรุณาตรวจสอบ[แอปพลิเคชัน Aspose.PSD CLI อื่น ๆ](https://docs.aspose.com/psd/net/cli) สำหรับ .NET หากคุณต้องการเพิ่มการสนับสนุนสำหรับรูปแบบ PSD, PSB, และ AI ในขั้นทำงานของคุณ**

1. [Aspose.PSD CLI Convert](/psd/th/net/cli/convert)
2. [Aspose.PSD CLI Crop](/psd/th/net/cli/crop)
3. [Aspose.PSD CLI Resize](/psd/th/net/cli/resize)
4. [Aspose.PSD CLI Export](/psd/th/net/cli/export)
5. [Aspose.PSD CLI NLP Editor](/psd/th/net/cli/nlp-editor)

**กรุณาตรวจสอบ Aspose.PSD สำหรับ [.NET หรือแพลตฟอร์มอื่น]** 

แอปพลิเคชัน Aspose.PSD CLI คือ โซลูชั่นที่พร้อมใช้งานสำหรับการดำเนินงานอันได้รับความนิยม ถ้าคุณต้องการโซไลชันที่ยืดหยุหรือต้องการเช็คเวอร์ชั่นเต็มของ Aspose.PSD

1. [Aspose.PSD สำหรับ .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD สำหรับ Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD สำหรับ Python via .NET](https://releases.aspose.com/psd/python-net/)

## **เอกสารสำหรับ Aspose.PSD สำหรับ .NET**

นี่คือลิงค์ไปยังบางแหล่งทรัพยากรที่คุณอาจต้องการเพิื่อทำงานของคุณ

- [Aspose.PSD แอปพลิเคชันคำสั่งสำหรับ .NET เอกสารออนไลน์](/psd/th/net/cli/conversion)
- [Aspose.PSD สำหรับคำสั่งแอปพลิเคชันใน .NET บันทึกการออกแบบ](/psd/th/net/cli/conversion/release-notes/)
- [Aspose.PSD สำหรับคำสั่งแอปพลิเคชัน .NET หน้าผลิตภัณฑ์](https://products.aspose.com/psd/net/cli)
- [Aspose.PSD สำหรับ .NET คู่มืออ้างอิง API](https://reference.aspose.com/net/psd)
- [ดาวน์โหลดตัวอย่างที่เก็บการทำงานในเกิดฟี](https://github.com/aspose-psd/CLI-Applications)
- [Aspose.PSD สำหรับ .NET ฟอรัมรับสนับสนุนฟรี](https://forum.aspose.com/c/psd)
- [Aspose.PSD สำหรับ .NET ฟอรัมช่วยเหลือผ่านการสนับสนุนที่เสียค่า](https://helpdesk.aspose.com/)
