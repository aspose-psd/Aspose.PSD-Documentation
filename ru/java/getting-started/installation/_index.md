---
title: Установка
type: docs
weight: 40
url: /ru/java/installation/
---

## **Установка Aspose.PSD для Java из репозитория Maven**
Aspose размещает все Java API в [репозитории Maven](https://releases.aspose.com/java/repo/com/aspose/). Вы можете легко использовать [Aspose.PSD для Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) API непосредственно в ваших проектах Maven с простой конфигурацией.
### **Указание конфигурации репозитория Maven**
Сначала вам нужно указать конфигурацию/расположение репозитория Maven Aspose в вашем файле pom.xml следующим образом:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **Задание зависимости Aspose.PSD для Java API**
Затем определите зависимость Aspose.PSD для Java API в вашем pom.xml следующим образом:

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

После выполнения вышеуказанных шагов, зависимость Aspose.PSD для Java будет окончательно определена в вашем проекте Maven.
## **Поддерживаемые платформы**
Aspose.PSD для Java поддерживает самые популярные платформы разработки и развертывания.

|**Особенность**|**Описание**|
| :- | :- |
|Приложения для рабочего стола|Aspose.PSD для Java можно использовать для разработки приложений для рабочего стола в MS Windows.|
|Приложения для веб-приложений предприятий|Aspose.PSD для Java полностью поддерживает веб-приложения.|
|Linux/Unix|Aspose.PSD для Java является платформенно-независимым API и может работать в Linux и Unix окружениях.|
## **Поддерживаемые версии Java**
- JDK 1.6 или выше
