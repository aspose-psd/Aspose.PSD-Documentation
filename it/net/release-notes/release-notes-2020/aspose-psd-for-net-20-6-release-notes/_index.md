---
title: Aspose.PSD per .NET 20.6 - Note sulla versione
type: docs
weight: 70
url: /it/net/aspose-psd-per-net-20-6-note-sulla-versione/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 20.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-606 |Supporto di Risorsa LnkE|Funzionalità|
|PSDNET-386 |Supporto di britResource (Risorsa della Regolazione Luminosità/Contrasto)|Funzionalità|
|PSDNET-219|Spostamento dell'impostazione DefaultReplacementFont nella classe ImageOptionsBase|Potenziamento|
|PSDNET-596|Il Gruppo di Livelli con Modalità di Fusione diversa da PassThrough non viene Reso|Errore|
|PSDNET-610|Eccezione NullReference quando si tenta di convertire un file Psd specifico in un'immagine|Errore|
|PSDNET-636|Il ridimensionamento dei file PSD funziona in modo errato se c'è un mascheramento nel livello di regolazione che ha limiti vuoti|Errore|
|PSDNET-611|OverflowException quando si tenta di aprire un file Psd specifico|Errore|
|PSDNET-565|L'immagine Psd con modalità RGB a 16 bit/canale aggiorna i livelli solo in anteprima|Errore|
|PSDNET-652|Eccezione durante il caricamento di un file PSD specifico con la risorsa complessa LnkE e la proprietà adobeStockLicenseState|Errore|
|PSDNET-640|Le modifiche al livello di maschera PSD vengono scartate al salvataggio|Errore|
|PSDNET-593|Il salvataggio del file AI in formato Jpeg2000 non funziona|Errore|
|PSDNET-638|Ordine del Livello Errato dopo l'aggiunta di un Gruppo di Livelli a un Gruppo di Livelli vuoto|Errore|

## **Modifiche all'API Pubblica**
# **API Aggiunte:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.MaskRectangle
- P:Aspose.PSD.ImageOptionsBase.DefaultReplacementFont
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Type
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.OriginalFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.FileType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.FileCreator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.ChildDocId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.AssetModTime
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.AssetLockedState
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.IsLibraryLink
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.OriginalCompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.HasFileOpenDescriptor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Length
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.None
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFD
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFE
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFA
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.#ctor(System.Int32,System.Guid,System.String,System.String,System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.Date
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FileSize
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FullPath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.RelativePath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.ElementRef
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.ElementName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.AdobeStockId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.AdobeStockLicenseState
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.#ctor(System.Int32,System.Guid,System.String,System.String,System.String)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.IsEmpty
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.DataSourceCount
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.StringStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,System.String)
# **API Rimosse:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.DefaultReplacementFont

## **Esempi di Utilizzo:**
**PSDNET-606. Supporto di Risorsa LnkE**

{{< highlight java >}}

 string message = "L'esempio di supporto di LnkeResource funziona in modo non corretto.";

void AssertIsTrue(bool condition)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

void AssertAreEqual(object actual, object expected)

{

    if (!object.Equals(actual, expected))

    {

        throw new FormatException(message);

    }

}

// Questo esempio dimostra come ottenere e impostare le proprietà della Risorsa Photoshop Psd LnkE contenente informazioni su un file collegato esternamente.

void EsempioDiSupportoLnkERisorse(

    string percorsoFile,

    int lunghezza,

    int lunghezza2,

    int lunghezza3,

    int lunghezza4,

    string percorsoCompleto,

    string data,

    double assetModificato,

    string idDocBambino,

    bool bloccato,

    string uid,

    string nome,

    string nomeFileOriginale,

    string tipoFile,

    long dimensione)

{

    string nomeFile = Path.GetFileName(percorsoFile);

    string percorsoOutput = @"Output\" + nomeFile;

    using (PsdImage immagine = (PsdImage)Image.Load(percorsoFile))

    {

        LnkeResource risorsaLnke = null;

        foreach (var risorsa in immagine.GlobalLayerResources)

        {

            risorsaLnke = risorsa as LnkeResource;

            if (risorsaLnke != null)

            {

                AssertAreEqual(risorsaLnke.Length, lunghezza);

                AssertAreEqual(risorsaLnke.UniqueId, new Guid(uid));

                AssertAreEqual(risorsaLnke.FullPath, percorsoCompleto);

                AssertAreEqual(risorsaLnke.Date.ToString(CultureInfo.InvariantCulture), data);

                AssertAreEqual(risorsaLnke.AssetModTime, assetModificato);

                AssertAreEqual(risorsaLnke.AssetLockedState, bloccato);

                AssertAreEqual(risorsaLnke.FileName, nome);

                AssertAreEqual(risorsaLnke.FileSize, dimensione);

                AssertAreEqual(risorsaLnke.ChildDocId, idDocBambino);

                AssertAreEqual(risorsaLnke.Version, 7);

                AssertAreEqual(risorsaLnke.FileType, tipoFile);

                AssertAreEqual(risorsaLnke.FileCreator, string.Empty);

                AssertAreEqual(risorsaLnke.OriginalFileName, nomeFileOriginale);

                AssertAreEqual(risorsaLnke.CompId, -1);

                AssertAreEqual(risorsaLnke.OriginalCompId, -1);

                AssertIsTrue(risorsaLnke.HasFileOpenDescriptor);

                AssertIsTrue(!risorsaLnke.IsEmpty);

                AssertIsTrue(risorsaLnke.Type == LinkResourceType.liFE);

                risorsaLnke.FullPath =

                    @"file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png";

                AssertAreEqual(risorsaLnke.Length, lunghezza2);

                risorsaLnke.FileName = "rgb8_2x23.png";

                AssertAreEqual(risorsaLnke.Length, lunghezza3);

                risorsaLnke.ChildDocId = Guid.NewGuid().ToString();

                AssertAreEqual(risorsaLnke.Length, lunghezza4);

                risorsaLnke.Date = DateTime.Now;

                risorsaLnke.AssetModTime = double.MaxValue;

                risorsaLnke.FileSize = long.MaxValue;

                risorsaLnke.FileType = "test";

                risorsaLnke.FileCreator = "file";

                risorsaLnke.CompId = int.MaxValue;

                break;

            }

        }

        AssertIsTrue(risorsaLnke != null);

        immagine.Save(percorsoOutput, new PsdOptions(immagine));

    }

    using (PsdImage immagine = (PsdImage)Image.Load(percorsoOutput))

    {

        immagine.Save(

            Path.ChangeExtension(percorsoOutput, "png"),

            new PngOptions

            {

                ColorType = PngColorType.TruecolorWithAlpha

            });

    }

}

// Questo esempio dimostra come ottenere e impostare le proprietà della Risorsa PSD LnkE che contiene informazioni su un file JPEG esterno collegato.

this.EsempioDiSupportoLnkERisorse(

    @"..\..\..\Issues\IMAGINGNET-2375\photooverlay_5_new.psd",

    0x21c,

    0x26c,

    0x274,

    0x27c,

    @"file:///C:/Users/cvallejo/Desktop/photo.jpg",

    "05/09/2017 22:24:51",

    0,

    "F062B9DB73E8D124167A4186E54664B0",

    false,

    "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

    "photo.jpg",

    "photo.jpg",

    "JPEG",

    0x1520d);

// Questo esempio dimostra come ottenere e impostare le proprietà della Risorsa Photoshop Psd LnkE che contiene informazioni su un file PNG esterno collegato.

this.EsempioDiSupportoLnkERisorse(

    "rgb8_2x2_linked.psd",

    0x284,

    0x290,

    0x294,

    0x2dc,

    @"file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

    "04/14/2020 14:23:44",

    0,

    "",

    false,

    "5867318f-3174-9f41-abca-22f56a75247e",

    "rgb8_2x2.png",

    "rgb8_2x2.png",

    "png",

    0x53);

// Questo esempio dimostra come ottenere e impostare le proprietà della Risorsa PSD LnkE che contiene informazioni su un Asset delle librerie CC collegato esternamente.

this.EsempioDiSupportoLnkERisorse(

    "rgb8_2x2_asset_linked.psd",

    0x398,

    0x38c,

    0x388,

    0x3d0,

    @"CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (La funzione è disponibile in Photoshop CC 2015)",

    "01/01/0001 00:00:00",

    1588890915488.0d,

    "",

    false,

    "ec15f0a8-7f13-a640-b928-7d29c6e9859c",

    "rgb8_2x2_linked",

    "rgb8_2x2.png",

    "png",

    0);

{{< /highlight >}}

**PSDNET-201. Supporto per il progresso della conversione del documento**

{{< highlight java >}}

 string percorsoSorgenteFile = "Apple.psd";

Stream outputStream = new MemoryStream();

ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)

{

      string message = string.Format(

           "{0} {1}: {2} su {3}",

           progressInfo.Description,

           progressInfo.EventType,

           progressInfo.Value,

           progressInfo.MaxValue);

      Console.WriteLine(message);

};

Console.WriteLine("---------- Caricamento di Apple.psd ----------");

var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };

using (PsdImage immagine = (PsdImage)Image.Load(percorsoSorgenteFile, loadOptions))

{

      Console.WriteLine("---------- Salvataggio di Apple.psd in formato PNG ----------");

      immagine.Save(

           outputStream,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler

           });

      Console.WriteLine("---------- Salvataggio di Apple.psd in formato PSD ----------");

      immagine.Save(

           outputStream,

           new PsdOptions()

           {

                 ColorMode = ColorModes.Rgb,

                 ChannelsCount = 4,

                 ProgressEventHandler = localProgressEventHandler

           });

}

{{< /highlight >}}

**PSDNET-386. Supporto di britResource (Risorsa del Livello di Regolazione Luminosità/Contrasto)**

{{< highlight java >}}

 /* Questo esempio dimostra come è possibile modificare programmaticamente la Risorsa del Livello di Luminosità/Contrasto dell'immagine PSD

   Questo è un API di basso livello di Aspose.PSD. È possibile utilizzare il Livello di Luminosità/Contrasto tramite la sua API, che sarà molto più semplice, 

   ma la modifica diretta della risorsa PhotoShop ti dà più controllo sul contenuto del file PSD.  */

string percorso = @"BrightnessContrastPS6.psd";

string percorsoOutput = @"BrightnessContrastPS6_output.psd";

using (PsdImage immagine = (PsdImage)Image.Load(percorso))

{

    foreach (var livello in immagine.Layers)

    {

        if (livello is BrightnessContrastLayer)

        {

            foreach (var risorsaLivello in livello.Resources)

            {

                if (risorsaLivello is BritResource)

                {

                    var risorsa = (BritResource)risorsaLivello;

                    isRequiredResourceFound = true;

                    if (risorsa.Brightness != -40 ||

                        risorsa.Contrast != 10 ||

                        risorsa.LabColor != false ||

                        risorsa.MeanValueForBrightnessAndContrast != 127)

                    {

                        throw new Exception("La BritResource è stata letta in modo errato");

                    }

                    // Test modifica e salvataggio

                    risorsa.Brightness = 25;

                    risorsa.Contrast = -14;

                    risorsa.LabColor = true;

                    risorsa.MeanValueForBrightness