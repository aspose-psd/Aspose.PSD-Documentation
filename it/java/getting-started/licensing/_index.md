---
title: Licenza
type: docs
weight: 60
url: /it/java/licenza/
---

## **Limitazioni della Versione di Valutazione**
È possibile scaricare una versione di valutazione di Aspose.PSD per Java dalla [pagina di download](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). La versione di valutazione fornisce le stesse funzionalità della versione con licenza completa del componente con un paio di restrizioni. Quando si acquista Aspose.PSD, l'applicazione della licenza rimuove qualsiasi restrizione dalla versione di valutazione installata.

La versione di valutazione di Aspose.PSD per Java fornisce funzionalità complete del prodotto, con solo due limitazioni:

- **Un watermark su ogni immagine**: Ogni immagine che si salva, modifica o esporta ha un watermark che legge "Solo Valutazione. Creato con Aspose.PSD. Copyright 2018-2019 Aspose Pty Ltd.". Per immagini piccole, dove il watermark completo non può essere inserito, ci sono due linee diagonali sull'immagine al suo posto.
- **Nessun supporto per funzionalità di disegno di base**: In modalità di valutazione, i pixel dell'immagine non possono essere caricati o salvati nell'immagine. Per disegnare immagini, utilizzare invece la funzionalità di disegno avanzata. Questa limitazione influisce sulle funzionalità che dipendono dalla funzionalità di disegno di base. Aspose.PSD per Java consente di registrare il proprio formato di file. Tuttavia, questa funzionalità dipende dalla funzionalità di disegno di base, quindi non ha senso utilizzarla in modalità di valutazione perché non è possibile modificare il contenuto di quei file.

{{% alert color="primary" %}} 

Se si desidera testare Aspose.PSD per Java senza le limitazioni della versione di valutazione, richiedere una licenza temporanea di 30 giorni. Fare riferimento a [Come ottenere una Licenza Temporanea?](https://purchase.aspose.com/temporary-license) per ulteriori informazioni.

{{% /alert %}} 
## **Informazioni sul File di Licenza**
Una volta soddisfatti della valutazione di Aspose.PSD, è possibile acquistare una licenza sul [sito web di Aspose](https://purchase.aspose.com/default.aspx). Familiarizzarsi con i diversi tipi di abbonamento offerti. Per eventuali domande, non esitare a contattare il [team vendite di Aspose](https://company.aspose.com/contact).

Ogni licenza di Aspose comprende un abbonamento annuale per gli aggiornamenti software. Dopo il primo anno, rinnovare gli abbonamenti per continuare a ricevere le ultime funzionalità e correzioni. Il supporto tecnico è gratuito e illimitato ed è fornito sia agli utenti con licenza che a quelli in fase di valutazione tramite i nostri [Forum di Supporto](https://forum.aspose.com/).

La licenza è un file XML che contiene dettagli come il nome del prodotto, il numero di sviluppatori autorizzati, la data di scadenza dell'abbonamento e così via. Il file è firmato digitalmente, quindi non modificarlo: anche aggiungere accidentalmente una interlinea extra invalida il file.

Dopo aver acquistato Aspose.PSD, è necessario applicare la licenza prima di creare, modificare o comunque manipolare le immagini. Se si dimentica di applicare la licenza, le immagini di output avranno un watermark di valutazione.
È sufficiente impostare la licenza una volta per ogni applicazione o processo che si sviluppa.
## **Applicazione della Licenza**
È possibile scaricare una versione di valutazione di **Aspose.PSD** per Java dalla [sua pagina di download](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). La versione di valutazione fornisce assolutamente le stesse capacità della versione con licenza del prodotto. Inoltre, la versione di valutazione diventa semplicemente con licenza quando si acquista una licenza e si aggiungono un paio di righe di codice per applicare la licenza.

Una volta soddisfatti della valutazione di **Aspose.PSD**, è possibile [acquistare una licenza](http://www.aspose.com/Purchase/Components/Default.aspx) sul sito web di Aspose. Familiarizzarsi con i diversi tipi di abbonamento offerti. Per eventuali domande, non esitare a contattare il team vendite di Aspose.

Ogni licenza di Aspose comprende un abbonamento annuale per aggiornamenti gratuiti a nuove versioni o correzioni rilasciate durante questo periodo. Il supporto tecnico è gratuito e illimitato e fornito sia agli utenti con licenza che a quelli in fase di valutazione.

{{% alert color="primary" %}} 

Se si desidera testare **Aspose.PSD** senza le limitazioni della versione di valutazione, richiedere una licenza temporanea di 30 giorni. Fare riferimento a [Come ottenere una Licenza Temporanea?](http://www.aspose.com/corporate/how-to-get-temporary-license.aspx) per ulteriori informazioni.

{{% /alert %}} 
### **Impostazione di una Licenza**
La licenza è un file XML di testo che contiene dettagli come il nome del prodotto, il numero di sviluppatori autorizzati, la data di scadenza dell'abbonamento e così via. Il file è firmato digitalmente, quindi non modificarlo; anche l'aggiunta accidentale di una interlinea extra nel file lo invalida.

È necessario impostare una licenza prima di utilizzare **Aspose.PSD** se si desidera evitare le sue limitazioni di valutazione. È necessario impostare una licenza solo una volta per ogni applicazione o processo.

La licenza può essere caricata da uno stream o file nei seguenti posizioni:

1. Percorso esplicito.
1. La cartella che contiene Aspose.PSD.jar.

Utilizzare il metodo [License](http://www.aspose.com/api/java/psd/com.aspose.psd/classes/License).setLicense per concedere la licenza al componente. Spesso il modo più semplice per impostare una licenza è mettere il file di licenza nella stessa cartella di Aspose.PSD.jar e specificare solo il nome del file senza il percorso come mostrato nell'esempio seguente:
#### **Esempio 1**
In questo esempio **Aspose.PSD** cercherà di trovare il file di licenza nella cartella che contiene i JAR dell'applicativo.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense("Aspose.PSD.Java.lic");

{{< /highlight >}}
#### **Esempio 2**
Inizializza una licenza da uno stream.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense(new java.io.FileInputStream("Aspose.PSD.Java.lic"));

{{< /highlight >}}
### **Convalida della Licenza**
È possibile convalidare se la licenza è stata impostata correttamente o meno. La classe License ha il campo isLicensed che restituirà true se la licenza è stata impostata correttamente.

**Java**

{{< highlight csharp >}}

 License license = new License();

license.setLicense("Aspose.PSD.Java.lic");

if (License.isLicensed()) {

    System.out.println("Licenza impostata!");

}

{{< /highlight >}}
## **Dove Applicare una Licenza nella tua Applicazione**
Dove si applica una licenza dipende dal tipo di applicativo in fase di sviluppo. Seguire queste semplici regole:

- La licenza deve essere impostata solo una volta per dominio dell'applicazione. Chiamare License.setLicense più volte non è dannoso ma spreca tempo di elaborazione.
- Applicare la licenza prima di chiamare qualsiasi classe di Aspose.PSD.
- **Applicazioni Java**: chiamare License.SetLicense nel codice di avvio.
- **Libreria di Classi**: chiamare License.setLicense da un costruttore statico della classe che utilizza Aspose.PSD. Il costruttore statico viene eseguito prima che venga creata un'istanza della classe, assicurando che la licenza di Aspose.PSD sia correttamente impostata.
## **Utilizzo di Più Prodotti Aspose**
Se si utilizzano più di un prodotto Aspose nella propria applicazione, ad esempio Aspose.PSD e Aspose.Cells, ecco alcuni utili consigli.

- **Applicare la licenza per ogni prodotto Aspose separatamente**. Anche se si dispone di un unico file di licenza per tutti i componenti, ad esempio 'Aspose.Total.lic', è comunque necessario chiamare License.setLicense separatamente per ciascun prodotto Aspose nell'applicazione.
- **Utilizzare un nome di classe di licenza completamente qualificato**. Ogni prodotto Aspose ha una classe License nel suo namespace. Ad esempio, Aspose.PSD ha com.aspose.psd.license.License e Aspose.Cells ha com.aspose.cells.License. Utilizzare un nome di classe completamente qualificato evita confusione su quale licenza viene applicata a quale prodotto.
