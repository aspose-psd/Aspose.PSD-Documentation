---
title: Ebenenanpassungsebene "Kanal-Mixer"
type: docs
weight: 30
url: /de/java/ebenenarten/ebenanpassungsebene/kanal-mixer/
---

# Arbeiten mit der Photoshop-Kanal-Mixer-Anpassungsebene in Java

Heute werden wir sehen, wie man Kanalfarben in Photoshop-Dokumenten programmgesteuert in Java mischt. Da der Photoshop-Editor kein Java-Skripting unterstützt, werden wir eine spezielle PSD-Dateiformatmanipulationsbibliothek namens Aspose.PSD für Java verwenden.

Die Bibliothek enthält **APIs zum Arbeiten mit Farbkanälen**. Es gibt verschiedene Möglichkeiten, Farben zu mischen, aber in diesem Artikel konzentrieren wir uns auf die Kanal-Mixer-Anpassungsebene.

Die API der Kanal-Mixer-Anpassungsebene **ermöglicht das Spielen mit Farbkanälen**, um eingedämpfte Bilder zu erstellen oder verschiedene kreative Farbeffekte zu erzielen oder sogar das Bild in ein Schwarz-Weiß-Bild umzuwandeln. Als Nächstes erläutern wir, wie man die Kanal-Mixer-Anpassungsebene auf ein vorhandenes Photoshop-Dokument anwendet, indem wir Aspose.PSD für Java verwenden, aber zuerst müssen wir über die allgemeinen API-Funktionen sprechen.

## API-Übersicht

Es ist nichts Besonderes beim Erstellen einer Kanal-Mixer-Anpassungsebene. Sie kann über [die Standard-Fabrikmethode](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) hinzugefügt werden, die eine Instanz der Klasse ChannelMixerLayer zurückgibt. Diese Klasse enthält allgemeine Funktionalitäten wie die Monochrom-Option und eine Methode zum Abrufen eines Ausgabekanals. Ein bestimmter Ausgabekanal kann einer von zwei Typen sein: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) oder [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). Der Typ des [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) hängt vom [Farbmodus](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) des Bildes ab.

## Das Bild monochrom machen

Lassen Sie uns nun ein Beispiel betrachten, wie man eine Kanal-Mixer-Anpassungsebene auf ein vorhandenes Photoshop-Dokument anwendet. Da diese Art von Anpassungsebene noch keine Voreinstellungen unterstützt, werden wir **die Schwarz-Weiß-Infrarot (RGB) Photoshop-Voreinstellung** nachbilden. Die Voreinstellung wird auf das Bild eines blühenden Baumes angewendet. Als Ergebnis möchten wir den Effekt der Infrarotfotografie erzielen.

![Beispiel für Kanal-Mixer-Anpassungsebene](channel-mixer-adjustment-psd-layer-figure-1.png) Zuerst muss die Schwarz-Weiß-Infrarot (RGB) Photoshop-Voreinstellung nachgebildet werden, indem die Monochrom-Flagge aktiviert und geeignete Rohwerte für jede Farbe (Rot, Grün und Blau) für den Grau-Ausgabekanal festgelegt werden:

```java
ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
channelMixerLayer.setMonochrome( **true** );
RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
grayOutputChannel.setRed(( **short** )-70);
grayOutputChannel.setGreen(( **short** )200);
grayOutputChannel.setBlue(( **short** )-30);
```

Das Bild muss im RGB-Farbmodus sein, damit der Code funktioniert (aufgrund der Zuweisung zur RgbMixerChannel-Klasse). Der CMYK-Farbmodus wird ebenfalls unterstützt, aber nur für Bilder mit dem entsprechenden Farbmodus.

Beachten Sie, dass der Wert jeder Farbe sowie die Konstanten-Eigenschaft im Bereich von -200 bis 200 liegen müssen.

## Fazit

In diesem Artikel haben wir betrachtet, wie man mit der Kanal-Mixer-API von Aspose.PSD für Java arbeitet, um Farben in Farbkanälen anzupassen und das Bild in Schwarz-Weiß umzuwandeln.
