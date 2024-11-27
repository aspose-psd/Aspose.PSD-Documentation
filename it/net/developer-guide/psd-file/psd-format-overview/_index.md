---
title: Panoramica del formato PSD
type: docs
weight: 60
url: /it/net/panoramica-del-formato-psd/
---

## **Descrizione**
PSD, ovvero Photoshop Document, rappresenta il formato di file nativo di Adobe Photoshop utilizzato per il design grafico e lo sviluppo.

## **Specifiche del Formato di File** 
I dati in un file PSD sono memorizzati in ordine di byte big-endian. Ciò implica lo scambio di interi brevi e lunghi durante la lettura o la scrittura sulla piattaforma Windows. Il formato file di Photoshop è diviso in cinque parti principali. Esso contiene molti marcatori di lunghezza che possono essere utilizzati per spostarsi da una sezione all'altra. I marcatori di lunghezza sono solitamente riempiti con byte per arrotondare all'intervallo di 2 o 4 byte più vicino. Le cinque parti principali sono:

- Intestazione del File
- Dati della Modalità Colore
- Risorse Immagine
- Informazioni Livello e Maschera
- Dati Immagine

Per la conformità, i dati dovrebbero essere scritti in tutti questi campi della sezione, poiché Photoshop potrebbe cercare di leggere l'intera sezione. Ciò implica anche che zeri vengano scritti nei campi saltati durante la scrittura su un file. Il campo di lunghezza nelle sezioni delimitate dalla lunghezza dovrebbe essere utilizzato per decidere quando smettere di leggere. Nella maggior parte dei casi, il campo di lunghezza indica il numero di byte, non di record, a seguire. I punti seguenti devono essere tenuti presenti durante la lettura di un file:

- I valori nella colonna "Lunghezza" in tutte le tabelle sono in byte.
- Tutti i valori definiti come stringa Unicode consistono di:
- Un campo di lunghezza di 4 byte, che rappresenta il numero di caratteri nella stringa (non byte).
- La stringa di valori Unicode, due byte per carattere.

## **Caratteristiche del formato**
I file PSD possono includere livelli di immagine, livelli di regolazione, maschere di livello, annotazioni, informazioni sul file, parole chiave e altri elementi specifici di Photoshop. I file di Photoshop hanno l'estensione predefinita.PSD e presentano un'altezza e una larghezza massime di 30.000 pixel e un limite di lunghezza di due gigabyte.

## **Come può essere utilizzato**
1. Uno strumento per il Taglio di PSD.
1. [Convertire PSD](/it/psd/net/convertire-immagine-psd-in-formato-raster/) in HTML
1. Utilizzare [PSD come Modello](/it/psd/net/utilizzare-file-psd-come-modelli-per-le-carte-da-visita-di-automazione/) per Email
1. Dalla PSD all'HTML di un CMS specifico
1. Identikit nel File PSD (Disegno della Polizia)
1. Creare anteprime pseudo-3D utilizzando oggetti intelligenti per beni quali bottiglie, tazze, magliette, ecc.
1. Modifica rapida della PSD: Belezza automatica, Preimpostazioni, Oggetto Intelligente, Ritaglio Immagine del Livello Testo

E molto altro. Se hai realizzato qualcosa di grandioso con Aspose.PSD, condividi con noi il tuo caso di studio utilizzando i [Forum di Aspose](https://forum.aspose.com/).

Esempi aggiuntivi da cui puoi imparare:

- [Casi di Studio](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [Esempi](/it/psd/net/mostra-efficacia-html/)
