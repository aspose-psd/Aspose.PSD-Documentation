---
title: Aspose.PSD für .NET 23.7 - Versionshinweise
type: docs
weight: 60
url: /de/net/aspose-psd-fur-net-23-7-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                                       | **Kategorie** |
|:-------------|:--------------------------------------------------------------------------------------------------------------|:------------|
| PSDNET-802   | Möglichkeit hinzugefügt, jede Ebene der PSD-Datei in die animierte GIF-Datei zu exportieren                    | Feature     |
| PSDNET-1441  | Zuweisen der Füllungseigenschaft der Formebene aus VSCG-Ressource                                             | Feature     |
| PSDNET-1534  | Neue Arten von Warp hinzugefügt (Bogen & Bogen)                                                               | Feature     |
| PSDNET-1543  | Änderung der Anwendung, die die PSD-Datei speichert, auf Aspose.PSD, wenn die Eigenschaft UpdateMetadata auf true gesetzt ist | Feature |
| PSDNET-1567  | Bereich der Verformungsbildes erhöht                                                                          | Feature     |
| PSDNET-1471  | Schwarzweiß-Anpassungsebene verarbeitet die Halbtransparenz falsch                                           | Bug         |
| PSDNET-1505  | SmartObject ReplaceContents (wenn die Option AllowWarpRepaint aktiv ist) stürzt nach 2 Minuten Berechnung ab    | Bug         |
| PSDNET-1585  | Möglichkeit hinzugefügt, die tatsächliche LayerGroup-Position links und oben zu erhalten                      | Bug         |
| PSDNET-1589  | Ändern der Größe der Ebene funktioniert falsch, wenn die PSD-Datei eine VogkResource mit Strukturen in Punkten enthält | Bug |
| PSDNET-1608  | TextBound funktioniert nicht wie erwartet                                                                     | Bug         |
| PSDNET-1612  | Hinzufügen einer Ebene, die mit dem Standardkonstruktor erstellt wurde, zu einer PSD-Bild fügt keine Standardressourcen hinzu | Bug         |
| PSDNET-1623  | Timeline.LoopesCount wird beim Exportieren in animiertes GIF ignoriert                                      | Bug         |


## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **Entfernte APIs:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **Verwendungsbeispiele:**

**PSDNET-802. Möglichkeit hinzugefügt, jede Ebene der PSD-Datei in die animierte GIF-Datei zu exportieren**

{{< highlight csharp >}}
// Codebeispiel
{{< /highlight >}}

**PSDNET-1441. Zuweisen der Füllungseigenschaft der Formebene aus VSCG-Ressource**

{{< highlight csharp >}}
// Codebeispiel
{{< /highlight >}}

... (weitere Beispiele folgen) ...