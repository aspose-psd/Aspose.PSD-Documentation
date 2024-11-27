---
title: Lizenzierung
type: docs
weight: 60
url: /de/java/lizenzierung/
---

## **Evaluierungsversionseinschränkungen**
Sie können eine Evaluierungsversion von Aspose.PSD für Java von der [Download-Seite](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/) herunterladen. Die Evaluierungsversion bietet die gleichen Funktionen wie die vollständig lizenzierte Version des Komponenten mit ein paar Einschränkungen. Wenn Sie Aspose.PSD kaufen, werden durch das Anwenden der Lizenz alle Einschränkungen von der installierten Evaluierung entfernt.

Die Evaluierungsversion von Aspose.PSD für Java bietet vollständige Produktdaten, mit nur zwei Einschränkungen:

- **Ein Wasserzeichen auf jedem Bild**: Jedes Bild, das Sie speichern, bearbeiten oder exportieren, enthält ein Wasserzeichen mit der Aufschrift "Nur Evaluierung. Erstellt mit Aspose.PSD. Urheberrecht 2018-2019 Aspose Pty Ltd.". Bei kleinen Bildern, wo das gesamte Wasserzeichen nicht passt, sind stattdessen zwei diagonale Linien über dem Bild vorhanden.
- **Keine Unterstützung für grundlegende Zeichenfunktionen**: Im Evaluierungsmodus können Bilddaten nicht geladen oder im Bild gespeichert werden. Verwenden Sie stattdessen die erweiterte Zeichenfunktionalität, um Bilder zu zeichnen. Diese Einschränkung betrifft Funktionen, die von den grundlegenden Zeichenfunktionen abhängen. Aspose.PSD für Java ermöglicht es Ihnen, Ihr eigenes Dateiformat zu registrieren. Diese Funktion hängt jedoch von den grundlegenden Zeichenfunktionen ab, daher macht es keinen Sinn, sie im Evaluierungsmodus zu verwenden, da Sie den Inhalt dieser Dateien nicht ändern können.

{{% alert color="primary" %}}

Wenn Sie Aspose.PSD für Java ohne die Evaluierungseinschränkungen testen möchten, fordern Sie eine 30-tägige temporäre Lizenz an. Bitte lesen Sie [Wie erhalte ich eine temporäre Lizenz?](https://purchase.aspose.com/temporary-license) für weitere Informationen.

{{% /alert %}}
## **Über die Lizenzdatei**
Sobald Sie mit Ihrer Evaluierung von Aspose.PSD zufrieden sind, können Sie eine Lizenz auf der [Aspose-Website](https://purchase.aspose.com/default.aspx) erwerben. Machen Sie sich mit den verschiedenen angebotenen Abonnementtypen vertraut. Wenn Sie Fragen haben, zögern Sie nicht, das [Verkaufsteam von Aspose](https://company.aspose.com/contact) zu kontaktieren.

Jede Aspose-Lizenz wird mit einem einjährigen Abonnement für Software-Upgrades geliefert. Nach dem ersten Jahr verlängern Sie Ihre Abonnements, um weiterhin die neuesten Funktionen und Fixes zu erhalten. Der technische Support ist kostenlos und unbegrenzt und wird sowohl lizenzierten als auch Evaluierungsnutzern über unsere [Support-Foren](https://forum.aspose.com/) bereitgestellt.

Die Lizenz ist eine XML-Datei, die Details wie den Produktnamen, die Anzahl der lizenzierten Entwickler, das Ablaufdatum des Abonnements usw. enthält. Die Datei ist digital signiert, also ändern Sie sie nicht: Selbst das versehentliche Hinzufügen eines zusätzlichen Zeilenumbruchs macht die Datei ungültig.

Nach dem Kauf von Aspose.PSD müssen Sie die Lizenz anwenden, bevor Sie Bilder erstellen, bearbeiten oder anderweitig manipulieren. Wenn Sie vergessen, die Lizenz anzuwenden, werden alle Ausgabebilder ein Evaluierungswasserzeichen enthalten. 
Sie müssen die Lizenz nur einmal pro Anwendung oder Prozess setzen.
## **Anwendung der Lizenz**
Sie können eine Evaluierungsversion von **Aspose.PSD** für Java von der [Download-Seite](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/) herunterladen. Die Evaluierungsversion bietet absolut die gleichen Funktionen wie die lizenzierte Version des Produkts. Darüber hinaus wird die Evaluierungsversion einfach lizenziert, wenn Sie eine Lizenz erwerben und ein paar Codezeilen hinzufügen, um die Lizenz anzuwenden.

Sobald Sie mit Ihrer Evaluierung von **Aspose.PSD** zufrieden sind, können Sie eine [Lizenz erwerben](http://www.aspose.com/Purchase/Components/Default.aspx) auf der Aspose-Website. Machen Sie sich mit den verschiedenen angebotenen Abonnementtypen vertraut. Wenn Sie Fragen haben, zögern Sie nicht, das Verkaufsteam von Aspose zu kontaktieren.

Jede Aspose-Lizenz beinhaltet ein einjähriges Abonnement für kostenlose Upgrades zu allen neuen Versionen oder Fixes, die in dieser Zeit veröffentlicht werden. Technischer Support ist kostenlos und unbegrenzt und wird sowohl lizenzierten als auch Evaluierungsnutzern bereitgestellt.

{{% alert color="primary" %}}

Wenn Sie **Aspose.PSD** ohne Evaluierungsversionseinschränkungen testen möchten, fordern Sie eine 30-tägige temporäre Lizenz an. Bitte lesen Sie [Wie erhalte ich eine temporäre Lizenz?](http://www.aspose.com/corporate/how-to-get-temporary-license.aspx) für weitere Informationen.

{{% /alert %}}
### **Einstellung einer Lizenz**
Die Lizenz ist eine einfache Text-XML-Datei, die Details wie den Produktnamen, die Anzahl der lizenzierten Entwickler, das Ablaufdatum des Abonnements usw. enthält. Die Datei ist digital signiert, also ändern Sie die Datei nicht; sogar das versehentliche Hinzufügen eines zusätzlichen Zeilenumbruchs in die Datei macht sie ungültig.

Sie müssen eine Lizenz setzen, bevor Sie **Aspose.PSD** verwenden, wenn Sie die Evaluierungseinschränkungen vermeiden möchten. Sie müssen die Lizenz nur einmal pro Anwendung oder Prozess setzen.

Die Lizenz kann von einem Stream oder einer Datei an den folgenden Orten geladen werden:

1. Expliziter Pfad.
1. Der Ordner, der die Aspose.PSD.jar-Datei enthält.

Verwenden Sie die Methode [License](http://www.aspose.com/api/java/psd/com.aspose.psd/classes/License).setLicense, um die Komponente zu lizenzieren. Oft ist der einfachste Weg, eine Lizenz zu setzen, die Lizenzdatei in denselben Ordner wie Aspose.PSD.jar zu legen und nur den Dateinamen ohne Pfad anzugeben, wie im folgenden Beispiel gezeigt:
#### **Beispiel 1**
In diesem Beispiel versucht **Aspose.PSD**, die Lizenzdatei im Ordner zu finden, der die JARs Ihrer Anwendung enthält.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense("Aspose.PSD.Java.lic");

{{< /highlight >}}
#### **Beispiel 2**
Initialisiert eine Lizenz aus einem Stream.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense(new java.io.FileInputStream("Aspose.PSD.Java.lic"));

{{< /highlight >}}
### **Überprüfen der Lizenz**
Es ist möglich zu überprüfen, ob die Lizenz ordnungsgemäß gesetzt wurde oder nicht. Die Klasse License verfügt über das Feld isLicensed, das true zurückgibt, wenn die Lizenz ordnungsgemäß gesetzt wurde.

**Java**

{{< highlight csharp >}}

 License license = new License();

license.setLicense("Aspose.PSD.Java.lic");

if (License.isLicensed()) {

    System.out.println("Die Lizenz wurde festgelegt!");

}

{{< /highlight >}}
## **Wo Sie eine Lizenz in Ihrer Anwendung anwenden sollten**
Wo Sie eine Lizenz anwenden, hängt vom Typ der Anwendung ab, die Sie entwickeln. Befolgen Sie diese einfachen Regeln:

- Die Lizenz muss nur einmal pro Anwendungsdomäne festgelegt werden. Das mehrmalige Aufrufen von License.setLicense ist nicht schädlich, sondern verschwendet Prozessorzeit.
- Wenden Sie die Lizenz an, bevor Sie irgendwelche Aspose.PSD-Klassen aufrufen.
- **Java-Anwendungen**: rufen Sie License.SetLicense im Startcode auf.
- **Klassenbibliothek**: rufen Sie License.setLicense aus einem statischen Konstruktor der Klasse auf, die Aspose.PSD verwendet. Der statische Konstruktor wird ausgeführt, bevor eine Instanz Ihrer Klasse erstellt wird, um sicherzustellen, dass die Aspose.PSD-Lizenz ordnungsgemäß festgelegt ist.
## **Verwendung mehrerer Aspose-Produkte**
Wenn Sie mehr als ein Aspose-Produkt in Ihrer Anwendung verwenden, zum Beispiel Aspose.PSD und Aspose.Cells, hier sind ein paar nützliche Tipps.

- **Wenden Sie die Lizenz für jedes Aspose-Produkt separat an**. Selbst wenn Sie eine einzelne Lizenzdatei für alle Komponenten haben, z. B. 'Aspose.Total.lic', müssen Sie License.setLicense für jedes Aspose-Produkt in Ihrer Anwendung separat aufrufen.
- **Verwenden Sie einen voll qualifizierten Lizenzklassennamen**. Jedes Aspose-Produkt hat eine Lizenzklasse in seinem Namespace. Zum Beispiel hat Aspose.PSD com.aspose.psd.license.License und Aspose.Cells com.aspose.cells.License. Die Verwendung eines voll qualifizierten Klassennamens vermeidet Verwirrung darüber, welche Lizenz für welches Produkt angewendet wird.
