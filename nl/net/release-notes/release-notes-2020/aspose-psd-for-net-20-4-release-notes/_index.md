---
title: Aspose.PSD voor .NET 20.4 - Release-opmerkingen
type: docs
weight: 90
url: /nl/net/aspose-psd-voor-net-20-4-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Belangrijkste**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-567|Ondersteuning van de bron 'Vector Origination Data'|Functie|
|PSDNET-373|Ondersteuning van lclrResource (Bladkleur instelling)|Functie|
|PSDNET-563|Ondersteuning van eigenschappen van LengthRecord-gegevens. (Padbewerkingen (booleaanse operaties), index van de vorm in de laag, aantal bezier-knooprecord)|Functie|
|PSDNET-425|Ondersteuning van Image Section Resource #1010 Achtergrondkleur|Functie|
|PSDNET-530|Toevoegen van vullagen tijdens runtime|Functie|
|PSDNET-424|Ondersteuning van Image Section Resource #1009 Randinformatie|Functie|
|PSDNET-592|Ondersteuning van Lagen in AI Formaat Bestanden|Functie|
|PSDNET-256|Ondersteuning bij het Lezen en Bewerken van Gradiënt Overlay Laageffect|Functie|
|PSDNET-257|Weergave van Gradiënt Overlay Laageffect|Functie|
|PSDNET-585|` `Wijzigingen in de GradientOverlayEffect.BlendMode eigenschap worden niet weergegeven in Photoshop|Fout|
|PSDNET-561|Oplossing voor het opslaan van afbeelding in PSD-formaat met Grayscale ColorMode en 16 bit per kanaal naar Grayscale PSD-formaat|Fout|
|PSDNET-560|Oplossing voor het opslaan van afbeelding in PSD-formaat met Grayscale ColorMode en 16 bit per kanaal naar PNG-formaat|Fout|

## **Openbare API-wijzigingen**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Name
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsTemplate
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsLocked
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsShown
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPrinted
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPreview
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsImagesDimmed
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.DimValue
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorNumber
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Red
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Green
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Blue
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- T:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.Color
- T:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Width
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Unit
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.#ctor(System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.BezierKnotRecordsCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.ShapeIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.ShapeOriginSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.#ctor(System.Boolean,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidated
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.OriginIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.ExcludeOverlappingShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.CombineShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.SubtractFrontShape
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.IntersectShapeAreas
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.#ctor(Aspose.PSD.Color,System.Int32,System.Int32)
# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**
**PSDNET-567. Ondersteuning van de bron 'Vector Origination Data'**

{{< highlight java >}}

         // VogkResource-ondersteuning

        static void VoorbeeldVanVogkResourceOndersteuning()

        {

            string bestandsnaam = "VectorOriginationDataResource.psd";

            string uitBestandsnaam = "uit_VectorOriginationDataResource_.psd";

            using (var psdAfbeelding = (PsdImage)Image.Load(bestandsnaam))

            {

                var bron = GetVogkResource(psdAfbeelding);

                // Lezen

                if (bron.ShapeOriginSettings.Length != 1 ||

                    !bron.ShapeOriginSettings[0].IsShapeInvalidated ||

                    bron.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    throw new Exception("VogkResource is verkeerd gelezen.");

                }

                // Bewerken

                bron.ShapeOriginSettings = new[]

                {

                    bron.ShapeOriginSettings[0],

                    new VectorShapeOriginSettings(true, 1)

                };

                psdAfbeelding.Save(uitBestandsnaam);

            }

        }

        static VogkResource GetVogkResource(PsdAfbeelding afbeelding)

        {

            var laag = afbeelding.Layers[1];

            VogkResource bron = null;

            var bronnen = laag.Resources;

            for (int i = 0; i < bronnen.Length; i++)

            {

                if (bronnen[i] is VogkResource)

                {

                    bron = (VogkResource)bronnen[i];

                    break;

                }

            }

            if (bron == null)

            {

                throw new Exception("VogkResource niet gevonden.");

            }

            return bron;

        }   

{{< /highlight >}}

**PSDNET-373. Ondersteuning van lclrResource (Bladkleur instelling)**

{{< highlight java >}}

         static void ControleerBladKleurenEnOmgekeerd(SheetColorHighlightEnum[] bladKleuren, PsdAfbeelding img)

        {

            int aantalLagen = img.Layers.Length;

            for (int laagIndex = 0; laagIndex < aantalLagen; laagIndex++)

            {

                Laag laag = img.Layers[laagIndex];

                LaagResource[] bronnen = laag.Resources;

                foreach (LaagResource laagBron in bronnen)

                {

                    // De lclr-bron is altijd aanwezig in de psd-bestandsbronlijst.

                    LclrResource bron = laagBron as LclrResource;

                    if (bron != null)

                    {

                        if (bron.Color != bladKleuren[laagIndex])

                        {

                            throw new Exception("Bladkleur is verkeerd gelezen");

                        }

                        // Omgekeerd van stijlbladkleuren. Instellen van laagkleurmarkering op.

                        bron.Color = bladKleuren[aantalLagen - laagIndex - 1];

                        break;

                    }

                }

            }

        }

            string bronBestandsPad = "AlleLclrResourceKleuren.psd";

            string uitvoerBestandsPad = "AlleLclrResourceKleurenOmgekeerd.psd";

            // In het bestand zijn kleuren van laagmarkeringen in deze volgorde

            SheetColorHighlightEnum[] bladKleuren = new SheetColorHighlightEnum[] {

                SheetColorHighlightEnum.Rood,

                SheetColorHighlightEnum.Oranje,

                SheetColorHighlightEnum.Geel,

                SheetColorHighlightEnum.Groen,

                SheetColorHighlightEnum.Blauw,

                SheetColorHighlightEnum.Violet,

                SheetColorHighlightEnum.Grijs,

                SheetColorHighlightEnum.GeenKleur

            };            

            // Laagbladkleur wordt gebruikt om visueel lagen te markeren. 

            // Bijvoorbeeld u kunt enkele lagen in PSD bijwerken en vervolgens de laag markeren met een kleur waarvan u de aandacht wilt trekken.

            using (PsdAfbeelding img = (PsdAfbeelding)Image.Load(bronBestandsPad))

            {

                ControleerBladKleurenEnOmgekeerd(bladKleuren, img);

                img.Save(uitvoerBestandsPad, new PsdOpties());

            }

            using (PsdAfbeelding img = (PsdAfbeelding)Image.Load(uitvoerBestandsPad))

            {

                // Kleuren moeten worden omgekeerd

                Array.Reverse(bladKleuren);

                ControleerBladKleurenEnOmgekeerd(bladKleuren, img);

            }

{{< /highlight >}}

**PSDNET-563. Ondersteuning van eigenschappen van LengthRecord-gegevens. (Padbewerkingen (booleaanse operaties), index van de vorm in laag, aantal bezier-knooprecord)**

{{< highlight java >}}

            string bestandsnaam = "PadBewerkingenVorm.psd";

            using (var im = (PsdAfbeelding)Image.Load(bestandsnaam))

            {

                VsmsResource bron = null;

                foreach (var laagBron in im.Layers[1].Resources)

                {

                    if (laagBron is VsmsResource)

                    {

                        bron = (VsmsResource)laagBron;

                        break;

                    }

                }

                LengthRecord lengthRecord0 = (LengthRecord)bron.Paths[2];

                LengthRecord lengthRecord1 = (LengthRecord)bron.Paths[7];

                LengthRecord lengthRecord2 = (LengthRecord)bron.Paths[11];

                // Hier veranderen we de manier van combineren tussen vormen.

                lengthRecord0.PathOperations = PathOperations.ExcludeOverlappingShapes;

                lengthRecord1.PathOperations = PathOperations.IntersectShapeAreas;

                lengthRecord2.PathOperations = PathOperations.SubtractFrontShape;

                im.Save("uit_" + bestandsnaam);

            }

{{< /highlight >}}

**PSDNET-425. Ondersteuning van Image Section Resource #1010 Achtergrondkleur**

{{< highlight java >}}

             string bronBestand = "invoer.psd";

            string uitvoerBestand = "uitvoer.psd";

            using (var afbeelding = (PsdAfbeelding)Image.Load(bronBestand))

            {

                ResourceBlock[] afbeeldingsbronnen = afbeelding.ImageResources;

                BackgroundColorResource achtergrondkleurBron = null;

                foreach (var afbeeldingsbron in afbeeldingsbronnen)

                {

                    if (afbeeldingsbron is BackgroundColorResource)

                    {

                        achtergrondkleurBron = (BackgroundColorResource)afbeeldingsbron;

                        break;

                    }

                }

                // bijwerken van BackgroundColorResource

                achtergrondkleurBron.Color = Color.DarkRed;

                afbeelding.Save(uitvoerBestand);

            }

{{< /highlight >}}

**PSDNET-530. Toevoegen van vullagen tijdens runtime**

{{< highlight java >}}

             string uitvoerPsd = "uitvoer.psd";

            using (var afbeelding = new PsdAfbeelding(100, 100))

            {

                FillLayer kleurVulLaag = FillLayer.CreateInstance(FillType.Kleur);

                kleurVulLaag.DisplayName = "Kleur Vul Laag";

                afbeelding.AddLayer(kleurVulLaag);

                FillLayer verloopVulLaag = FillLayer.CreateInstance(FillType.Gradient);

                verloopVulLaag.DisplayName = "Verloop Vul Laag";

                afbeelding.AddLayer(verloopVulLaag);

                FillLayer patroonVulLaag = FillLayer.CreateInstance(FillType.Patroon);

                patroonVulLaag.DisplayName = "Patroon Vul Laag";

                patroonVulLaag.Opacity = 50;

                afbeelding.AddLayer(patroonVulLaag);

                afbeelding.Save(uitvoerPsd);

            }

{{< /highlight >}}

**PSDNET-424. Ondersteuning van Image Section Resource #1009 Randinformatie**

{{< highlight java >}}

             string bronBestand = "invoer.psd";

            string uitvoerBestand = "uitvoer.psd";

            using (var afbeelding = (PsdAfbeelding)Image.Load(bronBestand))

            {

                ResourceBlock[] afbeeldingsbronnen = afbeelding.ImageResources;

                BorderInformationResource randInfoBron = null;

                foreach (var afbeeldingsbron in afbeeldingsbronnen)

                {

                    if (afbeeldingsbron is BorderInformationResource)

                    {

                        randInfoBron = (BorderInformationResource)afbeeldingsbron;

                        break;

                    }

                }

                // bijwerken van BorderInformationResource

                randInfoBron.Width = 0.1;

                randInfoBron.Unit = PhysicalUnit.Inches;

                afbeelding.Save(uitvoerBestand);

            }

{{< /highlight >}}

**PSDNET-592. Ondersteuning van Lagen in AI Formaat Bestanden**

{{< highlight java >}}

         void AssertIsTrue(bool voorwaarde, string bericht)

        {

            if (!voorwaarde)

            {

                throw new FormatException(bericht);

            }

        }

        string bronBestandsnaam = "form_8_2l3_7.ai";

        string uitvoerBestandsnaam = "form_8_2l3_7_export";

        using (AiAfbeelding afbeelding = (AiAfbeelding)Image.Load(bronBestandsnaam))

        {

            AiLayerSection laag0 = afbeelding.Layers[0];

            AssertIsTrue(laag0 != null, "Laag 0 mag niet leeg zijn.");

            AssertIsTrue(laag0.Name == "Laag 4", "De Naam eigenschap van laag 0 moet Laag 4 zijn");

            AssertIsTrue(!laag0.IsTemplate, "De IsTemplate eigenschap van laag 0 moet onwaar zijn.");

            AssertIsTrue(laag0.IsLocked, "De IsLocked eigenschap van laag 0 moet waar zijn.");

            AssertIsTrue(laag0.IsShown, "De IsShown eigenschap van laag 0 moet waar zijn.");

            AssertIsTrue(laag0.IsPrinted, "De IsPrinted eigenschap van laag 0 moet waar zijn.");

            AssertIsTrue(!laag0.IsPreview, "De IsPreview eigenschap van laag 0 moet onwaar zijn.");

            AssertIsTrue(laag0.IsImagesDimmed, "De IsImagesDimmed eigenschap van la