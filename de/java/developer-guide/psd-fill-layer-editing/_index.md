---
title: Verwendung von PSD-Füllschichten in Java aktualisieren
weight: 100
type: docs
description: Beispiele zur Verwendung aller Arten von Anpassungsschichten, einschließlich Farbfüllung, Farbverlaufsfüllung und Musterfüllung
keywords: [Füllungsschicht, Farbfüllung, Farbverlaufsfüllung, Musterfüllung, psd api, java, Codebeispiel]
url: de/java/psd-fill-layer-editing/
---

## **Übersicht**

Das Erstellen einer regulären Ebene erfolgt durch Verwendung der createRegularLayer-Funktion, die Parameter zur Definition der Position und Größe der Ebene erfordert. Diese Funktion erstellt eine neue Ebene, legt ihre Begrenzungen fest und füllt sie mit einer bestimmten Farbe.

Für eine Farbfüllungsebene verwenden Sie die FillLayer.createInstance-Methode mit dem Parameter FillType.Color. Sobald die Füllungsebene erstellt ist, greifen Sie über die fill_settings-Eigenschaft auf deren Fülleinstellungen zu und setzen die gewünschte Farbe mithilfe der color-Eigenschaft der Klasse ColorFillSettings. In diesem Kontext wird die Farbe auf Color.getCoral() gesetzt. Darüber hinaus wird die clipping-Eigenschaft der Füllebene auf 1 gesetzt, sodass sie als Clipping-Maske funktioniert.

Farbverlaufsfüllungen werden ähnlich wie Farbfüllungsebenen erstellt, jedoch mit dem Parameter FillType.Gradient für die FillLayer.create_instance-Methode. Wie bei Farbfüllungsebenen greifen Sie über fill_settings auf die Fülleinstellungen zu und setzen die Farbpunkte des Farbverlaufs sowie Transparenzpunkte. In diesem Beispiel werden die Farbpunkte des Farbverlaufs mit der Klasse GradientColorPoint definiert und die Transparenzpunkte mit der Klasse GradientTransparencyPoint. Auch die clipping-Eigenschaft der Füllebene wird auf 1 gesetzt.

Musterfüllungsebenen werden mit FillLayer.createInstance und dem Parameter FillType.Pattern erstellt. Greifen Sie erneut über fill_settings auf die Fülleinstellungen zu und setzen Sie die Musterdaten sowie andere Eigenschaften. In diesem Code werden die Musterdaten mithilfe der Klasse PatternFillSettings definiert und die clipping-Eigenschaft wird auf 1 gesetzt.

Nachdem die Füllschichten erstellt wurden, fügen Sie sie dem PSD-Bild mit der addLayer-Methode hinzu, indem Sie den Anzeigenamen und andere Eigenschaften für jede Füllschicht angeben.

Speichern Sie schließlich das PSD-Bild und das entsprechende PNG-Bild mit dem bereitgestellten Code. Die PNG-Optionen sind konfiguriert, um echte Farbe mit Alpha für Transparenz zu verwenden.

Bitte beachten Sie das vollständige Beispiel für weitere Details.

## **Beispiel**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentation-Java-Aspose-psd-fill-layer-editing.java" >}}
