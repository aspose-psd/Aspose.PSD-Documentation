---
title: Note sulla release Aspose.PSD per .NET 22.9
type: docs
weight: 40
url: /it/net/aspose-psd-for-net-22-9-note-sulla-release/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla release per [Aspose.PSD per .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Questa release presenta un regresso nel caso delle esportazioni a 16 bit, quindi raccomandiamo cautela nell'utilizzo di questa funzionalità in questa release.
Si prega di non aggiornare Aspose.PSD alla versione 22.9 se il trattamento delle immagini a 16 bit è la funzionalità primaria.
- Per diverse versioni di Photoshop, gli utenti potrebbero riscontrare una finestra con un errore relativo alla lettura del layer, il che non influenzerà il lavoro con il file PSD.

Stiamo lavorando per risolvere questi problemi.

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-1237|Creare il modello interno LayerStyleFX che conterrà effetti e dati correlati per utilizzare il singolo modello nelle risorse degli effetti Lfx2, lmfx e mlst|Potenziamento|
|PSDNET-1227|Aggiungere lettura e scrittura delle strutture 'Lefx' con informazioni sugli effetti per gli stati di livello nei modelli della TimeLine|Funzionalità|
|PSDNET-1230|Applicare lo stato del livello di TimeLine al livello in PsdImage|Funzionalità|
|PSDNET-1072|Trasparenza non corretta durante il salvataggio del file PSD (RGB/16bit) sull'esportazione a 8 bit|Errore|
|PSDNET-1140|Eccezione durante il caricamento del passo delle risorse dei livelli globali durante l'apertura del documento PSB|Errore|
|PSDNET-1266|Memory leak sul processamento di file specifici|Errore|


## **Modifiche all'API pubblica**
# **API aggiunte:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.PositionOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.StateEffects
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.Effects
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddDropShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddInnerShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddOuterGlow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddColorOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddGradientOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddPatternOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.ClearLayerStyle
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.RemoveEffectAt(System.Int32)

# **API rimosse:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **Esempi di utilizzo:**

**PSDNET-1072. Trasparenza non corretta durante il salvataggio del file PSD (RGB/16bit) sull'esportazione a 8 bit**

{{< highlight csharp >}}
string filePsdInput    = "8bitConTrasparenza.psd";
string filePsdOutput   = "16bitConTrasparenza.psd";
string fileImmagineOutput = "OutputConTrasparenza.png";

using (var img = Image.Load(filePsdInput))
{
    // Opzioni di salvataggio a 16 bit
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(filePsdOutput, p16);
}
using (var img = Image.Load(filePsdOutput))
{
    // Salvare l'immagine con colori a 16 bit
    img.Save(fileImmagineOutput, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. Eccezione durante il caricamento del passo delle risorse dei livelli globali durante l'apertura del documento PSB**

{{< highlight csharp >}}
string filePsdSorgente = "input.psb";
string fileImmagineOutput = "output.png";

using (var image = (PsdImage)Image.Load(filePsdSorgente))
{
    // Qui non dovrebbe esserci alcuna eccezione.
    image.Save(fileImmagineOutput, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. Aggiungere lettura e scrittura delle strutture 'Lefx' con informazioni sugli effetti per gli stati di livello nei modelli della TimeLine**

{{< highlight csharp >}}
string fileSorgente = "4_animato.psd";
string fileOutput = "output.psd";

using (var psdImage = (PsdImage)Image.Load(fileSorgente))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    int[] idLivelli = timeLine.IdLivelli;

    var stateEffectsLivello11 = timeLine.Frames[1].StatiLivelli[idLivelli[1]].StatoEffetti;

    stateEffectsLivello11.AddDropShadow();
    stateEffectsLivello11.AddGradientOverlay();

    var stateEffectsLivello21 = timeLine.Frames[2].StatiLivelli[idLivelli[1]].StatoEffetti;
    stateEffectsLivello21.AddStroke(FillType.Color);
    stateEffectsLivello21.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(fileOutput);
}
{{< /highlight >}}

**PSDNET-1230. Applicare lo stato del livello di TimeLine al livello in PsdImage**

{{< highlight csharp >}}
string fileSorgente = "3_animato.psd";
string filePsdOutput = "output.psd";
string filePngOutput = "output.png";

using (var psdImage = (PsdImage)Image.Load(fileSorgente, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var idLivelli = timeLine.IdLivelli;

    var statoLivello11 = timeLine.Frames[1].StatiLivelli[idLivelli[1]];

    timeLine.Frames[1].StatiLivelli[idLivelli[1]].StatoEffetti.AddPatternOverlay();
    statoLivello11.BlendMode = BlendMode.Multiply;

    // Cambia il frame attivo da 0 a 1 per attivare l'applicazione dello StatoLivello al Livello
    timeLine.ActiveFrame = 1;

    // Applica le modifiche a PsdImage
    timeLine.ApplyTo(psdImage);

    psdImage.Save(filePsdOutput);
    psdImage.Save(filePngOutput, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. Memory leak sul processamento di file specifici**

{{< highlight csharp >}}
string[] fileDaCaricare = new string[] { "testPsd0.psd", "testPsd1.psd", "testPsd2.psd" };
int numeroInput = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(numeroInput, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double conteggioMemoria = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Byte totali utilizzati prima del test: {0:N2} MiB", conteggioMemoria);

double massimo = conteggioMemoria;

for (int i = 0; i < 50; i++)
{
    int indiceFile = i % numeroInput;
    string fileSorgente = Path.Combine(cartellaBase, fileDaCaricare[indiceFile]);

    // ControllaAperturaSalvataggio
    using (MemoryStream outputStream = new MemoryStream())
    {
        using (PsdImage psd = (PsdImage)Image.Load(fileSorgente, new PsdLoadOptions { LoadEffectsResource = true }))
        {
            psd.Save(outputStream, new JpegOptions() { Quality = 100 });
        }
    }

#if NETCOREAPP
    GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
    GC.Collect(numeroInput, GCCollectionMode.Forced);
    GC.WaitForFullGCComplete();

    conteggioMemoria = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
    massimo = Math.Max(massimo, conteggioMemoria);
}

conteggioMemoria = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Byte totali utilizzati dopo il test: {0:N2} MiB", conteggioMemoria);
Assert.IsTrue(Math.Abs(conteggioMemoria - massimo) < 20, "Rilevata perdita di memoria nella funzionalità di base!");
{{< /highlight >}}
