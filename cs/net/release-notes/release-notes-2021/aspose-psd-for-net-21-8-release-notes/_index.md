---
title: Aspose.PSD pro .NET 21.8 - Poznámky k vydání
type: docs
weight: 50
url: /cs/net/aspose-psd-pro-net-21-8-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klíč**|**Shrnutí**|**Kategorie**|
| :- | :- | :- |
|PSDNET-698|Podpora kompresních metod ZipWithPrediction|Funkce|
|PSDNET-663|Nesprávné mezerování textu v generovaném souboru PSD|Chyba|
|PSDNET-685|Výjimka při ukládání souboru PSD|Chyba|
|PSDNET-927|Nesprávná vzdálenost mezi řádky a symboly v Aspose.PSD, když je používán bez licence|Chyba|

## **Změny ve veřejném rozhraní API**
# **Přidaná API:**
- Žádné

# **Odebraná API:**
- Žádné

## **Příklady použití:**

**PSDNET-663. Nesprávné mezerování textu v generovaném souboru PSD**

{{< highlight csharp >}}
            string sourceFileName = "source.psd";
            string outputFileName = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. Výjimka při ukládání souboru PSD**

{{< highlight csharp >}}
            string sourceFileName = "File.psd";
            string outputFileName = "File2.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                var layer1 = (TextLayer)image.Layers[1];
                layer1.TextData.UpdateLayerData();

                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-698. Podpora kompresních metod ZipWithPrediction**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";

            string outputPng = "output.png";
            string outputRaw = "out_Raw.psd";
            string outputZip = "out_Zip.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(outputPng, new PngOptions());

                image.Save(outputRaw, new PsdOptions() { CompressionMethod = CompressionMethod.Raw });
                image.Save(outputZip, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. Nesprávná vzdálenost mezi řádky a symboly v Aspose.PSD, když je používán bez licence**

{{< highlight csharp >}}
            bool[] licenseStates = new bool[] { false, true };
            for (int i = 0; i < licenseStates.Length; i++)
            {
                bool testLicense = licenseStates[i];
                if (testLicense)
                {
                    License license = new License();
                    license.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string sourceFile = "psdnetTest927.psd";
                string outputFile = "out_" + testLicense.ToString() + "_psdnetTest927.png";

                using (var image = (PsdImage)Image.Load(sourceFile))
                {
                    image.Save(outputFile, new PngOptions());
                }
            }
{{< /highlight >}}
