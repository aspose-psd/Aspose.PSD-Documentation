---
title: Note sulla versione di Aspose.PSD per .NET 21.1
type: docs
weight: 120
url: /it/net/aspose-psd-per-net-21-1-note-sulla-versione/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Eccezione durante il tentativo di convertire un file psd particolare in png|Bug|
|PSDNET-792|Eccezione nel salvataggio di PSD con oggetto intelligente in PNG|Bug|

## **Modifiche all'API pubblica**
# **API aggiunte:**
- Nessuna

# **API rimosse:**
- Nessuna

## **Esempi di utilizzo:**
**PSDNET-766. Aspose.PSD 20.10: Eccezione durante il tentativo di convertire un file psd particolare in png**
{{< highlight csharp >}}
            const string cartellaBase = "PSDNET766_1\\";
            const string cartellaOutput = cartellaBase + "output\\";
            string percorsoFileSorgente = cartellaBase + "school-admission-flyer-template-05052019.psd";
            string percorsoFileOutput = cartellaOutput + "chool-admission-flyer-template-05052019_output.psd";
            string percorsoFilePngOutput = Path.ChangeExtension(percorsoFileOutput, ".png");
            PsdLoadOptions opzioni = new PsdLoadOptions();
            using (PsdImage immagine = (PsdImage)Image.Load(percorsoFileSorgente, opzioni))
            {
                immagine.Save(percorsoFileOutput, new PsdOptions(immagine));
                immagine.Save(percorsoFilePngOutput, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. Eccezione nel salvataggio di PSD con oggetto intelligente in PNG**
{{< highlight csharp >}}
            const string cartellaBase = "PSDNET792_1\\";
            const string cartellaOutput = cartellaBase + "output\\";
            string percorsoFileSorgente = cartellaBase + "1.psd";
            string percorsoFileOutput = cartellaOutput + "1_output.psd";
            string percorsoFilePngOutput = Path.ChangeExtension(percorsoFileOutput, ".png");
            PsdLoadOptions opzioni = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage immagine = (PsdImage)Image.Load(percorsoFileSorgente, opzioni))
            {
                var lunghezza = immagine.Layers.Length;
                for (int i = 0; i < lunghezza; i++)
                {
                    // Ricerca di Oggetto Intelligente
                    var smart = immagine.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // Stiamo caricando il Livello di Oggetto Intelligente da MemoryStream,
                        // Ma possiamo usare smart.ExportContents(somePath) per esportare l'oggetto intelligente su un file
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var immagineInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < immagineInSmart.Layers.Length; j++)
                                {
                                    // Ricerca di Livello Testo
                                    var textLayer = immagineInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // Possiamo usare un semplice UpdateText, ma in questo modo otteniamo la possibilità di modificare il testo per porzioni
                                        // Creare livelli di testo multiriga e altre funzionalità di formattazione del testo e del paragrafo
                                        // Si prega di fare attenzione. Se i contenuti dell'oggetto intelligente non sono PSD, non è possibile utilizzare questo metodo di modifica del testo
                                        // In questo caso, è necessario utilizzare l'API Grafica: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "Migliore";

                                        // Dovresti cambiare la dimensione del testo se vuoi che l'immagine sia visualizzata correttamente.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // È meglio usare ReplaceContents. Rirappresenterà automaticamente l'Oggetto Intelligente
                                smart.ReplaceContents(immagineInSmart);
                            }
                        }
                    }
                }

                // In questo modo stiamo salvando il file PSD modificato
                immagine.Save(percorsoFileOutput, new PsdOptions(immagine));
                immagine.Save(percorsoFilePngOutput, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
