---
title: Support of Fill Layers
type: docs
weight: 90
url: /it/support-of-fill-layers/
---


## **Livelli di Riempimento con Riempimento a Motivi**
Questo articolo dimostra come riempire il livello di [PSD](https://wiki.fileformat.com/image/psd/) con il riempimento a motivi. Un Motivo è un'immagine, un colore, un'ombra o una linea utilizzata per riempire un'area di un'immagine. Si prega di utilizzare la classe Aspose.PSD.FileFormats.Psd.Layers.FillLayer per aggiungere un Motivo nel livello PSD. I seguenti frammenti di codice caricano un file PSD, accedono alla classe [Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) e impostano il Motivo utilizzando le proprietà [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConverzioneImmagini-PSD-LivelloRiempimentoConMotivo-LivelloRiempimentoConMotivo.cs" >}}



Ecco un altro esempio che dimostra come [Aspose.PSD](https://products.aspose.com/psd/net) renderizza il motivo utilizzando [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) e [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConverzioneImmagini-PSD-ImplementareLivelloRiempimentoConMotivo-ImplementareLivelloRiempimentoConMotivo.cs" >}}
## **Livelli di Riempimento con Riempimento a Gradiente**
Questo articolo dimostra l'utilizzo del riempimento a gradiente per riempire il livello PSD. Le API di Aspose.PSD hanno esposto metodi efficienti e facili da utilizzare per raggiungere questo obiettivo. Aspose.PSD ha esposto le classi [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) e [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) per aggiungere un effetto gradient in un livello.

I passaggi per riempire [il livello PSD](https://wiki.fileformat.com/image/psd/) con un riempimento a gradiente sono semplici come segue:

- Carica un file PSD come immagine utilizzando il metodo di fabbrica [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) esposto dalla classe [Image](https://reference.aspose.com/net/psd/aspose.psd/image).
- Imposta le proprietà delle impostazioni del riempimento dell'oggetto [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer).
- Crea una lista di [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) con colori richiesti e posizioni dei colori.
- Crea una lista di punti di trasparenza con opacità richiesta e posizione del punto di trasparenza.
- Chiama il metodo [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update).
- Salva i risultati.

Il seguente frammento di codice mostra come aggiungere un riempimento a gradiente per riempire il livello PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConverzioneImmagini-PSD-LivelloRiempimentoAGradiente-LivelloRiempimentoAGradiente.cs" >}}



**Ecco un altro esempio che utilizza la proprietà [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** per riempire il livello PSD con un riempimento a gradiente. Aspose.PSD supporta i seguenti tipi di gradienti tramite l'enumerazione GradientType:

- **GradientType.Linear:** In un gradiente lineare, il colore passa dalla tonalità iniziale alla fine in una linea retta.
- **GradientType.Radial:** In un gradiente radiale, i colori si propagano dal punto di inizio in un modello circolare.
- **GradientType.Angle:** In un gradiente angolare, il gradiente si sposta in senso antiorario intorno al punto di inizio.
- **GradientType.Reflected:** In un gradiente riflessivo, il colore è specchiato su entrambi i lati del punto di inizio.
- **GradientType.Diamond:** Il gradiente a rombo crea una forma romboidale dal punto di inizio.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConverzioneImmagini-PSD-LivelliRiempimentoAGradiente-LivelliRiempimentoAGradiente.cs" >}}
## **Supporto della Proprietà di Scala per il Livello di Riempimento a Gradiente**
Questo articolo dimostra come scalare il livello di riempimento con riempimento a gradiente utilizzando Aspose.PSD per .NET. A questo scopo, è stata aggiunta una nuova proprietà **Scale** in [**IGradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings)**.** 

Di seguito è mostrata la dimostrazione del codice che mostra come utilizzare la proprietà **Scale**.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConverzioneImmagini-PSD-SupportoDellaProprietàDiScala-SupportoDellaProprietàDiScala.cs" >}}
## **Livelli di Riempimento con Riempimento a Colore**
Questo articolo dimostra come riempire il livello di [PSD](https://wiki.fileformat.com/image/psd/) con un Colore. Si prega di utilizzare la classe [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) per aggiungere un Colore nel livello PSD. Il seguente frammento di codice carica un file PSD, accede alla classe del livello di riempimento e imposta il colore utilizzando la proprietà [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConverzioneImmagini-PSD-LivelloRiempimentoColore-LivelloRiempimentoColore.cs" >}}


