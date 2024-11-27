---
title: PSD-Formatübersicht
type: docs
weight: 60
url: /de/net/psd-formatubersicht/
---

## **Beschreibung**
PSD, Photoshop-Dokument, repräsentiert das native Dateiformat von Adobe Photoshop, das für Grafikdesign und -entwicklung verwendet wird.
## **Dateiformatspezifikationen**
Daten in einer PSD-Datei werden in der Byte-Reihenfolge des Big-Endian gespeichert. Dies bedeutet, dass beim Lesen oder Schreiben auf der Windows-Plattform die kurzen und langen Ganzzahlen getauscht werden. Das Photoshop-Dateiformat ist in fünf Hauptteile unterteilt. Es hat viele Längenmarkierungen, die verwendet werden können, um von einem Abschnitt zum nächsten zu wechseln. Die Längenmarkierungen sind normalerweise mit Bytes gepolstert, um zum nächsten 2- oder 4-Byte-Intervall zu runden. Die fünf Hauptteile sind:

- Dateikopf
- Farbmodusdaten
- Bildressourcen
- Ebenen- und Maskeninformationen
- Bilddaten

Zur Konformität sollten Daten in alle diese Felder im Abschnitt geschrieben werden, da Photoshop versuchen kann, den gesamten Abschnitt zu lesen. Dies bedeutet auch, dass Nullen in übersprungene Felder geschrieben werden sollen, wenn sie in eine Datei geschrieben werden. Das Längenfeld in den längenbegrenzten Abschnitten sollte verwendet werden, um zu entscheiden, wann mit dem Lesen aufgehört werden soll. In den meisten Fällen gibt das Längenfeld die Anzahl der Bytes an, die folgen sollen, nicht die Datensätze. Die folgenden Punkte sollten beim Lesen einer Datei beachtet werden.

- Die Werte in der "Länge"-Spalte in allen Tabellen sind in Bytes.
- Alle Werte, die als Unicode-Zeichenfolge definiert sind, bestehen aus:
- Einem 4-Byte-Längenfeld, das die Anzahl der Zeichen in der Zeichenfolge (nicht Bytes) darstellt.
- Die Zeichenfolge von Unicode-Werten, zwei Bytes pro Zeichen.
## **Merkmale des Formats**
PSD-Dateien können Bildschichtebenen, Anpassungsebenen, Ebenenmasken, Annotationen, Dateiinformationen, Schlüsselwörter und andere Photoshop-spezifische Elemente enthalten. Photoshop-Dateien haben die Standarderweiterung .PSD und haben eine maximale Höhe und Breite von 30.000 Pixeln und ein Längenlimit von zwei Gigabyte.
## **Wie kann es verwendet werden**
1. Ein Werkzeug für PSD-Slicing.
1. [PSD in HTML konvertieren](/psd/de/net/psd-image-in-rasterformat-konvertieren/)
1. Verwendung von [PSD als Vorlage](/psd/de/net/verwendung-von-psd-dateien-als-vorlagen-fur-automatisierte-visitenkarten/) für E-Mails
1. PSD zu spezifischem CMS-HTML
1. Identikit in PSD-Datei (Polizeiskizze)
1. Pseudo-3D-Vorschaubilder mit Smart-Objekten für Waren wie Flaschen, Tassen, T-Shirts usw. erstellen.
1. Schnelle Bearbeitung von PSD: Autoton, Voreinstellungen, Smart-Objekt, Textebene, Bildausschnitt

Und vieles mehr. Wenn Sie etwas Tolles mit Aspose.PSD erstellt haben, teilen Sie uns bitte Ihre Fallstudie über die [Aspose-Foren](https://forum.aspose.com/) mit.


Zusätzliche Beispiele können Sie hier nachlesen:

- [Fallstudien](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [Vorführungen](/psd/de/net/showcases-html/)
