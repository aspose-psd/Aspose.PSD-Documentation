---
title: Note sulla release di Aspose.PSD per .NET 20.4
type: docs
weight: 90
url: /it/net/aspose-psd-per-net-20-4-note-sulla-release/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla release di [Aspose.PSD per .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-567|Supporto del'risorsa 'Dati di origine vettoriale'|Feature|
|PSDNET-373|Supporto dell'risorsa lclrResource (impostazione del colore del foglio)|Feature|
|PSDNET-563|Supporto delle proprietà dei dati LengthRecord (operazioni sui percorsi (operazioni booleane), indice della forma nel livello, conteggio dei record di nodi di Bezier)|Feature|
|PSDNET-425|Supporto del colore di sfondo dell'risorsa della sezione immagine n. 1010|Feature|
|PSDNET-530|Aggiunta di livelli di riempimento in tempo di esecuzione|Feature|
|PSDNET-424|Supporto dell'risorsa della sezione immagine n. 1009 con informazioni sui bordi|Feature|
|PSDNET-592|Supporto dei livelli nei file di formato AI|Feature|
|PSDNET-256|Supporto lettura e modifica dell'effetto di sovrapposizione gradiente del livello|Feature|
|PSDNET-257|Rendering dell'effetto di sovrapposizione gradiente del livello|Feature|
|PSDNET-585|I cambiamenti della proprietà BlendMode di GradientOverlayEffect non vengono visualizzati in Photoshop|Bug|
|PSDNET-561|Correzione del salvataggio dell'immagine PSD con ColorMode scala di grigi e 16 bit per canale nel formato PSD scala di grigi|Bug|
|PSDNET-560|Correzione del salvataggio dell'immagine PSD con ColorMode scala di grigi e 16 bit per canale nel formato PNG|Bug|

## **Modifiche all'API pubblica**
# **API aggiunte:**
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
# **API rimosse:**
- Nessuna

## **Esempi di utilizzo:**
**PSDNET-567. Supporto dell'risorsa 'Dati di origine vettoriale'**

{{< highlight java >}}

         // Supporto di VogkResource

        static void EsempioDiSupportoDiVogkResource()

        {

            string nomeFile = "RisorseDiOrigineVettoriale.psd";

            string nomeFileOut = "out_RisorseDiOrigineVettoriale_.psd";

            using (var psdImmagine = (PsdImmagine)Immagine.Carica(nomeFile))

            {

                var risorsa = OttieniVogkResource(psdImmagine);

                // Lettura

                if (risorsa.ShapeOriginSettings.Length != 1 ||

                    !risorsa.ShapeOriginSettings[0].IsShapeInvalidated ||

                    risorsa.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    lanciare nuovo Eccezione("VogkResource è stato letto in modo errato.");

                }

                // Modifica

                risorsa.ShapeOriginSettings = nuovo[]

                {

                    risorsa.ShapeOriginSettings[0],

                    nuovo VectorShapeOriginSettings(true, 1)

                };

                psdImmagine.Salva(nomeFileOut);

            }

        }

        static VogkResource OttieniVogkResource(PsdImmagine immagine)

        {

            var layer = immagine.Layers[1];

            VogkResource risorsa = null;

            var risorse = layer.Risorse;

            per int i = 0; i < risorse.Length; i++)

            {

                if (risorse[i] è VogkResource)

                {

                    risorsa = (VogkResource)risorse[i];

                    pausa;

                }

            }

            se (risorsa == null)

            {

                lanciare nuovo Eccezione("Risorsa Vogk non trovata.");

            }

            tornare risorsa;

        }   

{{< /highlight >}}

**PSDNET-373. Supporto dell'risorsa lclrResource (impostazione del colore del foglio)**

{{< highlight java >}}

         static void ControllaColoriFoglioEInverti(ColoriEvidenziazioneFoglio[] coloriFoglio, PsdImmagine immagine)

        {

            int numeroLivelli = immagine.Layers.Length;

            per (int indiceLivello = 0; indiceLivello < numeroLivelli; indiceLivello++)

            {

                Livello livello = immagine.Layers[indiceLivello];

                LayerResource[] risorse = livello.Risorse;

                per ogni (LayerResource risorsaLivello in risorse)

                {

                    // La risorsa lclr è sempre presente nell'elenco delle risorse dei file psd.

                    LclrResource risorsa = risorsaLivello come LclrResource;

                    se (risorsa != null)

                    {

                        se (risorsa.Color != coloriFoglio[indiceLivello])

                        {

                            lanciare nuovo Eccezione("Il colore del foglio è stato letto in modo errato");

                        }

                        // Inversione dei colori degli stili del foglio. Impostare del colore di evidenziazione del livello.

                        risorsa.Color = coloriFoglio[numeroLivelli - indiceLivello - 1];

                        pausa;

                    }

                }

            }

        }

            string percorsoFileSorgente = "TuttiIColoriRisorsaLclr.psd";

            string percorsoFileOutput = "TuttiIColoriRisorsaLclrInvertiti.psd";

            // Nel file i colori dell'evidenziazione dei livelli sono in questo ordine

            ColoriEvidenziazioneFoglio[] coloriFoglio = nuovo ColoriEvidenziazioneFoglio[] {

                ColoriEvidenziazioneFoglio.Rosso,

                ColoriEvidenziazioneFoglio.Arancione,

                ColoriEvidenziazioneFoglio.Giallo,

                ColoriEvidenziazioneFoglio.Verde,

                ColoriEvidenziazioneFoglio.Blu,

                ColoriEvidenziazioneFoglio.Viola,

                ColoriEvidenziazioneFoglio.Grizz,

                ColoriEvidenziazioneFoglio.NessunColore

            };            

            // Il colore del foglio del livello viene utilizzato per evidenziare visualmente i livelli. 

            // Ad esempio è possibile aggiornare alcuni livelli in un file PSD e poi evidenziare con un colore il livello su cui si desidera attirare l'attenzione.

            using (PsdImmagine immagine = (PsdImmagine)Immagine.Carica(percorsoFileSorgente))

            {

                ControllaColoriFoglioEInverti(coloriFoglio, immagine);

                immagine.Salva(percorsoFileOutput, nuovo PsdOpzioni());

            }

            usando (PsdImmagine immagine = (PsdImmagine)Immagine.Carica(percorsoFileOutput))

            {

                // I colori dovrebbero essere invertiti

                Array.Reverse(coloriFoglio);

                ControllaColoriFoglioEInverti(coloriFoglio, immagine);

            }

{{< /highlight >}}

**PSDNET-563. Supporto delle proprietà dei dati LengthRecord (operazioni sui percorsi (operazioni booleane), indice della forma nel livello, conteggio dei record di nodi di Bezier)**

{{< highlight java >}}

            string nomeFile = "PercorsoOperazioniForma.psd";

            using (var im = (PsdImmagine)Immagine.Carica(nomeFile))

            {

                VsmsResource risorsa = null;

                per ogni (var risorsaLivello in im.Layers[1].Risorse)

                {

                    se (risorsaLivello è VsmsResource)

                    {

                        risorsa = (VsmsResource)risorsaLivello;

                        pausa;

                    }

                }

                LengthRecord lengthRecord0 = (LengthRecord)risorsa.Paths[2];

                LengthRecord lengthRecord1 = (LengthRecord)risorsa.Paths[7];

                LengthRecord lengthRecord2 = (LengthRecord)risorsa.Paths[11];

                // Qui stiamo cambiando il modo di combinare le forme.

                lengthRecord0.PathOperations = PathOperations.ExcludeOverlappingShapes;

                lengthRecord1.PathOperations = PathOperations.IntersectShapeAreas;

                lengthRecord2.PathOperations = PathOperations.SubtractFrontShape;

                im.Salva("out_" + nomeFile);

            }

{{< /highlight >}}

**PSDNET-425. Supporto del colore di sfondo dell'risorsa della sezione immagine n. 1010**

{{< highlight java >}}

             string percorsoFileSorgente = "input.psd";

            string percorsoFileOutput = "output.psd";

            using (var immagine = (PsdImmagine)Immagine.Carica(percorsoFileSorgente))

            {

                ResourceBlock[] risorseImmagine = immagine.ImageResources;

                BackgroundColorResource risorsaColoreSfondo = null;

                per ogni (var risorsaImmagine in risorseImmagine)

                {

                    se (risorsaImmagine è BackgroundColorResource)

                    {

                        risorsaColoreSfondo = (BackgroundColorResource)risorsaImmagine;

                        pausa;

                    }

                }

                // aggiornare BackgroundColorResource

                risorsaColoreSfondo.Color = Colore.DeepRed;

                immagine.Salva(percorsoFileOutput);

            }

{{< /highlight >}}

**PSDNET-530. Aggiunta di livelli di riempimento in tempo di esecuzione**

{{< highlight java >}}

             string psdOutput = "output.psd";

            using (var immagine = new PsdImmagine(100, 100))

            {

                FillLayer coloreLivelloFill = FillLayer.CreateInstance(FillType.Color);

                coloreLivelloFill.DisplayName = "Livello di riempimento del colore";

                immagine.AddLayer(coloreLivelloFill);

                FillLayer coloLivelloGradient = FillLayer.CreateInstance(FillType.Gradient);

                coloLivelloGradient.DisplayName = "Livello di riempimento sfumato";

                immagine.AddLayer(coloLivelloGradient);

                FillLayer patternFillLayer = FillLayer.CreateInstance(FillType.Pattern);

                patternFillLayer.DisplayName = "Livello di riempimento modello";

                patternFillLayer.Opacity = 50;

                immagine.AddLayer(patternFillLayer);

                immagine.Salva(psdOutput);

            }

{{< /highlight >}}

**PSDNET-424. Supporto dell'risorsa della sezione immagine n. 1009 con informazioni sui bordi**

{{< highlight java >}}

             string percorsoFileSorgente = "input.psd";

            string percorsoFileOutput = "output.psd";

            using (var immagine = (PsdImmagine)Immagine.Carica(percorsoFileSorgente))

            {

                ResourceBlock[] risorseImmagine = immagine.ImageResources;

                BorderInformationResource risorsaInfoBordo = null;

                per ogni (var risorsaImmagine in risorseImmagine)

                {

                    se (risorsaImmagine è BorderInformationResource)

                    {

                        risorsaInfoBordo = (BorderInformationResource)risorsaImmagine;

                        pausa;

                    }

                }

                // aggiornare BorderInformationResource

                risorsaInfoBordo.Width = 0.1;

                risorsaInfoBordo.Unit = PhysicalUnit.Inches;

                immagine.Salva(percorsoFileOutput);

            }

{{< /highlight >}}

**PSDNET-592. Supporto dei livelli nei file di formato AI**

{{< highlight java >}}

         vuoto AssertIsTrue(booleano condizione, stringa messaggio)

        {

            se (!condizione)

            {

                lanciare nuovo FormatException(messaggio);

            }

        }

        string nomeFileSorgente = "form_8_2l3_7.ai";

        string nomeFileOutput = "esportazione_form_8_2l3_7";

        usando (AiImmagine immagine = (AiImmagine)Immagine.Carica(nomeFileSorgente))

        {

            AiLayerSection layer0 = immagine.Layers[0];

            AssertIsTrue(layer0 != null, "Il Livello 0 dovrebbe non essere nullo.");

            AssertIsTrue(layer0.Name == "Layer 4", "La proprietà Nome del livello 0 dovrebbe essere Layer 4");

            AssertIsTrue(!layer0.IsTemplate, "La proprietà IsTemplate del livello 0 dovrebbe essere falsa.");

           