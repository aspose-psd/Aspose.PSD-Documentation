---
title: Kurulum
type: docs
weight: 40
url: /tr/java/kurulum/
---

## **Maven Deposundan Aspose.PSD for Java'nın Yüklenmesi**
Aspose, tüm Java API'lerini [Maven deposunda](https://releases.aspose.com/java/repo/com/aspose/) barındırır. Basit yapılandırmalarla Maven Projelerinizde [Aspose.PSD for Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) API'sini doğrudan kullanabilirsiniz.
### **Maven Deposu Yapılandırmasını Belirtme**
İlk olarak, Maven pom.xml dosyanızda Aspose Maven Deposu yapılandırmasını/yolunu şu şekilde belirtmeniz gerekmektedir:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **Aspose.PSD for Java API Bağımlılığını Tanımlama**
Ardından, pom.xml dosyanızda Aspose.PSD for Java API bağımlılığını şu şekilde tanımlamanız gerekmektedir:

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

Yukarıdaki adımları gerçekleştirdikten sonra, Maven Projenizde Aspose.PSD for Java bağımlılığı sonunda tanımlanacaktır.
## **Desteklenen Platformlar**
Aspose.PSD for Java, en popüler geliştirme ve dağıtım platformlarını destekler.

|**Özellik**|**Açıklama**|
| :- | :- |
|Masaüstü Uygulamalar|Aspose.PSD for Java, MS Windows'ta Masaüstü uygulamalar geliştirmek için kullanılabilir.|
|Kurumsal Web Uygulamaları|Aspose.PSD for Java, Web uygulamalarını tamamen destekler.|
|Linux/Unix|Aspose.PSD for Java, platform bağımsız bir API'dir ve Linux ve Unix ortamlarında çalışabilir.|
## **Desteklenen Java Sürümleri**
- JDK 1.6 veya daha yükseği
