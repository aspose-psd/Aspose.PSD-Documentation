---
title: Verwendung von Einstellungsebene zur PSD-Verbesserung
weight: 100
type: docs
description: Beispiele zur Verwendung der Einstellungsebene über Aspose.PSD für Java
keywords: [Einstellungsebene, Fotoverbesserung, Kurvenanpassung, Ebenenanpassung, invertieren, Fotofilter, PSD API, Java, Codebeispiel]
url: de/java/einstellungsebene-verbesserung/
---

## **Überblick**

Dieser Artikel untersucht die Bearbeitung von Einstellungsebenen in Aspose.PSD für Java. Einstellungsebenen sind ein leistungsstarkes Feature in der Bildbearbeitung, das es Ihnen ermöglicht, nicht destruktive Änderungen an Ihren Bildern vorzunehmen. Aspose.PSD bietet eine umfassende Reihe von Klassen für Einstellungsebenen, die Sie verwenden können, um verschiedene Aspekte Ihrer Bilder zu modifizieren.

Um die Bearbeitung von Einstellungsebenen zu demonstrieren, werden wir am Ende der Seite einen Beispielcode bereitstellen, der ein PSD-Bild lädt und verschiedene Anpassungen an dessen Ebenen vornimmt.

Im folgenden Code-Snippet beginnen wir damit, das PSD-Bild mit der Methode PsdImage.load() zu laden. Anschließend stellen wir die Optionen für das Speichern der Ausgabebilddateien ein. Die Klasse PngOptions ermöglicht es uns, den Farbtyp des Ausgabeimages festzulegen.

Dann durchlaufen wir jede Ebene im PSD-Bild und überprüfen ihren Typ mit Hilfe der Methode isAssignable(). Wenn die Ebene einen bestimmten Typ hat, casten wir sie mit der Methode cast() zu diesem Typ und wenden die gewünschte Anpassung an. Zum Beispiel passen wir die Helligkeit und den Kontrast einer BrightnessContrastLayer an, modifizieren die Ebenen einer LevelsLayer, fügen einen Kurvenpunkt einer CurvesLayer hinzu etc.

Sie können zusätzlichen Code hinzufügen, um weitere Anpassungen an den entsprechenden Ebenen vorzunehmen. Aspose.PSD bietet eine Vielzahl von Klassen für Einstellungsebenen, wie z.B. [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) und mehr.

Abschließend speichern wir das modifizierte Bild mit der Methode save() der Klasse PsdImage.

Dies bietet einen grundlegenden Überblick darüber, wie Einstellungsebenen in Aspose.PSD für Java bearbeitet werden können. Sie können die Anpassungen entsprechend Ihren Anforderungen anpassen und die verschiedenen Optionen in der API-Dokumentation erkunden.

Bitte schauen Sie sich das vollständige Beispiel unten an.

## **Beispiel**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentation-Java-Aspose-Einstellungsebene-Verbesserung.java" >}}
