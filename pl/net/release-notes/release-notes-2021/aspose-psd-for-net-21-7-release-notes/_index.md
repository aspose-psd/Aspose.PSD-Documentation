---
title: Notatki wydania Aspose.PSD dla .NET 21.7
type: docs
weight: 60
url: /pl/net/aspose-psd-dla-net-21-7-notatki-o-wydaniu/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki wydania [Aspose.PSD dla .NET 21.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-806|Wsparcie dla edycji czcionek za pomocą TextPortions|Funkcja|
|PSDNET-917|Aspose.PSD 21.6: ImageSaveException podczas próby konwersji PSD do PNG|Błąd|
|PSDNET-858|Dodano konfigurację do Aspose.PSD .Net 5.0|Ulepszenie|

## **Zmiany w API publicznym**
# **Dodane interfejsy API:**
- M:Aspose.PSD.FontSettings.GetAdobeFontName(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontName

# **Usunięte interfejsy API:**
- Brak

## **Przykłady użycia:**

**PSDNET-806. Wsparcie dla edycji czcionek za pomocą TextPortions**

{{< highlight csharp >}}
            string outputFilePng = "wynik_testEdycjiCzcionek.png";
            string outputFilePsd = "testEdycjiCzcionek.psd";

            void AssertAreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Obiekty nie są równe.");
                }
            }

            using (var image = new PsdImage(500, 500))
            {
                FillLayer backgroundFillLayer = FillLayer.CreateInstance(FillType.Color);
                ((IColorFillSettings)backgroundFillLayer.FillSettings).Color = Color.White;
                image.AddLayer(backgroundFillLayer);

                TextLayer textLayer = image.AddTextLayer("Tekst 1", new Rectangle(10, 35, image.Width, 35));

                ITextPortion firstPortion = textLayer.TextData.Items[0];
                firstPortion.Style.FontName = FontSettings.GetAdobeFontName("Comic Sans MS");

                var secondPortion = textLayer.TextData.ProducePortion();
                secondPortion.Text = "Tekst 2";
                secondPortion.Paragraph.Apply(firstPortion.Paragraph);
                secondPortion.Style.Apply(firstPortion.Style);
                secondPortion.Style.FontName = FontSettings.GetAdobeFontName("Arial");

                textLayer.TextData.AddPortion(secondPortion);
                textLayer.TextData.UpdateLayerData();

                image.Save(outputFilePng, new PngOptions());
                image.Save(outputFilePsd);
            }

            using (var image = (PsdImage)Image.Load(outputFilePsd))
            {
                TextLayer textLayer = (TextLayer)image.Layers[2];

                string adobeFontName1 = FontSettings.GetAdobeFontName("Comic Sans MS");
                string adobeFontName2 = FontSettings.GetAdobeFontName("Arial");

                AssertAreEqual(adobeFontName1, textLayer.TextData.Items[0].Style.FontName);
                AssertAreEqual(adobeFontName2, textLayer.TextData.Items[1].Style.FontName);
            }
{{< /highlight >}}

**PSDNET-917. Aspose.PSD 21.6: ImageSaveException podczas próby konwersji PSD do PNG**

{{< highlight csharp >}}
            string srcFile = "wejscie.psd";
            string output = "wyjscie.png";

            using (var image = Aspose.PSD.Image.Load(srcFile))
            {
                image.Save(output, new Aspose.PSD.ImageOptions.PngOptions());
            }
{{< /highlight >}}
