---
title: Note sulla release di Aspose.PSD per .NET 19.12
type: docs
weight: 10
url: /it/net/aspose-psd-for-net-19-12-release-notes/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla release di [Aspose.PSD per .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-11|[Supporto del Livello Collegato](/psd/it/net/working-with-layers/#workingwithlayers-supportoflinkedlayers)|Caratteristica|
|PSDNET-131|[Supporto di SoCoResource](/psd/it/net/support-of-socoresource/)|Caratteristica|
|PSDNET-115|I linebreak vengono aggiunti ai linebreak esistenti se il TextLayer viene aggiornato con una stringa|Errore|
|PSDNET-157|Il salvataggio di PSB come PNG si blocca|Errore|
|PSDNET-250|Eccezione durante il caricamento di un file PSD CMYK senza livelli con compressione RLE|Errore|
|PSDNET-161|Eccezione durante l'aggiornamento dei livelli di testo|Errore|
|PSDNET-222|Il ridimensionamento di alcuni file PSD con maschere di livello non funziona correttamente|Errore|
|PSDNET-244|Il salvataggio di PSD con alcune impostazioni di Globalization.CultureInfo.CurrentCulture porta a eccezioni durante il caricamento|Errore|

## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **API Rimosse:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **Esempi di utilizzo:**
**PSDNET-11. Supporto del Livello Collegato**

{{< highlight java >}}

           usando (var psd = (PsdImage)Image.Load("esempio.psd"))

            {

                Layer[] layers = psd.Layers;

                // collega tutti i livelli in un unico gruppo collegato

                short layersLinkGroupId = psd.LinkedLayersManager.LinkLayers(layers);

                // ottiene l'id per un livello

                short linkGroupId = psd.LinkedLayersManager.GetLinkGroupId(layers[0]);

                se (layersLinkGroupId != linkGroupId)

                {

                    lancia una Eccezione("layersLinkGroupId e linkGroupId non sono uguali.");

                }

                // ottiene tutti i livelli collegati dall'id del gruppo collegato.

                Layer[] linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                // scollega ogni livello dal gruppo

                foreach (var linkedLayer in linkedLayers)

                {

                    psd.LinkedLayersManager.UnlinkLayer(linkedLayer);

                }

                // recupera NULL per un'id del gruppo collegato che non ha livelli nel gruppo.

                linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                se (linkedLayers != null)

                {

                    lancia una Eccezione("Il campo linkedLayers non è NULL.");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}

**PSDNET-131. Supporto di SoCoResource**

{{< highlight java >}}

      // Supporto di SoCoResource

    string nomeFileSorgente = "ColorFillLayer.psd";

    string percorsoEsportazione = "SoCoResource_Modificato.psd";

    var im = (PsdImage)Image.Load(nomeFileSorgente);

    usando (im)

    {

        per ogni var livello in im.Layers

        {

            se (livello è FillLayer)

            {

                var fillLayer = (FillLayer)livello;

                per ogni var risorsa in fillLayer.Resources

                {

                    se (risorsa è SoCoResource)

                    {

                        var socoResource = (SoCoResource)risorsa;

                        Assert.AreEqual(Color.FromArgb(63, 83, 141), socoResource.Color);

                        socoResource.Color = Color.Red;

                        interrompi;

                    }

                 }

                 interrompi;

             }

            im.Save(percorsoEsportazione);

        }

    }

{{< /highlight >}}

**PSDNET-115. I linebreak vengono aggiunti ai linebreak esistenti se il TextLayer viene aggiornato con una stringa**

{{< highlight java >}}

           const string NuovoTesto = "abcdef\rzxcvbn";

        string percorsoFileSorgente = "FileDiTestPerCaratteriAsiatici.psd");

        string percorsoFileOutput = "risultato.psd";

        usando (var immagine = (PsdImage)Image.Load(percorsoFileSorgente))

        {

            var livello = (TextLayer)immagine.Layers[0];

            var opzioniImmagine = new PsdOptions(immagine);

            livello.UpdateText(NuovoTesto);

            immagine.Save(percorsoFileOutput, opzioniImmagine);

        }

        usando (var immagineCreata = (PsdImage)Image.Load(percorsoFileOutput))

        {

            var livelloCreato = (TextLayer)immagineCreata.Layers[0];

            se (NuovoTesto != livelloCreato.Testo)

            {

                lancia una InvalidDataException("Il testo aggiornato non è valido");

            }

        }

{{< /highlight >}}

**PSDNET-157. Il salvataggio di PSB come PNG si blocca**

{{< highlight java >}}

       // Salvataggio di PSB come PNG 

    string nomeFileSorgente = "esempio.psb";

    string nomeFileUscita = "esempio.png";

    usando (PsdImage immagine = (PsdImage)Image.Load(nomeFileSorgente))

    {

        PngOptions opzioni = new PngOptions() { TipoColore = PngColorType.VeroColoreConAlfa };

        immagine.Save(nomeFileUscita, opzioni);

    }

{{< /highlight >}}



` `**PSDNET-250. Eccezione durante il caricamento di un file PSD CMYK senza layer con compressione RLE**

{{< highlight java >}}

     void CaricaDatiGrezziDaPsd()

        {

            string percorsoSorgente = "CmykConAlpha.psd";

            usando (RasterImage immagine = (RasterImage)Image.Load(percorsoSorgente))

            {

                var impostazioniDatiGrezzi = immagine.RawDataSettings;

                RawDataTester loader = new RawDataTester();

                immagine.LoadRawData(immagine.Bounds, impostazioniDatiGrezzi, loader);

            }

        }

        class RawDataTester : IPartialRawDataLoader

        {

            public void Process(Rectangle rettangolo, byte[] pixel, Point inizio, Point fine)

            {

            }

            public void Process(Rectangle rettangolo, byte[] pixel, Point inizio, Point fine, LoadOptions opzioniCaricamento)

            {

            }

        }

{{< /highlight >}}

` `**PSDNET-161. Eccezione durante l'aggiornamento dei livelli di testo**

{{< highlight java >}}

      // Carica un file PSD come immagine e convertilo in PsdImage

    usando (PsdImage immaginePsd = (PsdImage)Image.Load("esempio.psd"))

    {

        per ogni var livello in immaginePsd.Layers

        {

            se (il livello è TextLayer)

            {

                TextLayer livelloTesto = livello come TextLayer;

                livelloTesto.UpdateText("aggiornamento di testo", new Point(0, 0), 15.0f, Colore.Viola);

            }

        }

        immaginePsd.Save("AggiornaLivelloTestoInFilePSD_ou.psd");

    }

{{< /highlight >}}



**PSDNET-222. Ridimensionamento di alcuni file PSD con maschere di livello funziona in modo non corretto**

{{< highlight java >}}

     int scala = 2;

        string[] nomi = {

                             "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

                             "LevelsLayerWithLayerMaskRgb",

                             "LevelsLayerWithLayerMaskCmyk",

                             "ColorBalanceAdjustmentLayer"

                         };

        per (int i = 0; i < nomi.Length; i++)

        {

            string percorsoFileSorgente = nomi[i] + ".psd";

            string percorsoFileOutput = "output_" + percorsoFileSorgente;

            string percorsoFilePngOutput = "output_" + nomi[i] + ".png";

            var opzioniCaricamentoPsd = new PsdLoadOptions() { CaricaRisorseEffetti = true };

            usando (PsdImage immagine = (PsdImage)Image.Load(percorsoFileSorgente, opzioniCaricamentoPsd))

            {

                immagine.Ridimensiona(immagine.Larghezza * scala, immagine.Altezza * scala);

                immagine.Save(percorsoFileOutput, new PsdOptions());

                immagine.Save(percorsoFilePngOutput, new PngOptions() { TipoColore = PngColorType.VeroColoreConAlfa });

            }

        }

{{< /highlight >}}



**PSDNET-244. Il salvataggio di PSD con alcune impostazioni di Globalization.CultureInfo.CurrentCulture porta a eccezioni durante il caricamento**

{{< highlight java >}}

     per (int i = 0; i <= 6; i++)

        {

            string nomeFileSorgente = string.Format("esempio-{0}.psd", i);

            var opzioniCaricamentoPsd = new PsdLoadOptions() { CaricaRisorseEffetti = true };

            var opzioniSalvataggioPsd = new PsdOptions();

            var cultura = new System.Globalization.CultureInfo("ru-RU");

            System.Threading.Thread.CurrentThread.CurrentCulture = cultura;

            System.Threading.Thread.CurrentThread.CurrentUICulture = cultura;

            string nomeFileUscita = "output-" + nomeFileSorgente;

            // Carica un file PSD come immagine e convertilo in PsdImage

            usando (PsdImage immagine = (PsdImage)Image.Load(nomeFileSorgente, opzioniCaricamentoPsd))

            {

                immagine.Ridimensiona(160, 120);

                immagine.Save(nomeFileUscita, opzioniSalvataggioPsd);

            }

            cultura = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = cultura;

            System.Threading.Thread.CurrentThread.CurrentUICulture = cultura;

            // Carica un file PSD come immagine e convertilo in PsdImage

            usando (PsdImage immagine2 = (PsdImage)Image.Load(nomeFileSorgente, opzioniCaricamentoPsd))

            {

                immagine2.Ridimensiona(160, 120);

                immagine2.Save(nomeFileUscita, opzioniSalvataggioPsd);

            }

        }

{{< /highlight >}}



