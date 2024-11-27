---
title: Manipolazione Smart Filter in Aspose.PSD per Java
weight: 100
type: docs
description: Esempi su come utilizzare Smart Filter in file PSD
keywords: [smart filter, aggiungi rumore, sfocatura gaussiana, nitidezza, filtro, filtro psd, api psd, java, esempio di codice]
url: it/java/smart-filters/
---

## **Panoramica**

Ci sono 3 metodi per applicare smart filter in Aspose.PSD per Java.

## **Applicazione diretta del filtro**

Questo esempio di codice dimostra come applicare direttamente smart filter in Aspose.PSD per Java.

Inizialmente, il codice definisce il file PSD di origine, il file di output per l'immagine originale e il file di output per l'immagine aggiornata.

Successivamente, il codice carica l'immagine PSD utilizzando il metodo Image.load() e la converte in un oggetto PsdImage.

L'immagine originale viene salvata utilizzando il metodo save(), specificando il nome del file di output.

Viene istanziato un oggetto SharpenSmartFilter per rappresentare il filtro smart desiderato.

Successivamente, il codice recupera il layer regolare dall'immagine PSD utilizzando psdImage.getLayers()[1].

Viene utilizzato un ciclo per applicare il filtro di nitidezza al layer regolare tre volte.

Infine, l'immagine aggiornata viene salvata utilizzando il metodo save() con il nome del file di output fornito.

Questo codice esemplifica l'applicazione diretta di smart filter in Aspose.PSD per Java. Utilizzando gli opportuni oggetti filtro e applicandoli ai layer desiderati, è possibile ottenere gli effetti desiderati sulle immagini.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-direct-apply.java" >}}

## **Manipolazione Smart Filter negli Smart Objects**

Questo frammento di codice illustra come manipolare smart filter all'interno degli smart object in Aspose.PSD per Java.

Inizialmente, il codice definisce il file PSD di origine, il file di output per l'immagine originale e il file di output per l'immagine aggiornata.

L'immagine PSD viene caricata utilizzando il metodo Image.load() e poi convertita in un oggetto PsdImage.

L'immagine originale viene salvata utilizzando il metodo save(), specificando il nome del file di output.

Successivamente, il codice converte il secondo layer dell'immagine PSD in un oggetto SmartObjectLayer, rappresentante lo smart object layer.

Il codice quindi dimostra la modifica di smart filter, mostrando due tipi: GaussianBlurSmartFilter e AddNoiseSmartFilter.

Per GaussianBlurSmartFilter, il codice aggiorna i valori del filtro come raggio, modalità di blending, opacità e stato di attivazione.

Per AddNoiseSmartFilter, il codice imposta la distribuzione del rumore su NoiseDistribution.Uniform.

Successivamente, il codice aggiunge due nuovi elementi di filtro allo smart object layer: un altro GaussianBlur
