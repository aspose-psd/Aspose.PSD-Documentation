---
title: Aspose.PSD pro .NET 20.10 - Poznámky k vydání
type: docs
weight: 30
url: /cs/net/aspose-psd-pro-net-20-10-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-565|Výjimka při ukládání konkrétního souboru PSD s textovými vrstvami|Chyba|
|PSDNET-680|Písma jsou ztracena po cestách s Aspose.PSD|Chyba|
|PSDNET-704|Vyrendrování vrstvy Smart Object|Funkce|
|PSDNET-707|Podpora nedestruktivních transformací Smart Object|Funkce|
|PSDNET-711|Vrstva textu se posune po uložení bez jakýchkoli změn|Chyba|
|PSDNET-720|Aspose.PSD 20.8: Výjimka při konverzi Psd na Tiff|Chyba|

## **Změny v Veřejném API**
# **Přidaná API:**
- Žádná
# **Odebraná API:**
- Žádná

## **Příklady použití:**
**PSDNET-565. Výjimka při ukládání konkrétního souboru PSD s textovými vrstvami**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}

**PSDNET-680. Písma jsou ztracena po cestách s Aspose.PSD**
{{< highlight csharp >}}
            string sourceFilePath = "TwoFonts.psd";

            string outputPsd1 = "output1.psd";
            string outputPsd2 = "output2.psd";
            string outputPng1 = "output1.png";
            string outputPng2 = "output2.png";

            void AreEqual(int expected, int actual)
            {
                if (expected != actual)
                {
                    throw new Exception("Hodnoty nejsou stejné.");
                }
            }

            using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd1, new PsdOptions(psdImage));
                psdImage.Save(outputPng1, new PngOptions());
            }

            using (var psdImage = (PsdImage)Image.Load(outputPsd1))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd2, new PsdOptions(psdImage));
                psdImage.Save(outputPng2, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-704. Vyrendrování vrstvy Smart Object**
{{< highlight csharp >}}
            // Tento příklad ukazuje, jak nahradit obsah vrstvy chytrého objektu Adobe® Photoshop® a její správné vykreslení.
            string dataDir = "PSDNET704_1\\";
            string filePath = dataDir + "new_panama-papers-4-trans4.psd";
            string pngOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.png";
            string psdOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.psd";
            string newContentPath = dataDir + "new_huset.jpg";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                var smartObjectLayer = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                smartObjectLayer.ReplaceContents(newContentPath);
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }

            // Tento příklad ukazuje, jak aktualizovat mezipaměť obrázků vrstev chytrých objektů Adobe® Photoshop® a jejich správné vykreslení.
            filePath = dataDir + "LayeredSmartObjects8bit2.psd";
            pngOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.png";
            psdOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.psd";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                image.SmartObjectProvider.UpdateAllModifiedContent();
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }
{{< /highlight >}}

**PSDNET-707. Podpora nedestruktivních transformací Smart Object**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // Tyto příklady ukazují nedestruktivní transformace souboru PSD se SmartObjectLayer.
            // Můžeme zvětšit, otáčet, zkřivit, deformovat, perspektivně transformovat nebo deformovat vrstvu bez
            // ztráty původních údajů nebo kvality, protože transformace nepůsobí na původní data.

            // Tento příklad ukazuje, jak změnit velikost obrázku Adobe® Photoshop® se SmarObjectLayer:
            PríkladZměnyVelikostiSouboruSmartObjectImage("new_panama-papers-8-trans4-linked");
            PríkladZměnyVelikostiSouboruSmartObjectImage("picture-frame-4-linked3");
            PríkladZměnyVelikostiSouboruSmartObjectImage("gorilla");

            // Tento příklad ukazuje, jak změnit velikost souboru PSD se SmartObjectLayer.
            void PríkladZměnyVelikostiSouboruSmartObjectImage(string fileName)
            {
                const int scale = 4;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "ZměnaVelikosti_" + fileName + ".psd";
                string outputPngPath = outputDir + "ZměnaVelikosti_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    int newWidth = image.Width * scale;
                    int newHeight = image.Height * scale;
                    image.Resize(newWidth, newHeight);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}

**PSDNET-711. Vrstva textu se posune po uložení bez jakýchkoli změn**
{{< highlight csharp >}}
            string srcFile = "PsdCompressTest3.psd";
            string output = "PsdCompressTest3.psdoutput.psd";

            void AreNotEqual(object expected, object actual)
            {
                if (object.Equals(expected, actual))
                {
                    throw new Exception("Hodnoty jsou stejné.");
                }
            }

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PsdOptions(image));
            }

            using (PsdImage image = (PsdImage)Image.Load(output))
            {
                TextLayer txtLayer = (TextLayer)image.Layers[2];

                AreNotEqual(txtLayer.Left, txtLayer.TransformMatrix[4]);
                AreNotEqual(txtLayer.Top, txtLayer.TransformMatrix[5]);
            }
{{< /highlight >}}

**PSDNET-720. Aspose.PSD 20.8: Výjimka při konverzi Psd na Tiff**
{{< highlight csharp >}}
            using (var psdImage = (PsdImage)Image.Load("sarbarg.fin12.psd"))
            {
                psdImage.Save("result.tiff", new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
            }
{{< /highlight >}}