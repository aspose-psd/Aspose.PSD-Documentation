---
title: Manipolazione delle immagini PNG
type: docs
weight: 30
url: /it/java/manipolazione-immagini-png/
---

## **Specificare la trasparenza per le immagini PNG**
Uno dei vantaggi del salvataggio delle immagini in formato PNG è che il PNG può avere uno sfondo trasparente. Aspose.PSD for Java fornisce la funzionalità per specificare la trasparenza per le classi PngImage & RasterImage come dimostrato nella sezione sottostante. Aspose.PSD for Java API può essere utilizzato per impostare qualsiasi colore come trasparente durante la creazione di nuove immagini PNG o la conversione di immagini esistenti nel formato PNG. A tale scopo, l'API Aspose.PSD for Java ha esposto la proprietà TransparentColor e l'enumerazione PngColorType che possono essere impostate per specificare un colore da renderizzare come trasparente nell'immagine PNG. Il frammento di codice fornito di seguito dimostra come convertire un'immagine PSD esistente in un'immagine PNG utilizzando il costruttore sovraccaricato di PngImage e specificando il colore desiderato come trasparente.

## **Impostare la risoluzione per le immagini PNG**
Aspose.PSD for Java espone la classe ResolutionSetting che può essere utilizzata per impostare la risoluzione per tutti i formati di immagine, compreso il PNG. Questo articolo dimostra l'utilizzo dell'API Aspose.PSD for Java per impostare i parametri di risoluzione orizzontale e verticale per il formato di immagine PNG. Il frammento di codice seguente carica un'immagine PSD esistente e la converte nel formato PNG cambiando anche la risoluzione.

## **Comprimere i file PNG**
Il formato Portable Network Graphic (PNG) è un formato di compressione senza perdita di dati per la trasmissione di un bitmap attraverso le reti. Quando si salva un'immagine in un file PNG in qualsiasi programma, potrebbe essere richiesto di scegliere un livello di compressione in un intervallo da 0 a un massimo. Impostando questo valore si comprime effettivamente la dimensione del file senza ridurre la qualità dell'immagine. Questo articolo descrive come le API Aspose.PSD consentano di controllare la dimensione del file PNG. Le API Aspose.PSD possono essere utilizzate per impostare i livelli di compressione per il formato di file PNG utilizzando la classe PngOptions che ha la proprietà CompressionLevel di tipo int. Questa proprietà accetta un valore da 0 a 9 dove 9 è la massima compressione. Il frammento di codice fornito di seguito dimostra come impostare i livelli di compressione utilizzando Aspose.PSD for Java API.

## **Specificare la profondità dei bit per le immagini PNG**
La profondità dei bit nell'immagine è il numero di bit utilizzati per indicare il colore di un singolo pixel in un'immagine bitmap. Come tutti gli altri formati bitmap, la profondità del colore PNG è rappresentata anche in bit come ad esempio 1-bit (2 colori), 2-bit (4 colori), 4-bit (16 colori) e 8-bit (256 colori). L'API Aspose.PSD for Java può essere utilizzata per impostare la profondità dei bit per le immagini PNG utilizzando la proprietà BitDepth esposta dalla classe PngOptions. Al momento, la proprietà BitDepth può essere impostata su 1, 2, 4 o 8 bit per tipi di colore scala di grigi e a indice. Per tutti gli altri tipi di colore sono supportati solo 8 bit. Il frammento di codice fornito di seguito dimostra come impostare la Profondità dei Bit per un'immagine PNG.

## **Applicare metodi di filtro alle immagini PNG**
Aspose.PSD for Java espone l'enumerazione PngFilterType che può essere utilizzata per impostare il tipo di filtro per l'immagine PNG. Il frammento di codice fornito di seguito dimostra come applicare un filtro al file PSD esistente all'immagine PNG utilizzando PngFilterType.

## **Cambiare il colore di sfondo di un'immagine PNG trasparente**
Le immagini in formato PNG possono avere uno sfondo trasparente. Aspose.PSD for Java fornisce la funzionalità di cambiare il colore di sfondo di un'immagine PNG che ha uno sfondo trasparente. L'API Aspose.PSD for Java può essere utilizzata per impostare/cambiare il colore di uno sfondo trasparente di un'immagine PNG. Il frammento di codice fornito di seguito dimostra come impostare/cambiare il colore di sfondo di un'immagine PNG trasparente.
