---
title: Aspose.PSD dla .NET 20.9 - Notatki dotyczące wersji
type: docs
weight: 40
url: /pl/net/aspose-psd-dla-net-20-9-notatki-dotyczace-wersji/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki dotyczące wersji [Aspose.PSD dla .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-408|Wsparcie dla SoLEResource (zewnętrzny zasób warstwy inteligentnego obiektu) |Funkcja|
|PSDNET-614|Wsparcie dla powiązanych inteligentnych obiektów|Funkcja|
|PSDNET-615|Wsparcie dla osadzonych inteligentnych obiektów|Funkcja|
|PSDNET-690|Aktualizacja tekstu w podanym pliku PSD i zapisanie go zmienia niektóre warstwy i wiele parametrów tekstu|Błąd|
|PSDNET-696|Warstwa FillLayer nie jest aktualizowana po utworzeniu i nie może być poprawnie renderowana|Błąd|
|PSDNET-712|Regresja: Aspose.PSD 20.8.0 nie może otworzyć pliku|Błąd|
|PSDNET-714|W określonym pliku PSD, zmiana rozmiaru warstwy tekstowej powoduje uszkodzenie wartości lokalizacji|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String,Aspose.PSD.RectangleF)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoKerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StandardLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.DiscretionaryLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.ContextualAlternates
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.LanguageIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.VerticalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HorizontalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Fractions
- T:Aspose.PSD.FileFormats.Psd.AutoKerning
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Manual
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Metric
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Optical
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Item(System.Guid)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource.PlacedId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Version
- ...

# **Usunięte API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.#ctor(System.Guid,System.Boolean)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Version
- ...
   
## **Przykłady użycia:**
**PSDNET-408. Wsparcie dla SoLEResource (zewnętrzny zasób warstwy inteligentnego obiektu)**
{{< highlight csharp >}}
        void AssertIsTrue(bool condition)
        {
            ...
        }

        void AssertAreEqual(object actual, object expected)
        {
            ...
        }

        void CheckSmartObjectResourceValues(object[] expectedValue, SmartObjectResource resource)
        {
            ...
        }

        void SetNewSmartValues(SmartObjectResource resource, object[] newValues)
        {
            ...
        }

        object[] newSmartValues = new object[]
        {
            ...
        };

        object[] expectedValues = new object[]
        {
            ...
        };

        string dataDir = "PSDNET408_1\\";
        var sourceFilePath = dataDir + "rgb8_2x2_linked.psd";
        var outputPath = dataDir + "rgb8_2x2_linked_output.psd";
        using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
        {
            SoLeResource soleResource = null;

            ... //Reszta kodu pominięta dla zwięzłości
        }
{{< /highlight >}}

**PSDNET-614. Wsparcie dla powiązanych inteligentnych obiektów**
...

**PSDNET-615. Wsparcie dla osadzonych inteligentnych obiektów**
...

**PSDNET-690. Aktualizacja tekstu w podanym pliku PSD i zapisanie go zmienia niektóre warstwy i wiele parametrów tekstu**
...

**PSDNET-696. Warstwa FillLayer nie jest aktualizowana po utworzeniu i nie może być poprawnie renderowana**
...

**PSDNET-712. Regresja: Aspose.PSD 20.8.0 nie może otworzyć pliku**
...

**PSDNET-714. W określonym pliku PSD, zmiana rozmiaru warstwy tekstowej powoduje uszkodzenie wartości lokalizacji**
...**PSDNET-696. Warstwa FillLayer nie jest aktualizowana po utworzeniu i nie może być poprawnie renderowana**
{{< highlight csharp >}}
            string srcFile = "TestSimple.psd";
            string outputFile = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                for (int i = 0; i < image.Layers.Length; i++)
                {
                    var layer = image.Layers[i] as FillLayer;
                    if (layer != null)
                    {
                        layer.Update();
                    }
                }

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-712. Regresja: Aspose.PSD 20.8.0 nie może otworzyć pliku**
{{< highlight csharp >}}
            string dataDir = "PSDNET712_1\\";
            string filePath = dataDir + "sample2.psd";
            using (var _ = (PsdImage)Image.Load(filePath))
            {
            }
{{< /highlight >}}

**PSDNET-714. W określonym pliku PSD, zmiana rozmiaru warstwy tekstowej powoduje uszkodzenie wartości lokalizacji**
{{< highlight csharp >}}
            string srcFile = "A.psd";
            string outputFile = "output.psd";

            RectangleF oldBoxBounds = new RectangleF(16852.8613f, 16861.332f, 17.4458752f, 14.327f);
            RectangleF newBoxBounds = new RectangleF(PointF.Empty, oldBoxBounds.Size);

            using (var psdImage = (PsdImage)Image.Load(srcFile))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                // fix the text box bounds value by shifting it to zero position.
                textLayer.TextBoundBox = newBoxBounds;
                textLayer.TextData.UpdateLayerData();

                psdImage.Save(outputFile);
            }
{{< /highlight >}}