---
title: Applicazione Aspose.PSD CLI Editor NLP per .NET
type: docs
weight: 10
url: /it/net/cli/nlp-editor/
is_root: false
keywords: CLI Strumento Photoshop NLP Elaborazione-Linguaggio-Naturale PSD Console Libreria C# API PSD
description: Applicazione Aspose.PSD-based NLP Editor CLI per formati di file PSD, PSB e AI. Automazione CI/CD senza codice. Supporta l'elaborazione del linguaggio naturale per la modifica dei file PSD. Basta scrivere la tua richiesta in linguaggio naturale per eseguire diverse operazioni come conversione, regolazione, ridimensionamento e altro ancora. Non richiede l'installazione di Adobe Photoshop o Adobe Illustrator e può essere eseguito dalla console senza codice aggiuntivo.
---

**![Logo prodotto Aspose.PSD per .NET](home_1.png)**

**Benvenuti nell'Applicazione Aspose.PSD NLP Editor CLI per .NET**

L'applicazione Aspose.PSD CLI NLP Editor è un'utilità console leggera per modificare file PSD utilizzando comandi in linguaggio naturale. Facile integrazione nei flussi di lavoro CI/CD.

**Disclaimer**

Questa è un'applicazione sperimentale. Provala e lascia un feedback. Qualsiasi feedback è molto apprezzato. Vogliamo portare l'applicazione senza codice al livello successivo. La nostra meta è l'integrazione semplice in qualsiasi flusso di lavoro di creazione o processo aziendale.

**Funzionalità principali dell'Applicazione Aspose.PSD NLP Editor CLI per .NET**

1. Eseguire operazioni su file PSD, PSB, AI utilizzando comandi in linguaggio naturale.
2. Supporta varie operazioni come conversione, regolazione, ridimensionamento e altro ancora.
3. Automazione CI/CD senza codice.
4. Supporta la scrittura di richieste in linguaggio naturale per la modifica dei file PSD.

## **Utilizzo dalla riga di comando:**

{{% alert color="primary" %}}
Installare prima questo strumento dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Prima dell'utilizzo iniziale, raccomandiamo di eseguire il seguente comando:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Dopo questo comando sarai in grado di eseguire questa applicazione con il nome abbreviato nlp.cli anziché Aspose.PSD.CLI.NLP.Editor. Puoi specificare il tuo nome abbreviato personalizzato.
{{% /alert %}}

**Parametri disponibili per l'Applicazione Crop Aspose.PSD.CLI**

| **Argomento** | **Descrizione**                         |
|:-------------|:----------------------------------------|
| qualsiasi testo     | Richiesto. Il tuo comando in lingua naturale per aggiornare il file PSD o PSB      |
| licenza      | Percorso della licenza.                    |
| verbose      | Mostra più informazioni su un comando specifico. |
| setup        | Crea un file bat nella cartella degli strumenti per una rapida chiamata dalla console. Esempio: --setup psd.nlp. Quindi puoi chiamare lo strumento con il comando psd.nlp |

**Esempi di utilizzo**

1. Questo comando convertirà il primo file trovato (che può essere aperto con aspose.psd) dalla cartella corrente e lo salverà nel formato png con trasparenza. Inoltre, la licenza sarà impostata. È necessario specificare la licenza solo una volta. Le esecuzioni successive utilizzeranno la licenza dal percorso specificato. Questo comando mostrerà il log dettagliato del NLP processing, se disponibile.
{{< highlight bash >}}
  nlp.cli Converti file da questa cartella nel formato png con canale alfa --license "C:\Aspose\FileLicenza.lic --verbose "
{{< /highlight >}}

2. Questo comando troverà il file con il nome più simile a "smth.psd". Poi regolerà il contrasto e lo salverà in jpeg con la miglior qualità. Il nome del file di output verrà stampato. Sarà smth.jpg.
{{< highlight bash >}}
Regola il contrasto al 10 dello strato con nome ellipse nel file smth.psd e salvalo con la migliore qualità come output.jpg
{{< /highlight >}}

3. Questo comando ruoterà il file nel percorso specificato e ne ridurrà le dimensioni al 25%. Il file di output verrà stampato. Sarà salvato nella cartella corrente della console.
{{< highlight bash >}}
Ridimensiona il file C:\Utenti\qualcheutente\Desktop\input.psd del 25%
{{< /highlight >}}

4. Questo comando troverà il file input.psd in C:\Utenti\qualcheutente\Desktop\. Poi troverà lo strato con indice 3 e lo ridimensionerà alla larghezza di 50px e all'altezza di 100px. Poi questo strato sarà salvato come PDF in C:\Utenti\qualcheutente\Desktop\output.pdf
{{< highlight bash >}}
 Ridimensiona lo strato con indice 3 di C:\Utenti\qualcheutente\Desktop\input.psd alla larghezza 50 e all'altezza 100 e salvane una copia in C:\Utenti\qualcheutente\Desktop\output.pdf
 {{< /highlight >}}

 5. Questo comando aprirà smth.psd nella cartella corrente, ma tutti gli effetti saranno disabilitati. Poi convertirà questo file nel formato BMP e lo salverà come output.bmp nella cartella corrente.
 {{< highlight bash >}}
 Apri smth.psd senza effetti e salvane una copia come output.bmp
  {{< /highlight >}}

**Controlla le altre [Applicazioni Aspose.PSD CLI](https://docs.aspose.com/psd/net/cli) per .NET se hai bisogno di aggiungere supporto ai formati di file PSD, PSB e AI al tuo flusso di lavoro**

1. [Aspose.PSD CLI Convert](/psd/it/net/cli/convert)
2. [Aspose.PSD CLI Crop](/psd/it/net/cli/crop)
3. [Aspose.PSD CLI Resize](/psd/it/net/cli/resize)
4. [Aspose.PSD CLI Export](/psd/it/net/cli/export)
5. [Aspose.PSD CLI NLP Editor](/psd/it/net/cli/nlp-editor)

**Controlla Aspose.PSD per .NET o [altri platform]**

Le Applicazioni Aspose.PSD CLI sono una soluzione pronta all'uso per operazioni popolari. Se hai bisogno di una soluzione flessibile, controlla la versione completa di Aspose.PSD

1. [Aspose.PSD per .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD per Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD per Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Risorse Aspose.PSD per .NET**

Ecco i link a risorse utili che potresti aver bisogno per completare i tuoi compiti.

- [Documentazione online delle Applicazioni Aspose.PSD CLI per .NET](/psd/it/net/cli/conversion)
- [Note di rilascio delle Applicazioni Aspose.PSD CLI per .NET](/psd/it/net/cli/conversion/release-notes/)
- [Pagina del prodotto delle Applicazioni Aspose.PSD CLI .NET](https://products.aspose.com/psd/net/cli)
- [Guida di riferimento API di Aspose.PSD per .NET](https://reference.aspose.com/net/psd)
- [Scarica esempi nel repository GitHub](https://github.com/aspose-psd/CLI-Applications)
- [Forum di supporto gratuito per Aspose.PSD per .NET](https://forum.aspose.com/c/psd)
- [Helpdesk di supporto a pagamento per Aspose.PSD per .NET](https://helpdesk.aspose.com/)
