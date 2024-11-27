---
title: Aspose.PSD für .NET 24.7 - Versionshinweise
type: docs
weight: 60
url: /de/net/aspose-psd-fur-net-24-7-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                               | **Kategorie** |
|:-------------|:--------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029  | "Bildladefehler." Ausnahme beim Öffnen des AI-Dokuments                                            | Fehler  |
| PSDNET-2022  | Text in AusgabepDF-Dateien falsch gerendert                                                        | Fehler  |
| PSDNET-2061  | Beheben von ImageSaveException: Bildexport fehlgeschlagen für die angegebene Datei unter Linux     | Fehler  |
| PSDNET-2080  | Beheben des Ladens von Schriftarten bei Verwendung von Aspose.Drawing                              | Fehler  |
| PSDNET-2085  | 'Arithmetischer Überlauf führte zu einem Überlauf' beim Erstellen einer Smart-Objekt-Ebene mit großem JPEG | Fehler  |
| PSDNET-2100  | Die AI-Datei kann nicht in eine JPG-Datei konvertiert werden                                      | Fehler  |

## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- Keine

# **Entfernte APIs:**
- Keine

## **Beispiele:**

**PSDNET-1029. "Bildladefehler." Ausnahme beim Öffnen des AI-Dokuments**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Text in AusgabepDF-Dateien falsch gerendert**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. Beheben von ImageSaveException: Bildexport fehlgeschlagen für die angegebene Datei unter Linux**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. Beheben des Ladens von Schriftarten bei Verwendung von Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Vor Aktualisierung. Installierte Schriftartenanzahl: " + installedFonts.Families.Length);
    Console.WriteLine("- Plattform: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- Aktualisieren Sie den Schriftcache, indem Sie versuchen, den Adobe-Schriftnamen für 'Arial' zu erhalten: "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- Nach der Aktualisierung. Installierte Schriftartenanzahl: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'Arithmetischer Überlauf führte zu einem Überlauf' beim Erstellen einer Smart-Objekt-Ebene mit großem JPEG**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Test Layer";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. Die AI-Datei kann nicht in eine JPG-Datei konvertiert werden**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}
