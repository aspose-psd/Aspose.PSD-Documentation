---
title: Wie man einen YouTube-Thumbnail-Generator programmatisch in Java erstellt
type: docs
weight: 10
url: /de/java/wie-man-einen-youtube-thumbnail-generator-programmatisch-in-java-erstellt/
---

## **Einführung**
Der Zweck dieses Dokuments besteht darin, die API-Nutzung einiger Verbundwerkzeuge von [Aspose.PSD für Java](https://products.aspose.com/psd/java) anhand eines realen Beispiels zu demonstrieren. In diesem Artikel wird **ein einfaches Java-Programm vorgestellt, das YouTube-Thumbnails** für den [DW-Dokumentationskanal](https://www.youtube.com/channel/UCW39zufHfsuGgpLviKh297Q) generiert und erklärt. Dieser Kanal wurde aus der realen Welt ausgewählt, weil seine Thumbnails recht standardmäßig sind und sie die Verwendung einiger beliebter Verbundwerkzeuge von Aspose.PSD für Java (z. B. Schatteneffekt, radialer Verlauf, Zeichnen von Text und Formen) veranschaulichen:

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_1.png)

## **Wie es im Detail funktioniert**
Ein einfaches Java-Programm erhält zwei Argumente als Eingabe: eine Beschriftung und ein Bild. Ein **in-Memory-Photoshop-Dokument (PSD) wird aus dieser Eingabe mit Hilfe von Aspose.PSD für Java generiert**. Anschließend wird das Dokument **von PSD in das PNG-Dateiformat konvertiert**, um ein YouTube-Thumbnail mit einer Größe von 1280x720 Pixeln zu erhalten. Das Ausgabebild sieht ähnlich wie folgt aus:

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_2.png)

## **Technische Anforderungen**
Die folgenden Technologien sind erforderlich, um den Code dieses Artikels erfolgreich auszuführen:

- Java 6+
- [Aspose.PSD für Java](/psd/de/java/installation/) (Neueste Version)

## **Erste Schritte**
Wie bereits erwähnt, verwendet das Programm ein in-Memory-PSD, um ein Thumbnail zu generieren. Fangen wir also zunächst damit an, **ein PSD-Dokument zu erstellen**:

PsdImage psdImage = new PsdImage(1280, 720);

Wenn Sie sich das obige YouTube-Thumbnail genauer ansehen, können Sie feststellen, dass **es aus mehreren Komponenten besteht**:

1. ein Hintergrundbild (gedruckte Maske)
2. ein radialer PSD-Verlauf (betont den Bereich oben rechts)
3. ein Logotyp mit Schatteneffekt
4. eine Beschriftung und eine einfache Zeichnung (blaues Rechteck)

Tauchen wir tiefer ein, um zu sehen, wie jede dieser Komponenten mithilfe von Aspose.PSD für Java in den nächsten Abschnitten implementiert werden kann.

## **1. Fügen Sie ein Hintergrundbild hinzu**
Die Reihenfolge der Ebenen ist wichtig. Daher muss zuerst ein Hintergrundbild hinzugefügt werden, um andere Ebenen nicht zu überlappen. Beachten Sie, dass derzeit nur [Rasterdateiformate unterstützt werden](/psd/de/java/supported-file-formats/).

### **1.1. Fügen Sie ein Hintergrundbild zu einer Photoshop-Ebene hinzu**
Um ein **Rasterbild in PSD einzufügen**, muss ein Eingabestrom als Argument während der Konstruktion der Ebene übergeben werden (siehe weitere [Beispiele zum Laden von Rasterbildern](https://docs.aspose.com/display/psdnet/Creating%2C+Opening+and+Saving+Images)):

```java
// Code hier einfügen
```

1.2. Passen Sie das Hintergrundbild an die Leinwand an

Die folgenden 2 Aktionen (Größenänderung, Positionierung) sind nützlich für die Fälle, wenn **die Bildgröße von der Leinwandgröße abweicht**, obwohl das Bild in diesem Artikel die gleiche Größe wie die Leinwand hat (nehmen Sie an, dass dies nicht immer der Fall ist).

Stellen Sie sicher, dass das geladene Bild **auf die Größe der Leinwand passt** (siehe weitere [Beispiele zur Größenänderung](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages)):

```java
// Code hier einfügen
```

Nach der Größenänderung wird die Bildposition verändert. Um die Position des Bildes zurückzusetzen, verschieben Sie das verkleinerte Bild in die obere linke Ecke:

```java
// Code hier einfügen
```

## **2. Fügen Sie einen radialen Verlauf hinzu**
Es gibt **zwei Möglichkeiten, einen radialen Verlauf hinzuzufügen**, nämlich:

- einen [Verlaufüberlagerungseffekt](/psd/de/java/aspose-psd-for-java-20-4-release-notes/#-~-text=psdjava-163) auf einer vorhandenen Ebene (ein Verlaufseffekt, der an die aktuelle Ebene gebunden ist und auf deren Inhalt angewendet wird)
- eine neue [Verlaufeinfachebene](/psd/de/java/support-of-fill-layers/#supportoffilllayers-supportoffilllayerswithgradientfill) (eine separate Ebene, die die eigenständige Konfiguration des Verlaufs beibehält)

Für dieses Beispiel ist es ausreichend, den Verlaufüberlagerungseffekt zu verwenden. Um diesen Artikel jedoch interessanter und nützlicher zu gestalten, wird **die Verlaufeinfachebene verwendet**, da alle Ebeneneffekte ähnlich angewendet werden und im nächsten Abschnitt ein weiterer Ebeneneffekt verwendet wird.

### **2.1. Fügen Sie eine Verlauffüllebene hinzu**
Der Prozess, eine neue Verlauffüllebene hinzuzufügen, besteht aus den folgenden 2 Schritten:

1. Es ist erforderlich, **Verlauffülleinstellungen zu deklarieren**, da keine vordefinierten vorhanden sind. Die minimal erforderliche Konfiguration sieht wie folgt aus (angenommen, dass Verlaufstyp, Skala, Farbe und Transparenzpunkte erforderliche Eigenschaften sind):

```java
// Code hier einfügen
```

Die obige Konfiguration deklariert einen radialen Verlauf, der an den Rändern transparent ist und in der Mitte dunkelblau ist. Die Verlaufsposition ist standardmäßig in der Mitte der Leinwand.

Um den Verlauffüllung umzukehren und ihn leicht in die obere rechte Ecke zu verschieben, verwenden Sie die entsprechenden optionalen Eigenschaften:

```java
// Code hier einfügen
```

2. Wenn die Konfiguration abgeschlossen ist, fügen Sie eine Verlauffüllebene zusammen mit ihren Einstellungen in die PSD ein:

```java
// Code hier einfügen
```

## **Fügen Sie einen Logotyp mit einem Schatten hinzu**
Der **Schattenwurf** ist ein Effekt, der es ermöglicht, einen benutzerdefinierten Schatten entlang der Kontur des Objekts (Bild, Text usw.) hinzuzufügen.

### **3.1. Fügen Sie einen Logotyp zu einer Photoshop-Ebene hinzu**
Der gleiche Ansatz wie in Abschnitt 1.1. kann verwendet werden, um **einen Logotyp in PSD einzufügen**:

```java
// Code hier einfügen
```

### **3.2. Positionieren Sie den Logotyp**
Das geladene Bild ist standardmäßig eng an der oberen linken Ecke angebracht. Es müssen jedoch einige **Seitenränder hinzugefügt** werden, um dem Original-YouTube-Thumbnail auf dem Kanal ähnlich zu sehen. Daher sollte die Bildposition von den Rändern der Ebene weg verschoben werden:

```java
// Code hier einfügen
```

### **3.3. Fügen Sie einen Schattenwurfeffekt zum Logotyp hinzu**
Der Logotyp kann unsichtbar sein, wenn ein helles Hintergrundbild verwendet wird. Daher ist es wünschenswert, **einen Schatteneffekt hinzuzufügen** über Eigenschaften der Überblendoptionen (siehe weitere [Beispiele von Schattierungen](/psd/de/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect)):

```java
// Code hier einfügen
```

Der Schatteneffekt hat nicht die erforderlichen Eigenschaften aufgrund der Standardkonfiguration (er sieht aus wie der von Photoshop). Der oben gezeigte Schatten wurde jedoch so modifiziert, dass er wie ein durchscheinender Rand aussieht, der an den Rändern verschwimmt.

## **4. Fügen Sie eine Zeichnung von Text und einer Form hinzu**
### **4.1. Erstellen Sie eine Grafikebene**
Das Zeichnen wird von einer regulären Ebene nicht direkt unterstützt. Daher wird neben der Ebene der Grafikmodus verwendet, um eine API zum Zeichnen bereitzustellen (siehe weitere [Beispiele zum Zeichnen](/psd/de/java/drawing-images-using-graphics/)):

```java
// Code hier einfügen
```

### **4.2. Zeichnen Sie mehrzeiligen Text**
Ein kenntnisreicher Leser könnte fragen: Warum nicht eine Textebene verwenden, um einen Text hinzuzufügen? Nun, es gibt ein paar Gründe: Textbearbeitung ist in diesem Fall nicht erforderlich, da PSD jedes Mal von Grund auf neu generiert wird; die Anpassung der Schriftart wird vom [Text-API](https://docs.aspose.com/display/psdnet/Working+With+Text+Layers) noch nicht unterstützt (v20.6 zum Zeitpunkt des Schreibens).

Es ist einfach, **einen Text mit einer benutzerdefinierten Schriftart zu zeichnen**, indem eine gewünschte Schriftart instanziiert wird und die entsprechende Methode aus dem Grafikmodus aufgerufen wird. Um jedoch ein Rechteck zu erstellen (siehe Einzelheiten im nächsten Abschnitt), das seine Höhe automatisch basierend auf der Anzahl der Textzeilen ändert, ist ein wenig schwieriger. Die genaue Höhe aller Zeilen muss zunächst berechnet werden:

```java
// Code hier einfügen
```

Dort ist 1.15 die Zeilenhöhe, 3 ist die Textpolsterung.
### **4.3. Zeichnen Sie ein Rechteck**
Ein Rechteck lässt sich ebenfalls leicht zeichnen, auch mit einem Farbverlaufspinsel (legen Sie einfach einen Bereich fest, um zu zeichnen und einen Farbbereich). Wenn die Höhe des Texts bekannt ist, werden die Größe und die Position des Rechtecks berechnet. Um ein **gefülltes Rechteck in PSD zu zeichnen** (nicht nur einen Rahmen), rufen Sie die entsprechende Methode aus dem Grafikmodus mit all dem auf:

```java
// Code hier einfügen
```

Dort 40, 15, 25 sind Einzüge.

## **Ergebnis**
Die Gestaltung des Thumbnails ist abgeschlossen. Daher ist es an der Zeit, das Thumbnail in ein Rasterdateiformat (z. B. PNG) zu exportieren, um es weiterzuverteilen:

```java
// Code hier einfügen
```

## **Fazit**
In diesem Artikel haben wir einen YouTube-Thumbnail-Generator für den DW-Dokumentationskanal erstellt und erklärt, wie einige der beliebtesten Verbundwerkzeuge wie Schatteneffekt, radialer Verlauf, Textzeichnen und Formen verwendet werden.

## **Vollständiges Beispiel**
Sie können das [Aspose.PSD SDK herunterladen](https://products.aspose.com/psd/net)

```java
// Code hier einfügen
```