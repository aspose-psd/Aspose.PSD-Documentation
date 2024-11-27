---
title: Note sulla versione di Aspose.PSD per .NET 21.8
type: docs
weight: 50
url: /it/net/aspose-psd-for-net-21-8-note-sulla-versione/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-698|Supporto dei metodi di compressione ZipWithPrediction|Feature|
|PSDNET-663|Lo spaziatura del testo è incorretta nel PSD generato|Bug|
|PSDNET-685|Eccezione durante il salvataggio di PSD|Bug|
|PSDNET-927|Distanza incorretta tra righe e simboli in Aspose.PSD quando non lo utilizziamo con una licenza|Bug|

## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**
- Nessuna

# **API Rimosse:**
- Nessuna

## **Esempi di utilizzo:**

**PSDNET-663. Lo spaziatura del testo è incorretta nel PSD generato**

{{< highlight csharp >}}
            string nomeFileSorgente = "sorgente.psd";
            string nomeFileOutput = "output.png";

            using (PsdImage immagine = (PsdImage)Image.Load(nomeFileSorgente))
            {
                immagine.Save(nomeFileOutput, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. Eccezione durante il salvataggio di PSD**

{{< highlight csharp >}}
            string nomeFileSorgente = "File.psd";
            string nomeFileOutput = "File2.psd";

            using (PsdImage immagine = (PsdImage)Image.Load(nomeFileSorgente))
            {
                var layer1 = (TextLayer)immagine.Layers[1];
                layer1.TextData.UpdateLayerData();

                immagine.Save(nomeFileOutput);
            }
{{< /highlight >}}

**PSDNET-698. Supporto dei metodi di compressione ZipWithPrediction**

{{< highlight csharp >}}
            string percorsoFileInput = "zipTest698.psd";

            string outputPng = "output.png";
            string outputRaw = "out_Raw.psd";
            string outputZip = "out_Zip.psd";

            using (Image immagine = Image.Load(percorsoFileInput))
            {
                immagine.Save(outputPng, new PngOptions());

                immagine.Save(outputRaw, new PsdOptions() { CompressionMethod = CompressionMethod.Raw });
                immagine.Save(outputZip, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. Distanza incorretta tra righe e simboli in Aspose.PSD quando non lo utilizziamo con una licenza**

{{< highlight csharp >}}
            bool[] statiLicenza = new bool[] { false, true };
            for (int i = 0; i < statiLicenza.Length; i++)
            {
                bool testLicenza = statiLicenza[i];
                if (testLicenza)
                {
                    License licenza = new License();
                    licenza.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string fileSorgente = "psdnetTest927.psd";
                string fileOutput = "out_" + testLicenza.ToString() + "_psdnetTest927.png";

                using (var immagine = (PsdImage)Image.Load(fileSorgente))
                {
                    immagine.Save(fileOutput, new PngOptions());
                }
            }
{{< /highlight >}}
