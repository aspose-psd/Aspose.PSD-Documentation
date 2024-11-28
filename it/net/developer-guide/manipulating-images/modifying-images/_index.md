---
title: Modifica Immagini
type: docs
weight: 50
url: /it/net/modifica-immagini/
---

## **Dithering per Immagini Raster**
Il dithering è una tecnica per creare l'illusione di nuovi colori e sfumature variando il pattern di punti che effettivamente compongono un'immagine. È il mezzo più comune per ridurre la gamma di colori delle immagini a 256 (o meno) colori. Aspose.PSD fornisce il supporto al dithering per la classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) introducendo il metodo Dither che accetta due parametri. Il primo è di tipo DitheringMethod da applicare con due possibili opzioni: FloydSteinbergDithering e ThresholdDithering. Il secondo parametro per il metodo [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) è il BitCount in formato intero. BitCount definisce la dimensione del campionamento per il risultato del dithering. Il valore predefinito è 1 che rappresenta bianco e nero, mentre i valori consentiti sono 1, 4, 8 generando palette con rispettivamente 2, 4 e 256 colori.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.cs" >}}

## **Regolazione Luminosità, Contrasto e Gamma**
I ritocchi colore nelle immagini digitali sono una delle funzionalità principali che la maggior parte delle librerie di elaborazione delle immagini fornisce. I ritocchi colore possono essere categorizzati nei seguenti modi:

1. La luminosità si riferisce alla chiarezza o scurità di un colore. Aumentare la luminosità di un'immagine illumina tutti i colori mentre diminuirla scurisce tutti i colori.
1. Il contrasto si riferisce a rendere più evidenti gli oggetti o i dettagli all'interno di un'immagine. Aumentare il contrasto di un'immagine aumenta la differenza tra le aree chiare e scure in modo che le aree chiare diventino più chiare e le aree scure diventino più scure. Diminuire il contrasto farà sì che le aree più chiare e più scure rimangano approssimativamente le stesse ma l'immagine complessiva diventa più omogenea.
1. Il gamma ottimizza il contrasto e la luminosità della luce indiretta che illumina un oggetto nell'immagine.
### **Regolazione Luminosità**
Aspose.PSD fornisce il metodo [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) per la classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) che può essere utilizzato per regolare la luminosità dell'immagine passando un valore intero come parametro. Il valore più alto del parametro indica un'immagine più luminosa. Di seguito è riportata l'immagine originale e l'immagine risultante per il confronto.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.cs" >}}


### **Regolazione Contrasto**
Il metodo [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) esposto dalla classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) può essere utilizzato per regolare il contrasto di un'immagine passando un valore float come parametro.

Il valore più alto del parametro indica un contrasto più accentuato nell'immagine fornita. Di seguito è riportata l'immagine originale e l'immagine risultante per il confronto.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.cs" >}}
### **Regolazione Gamma**
Il metodo [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) esposto dalla classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) ha due versioni. Uno degli overload accetta un valore float e esegue la correzione Gamma per i coefficienti dei canali rosso, blu e verde. Mentre l'altro overload accetta tre parametri float rappresentanti ciascun coefficente di colore separatamente. Il seguente esempio di codice dimostra come regolare il Gamma su un'immagine.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.cs" >}}
## **Sfocatura di un'Immagine**
Questo articolo dimostra l'uso di Aspose.PSD per .NET per eseguire l'effetto Sfocatura su un'immagine. Le API di Aspose.PSD hanno esposto metodi efficienti e facili da usare per raggiungere questo obiettivo. Aspose.PSD for .NET ha esposto la classe [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) per creare un effetto sfocatura al volo. La classe [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) richiede valori di raggio e sigma per creare un effetto sfocatura su un'immagine. I passaggi per eseguire il ridimensionamento sono semplici come di seguito:

1. Caricare un'immagine utilizzando il metodo di fabbrica Load esposto dalla classe Image.
1. Convertire l'immagine in [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. Creare un'istanza della classe [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) con il costruttore predefinito o fornire valori di raggio e sigma nel costruttore.
1. Chiamare il metodo [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter specificando il rettangolo come limiti dell'immagine e un'istanza della classe [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions).
1. Salvare i risultati.

Il seguente esempio di codice dimostra come creare un effetto sfocatura su un'immagine.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-BluranImage-BluranImage.cs" >}}
## **Verificare la Trasparenza dell'Immagine**
Questo articolo dimostra l'uso di Aspose.PSD per .NET per verificare la trasparenza dell'immagine. I passaggi per verificare la trasparenza dell'immagine sono semplici come di seguito:

1. Caricare un'immagine utilizzando il metodo di fabbrica [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) esposto dalla classe [Image](https://reference.aspose.com/psd/net/aspose.psd/image).
1. Verificare l'opacità dell'immagine; se l'opacità è zero, l'immagine è trasparente.
1. Il seguente esempio di codice dimostra come verificare se l'immagine è trasparente o meno.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.cs" >}}
## **Implementare un Compressore GIF Lossy**
Utilizzando Aspose.PSD per .NET, gli sviluppatori possono impostare una differenza di pixel. La compressione GIF si basa su un "dizionario" di stringhe di pixel viste. Un codificatore normale cerca nel dizionario la stringa più lunga di pixel che corrisponde esattamente ai pixel nell'immagine. Un codificatore lossy sceglie la stringa più lunga di pixel che è "abbastanza simile" ai pixel nell'immagine. Di seguito è riportato il codice dimostrativo della suddetta funzionalità.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.cs" >}}
## **Implementare il Ri-dimensionamento Bicubico**
Il ri-dimensionamento significa che stai cambiando le dimensioni dei pixel di un'immagine. Quando campionata, stai eliminando pixel e quindi cancellando informazioni e dettagli dall'immagine. Quando ingrandisci, stai aggiungendo pixel. Photoshop aggiunge questi pixel usando l'interpolazione. Questo articolo dimostra come puoi eseguire il Ri-dimensionamento Bicubico utilizzando Aspose.PSD per .NET.

Di seguito è riportato il codice dimostrativo della suddetta funzionalità.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.cs" >}}
## **Livello di Regolazione del Bilanciamento del Colore**
Questo articolo dimostra l'uso di Aspose.PSD per .NET per eseguire il **livello di regolazione del bilanciamento del colore** su un'immagine. Il livello di regolazione del bilanciamento del colore ti dà la possibilità di apportare regolazioni alla colorazione delle immagini. Presenta i tre canali di colore e i loro colori complementari e puoi regolare il bilanciamento di questi coppie per cambiare l'aspetto di una foto.

Di seguito è riportato il codice dimostrativo della suddetta funzionalità.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ColorBalanceAdjustment-ColorBalanceAdjustment.cs" >}}
## **Livello di Regolazione dell'Invertito**
Questo articolo dimostra come puoi eseguire il **livello di regolazione invertito** utilizzando Aspose.PSD for .NET.  Un livello di regolazione è un tipo speciale di livello utilizzato principalmente per la correzione del colore. Piuttosto che avere un proprio contenuto, regolano le informazioni sui livelli sottostanti. Il livello di regolazione invertito crea un effetto negativo di una foto invertendo i colori di un'immagine.

Di seguito è riportato il codice dimostrativo della suddetta funzionalità.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.cs" >}}
