---
title: Aspose.PSD für .NET 20.4 - Versionshinweise
type: docs
weight: 90
url: /de/net/aspose-psd-für-net-20-4-versionshinweise/
---

{{% alert color="primary" %}} 

Diese Seite enthält die Versionshinweise für [Aspose.PSD für .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-567|Unterstützung des weiteren Elements 'Vektor-Erzeugungsdaten'|Feature|
|PSDNET-373|Unterstützung von lclrResource (Farbeinstellung des Blattes)|Feature|
|PSDNET-563|Unterstützung von Eigenschaften aus LengthRecord-Daten. (Pfadoperationen (boolesche Operationen), Index der Form in der Ebene, Anzahl der Bezier-Knoten)|Feature|
|PSDNET-425|Unterstützung der Hintergrundfarbe des Bildabschnittsressourcen #1010|Feature|
|PSDNET-530|Hinzufügen von Füllschichten zur Laufzeit|Feature|
|PSDNET-424|Unterstützung von Bildabschnittsressource #1009 Border-Informationen|Feature|
|PSDNET-592|Unterstützung von Ebenen in AI-Formatdateien|Feature|
|PSDNET-256|Unterstützung des Lesens und Bearbeitens des Überlagerungsschichteffekts auf dem Gradienten|Feature|
|PSDNET-257|Rendering des Überlagerungsschichteffekts auf dem Gradienten|Feature|
|PSDNET-585|Änderungen an der Eigenschaft BlendMode der GradientOverlayEffect werden in Photoshop nicht angezeigt|Bug|
|PSDNET-561|Beheben des Speicherns von PSD-Bildern mit Graustufen-Farbraum und 16 Bit pro Kanal im Graustufen-PSD-Format|Bug|
|PSDNET-560|Beheben des Speicherns von PSD-Bildern mit Graustufen-Farbraum und 16 Bit pro Kanal im PNG-Format|Bug|

## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
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
# **Entfernte APIs:**
- Keine

## **Beispiele zur Verwendung:**
**PSDNET-567. Unterstützung des weiteren Elements 'Vektor-Erzeugungsdaten'**

{{< highlight java >}}

         // VogkResource Support

        static void BeispielFürVogkResourceSupport()

        {

            string dateiName = "VectorOriginationDataResource.psd";

            string ausgabeDateiName = "out_VectorOriginationDataResource_.psd";

            using (var psdBild = (PsdImage)Image.Load(dateiName))

            {

                var resource = GetVogkResource(psdBild);

                // Lesen

                if (resource.ShapeOriginSettings.Length != 1 ||

                    !resource.ShapeOriginSettings[0].IsShapeInvalidated ||

                    resource.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    throw new Exception("VogkResource wurde falsch gelesen.");

                }

                // Bearbeiten

                resource.ShapeOriginSettings = new[]

                {

                    resource.ShapeOriginSettings[0],

                    new VectorShapeOriginSettings(true, 1)

                };

                psdBild.Save(ausgabeDateiName);

            }

        }

        static VogkResource GetVogkResource(PsdImage bild)

        {

            var ebene = bild.Layers[1];

            VogkResource resource = null;

            var ressourcen = ebene.Resources;

            for (int i = 0; i < ressourcen.Length; i++)

            {

                if (ressourcen[i] is VogkResource)

                {

                    resource = (VogkResource)ressourcen[i];

                    break;

                }

            }

            if (resource == null)

            {

                throw new Exception("VogkResource nicht gefunden.");

            }

            return resource;

        }   

{{< /highlight >}}

**PSDNET-373. Unterstützung von lclrResource (Farbeinstellung des Blattes)**

{{< highlight java >}}

         static void ÜberprüfeBlattfarbenUndUmkehr(SheetColorHighlightEnum[] blattFarben, PsdImage img)

        {

            int ebenenAnzahl = img.Layers.Length;

            for (int ebenenIndex = 0; ebenenIndex < ebenenAnzahl; ebenenIndex++)

            {

                Layer ebene = img.Layers[ebenenIndex];

                LayerResource[] ressourcen = ebene.Resources;

                foreach (LayerResource ebenenRessource in ressourcen)

                {

                    // Die lcrl-Ressource ist immer in der psd-Datei-Ressourcenliste vorhanden.

                    LclrResource resource = ebenenRessource as LclrResource;

                    if (resource != null)

                    {

                        if (resource.Color != blattFarben[ebenenIndex])

                        {

                            throw new Exception("Blattfarbe wurde falsch gelesen");

                        }

                        // Umkehrung der Styleblattfarben. Einstellen der Farbmarkierung der Ebene.

                        resource.Color = blattFarben[ebenenAnzahl - ebenenenIndex - 1];

                        break;

                    }

                }

            }

        }

            string quelleDateiPfad = "AlleLclrResourceFarben.psd";

            string ausgabeDateiPfad = "AlleLclrResourceFarbenUmgekehrt.psd";

            // In der Datei sind die Farben der Ebenenmarkierung in dieser Reihenfolge

            SheetColorHighlightEnum[] blattFarben = new SheetColorHighlightEnum[] {

                SheetColorHighlightEnum.Red,

                SheetColorHighlightEnum.Orange,

                SheetColorHighlightEnum.Yellow,

                SheetColorHighlightEnum.Green,

                SheetColorHighlightEnum.Blue,

                SheetColorHighlightEnum.Violet,

                SheetColorHighlightEnum.Gray,

                SheetColorHighlightEnum.NoColor

            };            

            // Farbmarkierung der Ebene wird verwendet, um Ebenen visuell hervorzuheben. 

            // Sie können beispielsweise einige Ebenen in der PSD aktualisieren und dann die Ebene durch Farbe markieren, um die Aufmerksamkeit darauf zu lenken.

            using (PsdImage img = (PsdImage)Image.Load(quelleDateiPfad))

            {

                ÜberprüfeBlattfarbenUndUmkehr(blattFarben, img);

                img.Save(ausgabeDateiPfad, new PsdOptions());

            }

            using (PsdImage img = (PsdImage)Image.Load(ausgabeDateiPfad))

            {

                // Farben sollten umgekehrt sein

                Array.Reverse(blattFarben);

                ÜberprüfeBlattfarbenUndUmkehr(blattFarben, img);

            }

{{< /highlight >}}

**PSDNET-563. Unterstützung von Eigenschaften aus LengthRecord-Daten. (Pfadoperationen (boolesche Operationen), Index der Form in der Ebene, Anzahl der Bezier-Knoten)**

{{< highlight java >}}

            string dateiName = "PathOperationsShape.psd";

            using (var im = (PsdImage)Image.Load(dateiName))

            {

                VsmsResource resource = null;

                foreach (var ebenenRessource in im.Layers[1].Resources)

                {

                    if (ebenenRessource is VsmsResource)

                    {

                        resource = (VsmsResource)ebenenRessource;

                        break;

                    }

                }

                LengthRecord lengthRecord0 = (LengthRecord)resource.Paths[2];

                LengthRecord lengthRecord1 = (LengthRecord)resource.Paths[7];

                LengthRecord lengthRecord2 = (LengthRecord)resource.Paths[11];

                // Hier ändern wir die Art der Kombination zwischen Formen.

                lengthRecord0.PathOperations = PathOperations.ExcludeOverlappingShapes;

                lengthRecord1.PathOperations = PathOperations.IntersectShapeAreas;

                lengthRecord2.PathOperations = PathOperations.SubtractFrontShape;

                im.Save("out_" + dateiName);

            }

{{< /highlight >}}

**PSDNET-425. Unterstützung der Hintergrundfarbe des Bildabschnittsressourcen #1010**

{{< highlight java >}}

             string quelleDatei = "Eingabe.psd";

            string ausgabeDatei = "Ausgabe.psd";

            using (var bild = (PsdImage)Image.Load(quelleDatei))

            {

                ResourceBlock[] bildRessourcen = bild.ImageResources;

                BackgroundColorResource hintergrundfarbenRessource = null;

                foreach (var bildRessource in bildRessourcen)

                {

                    if (bildRessource is BackgroundColorResource)

                    {

                        hintergrundfarbenRessource = (BackgroundColorResource)bildRessource;

                        break;

                    }

                }

                // Aktualisieren der HintergrundfarbenRessource

                hintergrundfarbenRessource .Color = Color.DarkRed;

                bild.Save(ausgabeDatei);

            }

{{< /highlight >}}

**PSDNET-530. Hinzufügen von Füllschichten zur Laufzeit**

{{< highlight java >}}

             string ausgabePsd = "Ausgabe.psd";

            using (var bild = new PsdImage(100, 100))

            {

                FillLayer farbFüllschicht = FillLayer.CreateInstance(FillType.Color);

                farbFüllschicht.DisplayName = "Farbfüllschicht";

                bild.AddLayer(farbFüllschicht);

                FillLayer gradientFüllschicht = FillLayer.CreateInstance(FillType.Gradient);

                gradientFüllschicht.DisplayName = "Gradientenfüllschicht";

                bild.AddLayer(gradientFüllschicht);

                FillLayer musterFüllschicht = FillLayer.CreateInstance(FillType.Pattern);

                musterFüllschicht.DisplayName = "Musterfüllschicht";

                musterFüllschicht.Opacity = 50;

                bild.AddLayer(musterFüllschicht);

                bild.Save(ausgabePsd);

            }

{{< /highlight >}}

**PSDNET-424. Unterstützung der Bildabschnittsressource #1009 Border-Informationen**

{{< highlight java >}}

             string quelleDatei = "Eingabe.psd";

            string ausgabeDatei = "Ausgabe.psd";

            using (var bild = (PsdImage)Image.Load(quelleDatei))

            {

                ResourceBlock[] bildRessourcen = bild.ImageResources;

                BorderInformationResource rahmenInfoRessource = null;

                foreach (var bildRessource in bildRessourcen)

                {

                    if (bildRessource is BorderInformationResource)

                    {

                        rahmenInfoRessource = (BorderInformationResource)bildRessource;

                        break;

                    }

                }

                // Aktualisieren der BorderInformationResource

                rahmenInfoRessource.Width = 0.1;

                rahmenInfoRessource.Unit = PhysicalUnit.Inches;

                bild.Save(ausgabeDatei);

            }

{{< /highlight >}}

**PSDNET-592. Unterstützung von Ebenen in AI-Formatdateien**

{{< highlight java >}}

         void AssertIsTrue(bool bedingung, string nachricht)

        {

            if (!bedingung)

            {

                throw new FormatException(nachricht);

            }

        }

        string quelleDateiName = "form_8_2l3_7.ai";

        string ausgabeDateiName = "form_8_2l3_7_export";

        using (AiImage bild = (AiImage)Image.Load(quelleDateiName))

        {

            AiLayerSection ebene0 = bild.Layers[0];

            AssertIsTrue(ebene0 != null, "Ebene 0 sollte nicht null sein.");

            AssertIsTrue(ebene0.Name == "Ebene 4", "Der Name der Ebene 0 sollte Ebene 4 sein");

            AssertIsTrue(!ebene0.IsTemplate, "Die IsTemplate-Eigenschaft der Ebene 0 sollte falsch sein.");

            AssertIsTrue(ebene0.IsLocked, "Die IsLocked-Eigenschaft der Ebene 0 sollte wahr sein.");

            AssertIsTrue(ebene0.IsShown, "Die IsShown-Eigenschaft der Ebene 0 sollte wahr sein.");

            AssertIsTrue(ebene0.IsPrinted, "Die IsPrinted-Eigenschaft der Ebene 0 sollte wahr sein.");

            AssertIsTrue(!ebene0.IsPreview, "Die IsPreview-Eigenschaft der Ebene 0 sollte falsch sein.");

            AssertIsTrue(ebene0.IsImagesDimmed, "Die IsImagesDimmed-Eigenschaft der Ebene 0 sollte wahr sein.");

            AssertIsTrue(ebene0.DimValue == 51, "Die DimValue-Eigenschaft der Ebene 0 sollte 51 sein.");

            AssertIsTrue(ebene0.ColorNumber == 0, "Die ColorNumber-Eigenschaft der Ebene 0 sollte 0 sein.");

            AssertIsTrue(ebene0.Red == 79, "Die Red-Eigenschaft der Ebene 0 sollte