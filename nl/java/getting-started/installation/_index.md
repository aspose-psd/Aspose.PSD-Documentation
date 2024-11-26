---
title: Installatie
type: docs
weight: 40
url: /nl/java/installatie/
---

## **Aspose.PSD voor Java installeren vanuit Maven Repository**
Aspose host alle Java API's op de [Maven-repository](https://releases.aspose.com/java/repo/com/aspose/). U kunt [Aspose.PSD voor Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) API eenvoudig rechtstreeks gebruiken in uw Maven-projecten met eenvoudige configuraties.
### **Specificeer Maven Repository-configuratie**
Ten eerste moet u de Aspose Maven Repository-configuratie/locatie specificeren in uw Maven pom.xml als volgt:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **Definieer Aspose.PSD voor Java API-afhankelijkheid**
Definieer vervolgens de afhankelijkheid van Aspose.PSD voor Java API in uw pom.xml als volgt:

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

Na het uitvoeren van de bovenstaande stappen, zal de afhankelijkheid van Aspose.PSD voor Java uiteindelijk worden gedefinieerd in uw Maven-project.
## **Ondersteunde platforms**
Aspose.PSD voor Java ondersteunt de meest populaire ontwikkelings- en implementatieplatforms.

|**Functie**|**Beschrijving**|
| :- | :- |
|Desktop-applicaties|Aspose.PSD voor Java kan worden gebruikt om desktoptoepassingen te ontwikkelen in MS Windows.|
|Ondernemingswebapplicaties|Aspose.PSD voor Java ondersteunt volledig webapplicaties.|
|Linux/Unix|Aspose.PSD voor Java is een platformonafhankelijke API en kan werken in een Linux- en Unix-omgeving.|
## **Ondersteunde Java-versies**
- JDK 1.6 of hoger
