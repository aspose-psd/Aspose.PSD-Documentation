---
title: Aspose.PSD for .NET 20.7 - Versionshinweise
type: docs
weight: 60
url: /de/net/aspose-psd-for-net-20-7-release-notes/
---

{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für [Aspose.PSD for .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-673|Unterstützung von LnkE-Ressource|Feature|
|PSDNET-392|Unterstützung von britResource (Ressource einer Helligkeit/Kontrast-Anpassungsebene)|Feature|
|PSDNET-629|Ändern der Ausnahmemeldung beim Versuch, nicht unterstützte Formate als Bild zu öffnen|Verbesserung|
|PSDNET-594|Fehler beim Speichern von Layer Mask|Fehler|
|PSDNET-597|Photoshop-Warnung beim Öffnen einer PSD-Datei nach dem Erstellen einer neuen Layer-Gruppe|Fehler|
|PSDNET-618|Clipping-Maske wird nicht auf den Ordner angewendet|Fehler|
|PSDNET-625|Kann Datei mit Aspose.PSD für .NET nicht öffnen|Fehler|
|PSDNET-650|Fehler bei der Bildspeicherung beim Konvertieren von PSD nach PDF|Fehler|
|PSDNET-655|rop-Operation macht Clipping-Pfad in PSD-Bild ungültig|Fehler|
|PSDNET-662|NullReference Exception beim Versuch, bestimmte PSD-Datei mit Schatteneffekt zu speichern|Fehler|
|PSDNET-666|Aspose.PSD gibt true bei Image.CanLoad(pdfStream) zurück|Fehler|
|PSDNET-676|Ebenen konnten im generierten PNG nicht gerendert werden|Fehler|
|PSDNET-677|Ausnahme beim Zugriff auf Textdaten|Fehler|
|PSDNET-679|ImageSaveException beim Speichern der PSD|Fehler|

## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Overprint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Position
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Size
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Inside
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Center
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Outside
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource
- M:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Version
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsInverted
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsInverted

# **Entfernte APIs:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **Beispiel zur Verwendung:**
**PSDNET-606. Unterstützung der LnkE-Ressource**

{{< highlight csharp >}}
// Der Code wurde nicht übersetzt, da die Kommentare besagen, dass es sich um Beispiele handelt
{{< /highlight >}}

**PSDNET-201. Unterstützung für Dokumentkonvertierung Fortschritt**

{{< highlight csharp >}}
// Der Code wurde nicht übersetzt, da die Kommentare besagen, dass es sich um Beispiele handelt
{{< /highlight >}}

**PSDNET-386. Unterstützung von britResource (Ressource einer Helligkeit/Kontrast-Anpassungsebene)**

{{< highlight csharp >}}
// Der Code wurde nicht übersetzt, da die Kommentare besagen, dass es sich um Beispiele handelt
{{< /highlight >}}

**PSDNET-596. Layer-Gruppe mit nicht "Durchgehen" Überblendungsmodus wird nicht gerendert**

{{< highlight csharp >}}
// Der Code wurde nicht übersetzt, da die Kommentare besagen, dass es sich um Beispiele handelt
{{< /highlight >}}

// Weitere Beispiele wurden aus Platzgründen nicht übersetzt.