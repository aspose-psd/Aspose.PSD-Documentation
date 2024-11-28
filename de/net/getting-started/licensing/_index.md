---
title: Lizenzierung
type: docs
weight: 70
url: /de/net/licensing/
description: Bewerten Sie die PSD Photoshop C#-Bibliothek von NuGet und wenden Sie die Lizenz mit einer Datei oder einem Stream an, um alle Einschränkungen der installierten Evaluation zu entfernen.
---

## **Einschränkungen der Evaluierungsversion**
Sie können eine Evaluierungsversion von Aspose.PSD für .NET von [NuGet](https://www.nuget.org/packages/Aspose.psd) herunterladen. Die Evaluierungsversion bietet die gleichen Funktionen wie die voll lizenzierte Version des Komponenten mit ein paar Einschränkungen. Wenn Sie Aspose.PSD kaufen, entfernt das Anwenden der Lizenz einfach alle Einschränkungen von der installierten Evaluation. Die Evaluierungsversion von Aspose.PSD für .NET bietet volle Produktfunktionalität, mit nur zwei Einschränkungen:

- **Ein Wasserzeichen auf jedem Bild**: Jedes Bild, das Sie speichern, ändern oder exportieren, hat ein Wasserzeichen mit der Aufschrift "Evaluation Only. Created with Aspose.PSD. Copyright 2010-2018 Aspose Pty Ltd.". Kleine Bilder, bei denen das gesamte Wasserzeichen nicht passt, weisen stattdessen zwei diagonale Linien über das Bild auf.
- **Keine Unterstützung für grundlegende Zeichenfunktionen**: Im Evaluierungsmodus können keine Bildpixel geladen oder im Bild gespeichert werden. Verwenden Sie stattdessen die erweiterten Zeichenfunktionen zum Zeichnen von Bildern. Diese Einschränkung betrifft Funktionen, die von den grundlegenden Zeichenfunktionen abhängen. Aspose.PSD für .NET ermöglicht es Ihnen, Ihr eigenes Dateiformat zu registrieren. Diese Funktion hängt jedoch von den grundlegenden Zeichenfunktionen ab, daher macht es keinen Sinn, sie im Evaluierungsmodus zu verwenden, da Sie den Inhalt dieser Dateien nicht ändern können.

Wenn Sie Aspose.PSD für .NET ohne die Evaluierungseinschränkungen testen möchten, fordern Sie eine 30-tägige temporäre Lizenz an. Bitte beachten Sie [Wie Sie eine temporäre Lizenz erhalten?](https://purchase.aspose.com/temporary-license) für weitere Informationen.
## **Über die Lizenzdatei**
Sobald Sie mit Ihrer Evaluation von Aspose.PSD zufrieden sind, können Sie eine Lizenz auf der [Aspose-Website](https://purchase.aspose.com/default.aspx) erwerben. Machen Sie sich mit den verschiedenen angebotenen Abonnementtypen vertraut. Bei Fragen zögern Sie nicht, sich an das [Verkaufsteam von Aspose](https://company.aspose.com/contact) zu wenden. Jede Aspose-Lizenz wird mit einem einjährigen Abonnement für Software-Upgrades geliefert. Nach dem ersten Jahr erneuern Sie Ihre Abonnements, um die neuesten Funktionen und Fixes zu erhalten. Technischer Support ist kostenlos und unbegrenzt und wird sowohl lizenzierten als auch Evaluierungsnutzern über unsere [Support-Foren](https://forum.aspose.com/) angeboten. Die Lizenz ist eine XML-Datei, die Details wie den Produktnamen, die Anzahl der lizenzierten Entwickler, das Ablaufdatum des Abonnements usw. enthält. Die Datei ist digital signiert, daher dürfen Sie sie nicht ändern: selbst das unbeabsichtigte Hinzufügen eines zusätzlichen Zeilenumbruchs macht die Datei ungültig. Nach dem Kauf von Aspose.PSD müssen Sie die Lizenz anwenden, bevor Sie Bilder erstellen, bearbeiten oder anderweitig manipulieren. Wenn Sie vergessen, die Lizenz anzuwenden, werden alle Ausgabebilder ein Evaluierungswasserzeichen haben. Sie müssen die Lizenz nur einmal pro Anwendung oder Prozess setzen.
## **Wo Sie eine Lizenz in Ihrer Anwendung anwenden**
Wo Sie eine Lizenz anwenden, hängt vom Typ der Anwendung ab, die Sie entwickeln. Befolgen Sie diese einfachen Regeln:

- Wenden Sie die Lizenz nur einmal pro Anwendungsdomäne an. Das mehrmalige Aufrufen von License.SetLicense ist nicht schädlich, verschwendet aber Prozessorzeit.
- Wenden Sie die Lizenz an, bevor Sie Aspose.PSD für .NET-Klassen aufrufen.
- **Windows Forms- oder Konsolenanwendungen**: Rufen Sie License.SetLicense im Startcode auf, bevor Sie Aspose.PSD für .NET-Klassen verwenden.
- **ASP.NET-Anwendungen**: Rufen Sie License.SetLicense aus der Global.asax.cs (Global.asax.vb)-Datei im Application_Start geschützten Methoden auf. Auf diese Weise wird es einmal beim Starten der Anwendung aufgerufen. Rufen Sie License.SetLicense nicht innerhalb der Page_Load-Methoden auf, da die Lizenz jedes Mal geladen wird, wenn eine Webseite geladen wird.
- **Silverlight-Anwendungen**: Rufen Sie License.SetLicense aus dem Application_Startup-Ereignis in der App.xaml.cs (App.xaml.vb)-Datei auf.
- **Klassenbibliothek**: Rufen Sie License.SetLicense aus einem statischen Konstruktor der Klasse auf, die Aspose.PSD verwendet. Der statische Konstruktor wird ausgeführt, bevor eine Instanz Ihrer Klasse erstellt wird, was sicherstellt, dass die Aspose.PSD-Lizenz ordnungsgemäß gesetzt ist.
## **Lizenz anwenden**
Sie können leicht eine Evaluierungsversion von Aspose.PSD von der NuGet [Download-Seite](https://www.nuget.org/packages/Aspose.psd/) herunterladen. Die Evaluierungsversion bietet absolut die gleichen Funktionen wie die lizenzierte Version von Aspose.PSD. Darüber hinaus wird die Evaluierungsversion einfach lizenziert, wenn Sie eine Lizenz kaufen und ein paar Zeilen Code hinzufügen, um die Lizenz anzuwenden.
### **Verwendung einer Datei oder eines Streams**
Wenn Sie mit den Evaluierungseinschränkungen nicht arbeiten möchten, müssen Sie eine Lizenz setzen, bevor Sie Aspose.PSD verwenden. Sie müssen die Lizenz nur einmal pro Anwendung (oder Prozess) setzen.
### **Anwenden einer Lizenz aus einer Datei**
Der einfachste Weg, eine Lizenz anzuwenden, besteht darin, die Lizenzdatei im gleichen Ordner wie die Aspose.PSD.dll zu platzieren. Dann können Sie den Dateinamen im Code anstelle eines vollständigen Pfads angeben.



{{< highlight java >}}

 // Instantiieren Sie eine Instanz der Lizenz und wenden Sie die Lizenz unter Verwendung eines vollständigen Pfads an

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense("Aspose.PSD.lic");



{{< /highlight >}}



Wenn Sie die SetLicense-Methode aufrufen, sollte der Lizenzname dem Namen Ihrer Lizenzdatei entsprechen. Wenn Sie beispielsweise den Namen der Lizenzdatei in "Aspose.PSD.lic.xml" ändern, sollten Sie diesen Lizenznamen für die SetLicense-Methode verwenden.
### **Anwenden einer Lizenz unter Verwendung eines Streams**
Es ist auch möglich, eine Lizenz aus einem Stream zu laden, wie unten dargestellt.



{{< highlight java >}}



// Instantiieren Sie eine Instanz der Lizenz und wenden Sie die Lizenz unter Verwendung eines Streams an

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense(myStream);



{{< /highlight >}}
### **Überprüfen des Lizenzstatus**
Die Klasse Aspose.PSD.License verfügt über die IsLicensed-Eigenschaft, die true zurückgibt, wenn die Lizenz ordnungsgemäß gesetzt wurde.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("Lizenz ist gesetzt!");

}

{{< /highlight >}}
### **Verwendung einer eingebetteten Ressource**
Eine praktische Möglichkeit, die Lizenz mit Ihrer Anwendung zu verpacken und sicherzustellen, dass sie nicht verloren geht, besteht darin, sie als eingebettete Ressource in eine der Assemblys einzuschließen, die Aspose.PSD aufruft. Um die Lizenzdatei als eingebettete Ressource einzuschließen:

1. Klicken Sie in Visual Studio .NET auf das **Datei**-Menü und wählen Sie **Vorhandenes Element hinzufügen**.
1. Fügen Sie die Lizenzdatei (Erweiterung .lic) dem Projekt hinzu.
1. Wählen Sie die Datei im Lösungsfenster aus.
1. Setzen Sie im Eigenschaftenfenster **Build Action** auf **Eingebettete Ressource**.

Es ist nicht erforderlich, die Methoden GetExecutingAssembly oder GetManifestResourceStream der System.Reflection.Assembly in das Microsoft .NET Framework aufzurufen, um auf eine eingebettete Lizenz zuzugreifen. Betten Sie stattdessen die Datei als Ressource in das Projekt ein und übergeben Sie den Dateinamen der Lizenzdatei an die SetLicense-Methode. Die Klasse License findet die Lizenzdatei automatisch in den eingebetteten Ressourcen. Das folgende Beispiel zeigt, wie Sie die Lizenz als eingebettete Ressource einschließen und auf Ihre Anwendung anwenden.



{{< highlight java >}}

 // Instantiieren Sie die Lizenzklasse

Aspose.PSD.License license = new Aspose.PSD.License();



// Geben Sie den Namen der eingebetteten Lizenzdatei an

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}


### **Überprüfen des Lizenzstatus**
Die Klasse Aspose.PSD.License verfügt über die IsLicensed-Eigenschaft, die true zurückgibt, wenn die Lizenz ordnungsgemäß gesetzt wurde.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("Lizenz ist gesetzt!");

}

{{< /highlight >}}
