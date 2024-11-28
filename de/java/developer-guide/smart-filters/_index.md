---
title: Intelligente Filtermanipulation in Aspose.PSD für Java
weight: 100
type: docs
description: Beispiele zur Verwendung von Smart Filtern in PSD-Datei
keywords: [intelligenter Filter, Rauschen hinzufügen, Gauß'scher Unscharfmaskierung, Schärfen, Filter, psd Filter, psd api, Java, Codebeispiel]
url: de/java/smart-filters/
---

## **Übersicht**

Es gibt 3 Methoden zur Anwendung von Smart-Filtern in Aspose.PSD für Java.

## ** Direkte Filteranwendung **
Dieses Codebeispiel zeigt, wie Smart-Filter direkt in Aspose.PSD für Java angewendet werden.

Zunächst definiert der Code die Quell-PSD-Datei, die Ausgabedatei für das Originalbild und die Ausgabedatei für das aktualisierte Bild.

Dann lädt der Code das PSD-Bild mithilfe der Methode Image.load() und konvertiert es in ein PsdImage-Objekt.

Das Originalbild wird mithilfe der Methode save() gespeichert und der Ausgabedateiname wird angegeben.

Es wird ein SharpenSmartFilter-Objekt instanziiert, um den gewünschten Smart-Filter zu repräsentieren.

Anschließend ruft der Code die normale Ebene aus dem PSD-Bild mithilfe von psdImage.getLayers()[1] ab.

Eine Schleife wird genutzt, um den Schärfenfilter dreimal auf die normale Ebene anzuwenden.

Abschließend wird das aktualisierte Bild mithilfe der Methode save() mit dem bereitgestellten Ausgabedateinamen gespeichert.

Dieser Code veranschaulicht die direkte Anwendung von Smart-Filtern in Aspose.PSD für Java. Durch die Verwendung geeigneter Filterobjekte und das Anwenden auf gewünschte Ebenen können gewünschte Effekte auf Bilder erzielt werden.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentation-Java-Aspose-psd-smart-filter-direct-apply.java" >}}

## ** Smart-Filtermanipulation in den Smart-Objekten **

Dieser Codeausschnitt zeigt, wie Smart-Filter in den Smart-Objekten in Aspose.PSD für Java manipuliert werden können.

Zunächst definiert der Code die Quell-PSD-Datei, die Ausgabedatei für das Originalbild und die Ausgabedatei für das aktualisierte Bild.

Das PSD-Bild wird mithilfe der Methode Image.load() geladen und dann in ein PsdImage-Objekt konvertiert.

Das Originalbild wird mithilfe der Methode save() gespeichert und der Ausgabedateiname wird angegeben.

Der Code konvertiert dann die zweite Ebene des PSD-Bildes in ein SmartObjectLayer-Objekt, das die Smart-Objekt-Ebene darstellt.

Anschließend zeigt der Code die Bearbeitung von Smart-Filtern, wobei zwei Typen dargestellt werden: GaussianBlurSmartFilter und AddNoiseSmartFilter.

Für den GaussianBlurSmartFilter aktualisiert der Code Filterwerte wie Radius, Mischmodus, Deckkraft und Aktivierungsstatus.

Für den AddNoiseSmartFilter setzt der Code die Rauschverteilung auf NoiseDistribution.Uniform.

Als nächstes fügt der Code zwei neue Filterelemente der Smart-Objekt-Ebene hinzu: einen weiteren GaussianBlurSmartFilter und einen AddNoiseSmartFilter.

Nachdem neue Filter hinzugefügt wurden, werden Änderungen mit der Methode updateResourceValues() angewendet.

Zuletzt zeigt der Code das direkte Anwenden von Filtern auf die Ebene und ihre Maske mithilfe der Methoden apply() und applyToMask().

Das aktualisierte Bild wird dann mithilfe der Methode save() mit dem bereitgestellten Ausgabedateinamen gespeichert.

Durch das Folgen dieses Codebeispiels können Sie verstehen, wie Smart-Filter in Smart-Objekten in Aspose.PSD für Java manipuliert werden können. Die Bibliothek bietet eine Vielzahl von Smart-Filtern, von denen jeder über eine eigene Reihe von Eigenschaften und Methoden verfügt, die angepasst werden können, um gewünschte Effekte auf Bilder zu erzielen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentation-Java-Aspose-psd-smart-filter-features.java" >}}

## ** Anwendung von Smart-Filtern auf Ebenenmaske **

Anwendung von Smart-Filtern auf Masken: Eine wirkungsvolle Bildbearbeitungstechnik

Intelligente Filter, die in der Bildbearbeitungssoftware weit verbreitet sind, ermöglichen es Benutzern, verschiedene Filter und Effekte auf ihre Bilder anzu-wenden. Eine faszinierende Technik, die durch Smart-Filter ermöglicht wird, ist deren Anwendung auf Masken. Dieser Artikel untersucht die Anwendung von Smart-Filtern auf Masken und diskutiert ihre Nützlichkeit im Bereich der Bildbearbeitung.

Verständnis von Masken: Bevor man sich mit der Anwendung von Smart-Filtern auf Masken befasst, ist es entscheidend, das Konzept einer Maske zu verstehen. In der Bildbearbeitung ist eine Maske ein Graustufenbild, das die Transparenz bestimmter Bereiche innerhalb eines Bildes bestimmt. Masken ermöglichen eine selektive Anwendung von Filtern, Anpassungen oder Effekten auf bestimmte Teile eines Bildes, während andere unberührt bleiben.

Anwendung von Smart-Filtern auf Masken: Wenn Smart-Filter auf Masken angewendet werden, beeinflussen sie nur die durch die Maske spezifizierten Bereiche und bieten dadurch eine präzise Steuerung über den Einfluss des Filters. Durch die Manipulation der Maske können Benutzer die Intensität und den Umfang der Filterwirkung abstimmen.

Bitte beachten Sie das vorherige Beispiel und die Methode: [API-Referenz Anwendung eines Smart-Filters auf Maske](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)
