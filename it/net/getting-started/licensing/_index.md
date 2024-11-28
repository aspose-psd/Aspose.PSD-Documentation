---
title: Licensing
type: docs
weight: 70
url: /it/net/licensing/
description: Valuta la libreria PSD Photoshop C# da NuGet e applica la licenza utilizzando un file o uno stream per rimuovere eventuali restrizioni dalla versione di valutazione installata.
---

## **Limitazioni della Versione di Valutazione**
È possibile scaricare una versione di valutazione di Aspose.PSD per .NET da [NuGet](https://www.nuget.org/packages/Aspose.psd/). La versione di valutazione fornisce le stesse funzionalità della versione con licenza completa del componente con un paio di restrizioni. Acquistando Aspose.PSD, l'applicazione della licenza rimuove qualsiasi restrizione dalla versione di valutazione installata. La versione di valutazione di Aspose.PSD per .NET fornisce piena funzionalità del prodotto, con solo due limitazioni:

- **Un watermark su ogni immagine**: Qualsiasi immagine che si salva, modifica o esporta ha un watermark che riporta "Solo per Valutazione. Creato con Aspose.PSD. Copyright 2010-2018 Aspose Pty Ltd.". Immagini di dimensioni ridotte, dove il watermark completo non si adatta, hanno invece due linee diagonali attraverso l'immagine.
- **Nessun supporto per la funzionalità di disegno di base**: In modalità di valutazione, i pixel dell'immagine non possono essere caricati o salvati nell'immagine. Per disegnare immagini, utilizzare piuttosto la funzionalità di disegno avanzata. Questa limitazione influisce sulle funzionalità che dipendono dalla funzionalità di disegno di base. Aspose.PSD per .NET consente di registrare il proprio formato file. Tuttavia, questa funzionalità dipende dalla funzionalità di disegno di base quindi non ha senso utilizzarla in modalità di valutazione poiché non è possibile modificare il contenuto di quei file.

Se desideri testare Aspose.PSD per .NET senza le limitazioni della versione di valutazione, richiedi una licenza temporanea di 30 giorni. Consulta [Come ottenere una Licenza Temporanea?](https://purchase.aspose.com/temporary-license) per ulteriori informazioni.
## **Informazioni sul File di Licenza**
Una volta che sei soddisfatto della tua valutazione di Aspose.PSD, puoi acquistare una licenza sul [sito web di Aspose](https://purchase.aspose.com/default.aspx). Familiarizza con i diversi tipi di abbonamento offerti. Se hai domande, non esitare a contattare il [team commercial di Aspose](https://company.aspose.com/contact). Ogni licenza Aspose comprende un abbonamento annuale per gli aggiornamenti software. Dopo il primo anno, rinnova i tuoi abbonamenti per continuare a ottenere le ultime funzionalità e correzioni. Il supporto tecnico è gratuito e illimitato ed è fornito sia agli utenti con licenza sia agli utenti di valutazione tramite i nostri [Forum di Supporto](https://forum.aspose.com/). Il file di licenza è un file XML che contiene dettagli come il nome del prodotto, il numero di sviluppatori autorizzati, la data di scadenza dell'abbonamento e così via. Il file è firmato digitalmente, quindi non modificarlo: anche aggiungere involontariamente una riga extra lo rende non valido. Dopo aver acquistato Aspose.PSD, è necessario applicare la licenza prima di creare, modificare o manipolare immagini in altro modo. Se dimentichi di applicare la licenza, tutte le immagini di output avranno un watermark di valutazione. È sufficiente impostare la licenza una sola volta per ogni applicazione o processo che sviluppi.
## **Dove Applicare una Licenza nella tua Applicazione**
Dove si applica una licenza dipende dal tipo di applicazione che stai sviluppando. Segui queste semplici regole:

- Applica la licenza solo una volta per dominio dell'applicazione. Chiamare License.SetLicense più volte non è dannoso ma spreca tempo del processore.
- Applica la licenza prima di chiamare qualsiasi classe Aspose.PSD per .NET.
- **Applicazioni Windows Forms o Console**: chiamare License.SetLicense nel codice di avvio, prima di utilizzare qualsiasi classe Aspose.PSD per .NET.
- **Applicazioni ASP.NET**: chiamare License.SetLicense dal file Global.asax.cs (Global.asax.vb), nel metodo protetto Application_Start. In questo modo, viene chiamato una sola volta quando l'applicazione si avvia. Non chiamare License.SetLicense all'interno dei metodi Page_Load altrimenti la licenza verrà caricata ogni volta che viene caricata una pagina web.
- **Applicazioni Silverlight**: chiamare License.SetLicense dall'evento Application_Startup nel file App.xaml.cs (App.xaml.vb).
- **Libreria di Classi**: chiamare License.SetLicense da un costruttore statico della classe che utilizza Aspose.PSD. Il costruttore statico esegue prima di creare un'istanza della tua classe, garantendo che la licenza di Aspose.PSD sia correttamente impostata.
## **Applicazione di una Licenza**
È possibile scaricare facilmente una versione di valutazione di Aspose.PSD da NuGet [pagina di download](https://www.nuget.org/packages/Aspose.psd/). La versione di valutazione fornisce esattamente le stesse funzionalità della versione con licenza di Aspose.PSD. Inoltre, la versione di valutazione diventa semplicemente licenziata quando si acquista una licenza e si aggiungono un paio di righe di codice per applicare la licenza.
### **Utilizzo di un File o uno Stream**
Se si desidera evitare di lavorare con le limitazioni della valutazione, è necessario impostare una licenza prima di utilizzare Aspose.PSD. È sufficiente impostare una licenza una sola volta per applicazione (o processo).
### **Applicazione di una licenza da un file**
Il modo più semplice per applicare una licenza è mettere il file di licenza nella stessa cartella del file Aspose.PSD.dll. Quindi è possibile specificare il nome del file nel codice anziché un percorso completo.



{{< highlight java >}}

 // Creare un'istanza di licenza e applicare la licenza utilizzando un percorso completo

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense("Aspose.PSD.lic");



{{< /highlight >}}



Quando si chiama il metodo SetLicense, il nome della licenza deve essere lo stesso del nome del file di licenza. Ad esempio, se si cambia il nome del file di licenza in "Aspose.PSD.lic.xml" si dovrebbe utilizzare questo nome di licenza per il metodo SetLicense.
### **Applicazione di una licenza utilizzando uno Stream**
È anche possibile caricare una licenza da uno Stream come mostrato di seguito.



{{< highlight java >}}



// Creare un'istanza di licenza e applicare la licenza utilizzando uno Stream

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense(myStream);



{{< /highlight >}}
### **Verifica dello stato della licenza**
La classe Aspose.PSD.License ha la proprietà IsLicensed che restituirà true se la licenza è stata correttamente impostata.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("Licenza impostata!");

}

{{< /highlight >}}
### **Utilizzo di una Risorsa Incorporata**
Un modo pratico per confezionare la licenza con la tua applicazione e assicurarti che non venga persa, è includerla come risorsa incorporata in uno dei assembly che chiama Aspose.PSD. Per includere il file di licenza come risorsa incorporata:

1. In Visual Studio .NET, fare clic sul menu **File** e selezionare **Aggiungi Elemento Esistente**.
1. Includere il file di licenza (estensione .lic) nel progetto.
1. Selezionare il file nell'Esplora soluzioni.
1. Nella finestra delle Proprietà, impostare **Azione di Compilazione** su **Risorsa Incorporata**.

Non è necessario chiamare i metodi GetExecutingAssembly o GetManifestResourceStream della classe System.Reflection.Assembly nel framework .NET di Microsoft per accedere a una licenza incorporata. Invece, incorporare il file come risorsa nel progetto e quindi passare il nome del file di licenza al metodo SetLicense. La classe License troverà automaticamente il file di licenza nelle risorse incorporate. L'esempio seguente mostra come includere la licenza come risorsa incorporata e applicarla alla tua applicazione.



{{< highlight java >}}

 // Istanziare la classe License

Aspose.PSD.License license = new Aspose.PSD.License();



// Passare il nome del file di licenza incorporato

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}
### **Verifica dello stato della licenza**
La classe Aspose.PSD.License ha la proprietà IsLicensed che restituirà true se la licenza è stata correttamente impostata.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("Licenza impostata!");

}

{{< /highlight >}}
