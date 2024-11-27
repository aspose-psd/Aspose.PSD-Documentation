---
title: Aspose.PSD pro .NET 20.4 - Poznámky k vydání
type: docs
weight: 90
url: /cs/net/aspose-psd-pro-net-20-4-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 


|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-567|Podpora zdroje 'Vector Origination Data'|Funkce|
|PSDNET-373|Podpora lclrResource (nastavení barvy listu)|Funkce|
|PSDNET-563|Podpora vlastností z dat délkového záznamu. (Operace s cestami (logické operace), index tvaru ve vrstvě, počet záznamů uzlů s bezierovou křivkou)|Funkce|
|PSDNET-425|Podpora Zdroje Sekce Obrazovky #1010 Pozadí barvy|Funkce|
|PSDNET-530|Přidání vrstev výplně za běhu|Funkce|
|PSDNET-424|Podpora Zdroje Sekce Obrazovky #1009 Informace o ohraničení|Funkce|
|PSDNET-592|Podpora vrstev ve souborech formátu AI|Funkce|
|PSDNET-256|Podpora Čtení a Úpravy efektu Vrstevníků Průhledného Překrytí|Funkce|
|PSDNET-257|Rendrování efektu Průhledného Překrytí Přechodu|Funkce|
|PSDNET-585|Změny vlastnosti BlendMode v GradientOverlayEffect nejsou zobrazeny v Photoshopu|Chyba|
|PSDNET-561|Oprava ukládání obrázku PSD s režimem šedé stupnice a 16 bitů na kanál do formátu PSD ve šedé stupnici|Chyba|
|PSDNET-560|Oprava ukládání obrázku PSD s režimem šedé stupnice a 16 bitů na kanál do formátu PNG|Chyba|

## **Změny veřejného API**
# **Přidaná API:**
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
# **Odstraněná API:**
- Žádné

## **Příklady použití:**
**PSDNET-567. Podpora zdroje 'Vector Origination Data'**

{{< highlight java >}}

         // Podpora zdroje VogkResource

        static void ExampleOfVogkResourceSupport()

        {

            string fileName = "VectorOriginationDataResource.psd";

            string outFileName = "out_VectorOriginationDataResource_.psd";

            using (var psdImage = (PsdImage)Image.Load(fileName))

            {

                var resource = GetVogkResource(psdImage);

                // Čtení

                if (resource.ShapeOriginSettings.Length != 1 ||

                    !resource.ShapeOriginSettings[0].IsShapeInvalidated ||

                    resource.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    throw new Exception("VogkResource bylo čteno špatně.");

                }

                // Úprava

                resource.ShapeOriginSettings = new[]

                {

                    resource.ShapeOriginSettings[0],

                    new VectorShapeOriginSettings(true, 1)

                };

                psdImage.Save(outFileName);

            }

        }

        static VogkResource GetVogkResource(PsdImage image)

        {

            var layer = image.Layers[1];

            VogkResource resource = null;

            var resources = layer.Resources;

            for (int i = 0; i < resources.Length; i++)

            {

                if (resources[i] is VogkResource)

                {

                    resource = (VogkResource)resources[i];

                    break;

                }

            }

            if (resource == null)

            {

                throw new Exception("Nenalezen VogkResource.");

            }

            return resource;

        }   

{{< /highlight >}}

**PSDNET-373. Podpora lclrResource (nastavení barvy listu)**

{{< highlight java >}}

         static void CheckSheetColorsAndRerverse(SheetColorHighlightEnum[] sheetColors, PsdImage img)

        {

            int layersCount = img.Layers.Length;

            for (int layerIndex = 0; layerIndex < layersCount; layerIndex++)

            {

                Layer layer = img.Layers[layerIndex];

                LayerResource[] resources = layer.Resources;

                foreach (LayerResource layerResource in resources)

                {

                    // Zdroj lcrl je vždy přítomen v seznamu zdrojů souboru PSD.

                    LclrResource resource = layerResource as LclrResource;

                    if (resource != null)

                    {

                        if (resource.Color != sheetColors[layerIndex])

                        {

                            throw new Exception("Barva listu byla přečtena špatně");

                        }

                        // Obrácení stylu barev listů. Nastavení zvýraznění barvy vrstvy.

                        resource.Color = sheetColors[layersCount - layerIndex - 1];

                        break;

                    }

                }

            }

        }

            string sourceFilePath = "AllLclrResourceColors.psd";

            string outputFilePath = "AllLclrResourceColorsReversed.psd";

            // Barvy zvýrazňování vrstev v souboru jsou v tomto pořadí

            SheetColorHighlightEnum[] sheetColors = new SheetColorHighlightEnum[] {

                SheetColorHighlightEnum.Red,

                SheetColorHighlightEnum.Orange,

                SheetColorHighlightEnum.Yellow,

                SheetColorHighlightEnum.Green,

                SheetColorHighlightEnum.Blue,

                SheetColorHighlightEnum.Violet,

                SheetColorHighlightEnum.Gray,

                SheetColorHighlightEnum.NoColor

            };            

            // Barva oddělovníka vrstvy se používá k vizuálnímu zvýraznění vrstev. 

            // Například můžete aktualizovat některé vrstvy v souboru PSD a pak zvýraznit barvou vrstvu, na kterou chcete upozornit.

            using (PsdImage img = (PsdImage)Image.Load(sourceFilePath))

            {

                CheckSheetColorsAndRerverse(sheetColors, img);

                img.Save(outputFilePath, new PsdOptions());

            }

            using (PsdImage img = (PsdImage)Image.Load(outputFilePath))

            {

                // Barvy by měly být obráceny

                Array.Reverse(sheetColors);

                CheckSheetColorsAndRerverse(sheetColors, img);

            }

{{< /highlight >}}

**PSDNET-563. Podpora vlastností z dat délkového záznamu. (Operace cest (logické operace), index tvaru ve vrstvě, počet záznamů uzlů s bezierovou křivkou)**

{{< highlight java >}}

            string fileName = "PathOperationsShape.psd";

            using (var im = (PsdImage)Image.Load(fileName))

            {

                VsmsResource resource = null;

                foreach (var layerResource in im.Layers[1].Resources)

                {

                    if (layerResource is VsmsResource)

                    {

                        resource = (VsmsResource)layerResource;

                        break;

                    }

                }

                LengthRecord lengthRecord0 = (LengthRecord)resource.Paths[2];

                LengthRecord lengthRecord1 = (LengthRecord)resource.Paths[7];

                LengthRecord lengthRecord2 = (LengthRecord)resource.Paths[11];

                // Zde měníme způsob kombinace tvarů.

                lengthRecord0.PathOperations = PathOperations.ExcludeOverlappingShapes;

                lengthRecord1.PathOperations = PathOperations.IntersectShapeAreas;

                lengthRecord2.PathOperations = PathOperations.SubtractFrontShape;

                im.Save("out_" + fileName);

            }

{{< /highlight >}}

**PSDNET-425. Podpora Zdroje Sekce Obrazovky #1010 Pozadí barvy**

{{< highlight java >}}

             string sourceFile = "input.psd";

            string outputFile = "output.psd";

            using (var image = (PsdImage)Image.Load(sourceFile))

            {

                ResourceBlock[] imageResources = image.ImageResources;

                BackgroundColorResource backgroundColorResource = null;

                foreach (var imageResource in imageResources)

                {

                    if (imageResource is BackgroundColorResource)

                    {

                        backgroundColorResource = (BackgroundColorResource)imageResource;

                        break;

                    }

                }

                // aktualizace BackgroundColorResource

                backgroundColorResource .Color = Color.DarkRed;

                image.Save(outputFile);

            }

{{< /highlight >}}

**PSDNET-530. Přidání vrstev výplně za běhu**

{{< highlight java >}}

             string outputPsd = "output.psd";

            using (var image = new PsdImage(100, 100))

            {

                FillLayer colorFillLayer = FillLayer.CreateInstance(FillType.Color);

                colorFillLayer.DisplayName = "Vrstva s barvou";

                image.AddLayer(colorFillLayer);

                FillLayer gradientFillLayer = FillLayer.CreateInstance(FillType.Gradient);

                gradientFillLayer.DisplayName = "Vrstva s přechodem";

                image.AddLayer(gradientFillLayer);

                FillLayer patternFillLayer = FillLayer.CreateInstance(FillType.Pattern);

                patternFillLayer.DisplayName = "Vrstva s vzorem";

                patternFillLayer.Opacity = 50;

                image.AddLayer(patternFillLayer);

                image.Save(outputPsd);

            }

{{< /highlight >}}

**PSDNET-424. Podpora Zdroje Sekce Obrazovky #1009 Informace o ohraničení**

{{< highlight java >}}

             string sourceFile = "input.psd";

            string outputFile = "output.psd";

            using (var image = (PsdImage)Image.Load(sourceFile))

            {

                ResourceBlock[] imageResources = image.ImageResources;

                BorderInformationResource borderInfoResource = null;

                foreach (var imageResource in imageResources)

                {

                    if (imageResource is BorderInformationResource)

                    {

                        borderInfoResource = (BorderInformationResource)imageResource;

                        break;

                    }

                }

                // aktualizace BorderInformationResource

                borderInfoResource.Width = 0.1;

                borderInfoResource.Unit = PhysicalUnit.Inches;

                image.Save(outputFile);

            }

{{< /highlight >}}

**PSDNET-592. Podpora vrstev ve souborech formátu AI**

{{< highlight java >}}

         void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "form_8_2l3_7.ai";

        string outputFileName = "form_8_2l3_7_export";

        using (AiImage image = (AiImage)Image.Load(sourceFileName))

        {

            AiLayerSection layer0 = image.Layers[0];

            AssertIsTrue(layer0 != null, "Vrstva 0 by neměla být null.");

            AssertIsTrue(layer0.Name == "Vrstva 4", "Vlastnost Název vrstvy 0 by měla být Vrstva 4");

            AssertIsTrue(!layer0.IsTemplate, "Vlastnost IsTemplate vrstvy 0 by měla být false.");

            AssertIsTrue(layer0.IsLocked, "Vlastnost IsLocked vrstvy 0 by měla být true.");

            AssertIsTrue(layer0.IsShown, "Vlastnost IsShown vrstvy 0 by měla být true.");

            AssertIsTrue(layer0.IsPrinted, "Vlastnost IsPrinted vrstvy 0 by měla být true.");

            AssertIsTrue(!layer0.IsPreview, "Vlastnost IsPreview vrstvy 0 by měla být false.");

            AssertIsTrue(layer0.IsImagesDimmed, "Vlastnost IsImagesDimmed vrstvy 0 by měla být true.");

            AssertIsTrue(layer0.DimValue == 51, "Vlastnost DimValue vrstvy 0 by měla být 51.");

            AssertIsTrue(layer0.ColorNumber == 0, "Vlastnost CisloBarvy vrstvy 0 by měla být 0.");

            AssertIsTrue(layer0.Red == 79, "Vlastnost Red vrstvy 0 by měla být 79.");

            AssertIsTrue(layer0.Green == 128, "Vlastnost Green vrstvy 0 by měla být 