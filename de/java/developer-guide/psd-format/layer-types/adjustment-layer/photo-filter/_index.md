---
title: Fotofilter-Anpassungsebene
type: docs
weight: 30
url: /de/java/layer-types/adjustment-layer/photo-filter/
---

# Arbeiten mit der Photoshop Fotofilter-Anpassungsebene in Java

Heute werden wir sehen, wie man eine Fotofilter-Anpassungsebene auf ein vorhandenes Photoshop-Dokument anwendet, indem man Aspose.PSD für Java verwendet, das eine Bibliothek zur Manipulation des PSD-Dateiformats ist.

**Die API der Fotofilter-Anpassungsebene** ändert den Farbausgleich des Bildes durch Einfärbung. Das resultierende Bild wird genauso aussehen wie nach Verwendung eines echten Kamerafilters. Beachten Sie, dass die Fotofilter-Anpassungsebenen-API der Bibliothek geringfügig von der von Photoshop abweicht, da es noch keine vordefinierten Filter gibt. Dennoch ist sie in allen anderen Aspekten gleich. Das bedeutet, dass Sie die Farbe der Tönung festlegen und ihre Intensität (Dichte) ändern sowie die Option "Luminanz erhalten" verwenden können.

## API-Überblick

Die API der Fotofilter-Anpassungsebene ist recht einfach zu handhaben. Es gibt die Hauptklasse [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), die als Einstiegspunkt zu dieser Anpassungsebene dient und nur drei öffentliche Eigenschaften enthält, nämlich Farbe, Dichte und Luminanz erhalten, durch die die Anpassung erfolgt.

## Farbausgleich anpassen

Da es nicht viel zu besprechen gibt, betrachten wir **ein Beispiel für die Anpassung des Farbausgleichs** mit dem Fotofilter sofort. Wir werden einem Bild einer Hirschskulptur manuell einen Wärmefilter hinzufügen, um das Bild in warmen Tönen darzustellen, was angenehmer aussieht.

![Beispiel für die Fotofilter-Anpassungsebene](photo-filter-adjustment-layer-figure-1.png)

Zunächst fällt auf, dass [die Fabrikmethode](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-) sich von denen für [andere Anpassungsebenen](https://docs.aspose.com/display/psdjava/PSD+Adjustment+Layers) unterscheidet, da es keine Standardmethode (ohne Argumente) gibt. Daher wird zur Hinzufügung einer Fotofilter-Anpassungsebene in ein geladenes Photoshop-Dokument ein einzelnes Argument benötigt, nämlich die [Farbe](https://reference.aspose.com/psd/java/com.aspose.psd/Color). Um also den Effekt eines Wärmefilters nachzubilden, übergeben Sie einfach Orange als Argument an die Fabrikmethode, setzen dann die Dichte mit den entsprechenden Setzern:

    PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
    photoFilterLayer.setDensity(25);

Es ist erwähnenswert, dass die Eigenschaft Dichte einen Standardwert von 100 hat und dass true der Standardwert für die Eigenschaft "Luminanz erhalten" ist (deshalb aktivieren wir diese Option nicht explizit).

## Fazit

In diesem Artikel haben wir die Verwendung der Fotofilter-Anpassungsebenen-API von Aspose.PSD für Java betrachtet. Dieses Tool ist einfach zu verwenden und ermöglicht das Hinzufügen einer Tönung zu einem Bild mit variabler Dichte. Es ist ein schneller Weg, den Farbausgleich des gesamten Bildes anzupassen.
