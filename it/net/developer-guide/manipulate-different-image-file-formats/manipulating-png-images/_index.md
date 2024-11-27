---
title: Manipolazione delle immagini PNG
type: docs
weight: 40
url: /it/net/manipolazione-immagini-png/
---

## **Specificare la trasparenza per le immagini PNG**
Uno dei vantaggi del salvataggio delle immagini in formato PNG è che PNG può avere uno sfondo trasparente. Aspose.PSD per .NET fornisce la funzionalità per specificare la trasparenza per le immagini PNG e le immagini raster come dimostrato nella sezione sottostante. Aspose.PSD per .NET API può essere utilizzato per impostare qualsiasi colore come trasparente durante la creazione di nuove immagini PNG o la conversione di immagini esistenti nel formato PNG. A questo scopo, l'API Aspose.PSD per .NET ha esposto la proprietà [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) e l'enumerazione [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) che possono essere impostati per specificare qualsiasi colore da rendere trasparente nell'immagine PNG. Lo snippet di codice fornito di seguito dimostra come convertire un'immagine PSD esistente in un'immagine PNG specificando il colore desiderato come trasparente.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificareEConvertireImmagini-PNG-SpecificareTrasparenza-SpecificareTrasparenza.cs" >}}
## **Impostare la risoluzione per le immagini PNG**
Aspose.PSD per .NET espone la classe ResolutionSetting che può essere utilizzata per impostare la risoluzione per tutti i formati di immagine, inclusa PNG. Questo articolo dimostra l'utilizzo dell'API Aspose.PSD per .NET per impostare i parametri di risoluzione orizzontale e verticale per il formato immagine PNG. Lo snippet di codice seguente carica un'immagine PSD esistente e la converte anche nel formato PNG modificando anche la risoluzione.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificareEConvertireImmagini-PNG-ImpostareRisoluzione-ImpostareRisoluzione.cs" >}}
## **Comprimere i file PNG**
Il Portable Network Graphic (PNG) è un formato di compressione senza perdita per la trasmissione di una bitmap tramite reti. Quando si salva un'immagine come file PNG in qualsiasi programma, potrebbe essere richiesto di scegliere un livello di compressione in un intervallo da 0 a un livello massimo. Impostare questo valore comprime effettivamente le dimensioni del file e non diminuisce la qualità dell'immagine. Questo articolo descrive come le API di Aspose.PSD ti consentono di controllare le dimensioni dei file PNG. Le API di Aspose.PSD possono essere utilizzate per impostare i Livelli di Compressione per il formato file PNG utilizzando la classe PngOptions che ha una proprietà di tipo int [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel). Questa proprietà accetta un valore da 0 a 9 dove 9 rappresenta la massima compressione. Lo snippet di codice fornito di seguito dimostra come impostare i Livelli di Compressione utilizzando l'API di Aspose.PSD per .NET.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificareEConvertireImmagini-PNG-ComprimereFile-ComprimereFile.cs" >}}
## **Specificare la profondità dei bit per le immagini PNG**
La profondità di bit nell'immagine è il numero di bit utilizzati per indicare il colore di un singolo pixel in un'immagine bitmap. Come per tutti gli altri formati bitmap, la profondità del colore PNG è rappresentata anche in bit come ad esempio 1-bit (2 colori), 2-bit (4 colori), 4-bit (16 colori) e 8-bit (256 colori). Aspose.PSD per .NET API può essere utilizzato per impostare la profondità dei bit per le immagini PNG utilizzando la proprietà [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) esposta dalla classe PngOptions. Attualmente, la proprietà BitDepth può essere impostata su 1, 2, 4 o 8 bit per i tipi di colore in scala di grigi e a indice. Per tutti gli altri tipi di colore sono supportati solo 8 bit. Lo snippet di codice fornito di seguito dimostra come impostare la profondità dei bit per un'immagine PNG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificareEConvertireImmagini-PNG-SpecificareProfonditaBit-SpecificareProfonditaBit.cs" >}}
## **Applicare metodi di filtro alle immagini PNG**
La profondità di bit nell'immagine è il numero di bit utilizzati per indicare il colore di un singolo pixel in un'immagine bitmap. Come per tutti gli altri formati bitmap, la profondità del colore PNG è rappresentata anche in bit come ad esempio 1-bit (2 colori), 2-bit (4 colori), 4-bit (16 colori) e 8-bit (256 colori). Aspose.PSD per .NET API può essere utilizzato per impostare la profondità dei bit per le immagini PNG utilizzando la proprietà BitDepth esposta dalla classe PngOptions. Attualmente, la proprietà BitDepth può essere impostata su 1, 2, 4 o 8 bit per i tipi di colore in scala di grigi e a indice. Per tutti gli altri tipi di colore sono supportati solo 8 bit. Lo snippet di codice fornito di seguito dimostra come impostare la profondità dei bit per un'immagine PNG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificareEConvertireImmagini-PNG-ApplicareMetodoFiltro-ApplicareMetodoFiltro.cs" >}}
## **Cambiare il colore di sfondo di un'immagine PNG trasparente**
Le immagini in formato PNG possono avere uno sfondo trasparente. Aspose.PSD per .NET offre la funzionalità di cambiare il colore di sfondo di un'immagine PNG che ha uno sfondo trasparente. Aspose.PSD per .NET API può essere utilizzato per impostare/cambiare il colore di uno sfondo di un'immagine PNG trasparente. Lo snippet di codice fornito di seguito dimostra come impostare/cambiare il colore di sfondo di un'immagine PNG trasparente.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificareEConvertireImmagini-PNG-CambiareColoreSfondo-CambiareColoreSfondo.cs" >}}
