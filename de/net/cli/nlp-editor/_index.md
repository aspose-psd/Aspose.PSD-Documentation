---
title: Aspose.PSD CLI NLP Editor-Anwendung für .NET
type: docs
weight: 10
url: /de/net/cli/nlp-editor/
is_root: false
keywords: CLI Photoshop-Tool NLP Natural-Language-Processing PSD Konsole C#-Bibliothek PSD API
description: Aspose.PSD-basierte NLP-Editor-CLI-Anwendung für PSD-, PSB- und AI-Dateiformate. No-Code-CI/CD-Automatisierung. Unterstützt die natürliche Sprachverarbeitung zur Bearbeitung von PSD-Dateien. Schreiben Sie einfach Ihre Anfrage in natürlicher Sprache, um verschiedene Operationen wie Konvertierung, Anpassung, Größenänderung und mehr durchzuführen. Es ist nicht erforderlich, dass Adobe Photoshop oder Adobe Illustrator installiert sind, und kann ohne zusätzlichen Code von der Konsole aus ausgeführt werden.
---

**![Aspose.PSD-Produktlogo für .NET](home_1.png)**

**Willkommen bei der Aspose.PSD NLP Editor-CLI-Anwendung für .NET**

Die Aspose.PSD CLI NLP Editor-Anwendung ist ein leichtgewichtiges Konsolendienstprogramm zur Bearbeitung von PSD-Dateien mithilfe von Befehlen in natürlicher Sprache. Einfache Integration in CI/CD-Pipelines.

**Haftungsausschluss**

Dies ist eine experimentelle Anwendung. Bitte testen Sie sie und hinterlassen Sie Feedback. Jedes Feedback wird sehr geschätzt. Unser Ziel ist es, die No-Code-Anwendung auf das nächste Level zu heben. Eine einfache Integration in beliebige Build-Pipelines oder Geschäftsprozesse ist unser Ziel.

**Hauptfunktionen der Aspose.PSD NLP Editor-CLI-Anwendung für .NET**

1. Führen Sie Operationen an PSD-, PSB- und AI-Dateien mit Befehlen in natürlicher Sprache durch.
2. Unterstützt verschiedene Operationen wie Konvertierung, Anpassung, Größenänderung und mehr.
3. No-Code-CI/CD-Automatisierung.
4. Unterstützt das Schreiben von Anfragen in natürlicher Sprache zur Bearbeitung von PSD-Dateien.

## **Verwendung über die Befehlszeile:**

{{% alert color="primary" %}}
Installieren Sie zuerst dieses Dotnet-Tool:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Wir empfehlen vor dem ersten Gebrauch das folgende Kommando auszuführen:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Nach diesem Befehl können Sie diese Anwendung mit dem Kurznamen nlp.cli anstelle von Aspose.PSD.CLI.NLP.Editor ausführen. Sie können Ihren eigenen Kurznamen festlegen.
{{% /alert %}}

**Verfügbare Parameter für die Aspose.PSD.CLI.Crop-Anwendung**

| **Argument** | **Beschreibung**                         |
|:-------------|:----------------------------------------|
| beliebiger Text     | Erforderlich. Ihr Befehl in natürlicher Sprache zur Aktualisierung von PSD- oder PSB-Dateien      |
| Lizenz      | Pfad zur Lizenzdatei.                    |
| ausführlich      | Mehr Informationen zu einem bestimmten Befehl anzeigen. |
| setup        | Erstellt eine Batch-Datei im Tools-Ordner für schnellen Aufruf von der Konsole aus. Beispiel: --setup psd.nlp. Dann können Sie das Tool mit dem Befehl psd.nlp aufrufen |

**Beispiele zur Verwendung:**

1. Mit diesem Befehl wird die erste gefundene Datei (die mit Aspose.PSD geöffnet werden kann) im aktuellen Ordner konvertiert und im PNG-Format mit Transparenz gespeichert. Außerdem wird die Lizenz eingerichtet. Sie müssen die Lizenz nur einmal angeben. Bei den nächsten Ausführungen wird die Lizenz von dem angegebenen Pfad verwendet. Dieser Befehl zeigt das ausführliche Protokoll zur NLP-Verarbeitung an, wenn verfügbar.
{{< highlight bash >}}
  nlp.cli Datei aus diesem Ordner ins PNG-Format mit Alpha konvertieren --license "C:\Aspose\Lizenzdatei.lic --ausführlich "
{{< /highlight >}}

2. Dieser Befehl sucht die Datei mit dem Namen "smth.psd", die dem Namen am ähnlichsten ist. Dann wird der Kontrast angepasst und im JPEG-Format mit bester Qualität gespeichert. Der Name der Ausgabedatei wird angezeigt. Es wird smth.jpg sein.
{{< highlight bash >}}
Kontrast anpassen auf 10 der Ebene mit dem Namen Ellipse in der Datei smth.psd und als output.jpg mit bester Qualität speichern
{{< /highlight >}}

3. Mit diesem Befehl wird die Datei im angegebenen Pfad geöffnet und auf 25 % ihrer Größe reduziert. Die Ausgabedatei wird angezeigt. Sie wird im aktuellen Ordner der Konsole gespeichert.
{{< highlight bash >}}
Datei C:\Benutzer\irgendeiner\Desktop\input.psd auf 25 % verkleinern
{{< /highlight >}}

4. Mit diesem Befehl wird die Datei input.psd in C:\Benutzer\irgendeiner\Desktop\ gefunden. Dann wird die Ebene mit Index 3 angepasst und auf eine Breite von 50px und eine Höhe von 100px skaliert. Anschließend wird diese Ebene als PDF in C:\Benutzer\irgendeiner\Desktop\output.pdf gespeichert.
{{< highlight bash >}}
 Ebene mit Index 3 von C:\Benutzer\irgendeiner\Desktop\input.psd auf eine Breite von 50 und eine Höhe von 100 skalieren und als C:\Benutzer\irgendeiner\Desktop\output.pdf speichern
 {{< /highlight >}}

 5. Mit diesem Befehl wird smth.psd im aktuellen Ordner geöffnet, jedoch werden alle Effekte deaktiviert. Anschließend wird diese Datei im BMP-Format konvertiert und als output.bmp im aktuellen Ordner gespeichert.
 {{< highlight bash >}}
 Öffnen von smth.psd ohne Effekte und Speichern als output.bmp
  {{< /highlight >}}

**Weitere [Aspose.PSD CLI-Anwendungen](https://docs.aspose.com/psd/net/cli) für .NET finden Sie hier, wenn Sie Unterstützung für PSD-, PSB- und AI-Formate in Ihren Workflow integrieren möchten:**

1. [Aspose.PSD CLI Konvertieren](/psd/de/net/cli/convert)
2. [Aspose.PSD CLI Crop](/psd/de/net/cli/crop)
3. [Aspose.PSD CLI Größenänderung](/psd/de/net/cli/resize)
4. [Aspose.PSD CLI Export](/psd/de/net/cli/export)
5. [Aspose.PSD CLI NLP Editor](/psd/de/net/cli/nlp-editor)

**Bitte überprüfen Sie Aspose.PSD für .NET oder [andere Plattformen]** 

Aspose.PSD CLI-Anwendungen sind eine sofort einsatzbereite Lösung für gängige Operationen. Wenn Sie eine flexible Lösung benötigen, überprüfen Sie bitte die Vollversion von Aspose.PSD

1. [Aspose.PSD für .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD für Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD für Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Ressourcen für Aspose.PSD für .NET**

Hier sind Links zu einigen nützlichen Ressourcen, die Sie möglicherweise benötigen, um Ihre Aufgaben zu erledigen.

- [Aspose.PSD CLI-Anwendungen für .NET Online-Dokumentation](/psd/de/net/cli/conversion)
- [Aspose.PSD für CLI-Anwendungen für .NET Versionshinweise](/psd/de/net/cli/conversion/release-notes/)
- [Aspose.PSD für CLI-Anwendungen .NET Produktseite](https://products.aspose.com/psd/net/cli)
- [Aspose.PSD für .NET API-Referenzhandbuch](https://reference.aspose.com/net/psd)
- [Beispiele herunterladen im GitHub-Repository](https://github.com/aspose-psd/CLI-Applications)
- [Aspose.PSD für .NET kostenloser Supportforum](https://forum.aspose.com/c/psd)
- [Aspose.PSD für .NET kostenpflichtiger Support-Helpdesk](https://helpdesk.aspose.com/)

