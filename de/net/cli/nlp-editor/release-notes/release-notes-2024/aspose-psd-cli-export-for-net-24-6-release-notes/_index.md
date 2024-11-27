---
title: Aspose.PSD CLI NLP-Editor für .NET 24.6 - Versionshinweise
type: docs
weight: 90
url: /de/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

Diese Seite enthält die Versionshinweise für [Aspose.PSD CLI NLP-Editor für .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                            | **Kategorie** |
|:-------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110  | Erstveröffentlichung der Aspose.PSD CLI-Anwendungen: Aspose.PSD.CLI.Export und Aspose.PSD.CLI.NLP-Editor |  Verbesserung |


## **Beispiele für die Verwendung:**

**PSDNET-2110. Erstveröffentlichung der Aspose.PSD CLI NLP-Editor Anwendung**

## **Verwendung von der Befehlszeile:**

{{% alert color="primary" %}}
Installieren Sie zunächst dieses dotnet-Tool:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Wir empfehlen vor der ersten Verwendung, den folgenden Befehl auszuführen:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Nach diesem Befehl können Sie diese Anwendung mit dem Kurznamen nlp.cli anstelle von Aspose.PSD.CLI.NLP.Editor ausführen. Sie können auch Ihren eigenen Kurznamen angeben.
{{% /alert %}}

**Beispiele zur Verwendung**

1. Dieser Befehl wandelt die erste gefundene Datei (die mit Aspose.PSD geöffnet werden kann) im aktuellen Ordner in das png-Format mit Transparenz um. Außerdem wird die Lizenz eingerichtet. Sie müssen die Lizenz nur einmal angeben. Bei den nächsten Durchläufen wird die Lizenz aus dem angegebenen Pfad verwendet. Dieser Befehl zeigt das ausführliche Protokoll der NLP-Verarbeitung an, falls verfügbar.
{{< highlight bash >}}nlp.cli Konvertieren Sie die Datei aus diesem Ordner ins png-Format mit Alpha --license "C:\Aspose\Lizenzdatei.lic --verbose "{{< /highlight >}}

2. Dieser Befehl sucht nach der Datei mit dem ähnlichsten Namen zu "smth.psd". Anschließend wird der Kontrast angepasst und sie wird mit bester Qualität als jpeg gespeichert. Der Name der Ausgabedatei wird angezeigt. Es wird smth.jpg sein.
{{< highlight bash >}}Kontrast für Ebene 10 mit dem Namen Ellipse in der Datei smth.psd anpassen und sie mit bester Qualität als output.jpg speichern{{< /highlight >}}

3. Dieser Befehl wird die Datei im angegebenen Pfad öffnen und ihre Größe auf 25 % reduzieren. Die Ausgabedatei wird angezeigt. Sie wird im aktuellen Ordner der Konsole gespeichert.
{{< highlight bash >}}Größe der Datei C:\Benutzer\irgendeinbenutzer\Desktop\input.psd auf 25 % reduzieren{{< /highlight >}}

4. Dieser Befehl sucht nach der Datei input.psd in C:\Benutzer\irgendeinbenutzer\Desktop\. Anschließend wird die Ebene mit Index 3 gefunden und auf eine Breite von 50px und eine Höhe von 100px angepasst. Dann wird diese Ebene als PDF-Datei in C:\Benutzer\irgendeinbenutzer\Desktop\output.pdf gespeichert.
{{< highlight bash >}}Legen Sie die Ebene mit Index 3 von C:\Benutzer\irgendeinbenutzer\Desktop\input.psd auf eine Breite von 50 und eine Höhe von 100 fest und speichern Sie sie in C:\Benutzer\irgendeinbenutzer\Desktop\output.pdf{{< /highlight >}}

 5. Dieser Befehl öffnet smth.psd im aktuellen Ordner, jedoch werden alle Effekte deaktiviert. Anschließend wird diese Datei in das BMP-Format konvertiert und als output.bmp im aktuellen Ordner gespeichert.
 {{< highlight bash >}}Öffnen Sie smth.psd ohne Effekte und speichern Sie es als output.bmp{{< /highlight >}}

**Haftungsausschluss**

Dies ist eine experimentelle Anwendung. Bitte testen Sie sie und hinterlassen Sie Feedback. Jedes Feedback wird sehr geschätzt. Unser Ziel ist es, die NO-Code-Anwendung auf die nächste Ebene zu bringen. Eine einfache Integration in jeden Build-Pipeline oder Geschäftsprozess ist unser Ziel.
