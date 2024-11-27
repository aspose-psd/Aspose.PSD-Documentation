---
title: Kurven-Anpassungsschicht
type: docs
weight: 30
url: /de/java/layer-types/adjustment-layer/curves/
---

# Arbeiten mit der Photoshop Kurven-Anpassungsschicht in Java

Das Ziel dieses Artikels besteht darin, die Fähigkeiten der Bibliothek Aspose.PSD für Java bei der **Arbeit mit Kurven-Anpassungsschichten** in Adobe® Photoshop®-Dokumenten zu demonstrieren. Die Bibliothek ist vollständig eigenständig. Daher funktioniert sie ohne die Installation des Photoshop-Bildbearbeitungsprogramms. Die [vollständige Liste der Funktionen](https://docs.aspose.com/psd/java/features/) finden Sie in unserem Wissensdatenbank. Nun aber zurück zu den Kurven.

## API-Übersicht

Das Kurvenwerkzeug kann als diagonale Linie (Kurve) auf einem Diagramm dargestellt werden, mit Highlights in der oberen rechten Ecke und Schatten in der unteren rechten Ecke.

Die Bibliothek bietet eine API zur Arbeit mit der Kurve, nämlich die [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer)-Klasse. Diese Klasse hat jedoch **zwei vollständig unterschiedliche Ansätze** zur Bearbeitung der Kurve. Daher kann sie zur gleichen Zeit in einem von zwei Modi bearbeitet werden:

- Kontinuierlich (die Kurve wird als Pfad mit Biegepunkten dargestellt)
- Diskret (die Kurve wird als gestrichelte Linie dargestellt)

Die Bibliothek bietet also zwei Möglichkeiten, die Kurve mithilfe des [kontinuierlichen](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) und [diskreten Managers](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager) jeweils zu modifizieren. Im Folgenden erklären wir, wie man jeden von ihnen anhand eines spezifischen Beispiels verwendet.

## Farben und Ton mit dem Kontinuierlichen Kurven-Manager anpassen

Der [Kontinuierliche Kurven-Manager](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **konfiguriert Biegepunkte einer kontinuierlichen Kurve** für den zusammengesetzten Kanal (RGB) sowie für jeden einzelnen Farbkanal. Zu Demonstrationszwecken werden einige Kurvenanpassungen (a) auf einem verdunkelten Bild eines Orchesters (b) angewendet, um ein aufgehelltens Bild mit wärmeren Farben zu erhalten (c):

![Kurven-Anpassungsschicht Abbildung 1](curves-psd-adjustment-layer-figure-1.png)

Da es zwei Manager gibt, ist es erforderlich, vor dem Abrufen explizit einen auszuwählen (in diesem Fall den kontinuierlichen Manager). Anschließend können direkt Kurvenpunkte an bestimmten Koordinaten für die gewünschten Farbkanäle (zusammengesetztes RGB, Rot und Blau) hinzugefügt werden, um die Form der Kurve nachzubilden:
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

Der Koordinatenursprung befindet sich in der unteren linken Ecke. Der maximale Koordinatenwert eines Punktes ist auf den Datentyp (byte) begrenzt und beträgt 255 (127 für den vorzeichenbehafteten Typ).

Es gibt auch einige [andere Methoden](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager), die Sie verwenden können.

## Ton mit dem Diskreten Kurven-Manager anpassen

Der Diskrete Kurven-Manager erlaubt auch das Positionieren von Kurvenpunkten (tatsächliche Veränderung von Farbe und Ton), aber der Unterschied besteht darin, dass sie es anders machen. Erstens besteht die **Kurve aus Punkten** oder Punkten (keine durchgezogene Linie). Zweitens **setzt dieser Manager den Punkt nirgendwo hin** auf das Diagramm. Stattdessen **bewegt er den Punkt nach oben oder unten** im Wertebereich von 255 bis 0, umgekehrt. Standardmäßig nehmen die Werte der Kurvenpunkte inkrementell zu und formen eine Kurve, die in einem 45-Grad-Winkel steht.

Daher ist es einfach, den „Negativ (RBG)“-Photoshop-Voreinstellung (a) nachzubilden und auf ein Graustufenbild eines Tals anzuwenden, um am Ende eine negative Darstellung des Tals zu erhalten (c).

![Kurven-Anpassungsschicht Abbildung 2](curves-psd-adjustment-layer-figure-2.png) Vergessen Sie in erster Linie nicht, den entsprechenden Manager auszuwählen, um ihn verwenden zu können, und setzen Sie dann die Punkt-Werte der Kurve in absteigender Reihenfolge von 255 bis 0 für jeden Kurvenpunkt (insgesamt 255):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

Der Manager bietet auch einige [andere Methoden](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) zur Verwaltung der Kurve.

## Fazit

In diesem Artikel haben wir gelernt, wie man Kurven-Anpassungsschichten in Photoshop-Dokumenten unter Verwendung von Aspose.PSD für Java auf zwei vollständig unterschiedliche Weisen (kontinuierliche und diskrete Manager) bearbeitet.
