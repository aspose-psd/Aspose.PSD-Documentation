---
title: Notatki wydania dotyczące Aspose.PSD dla .NET 21.3
type: docs
weight: 100
url: /pl/net/aspose-psd-dla-net-21-3-notatki-wydania/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki wydania dotyczące [Aspose.PSD dla .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-823|Dodanie SectionDividerLayer w celu poprawy doświadczenia z grupami warstw|Udoskonalenie|
|PSDNET-694|Podczas odczytywania PattResource, szerokość i wysokość zostały zamienione miejscami|Błąd|
|PSDNET-789|Nieprawidłowe mieszanie efektów warstw|Błąd|
|PSDNET-805|Nieprawidłowa kolejność i logika mieszania, gdy istnieje więcej niż jedno działanie efektu warstwy|Błąd|
|PSDNET-842|Właściwości efektu konturu nie są zapisywane do pliku PSD|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **Usunięte API:**
- Brak

## **Przykłady użycia:**

**PSDNET-694. Podczas odczytywania PattResource, szerokość i wysokość zostały zamienione miejscami**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // wywołanie renderowania wzoru

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Nieprawidłowe mieszanie efektów warstw**

{{< highlight csharp >}}
            string srcFile = "source_789.psd";
            string outputSmartObjectPath = "output789.png";
            string outputFile = "output789.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // Szukanie warstwy tekstowej
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "Najlepszy";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // W ten sposób zapisujemy zmieniony plik PSD
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. Nieprawidłowa kolejność i logika mieszania, gdy istnieje więcej niż jedno działanie efektu warstwy**

{{< highlight csharp >}}
            string sourceFile = "1_200x200.psd";
            string contentFile = "Numbers1Best.png";

            string outputFilePng = "output.png";
            string outputFilePsd = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(contentFile);
                        break;
                    }
                }

                // W ten sposób zapisujemy zmieniony plik PSD
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. Dodanie SectionDividerLayer w celu poprawy doświadczenia z grupami warstw**

{{< highlight csharp >}}
            // Poniższy kod demonstruje warstwy SectionDividerLayer i sposób uzyskania z nimi powiązanej warstwy grupy.

            // Hierarchia warstw
            //    [0]: '</Layer group>' SectionDividerLayer dla Grupy 1
            //    [1]: 'Layer 1' Zwykła warstwa
            //    [2]: '</Layer group>' SectionDividerLayer dla Grupy 2
            //    [3]: '</Layer group>' SectionDividerLayer dla Grupy 3
            //    [4]: 'Grupa 3' Warstwa grupująca
            //    [5]: 'Grupa 2' Warstwa grupująca
            //    [6]: 'Grupa 1' Warstwa grupująca

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Obiekty nie są równe.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // Tworzenie hierarchii warstw
                // Dodanie warstwy LayerGroup 'Grupa 1'
                LayerGroup group1 = image.AddLayerGroup("Grupa 1", 0, true);
                // Dodanie zwykłej warstwy
                Layer layer1 = new Layer();
                layer1.DisplayName = "Warstwa 1";
                group1.AddLayer(layer1);
                // Dodanie warstwy LayerGroup 'Grupa 2'
                LayerGroup group2 = group1.AddLayerGroup("Grupa 2", 1);
                // Dodanie warstwy LayerGroup 'Grupa 3'
                LayerGroup group3 = group2.AddLayerGroup("Grupa 3", 0);

                // Pobieranie sekcji SectionDividerLayer
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // używając metody SectionDividerLayer.GetRelatedLayerGroup(), uzyskaj powiązany obiekt LayerGroup.
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // ta sama LayerGroup
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // ta sama LayerGroup
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // ta sama LayerGroup

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Grupa 1' zawiera 5 warstw
            }
{{< /highlight >}}

**PSDNET-842. Właściwości efektu konturu nie są zapisywane do pliku PSD**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Obiekty nie są równe.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // Nie spowoduje rzucenia ArgumentNullException

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // Sprawdzenie zapisanych wartości
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}
