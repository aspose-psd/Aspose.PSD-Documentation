---
title: Instalace
type: docs
weight: 40
url: /cs/java/instalace/
---

## **Instalace Aspose.PSD pro Java z repozitáře Maven**
Aspose hostuje všechny Java API na [Maven repozitáři](https://releases.aspose.com/java/repo/com/aspose/). Můžete snadno použít [Aspose.PSD pro Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) API přímo ve svých Maven projektech s jednoduchými konfiguracemi.
### **Specifikace konfigurace Maven repozitáře**
Nejprve musíte specifikovat konfiguraci/umístění Aspose Maven repozitáře ve vašem Maven pom.xml následovně:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **Definice závislosti na Aspose.PSD pro Java API**
Poté definujte závislost na Aspose.PSD pro Java API ve vašem pom.xml následovně:

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

Po provedení výše uvedených kroků bude závislost na Aspose.PSD pro Java konečně definována ve vašem Maven projektu.
## **Podporované platformy**
Aspose.PSD pro Java podporuje nejoblíbenější vývojové a nasazovací platformy.

| **Funkce** | **Popis** |
| :- | :- |
| Desktopové Aplikace | Aspose.PSD pro Java lze použít k vytvoření desktopových aplikací v systému MS Windows. |
| Firemní Webové Aplikace | Aspose.PSD pro Java plně podporuje webové aplikace. |
| Linux/Unix | Aspose.PSD pro Java je platformně nezávislé API a může pracovat v prostředí Linuxu a Unixu. |
## **Podporované verze Javy**
- JDK 1.6 nebo vyšší
