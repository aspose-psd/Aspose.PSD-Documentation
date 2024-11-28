---
title: Beispiel zur Verwendung von Gruppenebenen in Aspose.PSD für Java
weight: 100
type: docs
description: Verwendung der Gruppenebene einer PSD-Datei über Java
keywords: [Ebene gruppieren, Gruppenebene, Ebene zur Gruppe hinzufügen, psd api, java, Codebeispiel]
url: de/java/psd-group-layer/
---

## **Übersicht**

Die Verwendung von Gruppenebenen in Aspose.PSD für Java verbessert Ihre Fähigkeit, Ebenen innerhalb eines PSD-Bildes effektiv zu verwalten und zu organisieren. Gruppenebenen, auch als Ordner-Ebenen bezeichnet, ermöglichen es Ihnen, mehrere Ebenen zusammenzufassen und Transformationen oder Effekte kollektiv anzuwenden.

Beginnen Sie damit, ein neues PSD-Bild mit der Methode PsdImage.create() zu erstellen. Initialisieren Sie dann ein neues LayerGroup-Objekt über die Methode addLayerGroup des PsdImage-Objekts. Geben Sie den gewünschten Namen für die Gruppenebene ("Ordner") an, spezifizieren Sie den Einfügeindex (0) und setzen Sie ein boolesches Flag, das die Sichtbarkeit angibt (True).

Erstellen Sie anschließend zwei Layer-Objekte und setzen Sie ihre Anzeigenamen mit der Methode setDisplayName. Fügen Sie diese Ebenen der Gruppenebene mit der Methode addLayer hinzu.

Um auf die Ebenen innerhalb der Gruppe zuzugreifen, verwenden Sie das layers-Eigenschaft des LayerGroup-Objekts. Stellen Sie sicher, dass die Anzeigenamen der ersten und zweiten Ebenen in der Gruppe "Ebene 1" und "Ebene 2" sind.

Sobald Sie die Gruppenebenen manipuliert haben, speichern Sie das modifizierte PSD-Bild mit der Methode save des PsdImage-Objekts.

Dies dient als grundlegendes Beispiel, um sich mit der Arbeit mit Gruppenebenen unter Verwendung von Aspose.PSD für Java vertraut zu machen. Die Bibliothek bietet eine Vielzahl von erweiterten Funktionen für die Ebenenmanipulation und Transformation innerhalb von PSD-Bildern. Für weitere Details und Beispiele zur Nutzung von Gruppenebenen und anderen Funktionen der Bibliothek verweisen Sie auf die Aspose.PSD für Java-Dokumentation.

Um mit Gruppenebenen in Aspose.PSD für Java zu arbeiten, verwenden Sie die Klasse LayerGroup. Im Folgenden finden Sie einen Code-Schnipsel, der zeigt, wie man eine Gruppenebene erstellt, Ebenen hinzufügt und das modifizierte PSD-Bild speichert.

Bitte beachten Sie das vollständige bereitgestellte Beispiel.

## **Beispiel**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentation-Java-Aspose-psd-Gruppenebene.java" >}}
