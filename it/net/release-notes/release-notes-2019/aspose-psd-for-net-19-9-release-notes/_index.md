---
title: Note sulla versione di Aspose.PSD per .NET 19.9
type: docs
weight: 40
url: /it/net/aspose-psd-per-net-19-9-note-sulla-versione/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-160|Nome del layer estratto in modo errato|Feature|
|PSDNET-175|Ottenere le proprietà del testo da una diversa porzione di testo all'interno di TextLayer PSD|Feature|
|PSDNET-190|Supporto per Aggiungi gruppo di layer|Feature|
|PSDNET-192|Supporto della proprietà Scala per il layer di riempimento gradiente|Feature|
|PSDNET-162|Regolazione della luminosità|Potenziamento|
|PSDNET-174|IndexOutOfRangeException durante il salvataggio dell'immagine PSD come JPEG|Bug|
|PSDNET-180|L'aggiornamento del testo del layer di testo genera un'eccezione|Bug|
|PSDNET-182|Il salvataggio dell'immagine PSD dopo l'operazione RotateFlip produce un file danneggiato che non può essere aperto|Bug|

## **Modifiche nell'API pubblica**
# **API Aggiunte:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.AddLayerGroup(System.String,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.IText
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Text
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortion
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.AddPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.InsertPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.RemovePortion(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.UpdateLayerData
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Justification
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.FirstLineIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.StartIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EndIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceBefore
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceAfter
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoHyphenate
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.HyphenatedWordSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PreHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PostHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.ConsecutiveHyphens
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Zone
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.WordSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LetterSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.GlyphSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LeadingType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Hanging
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Burasagari
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.KinsokuOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EveryLineComposer
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Text
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Paragraph
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Leading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Tracking
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Kerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StrokeColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HindiNumbers
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TextData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Scale
# **API Rimosse:**
- Nessuna

## **Esempi di utilizzo:**
**PSDNET-160. Nome del layer errato estratto**

Per visualizzare correttamente il nome del layer, utilizzare la proprietà **DisplayName**. Ora è stata aggiunta un'impostazione per questa proprietà e la proprietà può essere modificata. Quando Photoshop salva il nome del layer utilizzando la proprietà Nome, i caratteri coreani vengono memorizzati come byte 63'?' in ASCII. Usare la proprietà **DisplayName** perché la proprietà Nome non supporta i caratteri coreani.

{{< highlight java >}}

             // apporta modifiche ai nomi dei layer e salva

            using (var image = (PsdImage)Image.Load("layers with names.psd"))

            {

                for (int i = 0; i < image.Layers.Length; i++)

                {

                    var layer = image.Layers[i];

                    // imposta il nuovo valore nella proprietà DisplayName

                    layer.DisplayName += "_changed";

                }

                image.Save("output.psd");

            }

{{< /highlight >}}

**PSDNET-175. Ottenere le proprietà del testo da una diversa porzione di testo all'interno di TextLayer PSD**

{{< highlight java >}}

            const double Tolleranza = 0.0001;

            var percorsoFile = "ParagrafiTreColori.psd";

            var percorsoOutput = "TreColoriParagrafo_out.psd";

            using (var im = (PsdImage)Image.Load(percorsoFile))

            {

                for (int i = 0; i < im.Layers.Length; i++)

                {

                    var layer = im.Layers[i] as TextLayer;

                    if (layer != null)

                    {

                        var porzioni = layer.TextData.Items;

                        if (porzioni.Length != 4)

                        {

                            throw new Exception();

                        }

                        // Verifica del testo di ogni porzione

                        if (porzioni[0].Text != "Vecchio " ||

                            porzioni[1].Text != "colore" ||

                            porzioni[2].Text != " testo\r" ||

                            porzioni[3].Text != "Secondo paragrafo\r")

                        {

                            throw new Exception();

                        }

                        // Verifica dei dati dei paragrafi

                        // I paragrafi hanno diverse giustificazioni

                        if (

                            porzioni[0].Paragraph.Justification != 0 ||

                            porzioni[1].Paragraph.Justification != 0 ||

                            porzioni[2].Paragraph.Justification != 0 ||

                            porzioni[3].Paragraph.Justification != 2)

                        {

                            throw new Exception();

                        }

                        // Tutte le altre proprietà del primo e del secondo paragrafo sono uguali

                        for (int j = 0; j < porzioni.Length; j++)

                        {

                            var paragrafo = porzioni[j].Paragraph;

                            if (Math.Abs(paragrafo.AutoLeading - 1.2) > Tolleranza ||

                                paragrafo.AutoHyphenate != false ||

                                paragrafo.Burasagari != false ||

                                paragrafo.ConsecutiveHyphens != 8 ||

                                Math.Abs(paragrafo.StartIndent) > Tolleranza ||

                                Math.Abs(paragrafo.EndIndent) > Tolleranza ||

                                paragrafo.EveryLineComposer != false ||

                                Math.Abs(paragrafo.FirstLineIndent) > Tolleranza ||

                                paragrafo.GlyphSpacing.Length != 3 ||

                                Math.Abs(paragrafo.GlyphSpacing[0] - 1) > Tolleranza ||

                                Math.Abs(paragrafo.GlyphSpacing[1] - 1) > Tolleranza ||

                                Math.Abs(paragrafo.GlyphSpacing[2] - 1) > Tolleranza ||

                                paragrafo.Hanging != false ||

                                paragrafo.HyphenatedWordSize != 6 ||

                                paragrafo.KinsokuOrder != 0 ||

                                paragrafo.LetterSpacing.Length != 3 ||

                                Math.Abs(paragrafo.LetterSpacing[0]) > Tolleranza ||

                                Math.Abs(paragrafo.LetterSpacing[1]) > Tolleranza ||

                                Math.Abs(paragrafo.LetterSpacing[2]) > Tolleranza ||

                                paragrafo.LeadingType != LeadingMode.Auto ||

                                paragrafo.PreHyphen != 2 ||

                                paragrafo.PostHyphen != 2 ||

                                Math.Abs(paragrafo.SpaceBefore) > Tolleranza ||

                                Math.Abs(paragrafo.SpaceAfter) > Tolleranza ||

                                paragrafo.WordSpacing.Length != 3 ||

                                Math.Abs(paragrafo.WordSpacing[0] - 0.8) > Tolleranza ||

                                Math.Abs(paragrafo.WordSpacing[1] - 1.0) > Tolleranza ||

                                Math.Abs(paragrafo.WordSpacing[2] - 1.33) > Tolleranza ||

                                Math.Abs(paragrafo.Zone - 36.0) > Tolleranza)

                            {

                                throw new Exception();

                            }

                        }

                        // Verifica dei dati di stile

                        // Gli stili hanno colori e dimensioni del font diversi

                        if (Math.Abs(porzioni[0].Style.FontSize - 12) > Tolleranza ||

                            Math.Abs(porzioni[1].Style.FontSize - 12) > Tolleranza ||

                            Math.Abs(porzioni[2].Style.FontSize - 12) > Tolleranza ||

                            Math.Abs(porzioni[3].Style.FontSize - 10) > Tolleranza)

                        {

                            throw new Exception();

                        }

                        if (porzioni[0].Style.FillColor != Color.FromArgb(255, 145, 0, 0) ||

                            porzioni[1].Style.FillColor != Color.FromArgb(255, 201, 128, 2) ||

                            porzioni[2].Style.FillColor != Color.FromArgb(255, 18, 143, 4) ||

                            porzioni[3].Style.FillColor != Color.FromArgb(255, 145, 42, 100))

                        {

                            throw new Exception();

                        }

                        for (int j = 0; j < porzioni.Length; j++)

                        {

                            var stile = porzioni[j].Style;

                            if (stile.AutoLeading != false ||

                                stile.HindiNumbers != false ||

                                stile.Kerning != 0 ||

                                stile.Leading != 0 ||

                                stile.StrokeColor != Color.FromArgb(255, 175, 90, 163) ||

                                stile.Tracking != 50)

                            {

                                throw new Exception();

                            }

                        }

                        // Esempio di modifica del testo

                        porzioni[0].Text = "Ciao ";

                        porzioni[1].Text = "Mondo";

                        // Esempio di rimozione di porzioni di testo

                        layer.TextData.RemovePortion(3);

                        layer.TextData.RemovePortion(2);

                        // Esempio di aggiunta di una nuova porzione di testo

                        var porzioneCreata = layer.TextData.ProducePortion();

                        porzioneCreata.Text = "!!!\r";

                        layer.TextData.AddPortion(porzioneCreata);

                        porzioni = layer.TextData.Items;

                        // Esempio di modifica del paragrafo e dello stile per le porzioni

                        // Imposta la giustificazione corretta

                        porzioni[0].Paragraph.Justification = 1;

                        porzioni[1].Paragraph.Justification = 1;

                        porzioni[2].Paragraph.Justification = 1;

                        // Colori diversi per ogni stile. Saranno modificati, ma il rendering non è completamente supportato

                        porzioni[0].Style.FillColor = Color.Acquamarina;

                        porzioni[1].Style.FillColor = Color.Viola;

                        porzioni[2].Style.FillColor = Color.AzzurroChiaro;

                        // Diverso font. Saranno modificati, ma il rendering non è completamente supportato

                        porzioni[0].Style.FontSize = 6;

                        porzioni[1].Style.FontSize = 8;

                        porzioni[2].Style.FontSize = 10;

                        layer.TextData.UpdateLayerData();

                        im.Save(percorsoOutput, new PsdOptions(im));

                        break;

                    }

                }

            }

{{< /highlight >}}

**PSDNET-190. Supporto per Aggiungi gruppo di layer**

{{< highlight java >}}

             // -Gruppo 1

            // --Layer 1

            // --Gruppo 2

            // ---Layer 2

            // ---Layer 3

            // --Layer 4

            string cartellaDati = "psdnet190_test.psd";

            var opzioniCreazione = new PsdOptions();

            opzioniCreazione.Source = new FileCreateSource(cartellaDati, false);

            opzioniCreazione.Palette = new PsdColorPalette(new Color[] { Color.Green });

            using (var immaginePsd = (PsdImage)Image.Create(opzioniCreazione, 500, 500))

            {

                LayerGroup gruppo1 = immaginePsd.AddLayerGroup("Gruppo 1", 0, true);

                Layer layer1 = new Layer(immaginePsd);

                layer1.Name = "Layer 1";

                gruppo1.AddLayer(layer1);

                LayerGroup gruppo2 = gruppo1.AddLayerGroup("Gruppo 2", 1);

                Layer layer2 = new Layer(immaginePsd);

                layer2.Name = "Layer 2";

                gruppo2.AddLayer(layer2);

                Layer layer3 = new Layer(immaginePsd);

                layer3.Name = "Layer 3";

                gruppo2.AddLayer(layer3);

                Layer layer4 = new Layer(immaginePsd);

                layer4.Name = "Layer 4";

                gruppo1.AddLayer(layer4);

                immaginePsd.Save();

            }

{{< /highlight >}}

**PSDNET-192. Supporto della proprietà Scala per il layer di riempimento gradiente**

{{< highlight java >}}

            using (var immagine = (PsdImage)Image.Load("FillLayerGradient.psd"))

            {

                // ottenere un layer di riempimento

                FillLayer layerRiempimento = null;

                foreach (var layer in immagine.Layers)

                {

                    layerRiempimento = layer as FillLayer;

                    if (layerRiempimento != null)

                    {

                        break;

                    }

                }

                var impostazioni = layerRiempimento.FillSettings as IGradientFillSettings;

                // aggiorna il valore della scala

                impostazioni.Scale = 200;

                layerRiempimento.Update(); // Aggiorna i dati dei pixel

                immagine.Save("immagineScala.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-174. IndexOutOfRangeException durante il salvataggio dell'immagine PSD come JPEG**

{{< highlight java >}}

         using (var immagine = Aspose.PSD.Image.Load("SamplePSD.psd"))

        {

            immagine.Save("sampleJPG.jpg", new JpegOptions());

        }

{{< /highlight >}}

**PSDNET-180. L'aggiornamento del testo del layer di testo genera un'eccezione**

{{< highlight java >}}

           // L'aggiornamento