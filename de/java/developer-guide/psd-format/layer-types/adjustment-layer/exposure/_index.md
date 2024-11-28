---
title: Belichtungsanpassungsschicht
type: docs
weight: 30
url: /de/java/layer-types/adjustment-layer/exposure/
---

# Arbeiten mit der Photoshop Belichtungsanpassungsschicht in Java

In diesem Artikel werden wir eine Belichtungsanpassungsschicht in ein Adobe® Photoshop® Dokument mithilfe der Aspose.PSD for Java - PSD Dateiformat-Manipulationsbibliothek hinzufügen. Die Bibliothek funktioniert ohne installierten Photoshop Editor, da sie eigene Bildverarbeitungsalgorithmen verwendet. Wir haben auch einige Details zur Belichtungsanpassung-API der Bibliothek gelernt.

## API Übersicht

Die Belichtungsanpassungsschicht wird durch die [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer) Klasse konfiguriert, die die folgenden Eigenschaften enthält, um mit der Belichtungsanpassung zu arbeiten:

- Sie definiert, wie viel Licht das Foto hat, indem sie das gesamte Histogramm im Vergleich zu den Schwarztönen zusammenzieht oder streckt. Daher wirkt es hauptsächlich auf die Highlights.
- Anders als der Belichtungsausgleich wirkt sich hauptsächlich auf die Schatten aus.
- Gammakorrektur. Es korrigiert die Helligkeit des Bildes.

## Richtige Belichtung

Die Korrektur der Belichtung und verwandte Eigenschaften sind so einfach wie die Änderung einiger Eigenschaften der Klasse. Lassen Sie uns eine Belichtungsanpassung (a) auf ein unterbelichtetes Foto einer Bibliothek (b) anwenden, um es für das menschliche Auge wahrnehmbar zu machen (c).

![Beispiel für eine Belichtungsanpassungsschicht](exposure-adjustment-layer-figure-1.png)

Die gesamte Anpassung erfolgt hauptsächlich unter Verwendung der Gammakorrektur. Allerdings werden Belichtung und Ausgleich auch leicht angepasst. Alles, was Sie tun müssen, ist, angemessene Werte für die bereits erwähnten Eigenschaften festzulegen:

    ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
    exposureLayer.setExposure(-0.03f);
    exposureLayer.setOffset(-0.0005f);
    exposureLayer.setGammaCorrection(1.85f);

Beachten Sie, dass die Belichtung im Bereich von -20,0 bis 20,0 liegen muss, der Offset-Wert im Bereich von -0,5 bis 0,5 liegen muss und der Bereich des Gamma-Korrekturwerts zwischen 9,99 und 0,01 liegen muss.

Weitere Details finden Sie im [API-Referenz der Belichtungsanpassungsschicht](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer).

## Fazit

In diesem Artikel haben wir gelernt, wie man eine Belichtungsanpassungsschicht in eine PSD-Datei hinzufügt, um das Bild aufzuhellen, sowie einige API-Details betrachtet.
