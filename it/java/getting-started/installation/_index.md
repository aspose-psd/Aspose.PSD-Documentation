---
title: Installazione
type: docs
weight: 40
url: /it/java/installazione/
---

## **Installazione di Aspose.PSD per Java dal repository Maven**
Aspose ospita tutte le API Java sul [repository Maven](https://releases.aspose.com/java/repo/com/aspose/). È possibile utilizzare facilmente [Aspose.PSD per Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) API direttamente nei progetti Maven con configurazioni semplici.
### **Specificare la Configurazione del Repository Maven**
Innanzitutto, è necessario specificare la configurazione/posizione del repository Maven di Aspose nel file pom.xml come segue:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>API Aspose Java</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **Definire la Dipendenza dell'API Aspose.PSD per Java**
Successivamente, definire la dipendenza dell'API Aspose.PSD per Java nel file pom.xml come segue:

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

Dopo aver eseguito i passaggi sopra indicati, la dipendenza di Aspose.PSD per Java sarà definita nel vostro progetto Maven.
## **Piattaforme Supportate**
Aspose.PSD per Java supporta le piattaforme di sviluppo e distribuzione più popolari.

|**Funzionalità**|**Descrizione**|
| :- | :- |
|Applicazioni Desktop|Aspose.PSD per Java può essere utilizzato per sviluppare applicazioni desktop in MS Windows.|
|Applicazioni Web Aziendali|Aspose.PSD per Java supporta completamente le applicazioni web.|
|Linux/Unix|Aspose.PSD per Java è una API indipendente dalla piattaforma e può funzionare in un ambiente Linux e Unix.|
## **Versioni Java Supportate**
- JDK 1.6 o superiore
