---
title: Lavorare con le maschere in Aspose.PSD per Java
weight: 100
type: docs
description: Esempi su come lavorare con le maschere di Clipping, Raster e Vettoriali all'interno di un file PSD
keywords: [maschere, maschera di livello, maschera vettoriale, maschera di clipping, psd, api psd, java, esempio di codice]
url: it/java/update-create-layer-mask/
---

## **Panoramica**

**Panoramica**
	
	Ci sono 3 tipi di maschere nei file PSD:
	1. Maschere di Clipping
	2. Maschere raster
	3. Maschere vettoriali
	
	Questo articolo copre tutti e 3 i tipi.


**Maschere di Clipping**

Le maschere di clipping sono una funzionalità robusta nei software di progettazione grafica e di editing di immagini, in particolare in Java. Consentono un controllo preciso sulla visibilità di uno strato in base alla forma e al contenuto di un altro strato. Fondamentalmente, una maschera di clipping limita la visibilità di uno strato alla forma di un altro strato sottostante.

Per implementare una maschera di clipping in Java, avrai bisogno innanzitutto di due strati: lo strato di base e lo strato che intendi ritagliare. Lo strato di base definisce la forma o l'area che rimarrà visibile, mentre lo strato da ritagliare contiene il contenuto che si conformerà alla forma dello strato di base.

Quando una maschera di clipping viene applicata in Java, il contenuto dello strato ritagliato è visibile solo all'interno dei confini dello strato di base. Eventuali contenuti al di fuori di questi confini saranno nascosti o ritagliati.

Le maschere di clipping si rivelano particolarmente preziose nell'applicare effetti, come texture o pattern, a specifiche aree di un'immagine o di un'opera d'arte. Utilizzando una maschera di clipping, è possibile confinare l'effetto all'area desiderata senza influenzare il resto dell'immagine.

Si rimanda all'esempio alla fine della pagina per una maggiore chiarezza.

**Maschere raster**

Le maschere raster nei file Java sono utilizzate per gestire la visibilità di specifiche aree all'interno di uno strato. A differenza delle maschere vettoriali, che utilizzano forme matematiche per definire le aree mascherate, le maschere raster si basano su informazioni basate sui pixel per determinare regioni visibili o nascoste.

Una maschera raster comprende un'immagine in scala di grigi applicata a uno strato. Le aree bianche della maschera indicano la visibilità, mentre le aree nere rappresentano porzioni nascoste. Le sfumature di grigio in mezzo possono creare trasparenze parziali o regioni semi-visible.

Si rimanda all'esempio alla fine della pagina per una migliore comprensione.

**Maschere vettoriali**

Le maschere vettoriali nei file Java sono strumenti versatili utilizzati per delineare la visibilità di aree specifiche all'interno di uno strato basate su forme matematiche. A differenza delle maschere raster, che dipendono dai dati basati sui pixel, le maschere vettoriali impiegano percorsi e curve per creare aree mascherate lisce e scalabili.

Una maschera vettoriale consiste essenzialmente in un percorso applicato a uno strato. La forma di questo percorso determina quali parti dello strato sono visibili e quali sono nascoste. Manipolando i punti di controllo e le curve del percorso, possono essere create aree mascherate precise e intricate.

Si rimanda alla [pagina sulle maschere vettoriali](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/layermaskdatashort/) per informazioni sull'aggiunta di maschere vettoriali utilizzando risorse.

## **Esempio**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-psd-update-create-layer-mask.java" >}}
