---
title: Beispiel zur Verwendung von Gruppenlayern in Aspose.PSD für C#
weight: 100
type: docs
description: Verwendung der Gruppenlage in einer PSD-Datei über C#
keywords: [Ebenengruppe, Gruppenlayer, Ebene zur Gruppe hinzufügen, psd api, C#, csharp, Codebeispiel]
url: de/net/psd-group-layer/
---

## Überblick

Gruppenlayer in Aspose.PSD für C# ermöglichen eine effiziente Organisation und Manipulation von Ebenen in einer PSD-Datei. Durch Verwendung von Ordnern können Sie mehrere Ebenen gruppieren und Transformationen oder Effekte auf die gesamte Gruppe anwenden.

Dieses Beispiel zeigt das Erstellen eines neuen PSD-Bildes mit `PsdImage.Create`. Anschließend wird ein neues `LayerGroup`-Objekt mit `AddLayerGroup` aus dem `PsdImage`-Objekt erstellt. Der Gruppenlayer wird "Folder" genannt, an Index 0 eingefügt und auf sichtbar gesetzt.

Als nächstes werden zwei `Layer`-Objekte mit gesetzten `DisplayName`-Eigenschaften erstellt. Diese Ebenen werden der Gruppenlage mit `AddLayer` hinzugefügt.

Ebenen innerhalb der Gruppe können über die `Layers`-Eigenschaft des `LayerGroup`-Objekts zugegriffen werden. Das Beispiel sagt voraus, dass die Anzeigenamen der ersten und zweiten Ebenen in der Gruppe "Ebene 1" und "Ebene 2" sind.

Nach der Bearbeitung der Gruppenlayer wird das aktualisierte PSD-Bild mit der `Save`-Methode des `PsdImage`-Objekts gespeichert.

Dieses grundlegende Beispiel zeigt die Arbeit mit Gruppenlayern in Aspose.PSD für C#. Die Bibliothek bietet erweiterte Funktionen zur Manipulation und Transformation von Ebenen in PSD-Dateien. Weitere detaillierte Beispiele und Funktionen finden Sie in der Aspose.PSD für C#-Dokumentation.

Hier ist ein Beispielcode, der die Verwendung von Gruppenlayern in Aspose.PSD für C# zeigt:

## Beispiel

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

Für weitere detaillierte Informationen und Beispiele besuchen Sie bitte die [Aspose.PSD für C#-Dokumentation](https://docs.aspose.com/psd/net/).
