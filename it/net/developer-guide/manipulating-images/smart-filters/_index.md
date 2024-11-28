---
title: Manipolazione intelligente dei filtri in Aspose.PSD for C#
weight: 100
type: docs
description: Esempi su come utilizzare i filtri intelligenti nei file PSD
keywords: [filtro intelligente, aggiungi rumore, sfocatura gaussiana, nitidezza, filtro, filtro psd, api psd, C#, csharp, esempio di codice]
url: it/net/filtri-intelligenti/
---

## Panoramica

Ci sono tre modi per applicare filtri intelligenti in Aspose.PSD per C#.

### Applicazione diretta del filtro

Questo esempio dimostra come applicare direttamente filtri intelligenti in Aspose.PSD per C#.

Prima, specifica il file PSD di origine, il file di output per l'immagine originale e il file di output per l'immagine aggiornata.

Successivamente, carica l'immagine PSD utilizzando il metodo `Image.Load` e convertila in un oggetto `PsdImage`.

Salva l'immagine originale utilizzando il metodo `Save` con il nome del file di output specificato.

Crea un oggetto `SharpenSmartFilter`, che rappresenta il filtro intelligente da applicare.

Recupera il livello regolare dall'immagine PSD utilizzando `psdImage.Layers[1]`.

Applica il `sharpenFilter` al livello regolare tre volte in un loop.

Infine, salva l'immagine aggiornata utilizzando il metodo `Save` con il nome del file di output specificato.

Questo codice dimostra come applicare direttamente filtri intelligenti in Aspose.PSD per C#. Utilizzando gli oggetti filtro appropriati e applicandoli ai livelli desiderati, è possibile ottenere gli effetti desiderati sulle immagini.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### Manipolazione dei filtri intelligenti negli oggetti intelligenti

Questo esempio mostra come manipolare i filtri intelligenti all'interno degli oggetti intelligenti.

Prima, specifica il file PSD di origine, il file di output per l'immagine originale e il file di output per l'immagine aggiornata.

Carica l'immagine PSD utilizzando il metodo `Image.Load` e convertila in un oggetto `PsdImage`.

Salva l'immagine originale utilizzando il metodo `Save` con il nome del file di output specificato.

Converti il secondo livello dell'immagine PSD in un oggetto `SmartObjectLayer`.

Modifica i filtri intelligenti. Questo esempio dimostra come lavorare con `GaussianBlurSmartFilter` e `AddNoiseSmartFilter`.

Per `GaussianBlurSmartFilter`, aggiorna i valori del filtro, inclusi raggio, modalità di miscelazione, opacità e stato abilitato.

Per `AddNoiseSmartFilter`, imposta la distribuzione del rumore su `NoiseDistribution.UNIFORM`.

Aggiungi nuovi elementi filtro al livello dell'oggetto intelligente: un altro `GaussianBlurSmartFilter` e `AddNoiseSmartFilter`.

Applica le modifiche utilizzando il metodo `UpdateResourceValues`.

Applica direttamente i filtri al livello e alla maschera del livello utilizzando rispettivamente i metodi `Apply` e `ApplyToMask`.

Salva l'immagine aggiornata utilizzando il metodo `Save` con il nome del file di output specificato.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### Applicazione di filtri intelligenti alla maschera del livello

I filtri intelligenti sono un potente strumento di modifica delle immagini che permettono agli utenti di applicare vari filtri ed effetti. Una tecnica interessante è applicarli alle maschere, che consentono di controllare precisamente le aree interessate dal filtro.

Una maschera è un'immagine in scala di grigi che determina la trasparenza di determinate aree dell'immagine, applicando selettivamente filtri, regolazioni o effetti.

Quando si applicano filtri intelligenti alle maschere, i filtri vengono applicati solo alle aree specificate dalla maschera. Questo controllo preciso consente di manipolare l'intensità e l'estensione del filtro.

Per informazioni più dettagliate ed esempi, fare riferimento alla [documentazione di Aspose.PSD per C#](https://docs.aspose.com/psd/net/).
