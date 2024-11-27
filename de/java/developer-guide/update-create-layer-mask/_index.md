---
title: Arbeiten mit Masken in Aspose.PSD für Java
weight: 100
type: docs
description: Beispiele, wie man mit Clipping-, Raster- und Vektormasken innerhalb einer PSD-Datei arbeitet
keywords: [masken, Ebenenmaske, Vektormaske, Clippingmaske, psd, psd api, java, Code-Beispiel]
url: de/java/update-create-layer-mask/
---

## **Überblick**

**Überblick**
	
	Es gibt 3 Arten von Masken in PSD-Dateien:
	1. Clipping-Masken
	2. Rastermasken
	3. Vektormasken
	
	Dieser Artikel behandelt alle 3 Arten.

** Clipping-Masken **

Clipping-Masken sind ein leistungsstarkes Merkmal in der Grafikgestaltung und Bildbearbeitungssoftware, insbesondere in Java. Sie ermöglichen eine präzise Kontrolle über die Sichtbarkeit einer Ebene basierend auf der Form und dem Inhalt einer anderen Ebene. Im Wesentlichen beschränkt eine Clipping-Maske die Sichtbarkeit einer Ebene auf die Form einer anderen Ebene darunter.

Um eine Clipping-Maske in Java zu implementieren, benötigen Sie zunächst zwei Ebenen: die Basisebene und die Ebene, die Sie zurechtschneiden möchten. Die Basisebene definiert die Form oder den Bereich, der sichtbar bleiben soll, während die zu schneidende Ebene den Inhalt enthält, der sich der Form der Basisebene anpassen soll.

Wenn eine Clipping-Maske in Java angewendet wird, ist der Inhalt der zugeschnittenen Ebene nur innerhalb der Grenzen der Basisebene sichtbar. Jeglicher Inhalt außerhalb dieser Grenzen wird verborgen oder beschnitten.

Clipping-Masken erweisen sich insbesondere beim Anwenden von Effekten wie Texturen oder Mustern auf spezifische Bereiche eines Bildes oder Kunstwerks als wertvoll. Durch den Einsatz einer Clipping-Maske können Sie den Effekt auf den gewünschten Bereich beschränken, ohne den Rest des Bildes zu beeinflussen.

Bitte beachten Sie das Beispiel am Ende der Seite zur Verdeutlichung.

** Rastermasken ** 

Rastermasken in Java-Dateien werden eingesetzt, um die Sichtbarkeit bestimmter Bereiche innerhalb einer Ebene zu steuern. Im Gegensatz zu Vektormasken, die mathematische Formen zur Definition maskierter Bereiche verwenden, basieren Rastermasken auf pixelbasierten Informationen, um sichtbare oder versteckte Regionen zu bestimmen.

Eine Rastermaske besteht aus einem Graustufenbild, das auf eine Ebene angewendet wird. Weiße Bereiche der Maske stehen für Sichtbarkeit, während schwarze Bereiche versteckte Teile darstellen. Graustufen dazwischen können teilweise Transparenz oder halb sichtbare Regionen erzeugen.

Bitte lesen Sie das Beispiel am Ende der Seite für ein besseres Verständnis.

** Vektormasken **

Vektormasken in Java-Dateien sind vielseitige Werkzeuge, um die Sichtbarkeit bestimmter Bereiche innerhalb einer Ebene basierend auf mathematischen Formen darzustellen. Im Gegensatz zu Rastermasken, die auf pixelbasierten Daten beruhen, verwenden Vektormasken Pfade und Kurven, um glatte und skalierbare maskierte Bereiche zu erstellen.

Eine Vektormaske besteht im Wesentlichen aus einem auf eine Ebene angewendeten Pfad. Die Form dieses Pfades bestimmt, welche Teile der Ebene sichtbar und welche verborgen sind. Durch Manipulation der Kontrollpunkte und Kurven des Pfades können präzise und komplexe maskierte Bereiche erstellt werden.

Bitte lesen Sie die [Seite zu Vektormasken](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/layermaskdatashort/) für Informationen zur Hinzufügung von Vektormasken mithilfe von Ressourcen.

## **Beispiel**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentation-Java-Aspose-psd-update-create-layer-mask.java" >}}
