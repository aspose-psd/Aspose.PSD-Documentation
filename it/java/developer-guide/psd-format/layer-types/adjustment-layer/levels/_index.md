---
title: Livello di regolazione in bianco e nero
type: docs
weight: 30
url: /it/java/layer-types/adjustment-layer/levels/
---

## Lavorare con il livello di regolazione Livelli di Photoshop in Java

In questo articolo impareremo come regolare l'intervallo tonale e il bilanciamento del colore di una foto nel formato file [PSD](/it/psd/java/psd-format/) in modo programmatico in Java. Non utilizziamo l'editor fotografico Adobe® Photoshop® stesso. Invece, utilizziamo la libreria Aspose.PSD per Java che funziona autonomamente per manipolare il documento Photoshop.

Anche se Aspose.PSD per Java supporta più che sufficienti [strumenti per modificare la foto](/it/psd/java/manipolazione-immagini/) come desideriamo, andiamo avanti con l'API del livello di regolazione Livelli, che è uno dei modi più semplici e veloci per fare il lavoro.

## Panoramica dell'API

L'attuale implementazione (20.6 al momento della stesura) dell'API del livello di regolazione Livelli **supporta tutte le funzionalità di base dei Livelli di Photoshop**, cioè, regolando i Livelli di input e di output per il canale composito (RGB) così come per ogni canale di colore primario (rosso, verde e blu).

L'API del livello di regolazione Livelli è diretta. La classe [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) è il punto di ingresso per la regolazione dei Livelli. Contiene un paio di metodi per accedere ai canali di colore: getMasterChannel e getChannel(int). Entrambi i metodi restituiscono [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel) che ha proprietà corrispondenti per la manipolazione dei Livelli di input e di output. La differenza è che getMasterChannel serve per regolare il canale di colore composito (RGB) mentre getChannel accede a un particolare canale di colore (rosso, verde o blu) tramite il suo indice.

## Compatibilità con le modalità di colore

È importante aggiungere che il livello di regolazione Livelli **è compatibile con la vasta maggioranza delle modalità di colore** secondo i Livelli di Photoshop. Pertanto, è possibile regolare i Livelli per immagini in Scala di grigi (canale grigio), RGB (RGB, canali rosso, verde e blu), CMYK (CMYK, canali ciano, magenta, giallo e nero), Duotono (canale monocromatico) e LAB (luminosità, a e b canali) modalità di colore.

## Regolare l'intervallo tonale

In poche parole, la correzione tonale si applica a un'immagine per riassegnare le ombre e gli highlights per una migliore distribuzione dei toni intermedi. In generale, **rende l'immagine più contrastata**, se fatta correttamente. Ad esempio, prendiamo una foto di un cane (b) e regoliamo il suo intervallo tonale (a - lo screenshot è catturato dalla finestra Livelli di Photoshop per chiarezza) per rendere la foto più contrastata (c).

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Figura 1 del Livello di Livelli](levels-adjustment-figure-1.png)|

Per **regolare l'intervallo tonale complessivo** di un'immagine, i Livelli di input del canale principale dovrebbero essere impostati:

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel((**short**) 229);

È necessario tenere presente che i Livelli di input dovrebbero essere compresi nell'intervallo da 0 a 253 per le ombre, da 9,99 a 0,01 per i toni intermedi e da 2 a 255 per gli highlights. L'intervallo dei Livelli di output deve essere compreso tra 0 e 255.

Hai bisogno di ulteriori esempi? Li puoi trovare su [Github](https://github.com/aspose-psd/Aspose.PSD-for-Java) e nella [knowledge base](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers).

## Conclusione

Per riassumere, Aspose.PSD per Java ha un'API comoda e semplice per cambiare l'intervallo tonale e il bilanciamento del colore di un'immagine che è compatibile con quasi tutte le modalità di colore. L'API del livello di regolazione Livelli della libreria assomiglia a Photoshop Livelli, pertanto, è facile iniziare anche se non hai mai lavorato con la libreria prima.
