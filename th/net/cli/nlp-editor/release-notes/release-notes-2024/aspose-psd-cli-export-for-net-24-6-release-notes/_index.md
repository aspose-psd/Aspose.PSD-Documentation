---
title: Aspose.PSD รายงานการเผยแพร่ Aspose.PSD CLI NLP Editor for .NET 24.6
type: docs
weight: 90
url: /th/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

หน้านี้มีรายงานการเผยแพร่สำหรับ [Aspose.PSD CLI NLP Editor for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Key**     | **สรุป**                                                                                   | **หมวดหมู่** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | การเผยแพร่เริ่มต้นของ Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export และ Aspose.PSD.CLI.NLP.Editor |  การปรับปรุง |


## **ตัวอย่างการใช้:**

**PSDNET-2110. การเผยแพร่เริ่มต้นของ Aspose.PSD CLI NLP Editor**

## **การใช้จากบรรทัดคำสั่ง:**

{{% alert color="primary" %}}
ติดตั้งเครื่องมือ dotnet นี้ก่อน:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

เราขอแนะนำก่อนการใช้งานครั้งแรกให้รันคำสั่งต่อไปนี้:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
หลังจากคำสั่งนี้ คุณจะสามารถรันแอปพลิเคชันนี้ได้โดยใช้ชื่อย่อ nlp.cli แทน Aspose.PSD.CLI.NLP.Editor คุณสามารถกำหนดชื่อย่อของคุณเองได้
{{% /alert %}}

**ตัวอย่างการใช้**

1. คำสั่งนี้จะแปลงไฟล์ที่พบครั้งแรก (ที่สามารถเปิดด้วย aspose.psd) จากโฟลเดอร์ปัจจุบันและจะบันทึกในรูปแบบ png พร้อมทั้งมีการตั้งค่าใบอนุญาต เราขอแนะนำให้ระบุใบอนุญาตเพียงครั้งเดียว เมื่อรันครั้งต่อไป ใบอนุญาตจะถูกใช้จากเส้นทางที่ระบุ การคำสั่งนี้จะแสดงบันทึกสรุปของการประมวลผล NLP ถ้าพร้อมใช้งาน
{{< highlight bash >}}nlp.cli แปลงไฟล์จากโฟลเดอร์นี้เป็นรูปแบบ png พร้อมทั้งความ๏ถวิล ใบอนุญาต "C:\Aspose\LicenseFile.lic" --verbose{{< /highlight >}}

2. คำสั่งนี้จะค้นหาไฟล์ที่มีชื่อคล้ายกับ "smth.psd" จากนั้นจะปรับความคมชัดและบันทึกเป็น jpeg พร้อมกับคุณภาพที่ดีที่สุด ชื่อของไฟล์ผลลัพธ์จะถูกพิมพ์ คือ smth.jpg 
{{< highlight bash >}}ปรับความคมชัดใน 10 ชั้นที่มีชื่อวงกลมในไฟล์ smth.psd และบันทึกเป็น output.jpg ด้วยคุณภาพที่ดีที่สุด{{< /highlight >}}

3. คำสั่งนี้จะห่อไฟล์ที่ระบุที่ทางเดิน และจะลดขนาดลง 25% ไฟล์ผลลัพธ์จะถูกพิมพ์ จะถูกบันทึกในโฟลเดอร์ปัจจุบันของคอนโซล
{{< highlight bash >}}Resize ไฟล์ C:\Users\someuser\Desktop\input.psd ลง 25%{{< /highlight >}}

4. คำสั่งนี้จะค้นหาไฟล์ input.psd ใน C:\Users\someuser\Desktop\ จากนั้นจะค้นหาชั้นที่มีดัชนี 3 และจะปรับขนาดเป็นควาว 50px และ สูง 100px จากนั้นชั้นนี้จะถูกบันทึกเป็น PDF ใน C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}ปรับขนาดชั้นด้วยดัชนี 3 ของ C:\Users\someuser\Desktop\input.psd เป็นควาว 50 และสูง 100 และบันทึกเป็น C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

5. คำสั่งนี้จะเปิด smth.psd ในโฟลเดอร์ปัจจุบัน แต่จะปิดทุกเอฟเฟกต์ จากนั้นไฟล์นี้จะถูกแปลงเป็นรูปแบบ BMP และเป็น output.bmp ในโฟลเดอร์ปัจจุบัน
 {{< highlight bash >}}เปิด smth.psd โดยไม่มีเอฟเฟกต์ และบันทึกเป็น output.bmp{{< /highlight >}}

**คำเตือน**
นี่เป็นแอปพลิเคชันทดลอง โปรดลองใช้และแสดงความคิดเห็น ความคิดเห็นใด ๆ ก็ยินดีต้อนรับ เราต้องการพัฒนาแอปพลิเคชันที่ไม่ต้องเขียนโค้ดสู่ระดับถัดไป การผสมผสานได้อย่างง่ายดายกับคิดเนอร์สตรีมเป็นเป้าหมายของเรา

