---
title: Lavorare con le maschere in Aspose.PSD per Python
weight: 100
type: docs
description: Esempi su come lavorare con Clipping, Raster e Vector Masks all'interno di un file PSD
keywords: [maschere, maschera di livello, maschera vettoriale, maschera di ritaglio, psd, api psd, python, esempio di codice]
url: it/python-net/update-create-layer-mask/
---

## **Panoramica**

**Panoramica**

Ci sono 3 tipi di maschere nei file PSD:
1. Maschere di ritaglio
2. Maschere raster
3. Maschere vettoriali

Questo articolo copre tutti e 3 i tipi.

**Maschere di ritaglio**

Le maschere di ritaglio sono una funzionalità potente nei software di progettazione grafica e di editing di immagini. Ti permettono di controllare la visibilità di un livello in base alla forma e al contenuto di un altro livello. In altre parole, una maschera di ritaglio limita la visibilità di un livello alla forma di un altro livello sottostante.

Per creare una maschera di ritaglio, hai bisogno di due livelli: il livello base e il livello che desideri ritagliare. Il livello base definisce la forma o l'area che sarà visibile, mentre il livello che vuoi ritagliare contiene il contenuto che verrà ritagliato alla forma del livello base.

Quando si applica una maschera di ritaglio, il contenuto del livello ritagliato è visibile solo all'interno dei confini del livello base. Eventuali contenuti al di fuori dei confini del livello base saranno nascosti o ritagliati.

Le maschere di ritaglio sono particolarmente utili quando si desidera applicare un effetto, come una texture o un motivo, a una specifica area di un'immagine o di un'opera d'arte. Utilizzando una maschera di ritaglio, è possibile limitare l'effetto all'area desiderata senza influenzare il resto dell'immagine.

Si prega di controllare l'esempio alla fine della pagina

**Maschere raster**

Le maschere raster nei file PSD sono utilizzate per controllare la visibilità di aree specifiche all'interno di un livello. A differenza delle maschere vettoriali, che utilizzano forme matematiche per definire le aree mascherate, le maschere raster utilizzano informazioni basate su pixel per determinare quali parti di un livlo sono visibili o nascoste.

Una maschera raster consiste in un'immagine in scala di grigi che viene applicata a un livello. Le aree bianche della maschera rappresentano le porzioni visibili, mentre le aree nere rappresentano le porzioni nascoste. Le sfumature di grigio possono essere utilizzate per creare trasparenze parziali o aree semi-visibili.

Si prega di controllare l'esempio alla fine della pagina

**Maschere vettoriali**

Le maschere vettoriali nei file PSD sono un'utensile versatile utilizzato per definire la visibilità di aree specifiche all'interno di un livello basandosi su forme matematiche. A differenza delle maschere raster, che utilizzano informazioni basate su pixel, le maschere vettoriali utilizzano percorsi e curve per creare aree mascherate lisce e scalabili.

Una maschera vettoriale è essenzialmente un percorso che viene applicato a un livello. La forma del percorso determina quali parti del livello sono visibili e quali sono nascoste. Manipolando i punti di controllo e le curve del percorso, è possibile creare aree mascherate precise e intricate.

Si prega di controllare la [pagina delle Maschere vettoriali](psd/it/net/layer-vector-mask/) per ottenere informazioni su come le maschere vettoriali possono essere aggiunte utilizzando le risorse.


## **Esempio**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-update-create-layer-mask.py" >}}
