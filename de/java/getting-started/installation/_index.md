---
title: Installation
type: docs
weight: 40
url: /de/java/installation/
---

## **Aspose.PSD für Java aus dem Maven-Repository installieren**
Aspose hostet alle Java-APIs im [Maven-Repository](https://releases.aspose.com/java/repo/com/aspose/). Sie können das [Aspose.PSD für Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) API mit einfachen Konfigurationen direkt in Ihren Maven-Projekten verwenden.
### **Maven-Repository-Konfiguration festlegen**
Zuerst müssen Sie die Aspose Maven-Repository-Konfiguration/Position in Ihrer Maven pom.xml wie folgt festlegen:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **Abhängigkeit von Aspose.PSD für Java API definieren**
Definieren Sie dann die Abhängigkeit von Aspose.PSD für Java API in Ihrer pom.xml wie folgt:

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

Nach Ausführung der obigen Schritte wird die Aspose.PSD für Java-Abhängigkeit schließlich in Ihrem Maven-Projekt definiert.
## **Unterstützte Plattformen**
Aspose.PSD für Java unterstützt die beliebtesten Entwicklungs- und Bereitstellungsplattformen.

|**Funktion**|**Beschreibung**|
| :- | :- |
|Desktop-Anwendungen|Aspose.PSD für Java kann verwendet werden, um Desktop-Anwendungen in MS Windows zu entwickeln.|
|Unternehmens-Webanwendungen|Aspose.PSD für Java unterstützt vollständig Webanwendungen.|
|Linux/Unix|Aspose.PSD für Java ist eine plattformunabhängige API und kann in einer Linux- und Unix-Umgebung arbeiten.|
## **Unterstützte Java-Versionen**
- JDK 1.6 oder höher
