---
title: Aspose.PSD voor .NET 20.10 - Release-opmerkingen
type: docs
weight: 30
url: /nl/net/aspose-psd-voor-net-20-10-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-565|Uitzondering bij opslaan van specifiek PSD-bestand met tekstlagen|Fout|
|PSDNET-680|Lettertypen gaan verloren na rondreizen met Aspose.PSD|Fout|
|PSDNET-704|Weergave van de Smart Object-laag|Functie|
|PSDNET-707|Ondersteuning van de Smart Object niet-destructieve transfomraties|Functie|
|PSDNET-711|Tekstlaag wordt verplaatst na opslaan zonder wijzigingen|Fout|
|PSDNET-720|Aspose.PSD 20.8: Uitzondering bij conversie van Psd naar Tiff|Fout|

## **Openbare API-wijzigingen**
# **Toegevoegde API's:**
- Geen
# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**
**PSDNET-565. Uitzondering bij opslaan van specifiek PSD-bestand met tekstlagen**
{{< highlight csharp >}}
            string bronBestandspad = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string uitvoerBestand = "result.psd";

            using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestandspad))
            {
                afbeelding.Save(uitvoerBestand, new PsdOptions(afbeelding));
            }
{{< /highlight >}}
**PSDNET-680. Lettertypen gaan verloren na rondreizen met Aspose.PSD**
{{< highlight csharp >}}
            string bronBestandspad = "TwoFonts.psd";

            string uitvoerPsd1 = "output1.psd";
            string uitvoerPsd2 = "output2.psd";
            string uitvoerPng1 = "output1.png";
            string uitvoerPng2 = "output2.png";

            void ZijnGelijk(int verwacht, int daadwerkelijk)
            {
                if (verwacht != daadwerkelijk)
                {
                    throw new Exception("Waarden zijn niet gelijk.");
                }
            }

            using (var psdAfbeelding = (PsdImage)Image.Load(bronBestandspad))
            {
                var tekstLaag = (TextLayer)psdAfbeelding.Layers[1];

                ZijnGelijk(1, tekstLaag.TextData.Items[0].Style.FontIndex);
                ZijnGelijk(0, tekstLaag.TextData.Items[1].Style.FontIndex);

                tekstLaag.TextData.UpdateLayerData();

                ZijnGelijk(1, tekstLaag.TextData.Items[0].Style.FontIndex);
                ZijnGelijk(0, tekstLaag.TextData.Items[1].Style.FontIndex);

                psdAfbeelding.Save(uitvoerPsd1, new PsdOptions(psdAfbeelding));
                psdAfbeelding.Save(uitvoerPng1, new PngOptions());
            }

            using (var psdAfbeelding = (PsdImage)Image.Load(uitvoerPsd1))
            {
                var tekstLaag = (TextLayer)psdAfbeelding.Layers[1];

                ZijnGelijk(1, tekstLaag.TextData.Items[0].Style.FontIndex);
                ZijnGelijk(0, tekstLaag.TextData.Items[1].Style.FontIndex);

                tekstLaag.TextData.UpdateLayerData();

                ZijnGelijk(1, tekstLaag.TextData.Items[0].Style.FontIndex);
                ZijnGelijk(0, tekstLaag.TextData.Items[1].Style.FontIndex);

                psdAfbeelding.Save(uitvoerPsd2, new PsdOptions(psdAfbeelding));
                psdAfbeelding.Save(uitvoerPng2, new PngOptions());
            }
{{< /highlight >}}
**PSDNET-704. Weergave van de Smart Object-laag**
{{< highlight csharp >}}
            // Dit voorbeeld toont hoe de inhoud van de Adobe® Photoshop® Smart Object-laag kan worden vervangen en correct kan worden weergegeven.
            string dataMap = "PSDNET704_1\\";
            string bestandspad = dataMap + "new_panama-papers-4-trans4.psd";
            string pngUitvoerpad = dataMap + "new_panama-papers-4-trans4_vervangen.png";
            string psdUitvoerpad = dataMap + "new_panama-papers-4-trans4_vervangen.psd";
            string nieuweInhoudspad = dataMap + "new_huset.jpg";
            using (PsdImage afbeelding = (PsdImage)Image.Load(bestandspad))
            {
                var smartObjectLaag = (SmartObjectLayer)afbeelding.Layers[afbeelding.Layers.Length - 1];
                smartObjectLaag.ReplaceContents(nieuweInhoudspad);
                afbeelding.Save(pngUitvoerpad, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                afbeelding.Save(psdUitvoerpad, new PsdOptions(afbeelding));
            }

            // Dit voorbeeld toont het bijwerken van de image cache van de Adobe® Photoshop® Smart Object-lagen en hun correcte weergave.
            bestandspad = dataMap + "LayeredSmartObjects8bit2.psd";
            pngUitvoerpad = dataMap + "LayeredSmartObjects8bit2_bijgewerkt.png";
            psdUitvoerpad = dataMap + "LayeredSmartObjects8bit2_bijgewerkt.psd";
            using (PsdImage afbeelding = (PsdImage)Image.Load(bestandspad))
            {
                afbeelding.SmartObjectProvider.UpdateAllModifiedContent();
                afbeelding.Save(pngUitvoerpad, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                afbeelding.Save(psdUitvoerpad, new PsdOptions(afbeelding));
            }
{{< /highlight >}}
**PSDNET-707. Ondersteuning van de Smart Object niet-destructieve transfomraties**
{{< highlight csharp >}}
            string dataMap = "PSDNET707_1\\";
            string uitvoerMap = dataMap;

            // Deze voorbeelden tonen niet-destructieve transformaties van het PSD-bestand met SmartObjectLayer.
            // We kunnen een laag schalen, roteren, schuintrekken, vervormen, perspectief transformeren of vervormen zonder
            // verlies van originele beeldgegevens of kwaliteit omdat de transformaties de originele gegevens niet beïnvloeden.

            // Dit voorbeeld toont hoe de afbeelding van Adobe® Photoshop® met slimme objectlagen kan worden vergroot:
            VoorbeeldVanSmartObjectAfbeeldingVergrotingsOndersteuning("new_panama-papers-8-trans4-linked");
            VoorbeeldVanSmartObjectAfbeeldingVergrotingsOndersteuning("picture-frame-4-linked3");
            VoorbeeldVanSmartObjectAfbeeldingVergrotingsOndersteuning("gorilla");

            // Dit voorbeeld toont hoe het PSD-bestand met slimme objectlagen kan worden vergroot.
            void VoorbeeldVanSmartObjectAfbeeldingVergrotingsOndersteuning(string bestandsnaam)
            {
                const int schaal = 4;
                string bestandspad = dataMap + bestandsnaam + ".psd";
                string uitvoerPad = uitvoerMap + "Resize_" + bestandsnaam + ".psd";
                string uitvoerPngPad = uitvoerMap + "Resize_" + bestandsnaam + ".png";
                using (PsdImage afbeelding = (PsdImage)Image.Load(bestandspad))
                {
                    int nieuweBreedte = afbeelding.Width * schaal;
                    int nieuweHoogte = afbeelding.Height * schaal;
                    afbeelding.Resize(nieuweBreedte, nieuweHoogte);
                    afbeelding.Save(uitvoerPad, new PsdOptions(afbeelding));
                    afbeelding.Save(uitvoerPngPad, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Dit voorbeeld toont hoe de slimme objectlaag van Adobe® Photoshop® kan worden vergroot.
            VoorbeeldVanSmartObjectLaagVergrotingsOndersteuning("new_panama-papers-8-trans4-linked");
            VoorbeeldVanSmartObjectLaagVergrotingsOndersteuning("gorilla");

            // Dit voorbeeld toont hoe een slimme objectlaag in het PSD-bestand kan worden vergroot.
            void VoorbeeldVanSmartObjectLaagVergrotingsOndersteuning(string bestandsnaam)
            {
                const double schaal = 3.5;
                string bestandspad = dataMap + bestandsnaam + ".psd";
                string uitvoerPad = uitvoerMap + "ResizeLast_" + bestandsnaam + ".psd";
                string uitvoerPngPad = uitvoerMap + "ResizeLast_" + bestandsnaam + ".png";
                using (PsdImage afbeelding = (PsdImage)Image.Load(bestandspad))
                {
                    var slimmeObjectlaag = afbeelding.Layers[afbeelding.Layers.Length - 1];
                    int nieuweBreedte = (int)(slimmeObjectlaag.Width * schaal);
                    int nieuweHoogte = (int)(slimmeObjectlaag.Height * schaal);
                    slimmeObjectlaag.Resize(nieuweBreedte, nieuweHoogte);
                    afbeelding.Save(uitvoerPad, new PsdOptions(afbeelding));
                    afbeelding.Save(uitvoerPngPad, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Dit voorbeeld toont hoe de slimme objectlaag van Adobe® Photoshop® kan worden bijgesneden.
            VoorbeeldVanSmartObjectLaagBijsnijdingsOndersteuning("new_panama-papers-8-trans4-linked");
            VoorbeeldVanSmartObjectLaagBijsnijdingsOndersteuning("gorilla");

            // Dit voorbeeld toont hoe een slimme objectlaag in het PSD-bestand kan worden bijgesneden.
            void VoorbeeldVanSmartObjectLaagBijsnijdingsOndersteuning(string bestandsnaam)
            {
                string bestandspad = dataMap + bestandsnaam + ".psd";
                string uitvoerPad = uitvoerMap + "CropLast_" + bestandsnaam + ".psd";
                string uitvoerPngPad = uitvoerMap + "CropLast_" + bestandsnaam + ".png";
                using (PsdImage afbeelding = (PsdImage)Image.Load(bestandspad))
                {
                    var slimmeObjectlaag = afbeelding.Layers[afbeelding.Layers.Length - 1];
                    slimmeObjectlaag.Crop(25, 15, 30, 10);
                    afbeelding.Save(uitvoerPad, new PsdOptions(afbeelding));
                    afbeelding.Save(uitvoerPngPad, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Dit voorbeeld toont hoe de slimme objectlaag van Adobe® Photoshop® kan worden bijgesneden:
            VoorbeeldVanSmartObjectAfbeeldingBijsnijdingsOndersteuning("new_panama-papers-8-trans4-linked");
            VoorbeeldVanSmartObjectAfbeeldingBijsnijdingsOndersteuning("gorilla");

            // Dit voorbeeld toont hoe het PSD-bestand met slimme objectlagen kan worden bijgesneden.
            void VoorbeeldVanSmartObjectAfbeeldingBijsnijdingsOndersteuning(string bestandsnaam)
            {
                string bestandspad = dataMap + bestandsnaam + ".psd";
                string uitvoerPad = uitvoerMap + "Crop_" + bestandsnaam + ".psd";
                string uitvoerPngPad = uitvoerMap + "Crop_" + bestandsnaam + ".png";
                using (PsdImage afbeelding = (PsdImage)Image.Load(bestandspad))
                {
                    afbeelding.Crop(25, 10, 30, 5);
                    afbeelding.Save(uitvoerPad, new PsdOptions(afbeelding));
                    afbeelding.Save(uitvoerPngPad, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Dit voorbeeld toont hoe de afbeelding van Adobe® Photoshop® met slimme objectlagen kan worden geroteerd en gespiegeld:
            VoorbeeldVanSmartObjectAfbeeldingRoteerSpiegelOndersteuning("gorilla", RotateFlipType.Rotate90FlipNone);
            VoorbeeldVanSmartObjectAfbeeldingRoteerSpiegelOndersteuning("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            VoorbeeldVanSmartObjectAfbeeldingRoteerSpiegelOndersteuning("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            VoorbeeldVanSmartObjectAfbeeldingRoteerSpiegelOndersteuning("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            VoorbeeldVanSmartObjectAfbeeldingRoteerSpiegelOndersteuning("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            VoorbeeldVanSmartObjectAfbeeldingRoteerSpiegelOndersteuning("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            VoorbeeldVanSmartObjectAfbeeldingRoteerSpiegelOndersteuning("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            VoorbeeldVanSmartObjectAfbeeldingRoteerSpiegelOndersteuning("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // Dit voorbeeld toont hoe de PSD-bestand met slimme objectlagen kan worden geroteerd en gespiegeld.
            void VoorbeeldVanSmartObjectAfbeeldingRoteerSpiegelOndersteuning(string bestandsnaam, RotateFlipType roteerSpiegelType)
            {
                string bestandspad = dataMap + bestandsnaam + ".psd";
                string uitvoerPad = uitvoerMap + roteerSpiegelType + "_" + bestandsnaam + ".psd";
                string uitvoerPngPad = uitvoerMap + roteerSpiegelType + "_" + bestandsnaam + ".png";
                using (PsdImage afbeelding = (PsdImage)Image.Load(bestandspad))
                {
                    afbeelding.RotateFlip(roteerSpiegelType);
                    afbeelding.Save(uitvoerPad, new PsdOptions(afbeelding));
                    afbeelding.Save(uitvoerPngPad, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Dit voorbeeld toont hoe de slimme objectlaag van Adobe® Photoshop® kan worden geroteerd en gespiegeld.
            VoorbeeldVanSmartObjectLaagRoteerSpiegelOndersteuning("gorilla", RotateFlipType.Rotate90FlipNone);
            VoorbeeldVanSmartObjectLaagRoteerSpiegelOndersteuning("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            VoorbeeldVanSmartObjectLaagRoteerSpiegelOndersteuning("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            VoorbeeldVanSmartObjectLaagRoteerSpiegelOndersteuning("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            VoorbeeldVanSmartObjectLaagRoteerSpiegelOndersteuning("r3-embedded-transform2", RotateFlipType.Rotate90FlipNone);
            VoorbeeldVanSmartObjectLaagRoteerSpiegelOndersteuning("r3-embedded-transform2", RotateFlipType.Rotate90FlipX);
            VoorbeeldVanSmartObjectLaagRoteerSpiegelOndersteuning("r3-embedded-transform2", RotateFlipType.Rotate90FlipY);
            VoorbeeldVanSmartObjectLaagRoteerSpiegelOndersteuning("r3-embedded-transform2", RotateFlipType.Rotate90FlipXY);

            // Dit voorbeeld toont hoe een slimme objectlaag in het PSD-bestand kan worden geroteerd en gespiegeld.
            void VoorbeeldVanSmartObjectLaagRoteerSpiegelOndersteuning(string bestandsnaam, RotateFlipType roteerSpiegelType)
            {
                string bestandspad = dataMap + bestandsnaam + ".psd";
                string uitvoerPad = uitvoerMap + roteerSpiegelType + "Last_" + bestandsnaam + ".psd";
                string uitvoerPngPad = uitvoerMap + roteerSpiegelType + "Last_" + bestandsnaam + ".png";
                using (PsdImage afbeelding = (PsdImage)Image.Load(bestandspad))
                {
                    var smartObjectLaag = (SmartObjectLaag)afbeelding.Layers[afbeelding.Layers.Length - 1];
                    smartObjectLaag.RotateFlip(roteerSpiegelType);
                    afbeelding.Save(uitvoerPad, new PsdOptions(afbeelding));
                    afbeelding.Save(uitvoerPngPad, new