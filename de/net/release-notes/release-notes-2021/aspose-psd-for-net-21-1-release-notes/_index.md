---
title: Aspose.PSD für .NET 21.1 - Versionshinweise
type: docs
weight: 120
url: /de/net/aspose-psd-fur-net-21-1-versionshinweise/
---

{{% alert color="primary" %}} 

Diese Seite enthält die Versionshinweise für [Aspose.PSD für .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Ausnahme beim Versuch, eine bestimmte Psd-Datei in png umzuwandeln|Fehler|
|PSDNET-792|Ausnahmebehandlung beim Speichern von PSD mit Smart-Objekt in PNG|Fehler|

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- None

# **Entfernte APIs:**
- None

## **Verwendungsbeispiele:**
**PSDNET-766. Aspose.PSD 20.10: Ausnahme beim Versuch, eine bestimmte Psd-Datei in png umzuwandeln**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET766_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "school-admission-flyer-template-05052019.psd";
            string outputFilePath = outputFolder + "chool-admission-flyer-template-05052019_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions();
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. Ausnahmebehandlung beim Speichern von PSD mit Smart-Objekt in PNG**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder+ "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // Suche nach Smart-Objekt
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // Wir laden Smart-Objekt-Layer aus dem Memory Stream,
                        // Aber wir können smart smart.ExportContents(somePath) verwenden, um das Smart-Objekt in eine Datei zu exportieren
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // Suche nach Text-Layer
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // Wir können einfach UpdateText verwenden, aber auf diese Weise haben wir die Möglichkeit, den Text portionsweise zu bearbeiten
                                        // Erstellen von mehrzeiligen Textlayern und andere Text- und Absatzformatierungsfunktionen
                                        // Bitte seien Sie vorsichtig. Wenn der Inhalt des Smart-Objekts kein PSD ist, können Sie diesen Weg der Textbearbeitung nicht verwenden
                                        // In einem solchen Fall sollten Sie die Graphic-API verwenden: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "Best";

                                        // Sie sollten die Textgröße ändern, wenn Sie möchten, dass das Bild gut aussieht.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // Es ist besser, ReplaceContents zu verwenden. Es rendert automatisch das Smart-Objekt neu
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // Auf diese Weise speichern wir die geänderte PSD-Datei
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
