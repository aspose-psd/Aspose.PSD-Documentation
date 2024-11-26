---
title: Instalacja
type: docs
weight: 40
url: /pl/java/installation/
---

## **Instalowanie Aspose.PSD dla Javy z Repozytorium Maven**
Aspose hostuje wszystkie API Javy na [repozytorium Maven](https://releases.aspose.com/java/repo/com/aspose/). Możesz łatwo używać [Aspose.PSD dla Javy](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) API bezpośrednio w swoich projektach Maven dzięki prostym konfiguracjom.
### **Określenie Konfiguracji Repozytorium Maven**
Najpierw musisz określić konfigurację/lokalizację Repozytorium Maven Aspose w swoim pliku pom.xml Maven, zgodnie z poniższym przykładem:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **Określenie Zależności Aspose.PSD dla Javy**
Następnie zdefiniuj zależność Aspose.PSD dla Javy w pliku pom.xml, zgodnie z poniższym przykładem:

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

Po wykonaniu powyższych kroków, zależność Aspose.PSD dla Javy zostanie ostatecznie zdefiniowana w twoim projekcie Maven.
## **Obsługiwane Platformy**
Aspose.PSD dla Javy obsługuje najpopularniejsze platformy rozwoju i wdrożeń.

|**Funkcja**|**Opis**|
| :- | :- |
|Aplikacje Pulpitowe|Aspose.PSD dla Javy może być używane do tworzenia aplikacji na pulpit w systemie MS Windows.|
|Aplikacje Sieciowe Przedsiębiorstw|Aspose.PSD dla Javy w pełni obsługuje aplikacje sieciowe.|
|Linux/Unix|Aspose.PSD dla Javy to API niezależne od platformy i może działać w środowisku Linux i Unix.|
## **Obsługiwane Wersje Javy**
- JDK 1.6 lub nowsza
