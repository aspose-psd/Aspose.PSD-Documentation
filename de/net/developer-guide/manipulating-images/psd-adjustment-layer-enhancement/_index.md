---
title: Verwendung von Anpassungsebene für PSD-Verbesserungen
weight: 100
type: docs
description: Beispiele zur Verwendung von Anpassungsebenen über Aspose.PSD für C#
keywords: [Anpassungsebene, Fotoverbesserung, Kurvenanpassung, Levels-Verbesserung, Invertieren, Fotofilter, psd api, C#, csharp, Codebeispiel]
url: de/adjustment-layer-verbesserung/
---

## Überblick

In diesem Artikel werden wir die Bearbeitung von Anpassungsebenen in Aspose.PSD für C# erkunden. Anpassungsebenen sind ein leistungsstarkes Feature bei der Bildbearbeitung, das es Ihnen ermöglicht, nicht destruktive Änderungen an Ihren Bildern vorzunehmen. Aspose.PSD bietet eine umfassende Reihe von Anpassungsebenenklassen, die Sie verwenden können, um verschiedene Aspekte Ihrer Bilder zu ändern.

Um die Bearbeitung von Anpassungsebenen zu demonstrieren, werden wir am Ende der Seite einen Beispielcode verwenden, der ein PSD-Bild lädt und verschiedene Anpassungen auf seine Ebenen anwendet.

Im unten stehenden Codeausschnitt starten wir mit dem Laden des PSD-Bildes über die Methode `PsdImage.Load()`. Anschließend richten wir die Optionen für das Speichern der Ausgabebilddateien ein. Die Klasse `PngOptions` ermöglicht es uns, den Farbtyp für das Ausgabebild festzulegen.

Dann durchlaufen wir jede Ebene im PSD-Bild und prüfen ihren Typ mit der Methode `IsAssignable()`. Wenn die Ebene einen bestimmten Typ hat, gießen wir sie in diesen Typ um mit der Methode `Cast()` und wenden die gewünschte Anpassung an. Zum Beispiel passen wir die Helligkeit und den Kontrast einer `BrightnessContrastLayer` an, bearbeiten die Pegel einer `LevelsLayer`, fügen einen Kurvenpunkt zu einer `CurvesLayer` hinzu, und so weiter.

Sie können zusätzlichen Code hinzufügen, um andere Anpassungen auf ihren jeweiligen Ebenen anzuwenden. Aspose.PSD bietet eine Vielzahl von Anpassungsebenenklassen, wie [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer) und mehr.

Zuletzt speichern wir das geänderte Bild über die Methode `Save()` der Klasse `PsdImage`.

Dieser Code gibt einen grundlegenden Überblick darüber, wie man Anpassungsebenen in Aspose.PSD für C# bearbeitet. Sie können die Anpassungen gemäß Ihren Anforderungen anpassen und die verschiedenen Optionen in der API-Dokumentation erkunden.

## Beispiel

Hier ist ein Codebeispiel, das zeigt, wie man Anpassungsebenen mit Aspose.PSD für C# verwendet:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

Für weitere Informationen und Beispiele besuchen Sie bitte die [Aspose.PSD für C# Dokumentation](https://docs.aspose.com/psd/net/).

