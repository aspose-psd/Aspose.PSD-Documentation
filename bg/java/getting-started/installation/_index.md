---
title: Инсталиране
type: docs
weight: 40
url: /bg/java/installation/
---

## **Инсталиране на Aspose.PSD за Java от Maven Repository**
Aspose предлага всички Java API в [Maven репозитория](https://releases.aspose.com/java/repo/com/aspose/). Лесно можете да използвате [Aspose.PSD за Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) API директно във вашия Maven проект с прости конфигурации.
### **Укажете конфигурацията на Maven Repository**
Първо, трябва да укажете конфигурацията/местонахождението на Aspose Maven Repository във вашия Maven pom.xml по следния начин:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **Дефинирайте зависимостта на Aspose.PSD за Java API**
След това дефинирайте зависимостта на Aspose.PSD за Java API във вашия pom.xml по следния начин:

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

След като извършите горните стъпки, зависимостта на Aspose.PSD за Java най-накрая ще бъде дефинирана във вашия Maven проект.
## **Поддържани Платформи**
Aspose.PSD за Java поддържа най-популярните платформи за разработка и развитие.

|**Функционалност**|**Описание**|
| :- | :- |
|Приложения за настолен компютър|Aspose.PSD за Java може да се използва за разработване на приложения за настолни компютри в MS Windows.|
|Приложения за уеб базирани системи|Aspose.PSD за Java напълно поддържа уеб приложения.|
|Linux/Unix|Aspose.PSD за Java е API, независимо от платформата и може да работи в Linux и Unix среда.|
## **Поддържани версии на Java**
- JDK 1.6 или по-нова