---
title: Aspose.PSD dla .NET 21.1 - Notatki dotyczące wydania
type: docs
weight: 120
url: /pl/net/aspose-psd-dla-net-21-1-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Wyjątek podczas próby konwersji określonego pliku Psd do png|Błąd|
|PSDNET-792|Wyjątek podczas zapisywania PSD ze smart objektem do PNG|Błąd|

## **Zmiany w publicznym API**
# **Dodane API:**
- Brak

# **Usunięte API:**
- Brak

## **Przykłady użycia:**
**PSDNET-766. Aspose.PSD 20.10: Wyjątek podczas próby konwersji określonego pliku Psd do png**
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


**PSDNET-792. Wyjątek podczas zapisywania PSD ze smart objektem do PNG**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder + "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // Szukamy Smart Object
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // Ładujemy warstwę Smart Object z Memory Stream,
                        // Ale możemy użyć smart.ExportContents(somePath), aby wyeksportować smart obiekt do pliku
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // Szukamy Warstwy Tekstu
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // Możemy użyć prostego UpdateText, ale ta metoda daje nam możliwość edycji tekstu fragmentami
                                        // Tworzymy warstwy tekstu wielolinijkowego i inne funkcje stylizacji tekstu i akapitu
                                        // Bądź ostrożny. Jeśli Zawartość Smart Object nie jest formatem PSD, nie można użyć tej metody edycji tekstu
                                        // W takim przypadku należy użyć API Graficznego: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "Najlepszy";

                                        // Powinieneś zmienić rozmiar tekstu, jeśli chcesz, aby obraz wyglądał dobrze.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // Lepiej jest użyć ReplaceContents. Automatycznie ponownie renderuje Smart Object
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // W ten sposób zapisujemy zmieniony plik PSD
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
