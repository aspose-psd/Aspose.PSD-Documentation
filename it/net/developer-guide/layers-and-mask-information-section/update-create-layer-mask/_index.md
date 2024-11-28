---
title: Lavorare con le maschere in Aspose.PSD per C#
weight: 100
type: docs
description: Esempi su come lavorare con Clipping, Raster e Vector Masks all'interno del file PSD
keywords: [maschere, maschera di livello, maschera vettoriale, maschera di ritaglio, psd, psd api, C#, codice di esempio]
url: it/net/update-create-layer-mask/
---

## Panoramica

Ci sono tre tipi di maschere nei file PSD:
1. Maschere di ritaglio
2. Maschere raster
3. Maschere vettoriali

Questo articolo copre tutti e tre i tipi.

### Maschere di ritaglio

Le maschere di ritaglio sono una potente funzionalità nei software di grafica e di editing di immagini che consentono di controllare la visibilità di uno strato in base alla forma e al contenuto di un altro strato. Fondamentalmente, una maschera di ritaglio limita la visibilità di uno strato alla forma definita da un altro strato sottostante.

Per creare una maschera di ritaglio, ti servono due strati: lo strato di base e lo strato di ritaglio. Lo strato di base definisce la forma o l'area che sarà visibile, mentre lo strato di ritaglio contiene il contenuto che sarà confinato alla forma dello strato di base.

Quando si applica una maschera di ritaglio, il contenuto dello strato di ritaglio è visibile solo all'interno dei confini dello strato di base. Qualsiasi contenuto al di fuori dei confini dello strato di base è nascosto o ritagliato.

Le maschere di ritaglio sono particolarmente utili per applicare effetti, come texture o motivi, a specifiche aree di un'immagine o di un'opera d'arte. Utilizzando una maschera di ritaglio, è possibile garantire che l'effetto sia limitato all'area desiderata senza influenzare il resto dell'immagine.

### Maschere raster

Le maschere raster nei file PSD sono essenziali per controllare la visibilità di aree specifiche all'interno di uno strato. A differenza delle maschere vettoriali, che utilizzano forme matematiche per definire le aree mascherate, le maschere raster utilizzano informazioni basate su pixel per determinare quali parti di uno strato sono visibili o nascoste.

Una maschera raster è composta da un'immagine in scala di grigi applicata a uno strato. Le aree bianche della maschera rappresentano le porzioni visibili, mentre le aree nere rappresentano le porzioni nascoste. Le sfumature di grigio intermedie creano aree parzialmente trasparenti o semi-visibili.

Utilizzando le maschere raster, è possibile ottenere effetti di mascheratura intricati, consentendo un controllo preciso sulla visibilità dello strato basato su dettagli a livello di pixel. Questa funzionalità è particolarmente utile per compiti che richiedono editing dettagliato e blending all'interno di un'immagine.

### Maschere vettoriali

Le maschere vettoriali nei file PSD sono uno strumento versatile utilizzato per definire la visibilità di aree specifiche all'interno di uno strato basata su forme matematiche. A differenza delle maschere raster, che utilizzano informazioni basate su pixel, le maschere vettoriali utilizzano percorsi e curve per creare aree mascherate lisce e scalabili.

Una maschera vettoriale è essenzialmente un percorso applicato a uno strato. La forma del percorso determina quali parti dello strato sono visibili e quali sono nascoste. Manipolando i punti di controllo e le curve del percorso, è possibile creare aree mascherate precise e intricate.

Le maschere vettoriali sono particolarmente utili per creare maschere pulite e scalabili che possono essere facilmente regolate senza perdita di qualità. Questa funzionalità è ideale per compiti che richiedono alta precisione e flessibilità nella definizione delle aree visibili all'interno di uno strato.

Per ulteriori informazioni sull'aggiunta di maschere vettoriali, visita la [pagina delle Maschere vettoriali](psd/it/net/layer-vector-mask/).

## Esempio
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "WorkingWithMasks-WorkingWithMasks.cs" >}}

Per informazioni più dettagliate ed esempi, visita la [documentazione di Aspose.PSD per C#](https://docs.aspose.com/psd/net/).
