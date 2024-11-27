---
title: Manipolazione Smart Filter in Aspose.PSD per Python
weight: 100
type: docs
description: Esempi su come utilizzare Smart Filters nel file PSD
keywords: [smart filter, aggiungere rumore, sfocatura gaussiana, nitidezza, filtro, filtro psd, api psd, python, campioni di codice]
url: it/python-net/smart-filters/
---

## **Panoramica**

Ci sono 3 modi per applicare smart filters in Aspose.PSD per Python.

## **Applicazione diretta del filtro**
In questo esempio di codice, possiamo vedere un esempio di come applicare direttamente smart filters in Aspose.PSD per Python.

Prima, il codice specifica il file PSD di origine, il file di output per l'immagine originale e il file di output per l'immagine aggiornata.

Successivamente, il codice carica l'immagine PSD utilizzando il metodo Image.load() e la converte in un oggetto PsdImage.

L'immagine originale viene quindi salvata utilizzando il metodo save(), specificando il nome del file di output.

Viene creato un oggetto SharpenSmartFilter, che rappresenta il filtro intelligente da applicare.

Il codice recupera quindi il livello regolare dall'immagine PSD utilizzando im.layers[1].

Viene quindi utilizzato un ciclo per applicare lo sharpenFilter al livello regolare tre volte.

Infine, l'immagine aggiornata viene salvata utilizzando il metodo save() e il nome del file di output specificato.

Questo codice dimostra come applicare direttamente smart filters in Aspose.PSD per Python. Utilizzando gli oggetti filtro appropriati e applicandoli ai livelli desiderati, è possibile ottenere gli effetti desiderati sulle immagini.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-direct-apply.py" >}}

## **Manipolazione Smart Filters negli Smart Objects**

Prima, il codice specifica il file PSD di origine, il file di output per l'immagine originale e il file di output per l'immagine aggiornata.

L'immagine PSD viene caricata utilizzando il metodo Image.load() e quindi convertita in un oggetto PsdImage.

L'immagine originale viene salvata utilizzando il metodo save(), specificando il nome del file di output.

Il codice converte quindi il secondo livello dell'immagine PSD in un oggetto SmartObjectLayer, che rappresenta lo smart object layer.

Il codice procede quindi ad modificare i smart filters. In questo esempio, si dimostra come lavorare con due tipi di smart filters: GaussianBlurSmartFilter e AddNoiseSmartFilter.

Per il GaussianBlurSmartFilter, il codice aggiorna i valori del filtro, inclusi il raggio, la modalità di fusione, l'opacità e se è abilitato o meno.

Per l'AddNoiseSmartFilter, il codice imposta la distribuzione del rumore su NoiseDistribution.UNIFORM.

Successivamente, il codice aggiunge due nuovi elementi filtro allo smart object layer: un altro GaussianBlurSmartFilter e un AddNoiseSmartFilter.

Dopo aver aggiunto i nuovi filtri, il codice applica le modifiche utilizzando il metodo update_resource_values().

Infine, il codice dimostra come applicare direttamente i filtri al livello e alla maschera del livello utilizzando rispettivamente i metodi apply() e apply_to_mask().

L'immagine aggiornata viene quindi salvata utilizzando il metodo save() e il nome del file di output specificato.

Seguendo questo esempio di codice, è possibile imparare come lavorare con smart filters in Aspose.PSD per Python. La libreria fornisce una vasta gamma di smart filters, ognuno con il proprio set di proprietà e metodi che possono essere personalizzati per ottenere gli effetti desiderati sulle immagini.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-features.py" >}}

## **Applicazione di Smart Filters alla Maschera del Livello**

Applicazione di Smart Filters alle Maschere: Una Potente Tecnica di Modifica Immagine

I smart filters sono una funzionalità popolare nei software di editing di immagini che permettono agli utenti di applicare vari filtri ed effetti alle proprie immagini. Una tecnica interessante che si può ottenere utilizzando i smart filters è applicarli alle maschere. In questo articolo, esploreremo come applicare i smart filters alle maschere e discuteremo il loro utilizzo nel mondo del photo editing.

Cos'è una Maschera? Prima di addentrarci nell'applicare i smart filters alle maschere, comprendiamo prima cos'è una maschera. Nel photo editing, una maschera è un'immagine in scala di grigi che determina la trasparenza di determinate aree di un'immagine. Una maschera può essere utilizzata per applicare selettivamente filtri, regolazioni o effetti a parti specifiche di un'immagine, lasciando immutate altre aree.

Applicazione di Smart Filters alle Maschere: Quando si applicano smart filters alle maschere, i filtri vengono applicati solo alle aree specificate dalla maschera. Ciò consente un controllo preciso su quali parti dell'immagine vengono influenzate dal filtro. Manipolando la maschera, è possibile determinare l'intensità ed estensione dell'effetto del filtro.

Si prega di controllare l'esempio precedente e il metodo: [Applicare Filtro Smart alla Maschera - Riferimento API](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)
