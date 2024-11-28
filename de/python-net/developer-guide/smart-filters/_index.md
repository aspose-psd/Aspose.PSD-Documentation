---
title: Intelligente Filtermanipulation in Aspose.PSD für Python
weight: 100
type: docs
description: Beispiele zur Verwendung von Smart Filtern in einer PSD-Datei
keywords: [intelligenter Filter, Rauschen hinzufügen, Gaußscher Weichzeichner, schärfen, Filter, PSD-Filter, PSD-API, Python, Codebeispiel]
url: de/python-net/smart-filters/
---

## **Übersicht**

Es gibt 3 Möglichkeiten, intelligente Filter in Aspose.PSD für Python anzuwenden.

## **Direkte Filteranwendung**
In diesem Codebeispiel sehen wir, wie intelligente Filter in Aspose.PSD für Python direkt angewendet werden können.

Zunächst gibt der Code die Quell-PSD-Datei, die Ausgabedatei für das Originalbild und die Ausgabedatei für das aktualisierte Bild an.

Anschließend lädt der Code das PSD-Bild mithilfe der Methode Image.load() und wandelt es in ein PsdImage-Objekt um.

Das Originalbild wird dann mithilfe der Methode save() mit dem angegebenen Ausgabedateinamen gespeichert.

Es wird ein SharpenSmartFilter-Objekt erstellt, das den anzuwendenden intelligenter Filter darstellt.

Der Code ruft dann die reguläre Ebene aus dem PSD-Bild unter Verwendung von im.layers[1] ab.

Eine Schleife wird anschließend verwendet, um den Schärfenfilter drei Mal auf die reguläre Ebene anzuwenden.

Schließlich wird das aktualisierte Bild mithilfe der Methode save() und des angegebenen Ausgabedateinamens gespeichert.

Dieser Code zeigt, wie intelligente Filter in Aspose.PSD für Python direkt angewendet werden können. Durch Verwendung der entsprechenden Filterobjekte und deren Anwendung auf die gewünschten Ebenen können Sie die gewünschten Effekte auf Ihren Bildern erzielen.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-direct-apply.py" >}}

## **Manipulation Intelligenter Filter in den Smart-Objekten**

Zunächst gibt der Code die Quell-PSD-Datei, die Ausgabedatei für das Originalbild und die Ausgabedatei für das aktualisierte Bild an.

Das PSD-Bild wird mithilfe der Methode Image.load() geladen und dann in ein PsdImage-Objekt umgewandelt.

Das Originalbild wird mithilfe der Methode save() mit dem angegebenen Ausgabedateinamen gespeichert.

Der Code wandelt dann die zweite Ebene des PSD-Bildes in ein SmartObjectLayer-Objekt um, das die Smart-Objektebene darstellt.

Der Code bearbeitet dann die intelligenten Filter. In diesem Beispiel wird gezeigt, wie mit zwei Arten von intelligenten Filtern gearbeitet wird: GaussianBlurSmartFilter und AddNoiseSmartFilter.

Für den GaussianBlurSmartFilter aktualisiert der Code die Filterwerte, einschließlich Radius, Mischmodus, Deckkraft und ob er aktiviert ist oder nicht.

Für den AddNoiseSmartFilter setzt der Code die Rauschverteilung auf NoiseDistribution.UNIFORM.

Als Nächstes fügt der Code der Smart-Objektebene zwei neue Filterelemente hinzu: einen weiteren GaussianBlurSmartFilter und einen AddNoiseSmartFilter.

Nach Hinzufügen der neuen Filter wendet der Code die Änderungen mithilfe der Methode update_resource_values() an.

Schließlich wird gezeigt, wie die Filter direkt auf die Ebene und auf die Maske der Ebene mit den Methoden apply() bzw. apply_to_mask() angewendet werden.

Das aktualisierte Bild wird dann mithilfe der Methode save() und des angegebenen Ausgabedateinamens gespeichert.

Durch die Verwendung dieses Codebeispiels können Sie lernen, wie man mit intelligenten Filtern in Aspose.PSD für Python arbeitet. Die Bibliothek bietet eine breite Palette von intelligenten Filtern, von denen jeder über eine Reihe von Eigenschaften und Methoden verfügt, die angepasst werden können, um die gewünschten Effekte auf Ihren Bildern zu erzielen.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-features.py" >}}

## **Anwendung von Smart-Filtern auf Ebenenmaske**

Anwendung von Smart-Filtern auf Masken: Eine leistungsstarke Bildbearbeitungstechnik

Intelligente Filter sind ein beliebtes Feature in Bildbearbeitungssoftware, das es Benutzern ermöglicht, verschiedene Filter und Effekte auf ihren Bildern anzuwenden. Eine interessante Technik, die mit intelligenten Filtern erreicht werden kann, besteht darin, sie auf Masken anzuwenden. In diesem Artikel werden wir erkunden, wie intelligente Filter auf Masken angewendet werden und ihre Verwendung in der Welt der Bildbearbeitung diskutieren.

Was ist eine Maske? Bevor wir uns damit befassen, intelligente Filter auf Masken anzuzuwenden, wollen wir zunächst verstehen, was eine Maske ist. In der Bildbearbeitung ist eine Maske ein Graustufenbild, das die Transparenz bestimmter Bereiche eines Bildes bestimmt. Eine Maske kann verwendet werden, um Filter, Anpassungen oder Effekte selektiv auf bestimmte Teile eines Bildes anzuwenden, während andere Bereiche unverändert bleiben.

Anwendung von Smart-Filtern auf Masken: Bei der Anwendung von intelligenten Filtern auf Masken werden die Filter nur auf die durch die Maske angegebenen Bereiche angewendet. Dies ermöglicht eine präzise Steuerung darüber, welche Teile des Bildes vom Filter betroffen sind. Durch die Manipulation der Maske können Sie die Intensität und den Umfang der Filterwirkung bestimmen.

Bitte überprüfen Sie das vorherige Beispiel und die Methode: [API-Referenz Anwenden eines intelligenten Filters auf Maske](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)
