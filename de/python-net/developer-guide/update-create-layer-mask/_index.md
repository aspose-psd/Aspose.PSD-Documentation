---
title: Arbeiten mit Masken in Aspose.PSD für Python
weight: 100
type: docs
description: Beispiele, wie man mit Clipping-, Raster- und Vektormasken innerhalb einer PSD-Datei arbeitet
keywords: [masken, Ebenenmaske, Vektormaske, Clipping-Maske, psd, psd api, python, Codebeispiel]
url: de/python-net/update-create-layer-mask/
---

## **Übersicht**

**Überblick**

Es gibt 3 Arten von Masken in PSD-Dateien:
1. Clipping-Masken
2. Rastermasken
3. Vektormasken

Dieser Artikel behandelt alle 3 Arten.

**Clipping-Masken**

Clipping-Masken sind ein leistungsmerkmal in Grafikdesign- und Bildbearbeitungssoftware. Sie ermöglichen es, die Sichtbarkeit einer Ebene basierend auf der Form und dem Inhalt einer anderen Ebene zu steuern. Mit anderen Worten, eine Clipping-Maske beschränkt die Sichtbarkeit einer Ebene auf die Form einer anderen Ebene darunter.

Um eine Clipping-Maske zu erstellen, benötigen Sie zunächst zwei Ebenen: die Basis-Ebene und die Ebene, die Sie ausblenden möchten. Die Basis-Ebene definiert die Form oder den Bereich, der sichtbar sein wird, während die Ebene, die Sie ausblenden möchten, den Inhalt enthält, der an die Form der Basis-Ebene angepasst wird.

Wenn Sie eine Clipping-Maske anwenden, ist der Inhalt der auszublendenden Ebene nur innerhalb der Grenzen der Basis-Ebene sichtbar. Jeglicher Inhalt außerhalb der Grenzen der Basis-Ebene wird verborgen oder ausgeblendet.

Clipping-Masken sind besonders nützlich, wenn Sie einen Effekt wie eine Textur oder ein Muster auf einen bestimmten Bereich eines Bildes oder Kunstwerks anwenden möchten. Durch Verwenden einer Clipping-Maske können Sie den Effekt auf den gewünschten Bereich beschränken, ohne den Rest des Bildes zu beeinträchtigen.

Bitte überprüfen Sie das Beispiel am Ende der Seite.

**Rastermasken**

Rastermasken in PSD-Dateien werden verwendet, um die Sichtbarkeit spezifischer Bereiche innerhalb einer Ebene zu steuern. Im Gegensatz zu Vektormasken, die mathematische Formen zur Definition der maskierten Bereiche verwenden, nutzen Rastermasken pixelbasierte Informationen, um festzulegen, welche Teile einer Ebene sichtbar oder verborgen sind.

Eine Rastermaske besteht aus einem Graustufenbild, das auf eine Ebene angewendet wird. Die weißen Bereiche der Maske repräsentieren die sichtbaren Teile, während die schwarzen Bereiche die verborgenen Teile repräsentieren. Grautöne dazwischen können verwendet werden, um teilweise Transparenz oder halb sichtbare Bereiche zu erstellen.

Bitte überprüfen Sie das Beispiel am Ende der Seite.

**Vektormasken**

Vektormasken in PSD-Dateien sind ein vielseitiges Werkzeug, um die Sichtbarkeit spezifischer Bereiche innerhalb einer Ebene basierend auf mathematischen Formen zu definieren. Im Gegensatz zu Rastermasken, die pixelbasierte Informationen verwenden, nutzen Vektormasken Pfade und Kurven, um glatte und skalierbare maskierte Bereiche zu erstellen.

Eine Vektormaske ist im Wesentlichen ein Pfad, der auf eine Ebene angewendet wird. Die Form des Pfads bestimmt, welche Teile der Ebene sichtbar und welche verborgen sind. Durch Manipulation der Steuerpunkte und Kurven des Pfads können Sie präzise und komplexe maskierte Bereiche erstellen.

Bitte besuchen Sie die [Vektormasken-Seite](psd/de/net/layer-vector-mask/), um Informationen darüber zu erhalten, wie die Vektormasken mittels Ressourcen hinzugefügt werden können.


## **Beispiel**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentation-Python-Aspose-psd-update-create-layer-mask.py" >}}
