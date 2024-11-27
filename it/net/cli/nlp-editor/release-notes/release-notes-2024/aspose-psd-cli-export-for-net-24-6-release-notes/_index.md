---
title: Note sulla versione di rilascio di Aspose.PSD CLI NLP Editor per .NET 24.6
type: docs
weight: 90
url: /it/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione per [Aspose.PSD CLI NLP Editor per .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                                                 | **Categoria** |
|:----------- |:------------------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Rilascio iniziale delle applicazioni CLI di Aspose.PSD: Aspose.PSD.CLI.Export e Aspose.PSD.CLI.NLP.Editor | Miglioramento |


## **Esempi di utilizzo:**

**PSDNET-2110. Rilascio iniziale dell'applicazione Aspose.PSD CLI NLP Editor**

## **Utilizzo da riga di comando:**

{{% alert color="primary" %}}
Installare prima questo strumento dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Prima dell'utilizzo iniziale, consigliamo di eseguire il seguente comando:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Dopo questo comando, sarà possibile eseguire questa applicazione con il nome abbreviato nlp.cli anziché Aspose.PSD.CLI.NLP.Editor. È possibile specificare il proprio nome abbreviato.
{{% /alert %}}

**Esempi di utilizzo**

1. Questo comando convertirà il primo file trovato (che può essere aperto con Aspose.PSD) dalla cartella corrente e lo salverà in formato png con trasparenza. Inoltre, la licenza verrà configurata. È necessario specificare la licenza solo una volta. Nei successivi utilizzi, la licenza sarà utilizzata dal percorso specificato. Questo comando mostrerà il log dettagliato dell'elaborazione NLP se disponibile.
{{< highlight bash >}}nlp.cli Converti file da questa cartella in formato png con alfa --licenza "C:\Aspose\FileLicenza.lic --dettagliato "{{< /highlight >}}

2. Questo comando troverà il file con il nome più simile a "smth.psd". Successivamente, regolerà il contrasto e lo salverà in jpeg con la migliore qualità. Il nome del file di output verrà stampato. Sarà smth.jpg
{{< highlight bash >}}Regola il contrasto al 10 dello strato con nome ellisse nel file smth.psd e salvato in output.jpg con la migliore qualità{{< /highlight >}}

3. Questo comando ruoterà il file nel percorso specificato e ne ridurrà le dimensioni al 25%. Il file di output verrà stampato. Sarà salvato nella cartella corrente della console.
{{< highlight bash >}}Ridimensiona il file C:\Utenti\someuser\Desktop\input.psd al 25%{{< /highlight >}}

4. Questo comando troverà il file input.psd in  C:\Utenti\someuser\Desktop\. Successivamente, troverà lo strato con indice 3 e lo ridurrà alla larghezza di 50px e all'altezza di 100px. Questo strato sarà quindi salvato come PDF in C:\Utenti\someuser\Desktop\output.pdf
{{< highlight bash >}}Ridimensiona lo strato con indice 3 di C:\Utenti\someuser\Desktop\input.psd alla larghezza di 50 e all'altezza di 100 e salvalo in C:\Utenti\someuser\Desktop\output.pdf{{< /highlight >}}

5. Questo comando aprirà smth.psd nella cartella corrente, ma tutti gli effetti saranno disattivati. Successivamente, il file sarà convertito in formato BMP e salvato come output.bmp nella cartella corrente.
{{< highlight bash >}}Apri smth.psd senza effetti e salvalo in output.bmp{{< /highlight >}}

**Avvertenza**

Questa è un'applicazione sperimentale. Provare e lasciare un feedback. Qualsiasi commento è molto apprezzato. Vogliamo portare l'applicazione senza codice al livello successivo. La facile integrazione con qualsiasi pipeline di compilazione o processo aziendale è il nostro obiettivo.
