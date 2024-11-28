---
title: Supporto di livelli di riempimento
type: docs
weight: 50
url: /it/java/supporto-di-livelli-di-riempimento/
---


## **Supporto di livelli di riempimento con riempimento a colori**
Questo articolo dimostra come riempire un livello PSD con colore. Si prega di utilizzare Aspose.PSD.FileFormats.Psd.Layers.FillLayer per aggiungere un colore al livello PSD. I seguenti frammenti di codice caricano un file PSD, accedono alla classe FillLayer e impostano il colore utilizzando la proprietà FillLayer.FillSettings.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Esempi-src-main-java-com-aspose-psd-esempi-ModificaEConvertiImmagini-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **Supporto di livelli di riempimento con riempimento gradiente**
Questo articolo dimostra l'uso del riempimento gradiente per riempire un livello PSD. Le API di Aspose.PSD hanno esposto metodi efficienti e facili da usare per raggiungere questo obiettivo. Aspose.PSD ha esposto le classi GradientColorPoint e GradientTransparencyPoint per aggiungere l'effetto gradiente a un livello.

I passaggi per riempire un livello PSD con riempimento gradiente sono semplici come segue:

- Carica un file PSD come un'immagine utilizzando il metodo Load esposto dalla classe Image.
- Imposta le proprietà delle impostazioni dell'oggetto FillLayer.
- Crea un elenco di ColorPoints con colori richiesti e posizione dei colori.
- Crea un elenco di TransparencyPoints con opacità richiesta e posizione del punto di trasparenza.
- Chiama il metodo FillLayer.Update.
- Salva i risultati.



Il seguente frammento di codice ti mostra come aggiungere un riempimento gradiente per riempire un livello PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Esempi-src-main-java-com-aspose-psd-esempi-ModificaEConvertiImmagini-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **Effetto di contorno con riempimento a colori**
Questo articolo dimostra come rendere l'effetto di contorno con riempimento a colori. L'effetto di contorno viene utilizzato per aggiungere tratti e bordi a livelli e forme. Può essere utilizzato per creare linee a tinta unita, gradienti colorati e bordi a motivi.

I passaggi per rendere l'effetto di contorno con riempimento a colori sono semplici come segue:

- Imposta la proprietà **LoadEffectsResource**.
- Carica un file PSD come un'immagine utilizzando il metodo Load esposto dalla classe Image e definisci **PsdLoadOptions**.
- Imposta le proprietà delle impostazioni di **ColorFillSetting.**
- Salva i risultati.

Il seguente frammento di codice ti mostra come rendere l'effetto di contorno con riempimento a colori.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Esempi-src-main-java-com-aspose-psd-esempi-ModificaEConvertiImmagini-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}



