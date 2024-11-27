---
title: Utilizzo dell'API grafica per modificare i livelli nei file PSD
weight: 100
type: docs
description: Esempio di utilizzo dell'API grafica in Aspose.PSD per Java
keywords: [aggiornare livello, disegnare cerchio, disegnare ellisse, disegnare cerchio pieno, grafica, api psd, java, esempio di codice]
url: it/java/api-grafica/
---

## **Panoramica**
Per iniziare, caricare il file PSD utilizzando il metodo Image.load() o creare un'immagine Psd da zero. Utilizza la variabile inputFile per rappresentare il percorso del tuo file PSD e specificare eventuali opzioni di caricamento con loadOpt, se necessario.

Successivamente, accedi al primo livello dell'immagine PSD utilizzando la sintassi psdImage.getLayers()[0] per ottenere un riferimento all'oggetto del livello da manipolare.

Per modificare il livello, crea un oggetto Graphics passando il livello come parametro. Questo oggetto fornisce vari metodi per disegnare forme e applicare pennelli.

Un oggetto Pen viene utilizzato per definire il colore e lo spessore del contorno delle forme. Allo stesso modo, i pennelli come LinearGradientBrush vengono utilizzati per definire i colori di riempimento.

Disegna forme sul livello utilizzando metodi come graphics.drawEllipse() per delineare le forme e graphics.fillEllipse() per riempirle.

Dopo aver apportato le modifiche desiderate al livello, salva l'immagine PSD modificata utilizzando psdImage.save().

Inoltre, puoi salvare l'immagine modificata in altri formati come PNG utilizzando le opzioni appropriate.

E questo è tutto! Hai utilizzato con successo l'API grafica di Aspose.PSD per Java per modificare i livelli in un file PSD. Esplora ulteriori funzionalità della libreria Aspose.PSD per migliorare le tue capacità di modifica delle immagini.

Per favore, controlla l'esempio completo.

## **Esempio**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-graphics-api.java" >}}
