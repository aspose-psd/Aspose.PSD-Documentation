---
title: التثبيت
type: docs
weight: 40
url: /ar/java/installation/
---

## **تثبيت Aspose.PSD للغة Java من مستودع Maven**
تستضيف Aspose جميع واجهات برمجة تطبيقات الجافا على [مستودع Maven](https://releases.aspose.com/java/repo/com/aspose/). يمكنك استخدام [واجهة برمجة تطبيقات Aspose.PSD للغة Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) بسهولة في مشاريع Maven الخاصة بك مع تكوينات بسيطة.
### **تحديد تكوين مستودع Maven**
أولاً، تحتاج إلى تحديد تكوين/موقع مستودع Maven الخاص بـ Aspose في ملف pom.xml الخاص بك كما يلي:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>واجهة برمجة تطبيقات الجافا Aspose</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **تعريف تبعية Aspose.PSD للغة Java API**
ثم يتعين عليك تحديد تبعية واجهة برمجة تطبيقات Aspose.PSD للغة Java في ملف pom.xml الخاص بك كما يلي:

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

بعد تنفيذ الخطوات المذكورة أعلاه، سيتم تحديد تبعية Aspose.PSD للغة Java في مشروع Maven الخاص بك.
## **المنصات المدعومة**
تدعم Aspose.PSD للغة Java أكثر المنصات شيوعًا للتطوير والنشر.

|**الميزة**|**الوصف**|
| :- | :- |
|تطبيقات سطح المكتب|يمكن استخدام Aspose.PSD للغة Java لتطوير تطبيقات سطح المكتب في نظام تشغيل مايكروسوفت ويندوز.|
|تطبيقات الويب الصناعية|تدعم Aspose.PSD للغة Java تمامًا تطبيقات الويب.|
|نظام التشغيل Linux/Unix|واجهة برمجة تطبيقات Aspose.PSD للغة Java هي واجهة برمجة تطبيقات مستقلة عن المنصة ويمكنها العمل في بيئة Linux و Unix.|
## **إصدارات الجافا المدعمة**
- JDK 1.6 أو أحدث