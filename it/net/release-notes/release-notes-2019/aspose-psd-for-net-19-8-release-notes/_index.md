---
title: Note sulla versione di Aspose.PSD per .NET 19.8
type: docs
weight: 50
url: /it/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di Aspose.PSD per .NET 19.8

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-184|Carica file immagine JPEG, PNG e altri in PsdImage da stream|Funzionalità|
|PSDNET-134|Implementa il rendering dello strato di riempimento: Gradiente|Funzionalità|
|PSDNET-166|Il salvataggio di PSD in PDF non fornisce testo selezionabile|Funzionalità|
|PSDNET-158|Supporto per il salvataggio di PSB in PDF|Funzionalità|
|PSDNET-189|Utilizzo elevato della memoria durante il caricamento di PSD in modalità di sola lettura|Potenziamento|
|PSDNET-171|Dopo la creazione di un nuovo TextLayer, il file PSD diventa illeggibile per PS|Bug|
|PSDNET-156|Eccezione durante il caricamento di PSD|Bug|

## **Cambiamenti nell'API pubblica**
# **API aggiunte:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **API rimosse:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Esempi di utilizzo:**
**PSDNET-184. Carica file immagine JPEG, PNG e altri in PsdImage da stream**

{{< highlight java >}}

    // Carica file immagine JPEG, PNG e altri in PsdImage da stream

    string percorsoFileOutput = "RisultatoPsd.psd";

    var elencoFile = new string[]

    {

        "EsempioPsd.psd",

        "EsempioBmp.bmp",

        "EsempioGif.gif",

        "EsempioJpeg2000.jpf",

        "EsempioJpeg.jpg",

        "EsempioPng.png",

        "EsempioTiff.tif",

    };

    using (var immagine = new PsdImage(200, 200))

    {

        foreach (var nomeFile in elencoFile)

        {

            string percorsoFile = nomeFile;

            using (var stream = new FileStream(percorsoFile, FileMode.Open))

            {

                Layer strato = null;

                try

                {

                     strato = new Layer(stream);

                     immagine.AddLayer(strato);

                }

                catch (Exception e)

                {

                    if (strato != null)

                    {

                        strato.Dispose();

                    }

                    throw e;

                }

            }

        }

        immagine.Save(percorsoFileOutput);

    }

{{< /highlight >}}

**PSDNET-134. Implementa il rendering dello strato di riempimento: Gradiente**

{{< highlight java >}}

             // Implementa il rendering dello strato di riempimento: Gradiente

            string nomeFile = "StratoRiempimentoGradiente.psd";

            GradientType[] tipiGradiente = new[]

            {

                GradientType.Lineare, GradientType.Radiale, GradientType.Angolare, GradientType.Riflesso, GradientType.Diamante

            };

            using (var immagine = Image.Load(nomeFile))

            {

                PsdImage psdImmagine = (PsdImage)immagine;

                FillLayer stratoRiempimento = (FillLayer)psdImmagine.Layers[0];

                GradientFillSettings impostazioniRiempimento = (GradientFillSettings)stratoRiempimento.FillSettings;

                foreach (var tipoGradiente in tipiGradiente)

                {

                    impostazioniRiempimento.GradientType = tipoGradiente;

                    stratoRiempimento.Update();

                    psdImmagine.Save(nomeFile + "_" + tipoGradiente.ToString() + ".png", new PngOptions() { TipoColore = PngColorType.VeroColoreConAlfa });

                }

            }

{{< /highlight >}}

**PSDNET-166. Il salvataggio di PSD in PDF non fornisce testo selezionabile**

{{< highlight java >}}

  // Il salvataggio di PSD in PDF non fornisce testo selezionabile

    string nomeFileSorgente = "testo.psd";

    using (PsdImage immagine = (PsdImage)Image.Load(nomeFileSorgente))

    {

        string nomeFileOutput = "testo.pdf";

        immagine.Save(nomeFileOutput, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. Dopo la creazione di un nuovo TextLayer, il file PSD diventa illeggibile per PS**

{{< highlight java >}}

 // Dopo la creazione di un nuovo TextLayer su Server di compilazione, il file PSD diventa illeggibile per PS

    string nomeFileSorgente = "UnSoloStrato.psd";

    string nomeFileOutput = "UnSoloStratoConTestoAggiunto.psd";

    using (PsdImage immagine = (PsdImage)Image.Load(nomeFileSorgente))

    {

        immagine.AddTextLayer("Un po' di testo", new Rectangle(50, 50, 100, 100));

        PsdOptions opzioni = new PsdOptions(immagine);

        immagine.Save(nomeFileOutput, opzioni);

    }

{{< /highlight >}}



**PSDNET-156. Eccezione durante il caricamento di PSD**

{{< highlight java >}}

 using (var immagine = Image.Load("copia_isolata.psd"))

{

}

{{< /highlight >}}


**PSDNET-189. Utilizzo elevato della memoria durante il caricamento di PSD in modalità di sola lettura**

{{< highlight java >}}

 // Utilizzo elevato della memoria con Aspose.PSD durante il caricamento di PSD in modalità di sola lettura

            string nomeFileSorgente = "TestoIn3D_Bianco.psd";

            string nomeFileOutput = "Esportato.png";

            LoadOptions opzioniCaricamento = new PsdLoadOptions() { ModalitàSolaLettura = true };

            ImageOptionsBase opzioniSalvataggio = new PngOptions() { TipoColore = PngColorType.VeroColoreConAlfa };

            using (PsdImage immagine = (PsdImage)Image.Load(nomeFileSorgente))

            {

                immagine.Save(nomeFileOutput, opzioniSalvataggio);

            }

            double memoriaUtilizzata = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // L'utilizzo della memoria deve essere inferiore a 100 MB per questi esempi

            if (memoriaUtilizzata > 100)

            {

                throw new Exception("L'utilizzo della memoria è troppo elevato");

            }

{{< /highlight >}}


**PSDNET-158. Supporto per il salvataggio di PSB in PDF**

{{< highlight java >}}

 // Supporto per il salvataggio di PSB in PDF

    string nomeFileSorgente = "esempio.psb";

    using (PsdImage immagine = (PsdImage)Image.Load(nomeFileSorgente))

    {

        string nomeFileOutput = "esempio.pdf";

        immagine.Save(nomeFileOutput, new PdfOptions());

    }

{{< /highlight >}}
