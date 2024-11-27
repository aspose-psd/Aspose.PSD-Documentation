---
title: Note sulla versione di Aspose.PSD per .NET 18.10
type: docs
weight: 30
url: /it/net/aspose-psd-per-net-18-10-note-sulla-versione/
---

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-14|Aggiunta del supporto delle modalità di fusione oltre a Normale|Caratteristica|
|PSDNET-69|Aggiunta del supporto dell'effetto Sovrapposizione colore|Caratteristica|
|PSDNET-70|Aggiunta del supporto dell'effetto Ombra portata|Caratteristica|
|PSDNET-71|Rendering per l'esportazione dell'effetto Sovrapposizione colore|Caratteristica|
|PSDNET-72|Rendering per l'esportazione dell'effetto Ombra portata|Caratteristica|
|PSDNET-74|Supporto dell'aggiunta degli Effetti livello in esecuzione|Caratteristica|
|PSDNET-73|Ottimizzazione delle prestazioni di caricamento delle risorse che contengono strutture osType|Errore|
|PSDNET-79|Rifattorizzazione e correzioni di memory leaks in LayerAndMaskInfo|Miglioramento|

## **Esempi di utilizzo:**
**PSDNET-14 Aggiunta del supporto delle modalità di fusione oltre a Normale**

{{< highlight java >}}

 var files = new string[]

{

    "Normale",

    "Dissolvenza",

    "Scuro",

    "Moltiplica",

    "ColoreBruciato",

    "CombLinear",

    "ColoreScuro",

    "Illumina",

    "Schermo",

    "SovrapposizioneColore",

    "AggiungiCombLinear",

    "ColoreIlluminato",

    "Sovrapposizione",

    "LuceTenue",

    "LuceIntensa",

    "LuceVivida",

    "LuceLineare",

    "LucePerforazione",

    "MescolaIntenso",

    "Differenza",

    "Esclusione",

    "Sottrai",

    "Dividi",

    "Tonalità",

    "Saturazione",

    "Colore",

    "Luminosità",

};

foreach (var fileName in files)

{

    using (var im = LoadFile(fileName + ".psd"))

    {

        // Esporta in PNG

        var saveOptions = new PngOptions();

        saveOptions.ColorType = PngColorType.VeroColoreConAlfa;

        var pngExportPath100 = "ModalitàFusione" + fileName + "_Test100.png";

        im.Save(pngExportPath100, saveOptions);

        // Imposta opacità al 50%

        im.Layers[1].Opacità = 127;

        var pngExportPath50 = "ModalitàFusione" + fileName + "_Test50.png";

        im.Save(pngExportPath50, saveOptions);

    }

}

{{< /highlight >}}

**PSDNET-69 Aggiunta del supporto dell'effetto Sovrapposizione colore**

{{< highlight java >}}

     // Modifica dell'effetto Sovrapposizione colore

    string sourceFileName = "SovrapposizioneColore.psd";

    string percorsoPsdDopoCambiamento = "SovrapposizioneColoreCambiato.psd";

    using (var im = LoadFile(sourceFileName))

    {

       var sovrapposizioneColore = (SovrapposizioneColore)(im.Layers[1].BlendingOptions.Effetti[0]);



       Assert.AreEqual(Colore.Rosso, sovrapposizioneColore.Colore);

       Assert.AreEqual(153, sovrapposizioneColore.Opacità);

       sovrapposizioneColore.Colore = Colore.Verde;

       sovrapposizioneColore.Opacità = 128;

       im.Save(percorsoPsdDopoCambiamento);

    }

{{< /highlight >}}

**PSDNET-70 Aggiunta del supporto dell'effetto Ombra portata**

{{< highlight java >}}

     // Modifica dell'effetto Ombra portata

    string sourceFileName = "Ombra.psd";

    string psdPathAfterChange = "OmbraCambiata.psd";

    using (var im = LoadFile(sourceFileName))

    {

       var effettoOmbra = (EffettoOmbraPortata)(im.Layers[1].BlendingOptions.Effetti[0]);



       Assert.AreEqual(Colore.Nero, effettoOmbra.Colore);

       Assert.AreEqual(255, effettoOmbra.Opacità);

       Assert.AreEqual(3, effettoOmbra.Distanza);

       Assert.AreEqual(7, effettoOmbra.Dimensione);

       Assert.AreEqual(true, effettoOmbra.UsaLuceGlobale);

       Assert.AreEqual(90, effettoOmbra.Angolo);

       Assert.AreEqual(0, effettoOmbra.Diffusione);

       Assert.AreEqual(0, effettoOmbra.Rumore);

       effettoOmbra.Colore = Colore.Verde;

       effettoOmbra.Opacità = 128;

       effettoOmbra.Distanza = 11;

       effettoOmbra.UsaLuceGlobale = false;

       effettoOmbra.Dimensione = 9;

       effettoOmbra.Angolo = 45;

       effettoOmbra.Diffusione = 3;

       effettoOmbra.Rumore = 50;

       im.Save(psdPathAfterChange);

    }

{{< /highlight >}}

**PSDNET-71 Rendering per l'esportazione dell'effetto Sovrapposizione colore**

{{< highlight java >}}

    // Modifica dell'effetto Sovrapposizione colore

    string sourceFileName = "SovrapposizioneColore.psd";

    string pngExportPath = "SovrapposizioneColore.png";

    using (var im = LoadFile(sourceFileName))

    {

       var sovrapposizioneColore = (EffettoSovrapposizioneColore)(im.Layers[1].BlendingOptions.Effetti[0]);



       Assert.AreEqual(Colore.Rosso, sovrapposizioneColore.Colore);

       Assert.AreEqual(153, sovrapposizioneColore.Opacità);

       // Salva PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.VeroColoreConAlfa;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-72 Rendering per l'esportazione dell'effetto Ombra portata**

{{< highlight java >}}

     // Esporta Ombra portata

    string sourceFileName = "Ombra.psd";

    string pngExportPath = "Ombra.png";

    using (var im = LoadFile(sourceFileName))

    {

       var effettoOmbra = (EffettoOmbraPortata)(im.Layers[1].BlendingOptions.Effetti[0]);



       Assert.AreEqual(Colore.Nero, effettoOmbra.Colore);

       Assert.AreEqual(255, effettoOmbra.Opacità);

       Assert.AreEqual(3, effettoOmbra.Distanza);

       Assert.AreEqual(7, effettoOmbra.Dimensione);

       Assert.AreEqual(true, effettoOmbra.UsaLuceGlobale);

       Assert.AreEqual(90, effettoOmbra.Angolo);

       Assert.AreEqual(0, effettoOmbra.Diffusione);

       Assert.AreEqual(0, effettoOmbra.Rumore);

       // Salva PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.VeroColoreConAlfa;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-74 Supporto dell'aggiunta degli Effetti livello in esecuzione**

{{< highlight java >}}

     // Aggiungi effetto livello sovrapposizione colore in esecuzione

    string sourceFileName = "TreLivelliRegolariConEffettoLivello.psd";

    string psdExportPath = "TreLivelliRegolariConEffettoLivelloCambiato.psd";

    string pngExportPath = "TreLivelliRegolariConEffettoLivelloCambiato.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };



    var testFolder = string.Empty;

    var im = (PsdImage)Image.Load(testPath, loadOptions) 

    using (im)

    {

        var effetto = im.Layers[1].BlendingOptions.AggiungiSovrapposizioneColore();

        effetto.Opacità = 128;

        effetto.Colore = Colore.Verde;

        effetto.ModoFusione = ModoFusione.Normale;

        var effetto = im.Layers[1].BlendingOptions.AggiungiOmbraPortata();

        effetto.Colore = Colore.Rosso;

        effetto.Opacità = 128;

        effetto.ModoFusione = ModoFusione.Normale;



        // Salva PSD    

        im.Save(psdExportPath);



        // Salva PNG

        var saveOptions = new PngOptions();

        im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}
