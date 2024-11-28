---
title: نصب
type: docs
weight: 40
url: /fa/java/installation/
---

## **نصب Aspose.PSD برای Java از مخزن Maven**
Aspose تمامی API های Java را در [مخزن Maven](https://releases.aspose.com/java/repo/com/aspose/) میزبانی می‌کند. شما می‌توانید به راحتی از [Aspose.PSD for Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) مستقیماً در پروژه‌های Maven خود با پیکربندی‌های ساده استفاده کنید.
### **مشخص کردن پیکربندی مخزن Maven**
ابتدا باید مکان/پیکربندی مخزن Maven Aspose را در فایل pom.xml خود به شکل زیر مشخص کنید:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **تعریف وابستگی Aspose.PSD for Java API**
سپس وابستگی Aspose.PSD for Java API را در فایل pom.xml خود به شکل زیر تعریف کنید:

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

پس از انجام مراحل فوق، وابستگی Aspose.PSD for Java به درستی در پروژه Maven شما تعریف خواهد شد.
## **پلتفرم‌های پشتیبانی شده**
Aspose.PSD برای Java پشتیبانی را از پرکاربردترین پلتفرم‌های توسعه و استقرار فراهم می‌کند.

|**ویژگی**|**توضیحات**|
| :- | :- |
|برنامه‌های دسکتاپ|Aspose.PSD for Java می‌تواند برای توسعه برنامه‌های دسکتاپ در MS Windows استفاده شود.|
|برنامه‌های وب سازمانی|Aspose.PSD for Java به طور کامل برنامه‌های وب را پشتیبانی می‌کند.|
|لینوکس/یونیکس|Aspose.PSD for Java یک API مستقل از پلتفرم است و می‌تواند در محیط‌های لینوکس و یونیکس کار کند.|
## **نسخه‌های Java پشتیبانی شده**
- JDK 1.6 یا بالاتر
