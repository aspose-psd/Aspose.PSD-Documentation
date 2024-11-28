---
title: Aspose.PSD per .NET 23.6 - Note sulla Release
type: docs
weight: 70
url: /it/net/aspose-psd-per-net-23-6-note-sulla-release/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla release per [Aspose.PSD per .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                                                                                  | **Categoria** |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1401 | Riorganizzazione API TimeLine                                                                                                                | Miglioramento |
| PSDNET-1517 | Rimozione artefatti durante il rendering della trasformazione                                                                                 | Miglioramento |
| PSDNET-1528 | Ottimizzazione rendering della trasformazione                                                                                                 | Miglioramento |
| PSDNET-147  | Supporto del livello di Regolazione della Soglia                                                                                              | Funzionalità  |
| PSDNET-149  | Supporto del livello di Regolazione Colori Selettivi                                                                                          | Funzionalità  |
| PSDNET-801  | Abilità di esportare la TimeLine PSD nel file Gif animato                                                                                     | Funzionalità  |
| PSDNET-1555 | Aggiunto supporto per TextLayer senza bordi rettangolari                                                                                      | Funzionalità  |
| PSDNET-1582 | Supporto di ShapeLayer                                                                                                                        | Funzionalità  |
| PSDNET-864  | La sostituzione dell'immagine in Smart object non viene aggiornata                                                                            | Bug          |
| PSDNET-1404 | Il file PSD non può essere salvato come PSD con la seguente eccezione: Rgb e Lab modes non possono contenere meno di 3 canali e più di 4 canali | Bug          |
| PSDNET-1546 | La Giustificazione del Testo è persa se si apre il TextLayer con la modalità di modifica di Photoshop                                          | Bug          |
| PSDNET-1548 | Eccezione di riferimento nullo durante il salvataggio del file PSD                                                                            | Bug          |
| PSDNET-1578 | Eccezione nel caricamento di ShapeLayer: I punti per i limiti dell'origine vettoriale non sono ancora supportati                                  | Bug          |
| PSDNET-1579 | Eccezione nel caricamento di VogkResource: I punti sono salvati come DoubleStructures, ma li leggiamo come UnitStructures                     | Bug          |
| PSDNET-1581 | Il LayerType del ShapeLayer è vuoto                                                                                                          | Bug          |


## **Cambiamenti nell'API Pubblica**
# **API Aggiunte:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ActiveFrameIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.LoopesCount
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.IO.Stream,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Timeline
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PointsUnitType
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Yellow
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Black
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Relative
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Absolute
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Reds
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Yellows
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Greens
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Cyans
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blues
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Magentas
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Whites
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Neutrals
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blacks
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.CorrectionMethod
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.GetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes)
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.SetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes,Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection)
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddSelectiveColorAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer.Level
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddThresholdAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.CreateInstance
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Path


# **API Rimosse:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)


## **Esempi di Utilizzo:**

**PSDNET-147. Supporto del Livello di Regolazione della Soglia**

{{< highlight csharp >}}
string fileSorgenteConLivelloDiSoglia = "fiori_sorgente_soglia.psd";
string filePsdConSogliaDiUscita = "fiori_soglia_output.psd";
string filePngConSogliaDiUscita = "fiori_soglia_output.png";

string fileSorgenteSenzaLivelloDiSoglia = "fiori_sorgente.psd";
string filePsdSenzaLivelloDiSoglia = "fiori_output.psd";
string filePngSenzaLivelloDiSoglia = "fiori_output.png";

void AssertAreEqual(object previsto, object effettivo)
{
    if (!object.Equals(previsto, effettivo))
    {
        throw new Exception("Gli oggetti non sono uguali.");
    }
}

// Ottenere, verificare e modificare il livello di regolazione della Soglia dall'immagine.
using (var immagine = (PsdImage)Image.Load(fileSorgenteConLivelloDiSoglia))
{
    foreach (var layer in immagine.Layers)
    {
        if (layer is ThresholdLayer)
        {
            // Ottenere il livello di regolazione della Soglia.
            ThresholdLayer layerSoglia = (ThresholdLayer)layer;
            var livello = layerSoglia.Level;

            // Verificare i parametri dei livelli.
            AssertAreEqual(livello, (short)115);

            // Impostare i parametri dei livelli.
            layerSoglia.Level = 50;

            immagine.Save(filePsdConSogliaDiUscita);
            immagine.Save(filePngConSogliaDiUscita, new PngOptions());
        }
    }
}

// Aggiungere e impostare il livello di regolazione della Soglia all'immagine.
using (var immagine = (PsdImage)Image.Load(fileSorgenteSenzaLivelloDiSoglia))
{
    // Aggiungere il livello di Regolazione della Soglia.
    ThresholdLayer livelloSoglia = immagine.AddThresholdAdjustmentLayer();

    // Impostare i parametri dei livelli.
    livelloSoglia.Level = 115;

    immagine.Save(filePsdSenzaLivelloDiSoglia);
    immagine.Save(filePngSenzaLivelloDiSoglia, new PngOptions());
}
{{< /highlight >}}

**(Continua nel prossimo commento)**