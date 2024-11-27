---
title: Note sulla release di Aspose.PSD per .NET 21.3
type: docs
weight: 100
url: /it/net/aspose-psd-per-net-21-3-note-sulla-release/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla release di [Aspose.PSD per .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-823|Aggiunta la SectionDividerLayer per migliorare l'esperienza con i gruppi di livelli|Miglioramento|
|PSDNET-694|Quando si legge PattResource, larghezza e altezza vengono invertite|Errore|
|PSDNET-789|Sfumatura scorretta di più di un effetto di livello|Errore|
|PSDNET-805|Ordine e logica di sfumatura errati quando ci sono più di un effetto di livello|Errore|
|PSDNET-842|Le proprietà dell'effetto di contorno non vengono salvate nel file PSD|Errore|

## **Cambiamenti nell'API pubblica**
# **API aggiunte:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **API rimosse:**
- Nessuna

## **Esempi di utilizzo:**

**PSDNET-694. Quando si legge PattResource, larghezza e altezza vengono invertite**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // invoca il rendering del modello

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Sfumatura scorretta di più di un effetto di livello**

{{< highlight csharp >}}
            string srcFile = "source_789.psd";
            string outputSmartObjectPath = "output789.png";
            string outputFile = "output789.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)

                                {
                                    // Alla ricerca di un livello di testo
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "Migliore";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // In questo modo salviamo il file PSD modificato
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. Ordine e logica di sfumatura errati quando ci sono più di un effetto di livello**

{{< highlight csharp >}}
            string sourceFile = "1_200x200.psd";
            string contentFile = "Numbers1Best.png";

            string outputFilePng = "output.png";
            string outputFilePsd = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(contentFile);
                        break;
                    }
                }

                // In questo modo salviamo il file PSD modificato
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. Aggiunta la SectionDividerLayer per migliorare l'esperienza con i gruppi di livelli**

{{< highlight csharp >}}
            // Il seguente codice dimostra i livelli di SectionDividerLayer e come ottenere il LayerGroup ad esso relativo.

            // Gerarchia dei livelli
            //    [0]: '</Layer group>' SectionDividerLayer per il Gruppo 1
            //    [1]: 'Livello 1' Livello regolare
            //    [2]: '</Layer group>' SectionDividerLayer per il Gruppo 2
            //    [3]: '</Layer group>' SectionDividerLayer per il Gruppo 3
            //    [4]: 'Gruppo 3' GroupLayer
            //    [5]: 'Gruppo 2' GroupLayer
            //    [6]: 'Gruppo 1' GroupLayer

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Gli oggetti non sono uguali.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // Creazione della gerarchia dei livelli
                // Aggiungi il LayerGroup 'Gruppo 1'
                LayerGroup group1 = image.AddLayerGroup("Gruppo 1", 0, true);
                // Aggiungi livello regolare
                Layer layer1 = new Layer();
                layer1.DisplayName = "Livello 1";
                group1.AddLayer(layer1);
                // Aggiungi il LayerGroup 'Gruppo 2'
                LayerGroup group2 = group1.AddLayerGroup("Gruppo 2", 1);
                // Aggiungi il LayerGroup 'Gruppo 3'
                LayerGroup group3 = group2.AddLayerGroup("Gruppo 3", 0);

                // Ottieni i SectionDividerLayer
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // utilizzando il metodo SectionDividerLayer.GetRelatedLayerGroup(), ottieni l'istanza del LayerGroup correlato
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // lo stesso LayerGroup
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // lo stesso LayerGroup
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // lo stesso LayerGroup

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Gruppo 1' contiene 5 livelli
            }
{{< /highlight >}}

**PSDNET-842. Le proprietà dell'effetto di contorno non vengono salvate nel file PSD**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Gli oggetti non sono uguali.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // Non solleverà ArgumentNullException

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // Verifica i valori salvati
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}
