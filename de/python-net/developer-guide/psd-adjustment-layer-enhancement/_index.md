---
title: Verwenden von Anpassungsebene zur PSD-Verbesserung
weight: 100
type: docs
description: Beispiele zur Verwendung von Anpassungsebenen über Aspose.PSD für Python
keywords: [Anpassungsebene, Fotoverbesserung, Kurvenanpassung, Ebenenverbesserung, invertieren, Fotofilter, psd api, python, Codebeispiel]
url: de/python-net/adjustment-layer-enhancement/
---

## **Überblick**

In diesem Artikel werden wir die Bearbeitung von Anpassungsebenen in Aspose.PSD für Python erkunden. Anpassungsebenen sind ein leistungsstarkes Feature der Bildbearbeitung, das es Ihnen ermöglicht, nicht-destruktive Änderungen an Ihren Bildern vorzunehmen. Aspose.PSD bietet eine umfassende Reihe von Anpassungsebenen-Klassen, die Sie verwenden können, um verschiedene Aspekte Ihrer Bilder zu modifizieren.

Um die Bearbeitung von Anpassungsebenen zu demonstrieren, werden wir ein Beispielcode-Schnipsel verwenden, der am Ende der Seite ein PSD-Bild lädt und verschiedene Anpassungen auf seine Ebenen anwendet.

Im folgenden Code-Schnipsel laden wir zunächst das PSD-Bild mithilfe der Methode PsdImage.load(). Anschließend richten wir die Optionen ein, um die Ausgabebilddateien im PNG-Format zu speichern. Die Klasse PngOptions ermöglicht es uns, den Farbtyp für das Ausgangsbild festzulegen.

Danach iterieren wir durch jede Ebene im PSD-Bild und überprüfen ihren Typ mithilfe der Methode is_assignable(). Wenn die Ebene von einem bestimmten Typ ist, gießen wir sie in diesen Typ mithilfe der Methode cast() und wenden die gewünschte Anpassung an. Beispielsweise passen wir die Helligkeit und den Kontrast einer BrightnessContrastLayer an, ändern die Ebenen eines LevelsLayer, fügen einem CurvesLayer einen Kurvenpunkt hinzu usw.

Sie können zusätzlichen Code hinzufügen, um weitere Anpassungen an den entsprechenden Ebenen vorzunehmen. Aspose.PSD bietet eine Vielzahl von Anpassungsebenen-Klassen wie [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) und mehr.

Abschließend speichern wir das geänderte Bild mithilfe der Methode save() der Klasse PsdImage.

Dieser Code bietet einen grundlegenden Überblick darüber, wie man Anpassungsebenen in Aspose.PSD für Python bearbeitet. Sie können die Anpassungen nach Ihren Anforderungen anpassen und die verschiedenen Optionen in der API-Dokumentation erkunden.

Bitte prüfen Sie das vollständige Beispiel.

## **Beispiel**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}
