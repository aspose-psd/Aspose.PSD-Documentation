---
title: Note sulla versione di rilascio di Aspose.PSD per .NET 19.5
type: docs
weight: 80
url: /it/net/aspose-psd-for-net-19-5-release-notes/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla versione di Aspose.PSD per .NET 19.5

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-133|Aggiunta del supporto ai livelli di riempimento: Pattern|Funzionalità|
|PSDNET-138|Supporto di PtFlResource|Funzionalità|
|PSDNET-129|Implementare il corretto metodo di ritaglio per i file PSD|Funzionalità|
|PSDNET-140|Supporto di VsmsResource|Funzionalità|
|PSDNET-121|I livelli visibili in una sotto-cartella visibile in una cartella invisibile vengono renderizzati, ma non dovrebbero|Bug|
|PSDNET-119|Il file PSD (modalità RGB a 16 bit per canale) non viene convertito correttamente in JPG|Bug|

## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**
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
# **API Rimosse:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)

## **Esempi di utilizzo:**
**PSDNET-133. Aggiunta del supporto ai livelli di riempimento: Pattern**

{{< highlight it >}}

 // Aggiunta del supporto ai livelli di riempimento: Pattern

    string nomeFileSorgente = "PatternFillLayer.psd";

    string percorsoEsportazione = "PatternFillLayer_Modificato.psd";

    double tolleranza = 0.0001;

    var im = (PsdImage)Image.Load(nomeFileSorgente);

    using (im)

    {

         foreach (var layer in im.Layers)

         {

             if (layer is FillLayer)

             {

                  FillLayer fillLayer = (FillLayer)layer;

                  PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;

                  if (fillSettings.HorizontalOffset != -46 || 

                      fillSettings.VerticalOffset != -45 || 

                      fillSettings.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5"||

                      fillSettings.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares" ||

                      fillSettings.AlignWithLayer != true ||

                      fillSettings.Linked != true ||

                      fillSettings.PatternHeight != 64 ||

                      fillSettings.PatternWidth != 64 ||

                      fillSettings.PatternData.Length != 4096 ||

                      Math.Abs(fillSettings.Scale - 50) > tolleranza) 

                      {

                          throw new Exception("L'immagine PSD è stata letta in modo errato");

                      }

                  // Modifica 

                  fillSettings.Scale = 300;

                  fillSettings.HorizontalOffset = 2;

                  fillSettings.VerticalOffset = -20;

                  fillSettings.PatternData = new int[]

                  {

                       Color.Red.ToArgb(), Color.Blue.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Red.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Blue.ToArgb(),  Color.Red.ToArgb()

                  };

                  fillSettings.PatternHeight = 3;

                  fillSettings.PatternWidth = 3;

                  fillSettings.AlignWithLayer = false;

                  fillSettings.Linked = false;

                  fillSettings.PatternId = Guid.NewGuid().ToString();

                  fillLayer.Update();

                  break;

             }

         }

         im.Save(percorsoEsportazione);

    }

{{< /highlight >}}

**PSDNET-138. Supporto di PtFlResource**

{{< highlight it >}}

  // Supporto di PtFlResource

    string nomeFileSorgente = "PatternFillLayer.psd";

    string percorsoEsportazione = "PtFlResource_Modificato.psd";

    double tolleranza = 0.0001;

    var im = (PsdImage)Image.Load(nomeFileSorgente);

    using (im)

    {

         foreach (var layer in im.Layers)

         {

             if (layer is FillLayer)

             {

                var fillLayer = (FillLayer)layer;

                var resources = fillLayer.Resources;

                foreach (var res in resources)

                {

                    if (res is PtFlResource)

                    {

                        // Lettura

                        PtFlResource resource = (PtFlResource)res;

                        if (

                            resource.Offset.X != -46 || 

                            resource.Offset.Y != -45 || 

                            resource.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5\0" ||

                            resource.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares\0" ||

                            resource.AlignWithLayer != true ||

                            resource.IsLinkedWithLayer != true ||

                            !(Math.Abs(resource.Scale - 50) < tolleranza)) {

                                throw new Exception("La risorsa PtFl è stata letta in modo errato");

                            }

                        // Modifica

                        resource.Offset = new Point(-11, 13);

                        resource.Scale = 200;

                        resource.AlignWithLayer = false;

                        resource.IsLinkedWithLayer = false;

                        fillLayer.Resources = fillLayer.Resources;

                        // Non abbiamo dati pattern in PattResource, quindi possiamo aggiungerli.

                        var fillSettings = (PatternFillSettings)fillLayer.FillSettings;

                        fillSettings.PatternData = new int[]

                        {

                            Color.Black.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                        };

                        fillSettings.PatternHeight = 1;

                        fillSettings.PatternWidth = 4;

                        fillSettings.PatternName = "$$$/Presets/Patterns/VerticalLine=Vertical Line New\0";

                        fillSettings.PatternId = Guid.NewGuid().ToString() + "\0";

                        fillLayer.Update();

                    }

                    break;

                }

                break;

            }

         }

         im.Save(percorsoEsportazione);

    } 

{{< /highlight >}}

**PSDNET-129. Implementare il corretto metodo di ritaglio per i file PSD**

{{< highlight it >}}

   // Implementare il corretto metodo di ritaglio per i file PSD.

            string nomeFileSorgente = "1.psd";

            string percorsoEsportazionePsd = "TestRitaglio.psd";

            string percorsoEsportazionePng = "TestRitaglio.png";

            using (RasterImage immagine = Image.Load(nomeFileSorgente) as RasterImage)

            {

                immagine.Crop(new Rectangle(10, 30, 100, 100));

                immagine.Save(percorsoEsportazionePsd, new PsdOptions());

                immagine.Save(percorsoEsportazionePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-140. Supporto di VsmsResource**

{{< highlight it >}}

 // Supporto di VsmsResource

        static void EsempioSupportoVsmsResource()

        {

            string nomeFileSorgente = "RettangoloVuoto.psd";

            string percorsoEsportazione = "RettangoloVuoto_modificato.psd";

            var im = (PsdImage)Image.Load(nomeFileSorgente);

            using (im)

            {

                var resource = GetVsmsResource(im);

                // Lettura

                if (resource.IsDisabled != false ||

                    resource.IsInverted != false ||

                    resource.IsNotLinked != false ||

                    resource.Paths.Length != 7 ||

                    resource.Paths[0].Type != VectorPathType.PathFillRuleRecord ||

                    resource.Paths[1].Type != VectorPathType.InitialFillRuleRecord ||

                    resource.Paths[2].Type != VectorPathType.ClosedSubpathLengthRecord ||

                    resource.Paths[3].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    resource.Paths[4].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    resource.Paths[5].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked||

                    resource.Paths[6].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked)

                {

                        throw new Exception("La risorsa Vsms è stata letta in modo errato");

                }

                var pathFillRule = (PathFillRuleRecord)resource.Paths[0];

                var initialFillRule = (InitialFillRuleRecord)resource.Paths[1];

                var subpathLength = (LengthRecord)resource.Paths[2];

                // La regola di riempimento del percorso non contiene informazioni aggiuntive

                if (pathFillRule.Type != VectorPathType.PathFillRuleRecord || 

                initialFillRule.Type != VectorPathType.InitialFillRuleRecord ||

                initialFillRule.IsFillStartsWithAllPixels != false ||

                subpathLength.Type != VectorPathType.ClosedSubpathLengthRecord ||

                subpathLength.IsClosed != true ||

                subpathLength.IsOpen != false) 

                {

                    throw new Exception("I percorsi della risorsa Vsms sono stati letti in modo errato");

                }

                // Modifica

                resource.IsDisabled = true;

                resource.IsInverted = true;

                resource.IsNotLinked = true;

                var bezierKnot = (BezierKnotRecord)resource.Paths[3];

                bezierKnot.Points[0] = new Point(0, 0);

                bezierKnot = (BezierKnotRecord)resource.Paths[4];

                bezierKnot.Points[0] = new Point(8039798, 10905191);

                initialFillRule.IsFillStartsWithAllPixels = true;

                subpathLength.IsClosed = false;

                im.Save(percorsoEsportazione);

            }         

        }

        static VsmsResource GetVsmsResource(PsdImage immagine)

        {

            var layer = immagine.Layers[1];

            VsmsResource resource = null;

            var resources = layer.Resources;

            for (int i = 0; i < resources.Length; i++)

            {

                if (resources[i] is VsmsResource)

                {

                    resource = (VsmsResource)resources[i];

                    break;

                }

            }

            if (resource == null)

            {

                throw new Exception("Risorsa Vsms non trovata");

            }

            return resource;

        }   

{{< /highlight >}}



**PSDNET-121: I livelli visibili in una sotto-cartella visibile in una cartella invisibile vengono renderizzati, ma non dovrebbero**

{{< highlight it >}}

 // I livelli visibili in una sotto-cartella visibile in una cartella invisibile vengono renderizzati, ma non dovrebbero

            string nomeFileSorgente = "MoltaSottocartelle.psd.psd";

            string percorsoFileUscitaJpg = "uscitaMoltaSottocartelle.jpg";

            string percorsoFileUscitaPsd = "uscitaMoltaSottocartelle.psd";

            var opzioni = new PsdLoadOptions();

            using (PsdImage immagine = (PsdImage)Image.Load(nomeFileSorgente, opzioni))

            {

                immagine.Save(percorsoFileUscitaPsd, new PsdOptions(immagine));

                immagine.Save(percorsoFileUscitaJpg, new JpegOptions() { Quality = 100 });

            }

{{< /highlight >}}



**PSDNET-119. Il file PSD (modalità RGB a 16 bit per canale) non viene convertito correttamente in JPG**

{{< highlight it >}}

  // Il file PSD non viene convertito correttamente in jpg

            string nomeFileSorgente = "in.psd";

            string percorsoEsportazione = "outRgb.jpg";

            var opzioni = new PsdLoadOptions();

            using (PsdImage immagine = (PsdImage)Image.Load(nomeFileSorgente, opzioni))

            {

                immagine.Save(percorsoEsportazione, new JpegOptions() { Quality = 100 });

            }

{{< /highlight >}}