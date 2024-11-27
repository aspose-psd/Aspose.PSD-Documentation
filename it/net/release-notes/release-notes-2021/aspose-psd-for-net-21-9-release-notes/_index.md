---
title: Note sulla versione di Aspose.PSD per .NET 21.9
type: docs
weight: 40
url: /it/net/aspose-psd-per-net-21-9-note-sulla-versione/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-574|Rendere la compressione RLE predefinita per il salvataggio PSD per evitare un output PSD enorme|Funzionalità|
|PSDNET-747|Supporto degli Effetti di Sovrapposizione del Modello di Colore Multicanale nel file PSD|Funzionalità|
|PSDNET-951|Dopo la creazione di un nuovo livello, la sua proprietà Risorse è nulla e impedisce le manipolazioni (ad esempio, il Ridimensionamento)|Errore|
|PSDNET-955|Non supportato dei metodi di compressione ZipWithPrediction per 8 bit|Errore|

## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**
- Nessuna

# **API Rimosse:**
- Nessuna 

## **Esempi di utilizzo:**

**PSDNET-574. Rendere la compressione RLE predefinita per il salvataggio PSD per evitare un output PSD enorme**

{{< highlight csharp >}}
            string inputFilePath = "file.psd";
            string output1 = "output_originale.psd";
            string output2 = "output_psdOpzioni.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(output1);
                image.Save(output2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. Supporto degli Effetti di Sovrapposizione del Modello di Colore Multicanale nel file PSD**

{{< highlight csharp >}}
            var fileName = "TuttiGliEffetti.psd";
            var outputFile = "TuttiGliEffetti_out.psd";
            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // Non dovrebbe generare un'eccezione
            using (var im = Image.Load(fileName, loadOptions))
            {
                // Non dovrebbe generare un'eccezione
                im.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-951. Dopo la creazione di un nuovo livello, la sua proprietà Risorse è nulla e impedisce le manipolazioni (ad esempio, il Ridimensionamento)**

{{< highlight csharp >}}
            string PSDFile = "Livello1.psd";
            string fileLivello1 = "Livello2.png";
            string fileLivello2 = "Livello3.png";
            string nomeFileFinale = "outputfinale.psd";

            void SostituisciColore(RasterImage image, Color vecchioColore, int diff, Color nuovoColore)
            {
                var pixel = image.LoadArgb32Pixels(image.Bounds);
                var lunghezza = pixel.Length;

                var vecchioR = vecchioColore.R;
                var vecchioG = vecchioColore.G;
                var vecchioB = vecchioColore.B;
                var nuovoValoreColore = nuovoColore.ToArgb();

                for (int i = 0; i < lunghezza; i++)
                {
                    // Rosso
                    var r = (byte)((pixel[i] >> 16) & 0xff);
                    // Verde
                    var g = (byte)((pixel[i] >> 8) & 0xff);
                    // Blu
                    var b = (byte)(pixel[i] & 0xff);

                    int diffAttuale = Math.Abs(r - vecchioR) + Math.Abs(g - vecchioG) + Math.Abs(b - vecchioB);

                    if (diffAttuale <= diff)
                    {
                        pixel[i] = nuovoValoreColore;
                    }
                }

                image.SaveArgb32Pixels(image.Bounds, pixel);
            }

            Layer Livello2 = null;
            Layer Livello3 = null;
            using (PsdImage image = (PsdImage)Image.Load(PSDFile))
            {
                #region Aggiunta Livello 1

                using (var stream = new FileStream(fileLivello1, FileMode.Open))
                {
                    Livello2 = new Layer(stream);

                    Livello2.Resize(image.Width, image.Height);
                    var larghezza = Livello2.Width;
                    var altezza = Livello2.Height;

                    Livello2.Sinistra = 675;
                    Livello2.Su = 0;

                    Livello2.Destra = Livello2.Sinistra + larghezza;
                    Livello2.Sotto = Livello2.Su + altezza;

                    image.AggiungiLivello(Livello2);
                }

                #endregion

                using (var stream = new FileStream(fileLivello2, FileMode.Open))
                {
                    Livello3 = new Layer(stream);
                    // Sostituzione del colore Bianco con Trasparente
                    SostituisciColore(Livello3, Color.Bianco, 256, Color.Transparent);
                    Livello2.DisegnaImmagine(new Point(0, 0), Livello3);
                }

                image.Save(nomeFileFinale, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. Non supportato dei metodi di compressione ZipWithPrediction per 8 bit**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";
            string outputZip8 = "out_Zip8bit.psd";
            string outputZip16 = "out_Zip16bit.psd";

            using (PsdImage image = (PsdImage)Image.Load(inputFilePath))
            {
                image.Save(outputZip8, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 8 });
                image.Save(outputZip16, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 16 });
            }
{{< /highlight >}}
