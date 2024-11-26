---
title: การติดตั้ง
type: docs
weight: 40
url: /th/java/installation/
---

## **การติดตั้ง Aspose.PSD สำหรับ Java จากที่เก็บข้อมูล Maven**
Aspose จัดเก็บ Java APIs ทั้งหมดไว้ใน [ที่เก็บข้อมูล Maven](https://releases.aspose.com/java/repo/com/aspose/) คุณสามารถใช้ [Aspose.PSD สำหรับ Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) API ได้โดยตรงในโครงการ Maven ของคุณอย่างง่ายด้วยการกำหนดการกำหนดค่าแบบง่าย
### **ระบุค่ากำหนดการเก็บข้อมูล Maven**
ก่อนอื่นคุณต้องระบุค่าการกำนดเก็บข้อมูล Maven ของ Aspose ในไฟล์ pom.xml ของคุณดังนี้:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **กำหนด Aspose.PSD สำหรับ Java API Dependency**
จากนั้นกำหนด Aspose.PSD สำหรับ Java API ในไฟล์ pom.xml ของคุณดังนี้:

{{< highlight java >}}

 <dependencies>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-psd</artifactId>
        <version>24.2</version>
        <classifier>jdk16</classifier>
    </dependency>
</dependencies>

{{< /highlight >}}

หลังจากทำขั้นตอนข้างต้น เสร็จแล้ว การทำตามขั้นตอนด้านบนจะช่วยกำหนดขึ้นที่เก็บข้อมูลสำหรับ Aspose.PSD สำหรับ Java ในโครงการ Maven ของคุณ
## **แพลตฟอร์มที่รองรับ**
Aspose.PSD สำหรับ Java รองรับแพลตฟอร์มการพัฒนาและการใช้งานที่นิยมที่สุด

|**คุณสมบัติ**|**คำอธิบาย**|
| :- | :- |
|แอปพลิเคชันบนเดสก์ทอป|Aspose.PSD สำหรับ Java สามารถใช้ในการพัฒนาแอปพลิเคชันบนเดสก์ทอปใน MS Windows|
|แอปพลิเคชัน Web ธุรกิจ|Aspose.PSD สำหรับ Java รองรับแอปพลิเคชัน Web อย่างเต็มรูปแบบ|
|Linux/Unix|Aspose.PSD สำหรับ Java เป็น API ที่ไม่ขึ้นต่อแพลตฟอร์ม และสามารถทำงานในระบบ Linux และ Unix|
## **รุ่น Java ที่รองรับ**
- JDK 1.6 หรือสูงกว่า
