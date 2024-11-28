---
title: Pixel-Datenmanipulation mit Aspose.PSD für C#
weight: 100
type: docs
description: Beispiel, wie Sie Rohpixel-Daten schnell und direkt mit der PSD C#-API aktualisieren können
keywords: [Pixel bearbeiten, PSD bearbeiten, Ebene bearbeiten, Rohdatenmanipulation, PSD-Daten bearbeiten, PSD API, C#, csharp, Codebeispiel]
url: de/net/pixel-datenmanipulation/
---

## Einführung

Aspose.PSD ist eine leistungsstarke Bibliothek, die es Ihnen ermöglicht, mit Adobe Photoshop-Dateien (PSD) in C# zu arbeiten. In diesem Artikel werden wir untersuchen, wie Sie Pixel-Daten in einer PSD-Datei mit Aspose.PSD für C# manipulieren können.

## Überblick

Der bereitgestellte Code zeigt, wie Sie eine PSD-Datei erstellen, eine neue Ebene hinzufügen, die Pixel-Daten direkt manipulieren und das geänderte Bild speichern.

### Schritte zur Manipulation von Pixel-Daten

1. **Erforderliche Module importieren**:
   Importieren Sie die erforderlichen Module. Sie müssen die Klassen `PsdImage` und `Layer` aus der Aspose.PSD-Bibliothek importieren.

2. **Definieren der Eingabe- und Ausgabedateipfade**:
   Geben Sie die Eingabe- und Ausgabedateipfade an.

3. **Öffnen der Eingabedatei als Stream**:
   Öffnen Sie die Eingabedatei als Stream im Lese-Modus mit der Klasse `FileStream`. Erstellen Sie ein Objekt vom Typ `PsdImage`, indem Sie den Stream laden.

4. **Neues PSD-Bild erstellen**:
   Erstellen Sie ein neues PSD-Bild mithilfe des Konstruktors `PsdImage` und geben Sie die Breite und Höhe der Ebene als Argumente an.

5. **Ebene dem PSD-Bild zuweisen**:
   Weisen Sie die Ebene der Eigenschaft `Layers` des PSD-Bildes zu.

6. **Pixel-Daten manipulieren**:
   Laden Sie die ARGB32-Pixel aus der Ebene mithilfe der Methode `LoadArgb32Pixels`. Definieren Sie eine Indizierung basierend auf der Länge des Pixel-Arrays und ändern Sie die Pixelwerte bei Bedarf.

7. **Geänderte Pixel-Daten speichern**:
   Speichern Sie die geänderten Pixel-Daten zurück in die Ebene mit der Methode `SaveArgb32Pixels`.

8. **PSD-Bild speichern**:
   Speichern Sie das PSD-Bild in der Ausgabedatei mit der Methode `Save`.

### Beispiel

Hier ist ein Codebeispiel, das zeigt, wie Sie Pixel-Daten mit Aspose.PSD für C# manipulieren können:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "PixelDataManipulation-PixelDataManipulation.cs" >}}

### Zusammenfassung

Aspose.PSD für C# bietet eine leistungsstarke Reihe von Funktionen zur Manipulation von Pixel-Daten in PSD-Dateien. Ob Sie Pixel basierend auf bestimmten Bedingungen ändern müssen oder komplexe Muster erstellen möchten, Aspose.PSD macht diese Aufgaben einfach und effizient.

Für weitere detaillierte Informationen und Beispiele besuchen Sie bitte die [Aspose.PSD für C#-Dokumentation](https://docs.aspose.com/psd/net/).
