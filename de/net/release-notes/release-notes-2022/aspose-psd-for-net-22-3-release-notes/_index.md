---
title: Aspose.PSD für .NET 22.3 - Versionshinweise
type: docs
weight: 100
url: /de/net/aspose-psd-fur-net-22-3-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-210|Eigenschaft IsOpen für Layer Group hinzufügen|Feature|
|PSDNET-643|PSD-Bild mit Raster-Ebenenmasken verwirft Masken beim Speichern als 16-Bit-PSD-Bild|Fehler|
|PSDNET-899|Überlagerungsmodus "Auflösen" wird nicht auf den Ordner mit Maske angewendet|Fehler|
|PSDNET-1047|Spezifische Datei kann nach dem Speichern in Aspose.PSD 21.11 nicht von Photoshop geöffnet werden|Fehler|
|PSDNET-1068|Fehlerhafte Darstellung der Ebene mit Überlagerungsmodus "Ineinanderkopieren (Hinzufügen)"|Fehler|
|PSDNET-1069|Fehler bei Musterfüll-Ebene wirft Ausnahme bei Aktualisierung nach dem Laden|Fehler|


## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **Entfernte APIs:**
- Keine


## **Verwendungsbeispiele:**


**PSDNET-210. Eigenschaft IsOpen für Layer Group hinzufügen**

{{< highlight csharp >}}
// Beispiel zum Lesen und Schreiben der IsOpen-Eigenschaft zur Laufzeit.
string sourceFileName = "LayerGroupOpenClose.psd";
string outputFileName = "Output" + sourceFileName;

using (var image = (PsdImage)Image.Load(sourceFileName))
{
    foreach (var layer in image.Layers)
    {
        if (layer is LayerGroup && layer.Name == "Gruppe 1")
        {
            bool istGeöffneteGruppe1 = ((LayerGroup)layer).IsOpen;
            ((LayerGroup)layer).IsOpen = !istGeöffneteGruppe1;
        }

        if (layer is LayerGroup && layer.Name == "Gruppe 2")
        {
            bool istGeöffneteGruppe2 = ((LayerGroup)layer).IsOpen;           
            ((LayerGroup)layer).IsOpen = !istGeöffneteGruppe2;
        }
    }

    image.Save(outputFileName);
}
{{< /highlight >}}


**PSDNET-643. PSD-Bild mit Raster-Ebenenmasken verwirft Masken beim Speichern als 16-Bit-PSD-Bild**

{{< highlight csharp >}}
            string sourceFilePath = "EineNormaleUndEineNormaleMitMaske.psd";
            string outputFilePath = "out_EineNormaleUndEineNormaleMitMaske.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFilePath, new PsdOptions(image)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}


**PSDNET-899. Überlagerungsmodus "Auflösen" wird nicht auf den Ordner mit Maske angewendet**

{{< highlight csharp >}}
            string sourceFile = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}


**PSDNET-1047. Spezifische Datei kann nach dem Speichern in Aspose.PSD 21.11 nicht von Photoshop geöffnet werden**

{{< highlight csharp >}}
            string sourceFile = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPsd);
            }

            // Output PSD muss manuell durch Photoshop geöffnet werden.

            using (PsdImage image = (PsdImage) Image.Load(outputPsd))
            {
                // keine Ausnahme.
            }
{{< /highlight >}}


**PSDNET-1068. Fehlerhafte Darstellung der Ebene mit Überlagerungsmodus "Ineinanderkopieren (Hinzufügen)"**

{{< highlight csharp >}}
            string sourceFile = "kaputt.psd";
            string outputPng = "out_kaputt.psd.png";

            using (var psdImage = (PsdImage) Image.Load(sourceFile))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}


**PSDNET-1069. Fehler bei Musterfüll-Ebene wirft Ausnahme bei Aktualisierung nach dem Laden**

{{< highlight csharp >}}
            string sourceFile = "AlleArtenLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(sourceFile))
            {
                var füllEbene = (FillLayer)image.Layers[9];
                füllEbene.Update();
            }
{{< /highlight >}}
