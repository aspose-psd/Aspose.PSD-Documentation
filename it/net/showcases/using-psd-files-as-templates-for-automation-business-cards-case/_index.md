---
title: Utilizzo dei file PSD come modelli per l'automazione - Caso dei biglietti da visita
type: docs
weight: 10
url: /it/net/utilizzo-dei-file-psd-come-modelli-per-lautomazione-caso-dei-biglietti-da-visita/
---

### **Panoramica**
Questo articolo descrive casi spesso utilizzati in cui è necessario aggiornare alcuni livelli in un [file PSD](https://wiki.fileformat.com/image/psd/) in modo programmato, quando il file PSD/PSB ha una struttura simile a un modello noto. Questo può essere utilizzato per creare un grande numero di biglietti da visita per persone diverse (Caso dei biglietti da visita). Oppure è necessario effettuare una traduzione del file PSD in diverse lingue con la sostituzione di alcuni materiali grafici al suo interno.

Dopo aver letto questo articolo, saprai come fare questo:

![todo:image_alt_text](utilizzo-dei-file-psd-come-modelli-per-lautomazione-caso-dei-biglietti-da-visita_1.png)
## **Caso semplice**
Ad esempio, hai qualche Modello PSD con i nomi dei livelli noti. Quindi è necessario cambiare, aggiornare o sostituire il Livello PSD tramite C#. Prima di tutto è necessario aprire il file del modello con Aspose.PSD.

Come aprire un file PSD tramite C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-PsdFileAsATemplate-Frammento-1.cs" >}}

![todo:image_alt_text](utilizzo-dei-file-psd-come-modelli-per-lautomazione-caso-dei-biglietti-da-visita_2.png)

Successivamente dobbiamo trovare un livello che desideriamo sostituire per nome. Ecco una semplice implementazione per questo.

Come trovare il livello nel file PSD per nome

{{< gist "aspose-com-gists" "8a4d34ccf28a7458c0dce974140" "Documentazione-CSharp-Aspose-PsdFileAsATemplate-Frammento-2.cs" >}}



Una volta trovato il livello, possiamo aggiornarlo in modo comune, utilizzando [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics):

Come disegnare sullo strato Graphics del PSD

{{< gist "aspose-com-gists" "8a4d34ccf28a7458c0dce974e149" "Documentazione-CSharp-Aspose-PsdFileAsATemplate-Frammento-3.cs" >}}


In questo caso, disegniamo una nuova immagine [PNG](https://wiki.fileformat.com/image/png/) sullo strato PSD esistente, quindi i vecchi dati saranno persi nel nuovo file.

Ma se avessimo bisogno anche di aggiornare il testo? Il processo sarà simile. Trova lo [strato di testo](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/testolivello) per nome e poi [aggiorniamo il Livello di testo del file di Photoshop](/psd/it/net/renderizza-testo-con-colori-differenziati-nel-livello-di-testo/).

Come aggiornare un Livello di testo in Photoshop usando C#

{{< gist "aspose-com-gists" "8a4d34ccf28a7458c0dce974175" "Documentazione-CSharp-Aspose-PsdFileAsATemplate-Frammento-4.cs" >}}


Alla fine dobbiamo salvare le nostre modifiche:

Come salvare un file PSD modificato utilizzando [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4d34ccf28a7458c0dce974175" "Documentazione-CSharp-Aspose-PsdFileAsATemplate-Frammento-5.cs" >}}


Immagine risultante:

![todo:image_alt_text](utilizzo-dei-file-psd-come-modelli-per-lautomazione-caso-dei-biglietti-da-visita_3.png)


## **Un caso complesso con funzionalità aggiuntive**
Sopra abbiamo mostrato il modo più semplice per sostituire un'immagine in uno strato del file PSD.

Ma Aspose.PSD può offrire funzionalità aggiuntive più complesse come l'aggiunta di un nuovo livello, la rimozione di vecchi livelli e l'aggiornamento dello strato di testo utilizzando stili diversi nel testo multilinea.

Possiamo trovare lo [Strato](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/strato) che vogliamo sostituire, quindi troviamo il suo indice nell'elenco degli Strati, lo rimuoviamo e inseriamo un nuovo Strato dopo averlo creato da un [file Jpeg](https://wiki.fileformat.com/image/jpeg/) nello stesso posto.

Crea un nuovo strato da un file e inseriscilo nell'immagine PSD utilizzando [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-PsdFileAsATemplate-Frammento-6.cs" >}}


Alla fine di questo frammento di codice, correggiamo la posizione dello strato e salviamo il nuovo array di livelli nell'Immagine Psd.

Come copiare le proprietà dello strato [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging/fileformats/psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-PsdFileAsATemplate-Frammento-7.cs" >}}



E dopo tutto ciò, è necessario aggiornare gli strati di testo nell'immagine PSD esistente tramite C#. Aspose.PSD supporta [l'aggiornamento del Livello di testo per Porzioni](/psd/it/net/lavorare-con-gli-strati-di-testo/). Ogni [porzione di testo](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/testo/porzione-di-testo) ha una combinazione unica di proprietà di stile e paragrafo.

Come copiare le proprietà dello strato [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging/fileformats/psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-PsdFileAsATemplate-Frammento-8.cs" >}}


Come risultato, abbiamo modificato il modello PSD tramite codice con un nuovo Livello da un file Jpeg, Png, J2k, Bmp, Gif o Tiff e testo multilinea con [stili diversi](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-esempi-csharp-aspose-modifica-e-conversione-immagini-psd-renderizzazionedistilidiversiinunlivelloditesto-renderizzazionedistilidiversiinunlivelloditesto-cs) in ogni riga.

![todo:image_alt_text](utilizzo-dei-file-psd-come-modelli-per-lautomazione-caso-dei-biglietti-da-visita_4.png)
