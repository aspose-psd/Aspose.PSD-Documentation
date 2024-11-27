---
title: Note sulla versione di Aspose.PSD per .NET 19.11
type: docs
weight: 20
url: /it/net/aspose-psd-for-net-19-11-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 19.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-151|[Supporto dell'Effetto ombra interna in un Livello](/it/psd/net/effetti-ombra-in-photoshop/#shadoweffectsinphotoshop-innershadoweffect)|Funzionalità|
|PSDNET-135|[Implementazione della resa di un Livello di Riempimento: Pattern](/it/psd/net/supporto-dei-livelli-di-riempimento/#supportoffilllayers-filllayerswithpatternfill)|Funzionalità|
|PSDNET-187|[Supporto delle Immagini raster nei File in Formato AI](/it/psd/net/manipolazione-dei-formati-adobe-illustrator/#manipolazioneformatiadobeillustrator-immaginirasterinillustrator)|Funzionalità|
|PSDNET-225|[Ottenere proprietà della formattazione inline di un Livello di testo](/it/psd/net/lavorare-con-i-livelli-di-testo/#lavorareconlivelliditesto-ottenereproprietàdeltestodautestuale)|Funzionalità|
|PSDNET-214|Esportazione non corretta di un file PSD in altri formati se contiene Effetti del Livello e Livelli di Regolazione|Errore|

## **Modifiche nell'API Pubblica**
# **API Aggiunte:**
- T:Aspose.PSD.FileFormats.Ai.AiSezione
- M:Aspose.PSD.FileFormats.Ai.AiSezione.GetData
- P:Aspose.PSD.FileFormats.Ai.AiImmagine.Livelli
- M:Aspose.PSD.FileFormats.Ai.AiImmagine.AggiungiLivello(Aspose.PSD.FileFormats.Ai.AiSezioneLivello)
- T:Aspose.PSD.FileFormats.Ai.AiSezioneLivello
- P:Aspose.PSD.FileFormats.Ai.AiSezioneLivello.ImmaginiRaster
- M:Aspose.PSD.FileFormats.Ai.AiSezioneLivello.AggiungiImmagineRaster(Aspose.PSD.FileFormats.Ai.AiSezioneImmagineRaster)
- T:Aspose.PSD.FileFormats.Ai.AiSezioneImmagineRaster
- P:Aspose.PSD.FileFormats.Ai.AiSezioneImmagineRaster.Nome
- P:Aspose.PSD.FileFormats.Ai.AiSezioneImmagineRaster.Pixel
- P:Aspose.PSD.FileFormats.Ai.AiSezioneImmagineRaster.RettangoloImmagine
- P:Aspose.PSD.FileFormats.Ai.AiSezioneImmagineRaster.OffsetX
- P:Aspose.PSD.FileFormats.Ai.AiSezioneImmagineRaster.OffsetY
- P:Aspose.PSD.FileFormats.Ai.AiSezioneImmagineRaster.Larghezza
- P:Aspose.PSD.FileFormats.Ai.AiSezioneImmagineRaster.Angle
- P:Aspose.PSD.FileFormats.Ai.AiSezioneImmagineRaster.SpostamentoInferioreSinistro
- P:Aspose.PSD.FileFormats.Ai.AiSezioneImmagineRaster.Altezza
- M:Aspose.PSD.FileFormats.Psd.Livelli.EffettiLivello.BlendingOptions.AggiungiOmbraInterna
- T:Aspose.PSD.FileFormats.Psd.Livelli.EffettiLivello.EffettoOmbraInterna
- P:Aspose.PSD.FileFormats.Psd.Livelli.EffettiLivello.EffettoOmbraInterna.Colore
- P:Aspose.PSD.FileFormats.Psd.Livelli.EffettiLivello.EffettoOmbraInterna.ModoMiscelazione
- P:Aspose.PSD.FileFormats.Psd.Livelli.EffettiLivello.EffettoOmbraInterna.Visibile
- P:Aspose.PSD.FileFormats.Psd.Livelli.EffettiLivello.EffettoOmbraInterna.Opacità
- P:Aspose.PSD.FileFormats.Psd.Livelli.EffettiLivello.EffettoOmbraInterna.Angolo
- P:Aspose.PSD.FileFormats.Psd.Livelli.EffettiLivello.EffettoOmbraInterna.UsaLuceGlobal
- P:Aspose.PSD.FileFormats.Psd.Livelli.EffettiLivello.EffettoOmbraInterna.Distanza
- P:Aspose.PSD.FileFormats.Psd.Livelli.EffettiLivello.EffettoOmbraInterna.Diffusione
- P:Aspose.PSD.FileFormats.Psd.Livelli.EffettiLivello.EffettoOmbraInterna.Dimensioen
- P:Aspose.PSD.FileFormats.Psd.Livelli.EffettiLivello.EffettoOmbraInterna.Rumore
- T:Aspose.PSD.FileFormats.Psd.Livelli.Effetti.IShadowEffect
- P:Aspose.PSD.FileFormats.Psd.Livelli.Effetti.IShadowEffect.Colore
- P:Aspose.PSD.FileFormats.Psd.Livelli.Effetti.IShadowEffect.Angolo
- P:Aspose.PSD.FileFormats.Psd.Livelli.Effetti.IShadowEffect.UsaLuceGlobal
- P:Aspose.PSD.FileFormats.Psd.Livelli.Effetti.IShadowEffect.Distanza
- P:Aspose.PSD.FileFormats.Psd.Livelli.Effetti.IShadowEffect.Diffusione
- P:Aspose.PSD.FileFormats.Psd.Livelli.Effetti.IShadowEffect.Dimensioen
- P:Aspose.PSD.FileFormats.Psd.Livelli.Effetti.IShadowEffect.Rumore
- M:Aspose.PSD.FileFormats.Psd.Livelli.Testo.GetFonts
- P:Aspose.PSD.FileFormats.Psd.Livelli.Testo.ITextStyle.FontIndex
- T:Aspose.PSD.FileFormats.Psd.Livelli.Testo.TextFontInfo
- P:Aspose.PSD.FileFormats.Psd.Livelli.Testo.TextFontInfo.FormatoFont
- P:Aspose.PSD.FileFormats.Psd.Livelli.Testo.TextFontInfo.Scrittura
- P:Aspose.PSD.FileFormats.Psd.Livelli.Testo.TextFontInfo.Sintetico
- P:Aspose.PSD.FileFormats.Psd.Livelli.Testo.TextFontInfo.NomePostScript
- P:Aspose.PSD.FileFormats.Psd.Livelli.Testo.TextFontInfo.NomeFamiglia
- P:Aspose.PSD.FileFormats.Psd.Livelli.Testo.TextFontInfo.Stile
# **API Rimosse:**
- M:Aspose.PSD.FileFormats.Ai.SezioneFinaleAi.GetData
- M:Aspose.PSD.FileFormats.Ai.SezioneImpostazioni.GetData

## **Esempi di utilizzo:**
**PSDNET-151. Supporto dell'Effetto ombra interna in un Livello**

{{< highlight java >}}

            string nomeFile = "esempio.psd";

            string nomeDestinazione = "esempio_out.psd";

            var opzioniCaricamento = new OpzioniCaricamentoPsd()

            {

                CaricaRisorseEffetti = true

            };

            // Carica un'immagine esistente in un'istanza della classe PsdImage

            using (var immagine = (PsdImage)Image.Load(nomeFile, opzioniCaricamento))

            {

                var livello = immagine.Livelli[immagine.Livelli.Length - 1];

                var effettoOmbra = (IShadowEffect)livello.BlendingOptions.Effetti[0];

                effettoOmbra.Colore = Color.Verde;

                effettoOmbra.Opacità = 128;

                effettoOmbra.Distanza = 1;

                effettoOmbra.UsaLuceGlobal = false;

                effettoOmbra.Dimensione = 2;

                effettoOmbra.Angolo = 45;

                effettoOmbra.Diffusione = 50;

                effettoOmbra.Rumore = 5;

                immagine.Save(nomeDestinazione, new OpzioniPsd(immagine));

            }

{{< /highlight >}}

**PSDNET-135. Implementazione della resa di un Livello di Riempimento: Pattern**

{{< highlight java >}}

            string nomeFile = "esempio.psd";
            string nomeDestinazione = "esempio_out.psd";
            // Carica un'immagine esistente in un'istanza della classe PsdImage

            using (var immagine = (PsdImage)Image.Load(nomeFile))

            {

                foreach (var livello in immagine.Livelli)

                {

                    if (livello is FillLayer)

                    {

                        var livelloRiempimento = (FillLayer)livello;

                        var impostazioni = (IPatternFillSettings)livelloRiempimento.ImpostazioniRiempimento;

                        impostazioni.OffsetOrizzontale = -5;

                        impostazioni.OffsetVerticale = 12;

                        impostazioni.Scala = 300;

                        impostazioni.Collegato = true;

                        impostazioni.DatiPattern = new int[]

                                                   {

                                                       Color.Nero.ToArgb(), Color.Rosso.ToArgb(),

                                                       Color.Verde.ToArgb(), Color.Blu.ToArgb(),

                                                       Color.Bianco.ToArgb(), Color.AzzurroChiaro.ToArgb(),

                                                       Color.Viola.ToArgb(), Color.Cioccolato.ToArgb(),

                                                       Color.RossoIndia.ToArgb(), Color.VerdeOlivaScuro.ToArgb(),

                                                       Color.BluCadetto.ToArgb(), Color.VerdeGiallo.ToArgb(),

                                                       Color.Nero.ToArgb(), Color.Azzurro.ToArgb(),

                                                       Color.ForestaVerde.ToArgb(), Color.Sienna.ToArgb(),

                                                   };

                        impostazioni.AltezzaPattern = 4;

                        impostazioni.LarghezzaPattern = 4;

                        impostazioni.NomePattern = "$$$/Predefiniti/Pattern/QuadratoColorato=Nuovo Quadrato Colorato\0";

                        impostazioni.IdPattern = Guid.NewGuid().ToString() + "\0";

                        livelloRiempimento.Aggiorna();

                        break;

                    }

                }

                immagine.Save(nomeDestinazione, new OpzioniPsd(immagine));

            }

{{< /highlight >}}

**PSDNET-187. Supporto delle Immagini raster nei File in Formato AI**

{{< highlight java >}}

            const double TolleranzaPredefinita = 1e-6;

void AssertIsTrue(bool condizione, string messaggio) {

 if (!condizione) {

  throw new FormatException(messaggio);

 }

}

string nomeFile = "esempio.ai";

using(AiImage immagine = (AiImage) Image.Load(nomeFile)) {

 AiLayerSection livello = immagine.Livelli[0];

 AssertIsTrue(livello.ImmaginiRaster != null, "La proprietà ImmaginiRaster dovrebbe essere diversa da null");

 AssertIsTrue(livello.ImmaginiRaster.Length == 1, "La proprietà ImmaginiRaster dovrebbe contenere esattamente un elemento");

 AiSezioneImmagineRaster immagineRaster = livello.ImmaginiRaster[0];

 AssertIsTrue(immagineRaster.Pixel != null, "La proprietà pixel dell'immagineRaster dovrebbe essere diversa da null");

 AssertIsTrue(immagineRaster.Pixel.Length == 100, "La proprietà Pixel dell'immagineRaster dovrebbe contenere esattamente 100 elementi");

 AssertIsTrue((uint) immagineRaster.Pixel[99] == 0xFFB21616, "immagineRaster.Pixel[99] dovrebbe essere 0xFFB21616");

 AssertIsTrue((uint) immagineRaster.Pixel[19] == 0xFF00FF00, "immagineRaster.Pixel[19] dovrebbe essere 0xFF00FF00");

 AssertIsTrue((uint) immagineRaster.Pixel[10] == 0xFF01FD00, "immagineRaster.Pixel[10] dovrebbe essere 0xFF01FD00");

 AssertIsTrue((uint) immagineRaster.Pixel[0] == 0xFF0000FF, "immagineRaster.Pixel[0] dovrebbe essere 0xFF0000FF");

 AssertIsTrue(Math.Abs(0.999875 - immagineRaster.Larghezza) < TolleranzaPredefinita, "immagineRaster.Larghezza dovrebbe essere 0.99987");

 AssertIsTrue(Math.Abs(0.999875 - immagineRaster.Altezza) < TolleranzaPredefinita, "immagineRaster.Altezza dovrebbe essere 0.99987");

 AssertIsTrue(Math.Abs(387 - immagineRaster.OffsetX) < TolleranzaPredefinita, "immagineRaster.OffsetX dovrebbe essere 387");

 AssertIsTrue(Math.Abs(379 - immagineRaster.OffsetY) < TolleranzaPredefinita, "immagineRaster.OffsetY dovrebbe essere 379");

 AssertIsTrue(Math.Abs(0 - immagineRaster.Angle) < TolleranzaPredefinita, "immagineRaster.Angle dovrebbe essere 0");

 AssertIsTrue(Math.Abs(0 - immagineRaster.SpostamentoInferioreSinistro) < TolleranzaPredefinita, "immagineRaster.SpostamentoInferioreSinistro dovrebbe essere 0");

 AssertIsTrue(Math.Abs(0 - immagineRaster.RettangoloImmagine.X) < TolleranzaPredefinita, "immagineRaster.RettangoloImmagine.X dovrebbe essere 0");

 AssertIsTrue(Math.Abs(0 - immagineRaster.RettangoloImmagine.Y) < TolleranzaPredefinita, "immagineRaster.RettangoloImmagine.Y dovrebbe essere 0");

 AssertIsTrue(Math.Abs(10 - immagineRaster.RettangoloImmagine.Larghezza) < TolleranzaPredefinita, "immagineRaster.RettangoloImmagine.Larghezza dovrebbe essere 10");

 AssertIsTrue(Math.Abs(10 - immagineRaster.RettangoloImmagine.Altezza) < TolleranzaPredefinita, "immagineRaster.RettangoloImmagine.Altezza dovrebbe essere 10");

}

{{< /highlight >}}

**PSDNET-225. Ottenere proprietà della formattazione inline di un Livello di testo**

{{< highlight java >}}

     using (var immaginePsd = (PsdImage)Image.Load("formattazione_in_linea.psd"))

            {

                List<ITextPortion> testoRegolare = new List<ITextPortion>();

                List<ITextPortion> testoGrassetto = new List<ITextPortion>();

                List<ITextPortion> testoCorsivo = new List<ITextPortion>();

                var livelli = immaginePsd.Livelli;

                for (int indice = 0; indice < livelli.Length; indice++)

                {

                    var livello = livelli[indice];

                    if (!(livello is TextLayer))

                    {

                        continue;

                    }

                    var livelloTesto = (TextLayer)livello;

                    // ottiene i font contenuti nel livello di testo

                    var fonts = livelloTesto.GetFonts();

                    var porzioniTesto = livelloTesto.DatiTesto.Items;

                    foreach (var porzioneTesto in porzioniTesto)

                    {

                        TextFontInfo font = fonts[porzioneTesto.Style.FontIndex];

                        if (font != null)

                        {

                            switch (font.Style)

                            {

                                case FontStyle.Regular:

                                    testoRegolare.Add(porzioneTesto);

                                    break;

                                case FontStyle.Bold:

                                    testoGrassetto.Add(porzioneTesto);

                                    break;

                                case FontStyle.Italic:

                                    testoCorsivo.Add(porzioneTesto);

                                    break;

                                default:

                                    throw new ArgumentOutOfRangeException();

                            }

                        }

                    }

                }

            }

{{< /highlight >}}



**PSDNET-214. Esportazione non corretta di un file PSD in altri formati se contiene Effetti del Livello e Livelli di Regolazione**

{{< highlight java >}}

     var opzioniCaricamento = new PsdLoadOptions();

   opzioniCaricamento.LoadEffectsResource = true;

   using (var immagine = (PsdImage)Image.Load("ombra_clip.psd", opzioniCaricamento))

   {

       immagine.Save("output.png", new PngOptions());

   }

{{< /highlight >}}