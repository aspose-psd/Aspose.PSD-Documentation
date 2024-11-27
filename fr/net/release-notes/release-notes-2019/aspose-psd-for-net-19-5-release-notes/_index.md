---
title: Aspose.PSD pour .NET 19.5 - Notes de version
type: docs
weight: 80
url: /fr/net/aspose-psd-pour-net-19-5-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour Aspose.PSD pour .NET 19.5

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-133|Ajouter le support des calques de remplissage : Motif|Fonctionnalité|
|PSDNET-138|Support de PtFlResource|Fonctionnalité|
|PSDNET-129|Mise en œuvre correcte de la méthode de recadrage pour les fichiers PSD|Fonctionnalité|
|PSDNET-140|Support de VsmsResource|Fonctionnalité|
|PSDNET-121|Les calques visibles dans un sous-dossier visible dans un dossier invisible sont rendus, mais ne devraient pas l'être|Bogue|
|PSDNET-119|PSD (mode RGB 16 bits par canal) n'est pas correctement converti en JPG|Bogue|

## **Modifications de l'API publique**
# **APIs ajoutées :**
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Linked
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PointType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternId
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternHeight
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternHeight
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.#ctor(System.String,System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Offset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.IsLinkedWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PatternId
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.TypeToolKey
- M:Aspose.PSD.Image.DoAfterCreate(System.Int64@,System.Int64)
- P:Aspose.PSD.ImageOptionsBase.BufferSizeHint
- M:Aspose.PSD.Metered.GetConsumptionCredit
# **APIs supprimées :**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)

## **Exemples d'utilisation :**
**PSDNET-133. Ajouter le support des calques de remplissage : Motif**

{{< highlight java >}}

 // Ajouter le support des calques de remplissage : Motif

    string nomFichierSource = "CalqueDeRemplissageDeMotif.psd";

    string cheminExport = "CalqueDeRemplissageDeMotif_Modifié.psd";

    double tolérance = 0,0001;

    var im = (PsdImage)Image.Load(nomFichierSource);

    using (im)

    {

         foreach (var calque in im.Layers)

         {

             if (calque is FillLayer)

             {

                  FillLayer calqueRemplissage = (FillLayer)calque;

                  PatternFillSettings paramètresRemplissage = (PatternFillSettings)calqueRemplissage.FillSettings;

                  if (paramètresRemplissage.HorizontalOffset != -46 || 

                      paramètresRemplissage.VerticalOffset != -45 || 

                      paramètresRemplissage.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5"||

                      paramètresRemplissage.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares" ||

                      paramètresRemplissage.AlignWithLayer != true ||

                      paramètresRemplissage.Linked != true ||

                      paramètresRemplissage.PatternHeight != 64 ||

                      paramètresRemplissage.PatternWidth != 64 ||

                      paramètresRemplissage.PatternData.Length != 4096 ||

                      Math.Abs(paramètresRemplissage.Scale - 50) > tolérance) 

                      {

                          throw new Exception("L'image PSD a été lue incorrectement");

                      }

                  // Modification 

                  paramètresRemplissage.Scale = 300;

                  paramètresRemplissage.HorizontalOffset = 2;

                  paramètresRemplissage.VerticalOffset = -20;

                  paramètresRemplissage.PatternData = new int[]

                  {

                       Color.Red.ToArgb(), Color.Blue.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Red.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Blue.ToArgb(),  Color.Red.ToArgb()

                  };

                  paramètresRemplissage.PatternHeight = 3;

                  paramètresRemplissage.PatternWidth = 3;

                  paramètresRemplissage.AlignWithLayer = false;

                  paramètresRemplissage.Linked = false;

                  paramètresRemplissage.PatternId = Guid.NewGuid().ToString();

                  calqueRemplissage.Update();

                  break;

             }

         }

         im.Save(cheminExport);

    }

{{< /highlight >}}

**PSDNET-138. Support de PtFlResource**

{{< highlight java >}}

  // Support de PtFlResource

    string nomFichierSource = "CalqueDeRemplissageDeMotif.psd";

    string cheminExport = "PtFlResource_Modifié.psd";

    double tolérance = 0,0001;

    var im = (PsdImage)Image.Load(nomFichierSource);

    using (im)

    {

         foreach (var calque in im.Layers)

         {

             if (calque is FillLayer)

             {

                var calqueRemplissage = (FillLayer)calque;

                var ressources = calqueRemplissage.Resources;

                foreach (var res in ressources)

                {

                    if (res is PtFlResource)

                    {

                        // Lecture

                        PtFlResource ressource = (PtFlResource)res;

                        if (

                            ressource.Offset.X != -46 || 

                            ressource.Offset.Y != -45 || 

                            ressource.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5\0" ||

                            ressource.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares\0" ||

                            ressource.AlignWithLayer != true ||

                            ressource.IsLinkedWithLayer != true ||

                            !(Math.Abs(ressource.Scale - 50) < tolérance)) {

                                throw new Exception("La ressource PtFl a été lue incorrectement");

                            }

                        // Modification

                        ressource.Offset = new Point(-11, 13);

                        ressource.Scale = 200;

                        ressource.AlignWithLayer = false;

                        ressource.IsLinkedWithLayer = false;

                        calqueRemplissage.Resources = calqueRemplissage.Resources;

                        // Nous n'avons pas de données de motif dans PattResource, nous pouvons donc l'ajouter.

                        var paramètresRemplissage = (PatternFillSettings)calqueRemplissage.FillSettings;

                        paramètresRemplissage.PatternData = new int[]

                        {

                            Color.Black.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                        };

                        paramètresRemplissage.PatternHeight = 1;

                        paramètresRemplissage.PatternWidth = 4;

                        paramètresRemplissage.PatternName = "$$$/Presets/Patterns/VerticalLine=Vertical Line New\0";

                        paramètresRemplissage.PatternId = Guid.NewGuid().ToString() + "\0";

                        calqueRemplissage.Update();

                    }

                    break;

                }

                break;

            }

         }

         im.Save(cheminExport);

    } 

{{< /highlight >}}

**PSDNET-129. Implémenter une méthode de recadrage correcte pour les fichiers PSD**

{{< highlight java >}}

             // Implémenter une méthode de recadrage correcte pour les fichiers PSD.

            string nomFichierSource = "1.psd";

            string cheminExportPsd = "TestRogner.psd";

            string cheminExportPng = "TestRogner.png";

            using (RasterImage image = Image.Load(nomFichierSource) as RasterImage)

            {

                image.Crop(new Rectangle(10, 30, 100, 100));

                image.Save(cheminExportPsd, new PsdOptions());

                image.Save(cheminExportPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-140. Support de VsmsResource**

{{< highlight java >}}

 // Support de VsmsResource

        static void ExempleDeSupportDeVsmsResource()

        {

            string nomFichierSource = "RectangleVide.psd";

            string cheminExport = "RectangleVide_modifié.psd";

            var im = (PsdImage)Image.Load(nomFichierSource);

            using (im)

            {

                var ressource = GetVsmsResource(im);

                // Lecture

                if (ressource.IsDisabled != false ||

                    ressource.IsInverted != false ||

                    ressource.IsNotLinked != false ||

                    ressource.Paths.Length != 7 ||

                    ressource.Paths[0].Type != VectorPathType.PathFillRuleRecord ||

                    ressource.Paths[1].Type != VectorPathType.InitialFillRuleRecord ||

                    ressource.Paths[2].Type != VectorPathType.ClosedSubpathLengthRecord ||

                    ressource.Paths[3].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    ressource.Paths[4].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    ressource.Paths[5].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked||

                    ressource.Paths[6].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked)

                {

                        throw new Exception("VsmsResource a été lu incorrectement");

                }

                var pathFillRule = (PathFillRuleRecord)ressource.Paths[0];

                var initialFillRule = (InitialFillRuleRecord)ressource.Paths[1];

                var subpathLength = (LengthRecord)ressource.Paths[2];

                // La règle de remplissage de chemin ne contient aucune information supplémentaire

                if (pathFillRule.Type != VectorPathType.PathFillRuleRecord || 

                initialFillRule.Type != VectorPathType.InitialFillRuleRecord ||

                initialFillRule.IsFillStartsWithAllPixels != false ||

                subpathLength.Type != VectorPathType.ClosedSubpathLengthRecord ||

                subpathLength.IsClosed != true ||

                subpathLength.IsOpen != false) 

                {

                    throw new Exception("Les chemins de VsmsResource ont été lus incorrectement");

                }

                // Modification

                ressource.IsDisabled = true;

                ressource.IsInverted = true;

                ressource.IsNotLinked = true;

                var bezierKnot = (BezierKnotRecord)ressource.Paths[3];

                bezierKnot.Points[0] = new Point(0, 0);

                bezierKnot = (BezierKnotRecord)ressource.Paths[4];

                bezierKnot.Points[0] = new Point(8039798, 10905191);

                initialFillRule.IsFillStartsWithAllPixels = true;

                subpathLength.IsClosed = false;

                im.Save(cheminExport);

            }         

        }

        static VsmsResource GetVsmsResource(PsdImage image)

        {

            var calque = image.Layers[1];

            VsmsResource ressource = null;

            var ressources = calque.Resources;

            for (int i = 0; i < ressources.Length; i++)

            {

                if (ressources[i] is VsmsResource)

                {

                    ressource = (VsmsResource)ressources[i];

                    break;

                }

            }

            if (ressource == null)

            {

                throw new Exception("VsmsResource non trouvé");

            }

            return ressource;

        }   

{{< /highlight >}}

**PSDNET-121: Les calques visibles dans un sous-dossier visible dans un dossier invisible sont rendus, mais ne devraient pas**

{{< highlight java >}}