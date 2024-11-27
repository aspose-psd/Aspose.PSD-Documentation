---
title: Rendering di livelli di testo ruotati
type: docs
weight: 40
url: /it/rendering-di-livelli-di-testo-ruotati/
---

## **Rendering di livelli di testo ruotati**
Aspose.PSD fornisce la funzionalità di rendering di livelli di testo ruotati. Nell'esempio seguente, un file PSD esistente viene caricato passando il percorso del file al metodo statico Load della classe Image. Ora chiamare il metodo [Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) dell'istanza [PsdImage](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage).

Il codice seguente ti mostra come rendere i [livelli di testo](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/textlayer) ruotati.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenderingOfRotatedTextLayer-RenderingOfRotatedTextLayer.cs" >}}
## **Ruota maschera vettoriale e livelli di testo**
Aspose.PSD fornisce la funzionalità di ruotare le maschere vettoriali e i livelli di testo. Aspose.PSD ha esposto il metodo RotateFlip per ruotare i livelli di maschera vettoriale e di testo. I passaggi per ruotare i livelli sono semplici come segue:

- Carica un file PSD come un'immagine utilizzando il metodo di fabbrica Load esposto dalla classe Image.
- Imposta il [RotateFlipType](https://reference.aspose.com/psd/net/aspose.psd/rotatefliptype) richiesto.
- Chiama il metodo [RotateFlip](https://reference.aspose.com/psd/net/aspose.psd/image/methods/rotateflip)
- Salva i risultati.

Il codice seguente ti mostra come ruotare i livelli di maschera vettoriale e di testo.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfRotateLayer-SupportOfRotateLayer.cs" >}}
