---
title: Livello di regolazione Filtro fotografico
type: docs
weight: 30
url: /it/java/layer-types/adjustment-layer/photo-filter/
---

# Lavorare con il livello di regolazione Filtro fotografico di Photoshop in Java

Oggi vedremo come applicare il livello di regolazione Filtro fotografico a un documento esistente di Photoshop utilizzando Aspose.PSD per Java che è la libreria per manipolare il formato di file PSD.

**L'API del livello di regolazione Filtro fotografico** cambia l'equilibrio del colore dell'immagine utilizzando l'intensità. L'immagine risultante sembrerà la stessa di dopo aver usato un filtro reale per macchine fotografiche. Si noti che l'API del livello di regolazione Filtro fotografico della libreria differisce leggermente da quella di Photoshop perché non ci sono ancora filtri predefiniti. Tuttavia, è la stessa in tutti gli altri aspetti. Significa che è possibile impostare un colore dell'intensità e cambiare la sua intensità (densità) così come utilizzare l'opzione di Preservare la luminosità.

## Panoramica dell'API

L'API del livello di regolazione Filtro fotografico è piuttosto semplice da utilizzare. C'è la classe principale [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer) che funge da punto di ingresso a questo livello di regolazione e contiene solo tre proprietà pubbliche, ossia, colore, densità e preservare la luminosità mediante le quali avviene la regolazione.

## Regolare l'equilibrio del colore

Dal momento che non c'è molto da dire, consideriamo **un esempio di regolazione dell'equilibrio del colore** utilizzando il Filtro fotografico subito. Aggiungeremo un filtro di riscaldamento (a) manualmente per l'immagine della scultura di un cervo (b) per ottenere l'immagine in toni caldi (c) che risulta più piacevole da guardare.

![Esempio di livello di regolazione Filtro fotografico](photo-filter-adjustment-layer-figure-1.png)

Innanzitutto, notate che [il metodo di fabbrica](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-) differisce da quelli per [gli altri livelli di regolazione](https://docs.aspose.com/display/psdjava/PSD+Adjustment+Layers) perché non c'è un metodo predefinito (senza argomenti). Pertanto, per aggiungere un livello di regolazione Filtro fotografico nel documento di Photoshop caricato è richiesto un unico argomento, ossia il [colore](https://reference.aspose.com/psd/java/com.aspose.psd/Color). Quindi, per ricreare l'effetto del filtro di riscaldamento, passare l'arancione come argomento al metodo di fabbrica, quindi impostare la densità utilizzando i relativi setter:

    PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
    photoFilterLayer.setDensity(25);

Vale la pena aggiungere che la proprietà Densità ha un valore predefinito che è 100 così come vero è il valore predefinito per la proprietà Preservare la luminosità (è il motivo per cui non abilitiamo esplicitamente questa opzione).

## Conclusione

In questo articolo abbiamo considerato l'utilizzo dell'API del livello di regolazione Filtro fotografico di Aspose.PSD per Java. Questo strumento è semplice da utilizzare e consente di aggiungere un'intensità a un'immagine con densità variabile. È un modo rapido per regolare l'equilibrio del colore dell'intera immagine.
