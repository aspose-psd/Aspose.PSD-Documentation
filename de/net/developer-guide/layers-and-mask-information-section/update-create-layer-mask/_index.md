---
title: Arbeiten mit Masken in Aspose.PSD für C#
weight: 100
type: docs
description: Beispiele zur Arbeit mit Clipping-, Raster- und Vektormasken innerhalb der PSD-Datei
keywords: [masken, Ebenenmaske, Vektormaske, Clipping-Maske, psd, psd api, C#, csharp, Codebeispiel]
url: de/net/update-create-layer-mask/
---

## Überblick

Es gibt drei Arten von Masken in PSD-Dateien:
1. Clipping-Masken
2. Rastermasken
3. Vektormasken

In diesem Artikel werden alle drei Arten abgedeckt.

### Clipping-Masken

Clipping-Masken sind eine leistungsstarke Funktion in der Grafikgestaltungs- und Bildbearbeitungssoftware, die es Ihnen ermöglicht, die Sichtbarkeit einer Ebene basierend auf der Form und dem Inhalt einer anderen Ebene zu steuern. Im Wesentlichen beschränkt eine Clipping-Maske die Sichtbarkeit einer Ebene auf die Form, die von einer anderen Ebene darunter definiert wird.

Um eine Clipping-Maske zu erstellen, benötigen Sie zwei Ebenen: die Basis-Ebene und die Maskierungsebene. Die Basis-Ebene definiert die Form oder den Bereich, der sichtbar sein wird, während die Maskierungsebene den Inhalt enthält, der auf die Form der Basis-Ebene beschränkt wird.

Wenn Sie eine Clipping-Maske anwenden, ist der Inhalt der Maskierungsebene nur innerhalb der Grenzen der Basis-Ebene sichtbar. Jeglicher Inhalt außerhalb der Grenzen der Basis-Ebene wird ausgeblendet oder beschnitten.

Clipping-Masken sind besonders nützlich, um Effekte wie Texturen oder Muster auf bestimmte Bereiche eines Bildes oder Kunstwerks anzuwenden. Durch die Verwendung einer Clipping-Maske können Sie sicherstellen, dass der Effekt auf den gewünschten Bereich beschränkt ist, ohne den Rest des Bildes zu beeinträchtigen.

### Rastermasken

Rastermasken in PSD-Dateien sind unverzichtbar, um die Sichtbarkeit bestimmter Bereiche innerhalb einer Ebene zu steuern. Im Gegensatz zu Vektormasken, die mathematische Formen zur Definition maskierter Bereiche verwenden, nutzen Rastermasken pixelbasierte Informationen, um zu bestimmen, welche Teile einer Ebene sichtbar oder verborgen sind.

Eine Rastermaske besteht aus einem Graustufenbild, das auf eine Ebene angewendet wird. Die weißen Bereiche der Maske repräsentieren die sichtbaren Teile, während die schwarzen Bereiche die verborgenen Teile darstellen. Graustufen dazwischen erzeugen eine teilweise Transparenz oder halb sichtbare Bereiche.

Durch die Verwendung von Rastermasken können Sie komplexe Maskierungseffekte erzielen, die eine präzise Steuerung über die Sichtbarkeit der Ebene basierend auf pixelgenauen Details ermöglichen. Diese Funktion ist besonders nützlich für Aufgaben, die detaillierte Bearbeitung und Überblendung innerhalb eines Bildes erfordern.

### Vektormasken

Vektormasken in PSD-Dateien sind ein vielseitiges Werkzeug, das zur Definition der Sichtbarkeit bestimmter Bereiche innerhalb einer Ebene basierend auf mathematischen Formen verwendet wird. Im Gegensatz zu Rastermasken, die pixelbasierte Informationen nutzen, verwenden Vektormasken Pfade und Kurven, um glatte und skalierbare maskierte Bereiche zu schaffen.

Eine Vektormaske ist im Wesentlichen ein Pfad, der auf eine Ebene angewendet wird. Die Form des Pfads bestimmt, welche Teile der Ebene sichtbar und welche verborgen sind. Durch die Manipulation der Kontrollpunkte und Kurven des Pfads können Sie präzise und komplexe maskierte Bereiche erstellen.

Vektormasken sind besonders nützlich für die Erstellung sauberer, skalierbarer Masken, die ohne Qualitätsverlust leicht angepasst werden können. Diese Funktion eignet sich ideal für Aufgaben, die eine hohe Präzision und Flexibilität bei der Definition sichtbarer Bereiche innerhalb einer Ebene erfordern.

Für weitere Informationen zum Hinzufügen von Vektormasken besuchen Sie bitte die [Seite zu Vektormasken](psd/de/layer-vector-mask/).

## Beispiel
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "WorkingWithMasks-WorkingWithMasks.cs" >}}

Für weitere detaillierte Informationen und Beispiele besuchen Sie bitte die [Aspose.PSD für C#-Dokumentation](https://docs.aspose.com/psd/de/).
