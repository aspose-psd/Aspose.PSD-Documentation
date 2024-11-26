---
title: Установка
type: docs
weight: 40
url: /uk/java/installation/
---

## **Встановлення Aspose.PSD для Java з репозиторію Maven**
Aspose розміщує всі Java API на [репозиторії Maven](https://releases.aspose.com/java/repo/com/aspose/). Ви можете легко використовувати [Aspose.PSD для Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) API безпосередньо у ваших проектах Maven з простими налаштуваннями.
### **Вказати конфігурацію репозиторію Maven**
Спочатку вам потрібно вказати конфігурацію/розташування репозиторію Maven Aspose у вашому pom.xml таким чином:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **Визначити залежність від Aspose.PSD для Java API**
Потім визначте залежність від Aspose.PSD для Java API у вашому файлі pom.xml наступним чином:

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

Після виконання вищезазначених кроків, залежність від Aspose.PSD для Java остаточно буде визначена у вашому проекті Maven.
## **Підтримувані Платформи**
Aspose.PSD для Java підтримує найпопулярніші платформи розробки та розгортання.

|**Функція**|**Опис**|
| :- | :- |
|Додатки для робочого столу|Aspose.PSD для Java може бути використаний для розробки додатків для робочого столу в операційній системі MS Windows.|
|Підприємницькі Веб-Додатки|Aspose.PSD для Java повністю підтримує веб-додатки.|
|Linux/Unix|Aspose.PSD для Java є платформонезалежним API та може працювати в середовищі Linux та Unix.|
## **Підтримувані версії Java**
- JDK 1.6 або вище
