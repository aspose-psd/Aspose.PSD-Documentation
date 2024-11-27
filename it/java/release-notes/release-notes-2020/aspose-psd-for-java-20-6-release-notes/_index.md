---
title: Note sulla versione di Aspose.PSD per Java 20.6
type: docs
weight: 50
url: /it/java/aspose-psd-for-java-20-6-note-sulla-versione/
---

{{% alert color="primary" %}} Questa pagina contiene le note sulla versione di [Aspose.PSD per Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) {{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-216|Supporto di LnkEResource (Risorsa del Livello Smart Object)|Feature|
|PSDJAVA-219|Supporto di britResource (Risorsa del Livello di Regolazione Luminosità/Contrasto)|Feature|
|PSDJAVA-222|Spostamento dell'impostazione di DefaultReplacementFont nella classe ImageOptionsBase|Potenziamento|
|PSDJAVA-217|Il ridimensionamento dei file PSD non funziona correttamente se c'è una maschera nel livello di regolazione che ha limiti vuoti|Errore|
|PSDJAVA-218|L'immagine Psd con modalità RGB a 16 bit/canale aggiorna i livelli solo nella visualizzazione preliminare|Errore|
|PSDJAVA-220|Le modifiche alla maschera del livello PSD vengono eliminate al salvataggio|Errore|
|PSDJAVA-221|Ordine del Livello Errato dopo l'aggiunta di un Gruppo di Livelli a un Gruppo di Livelli vuoto|Errore|
|PSDJAVA-223|Eccezione nel caricamento di file PSD specifico con la Risorsa composta LnkE e la proprietà adobeStockLicenseState|Errore|
|PSDJAVA-224|Il salvataggio del file AI nel formato Jpeg2000 non funziona|Errore|
|PSDJAVA-225|Il Gruppo di Livelli con Modalità di Fusione non in PassThrough non viene Renderizzato|Errore|
|PSDJAVA-226|Eccezione NullReference durante il tentativo di convertire un file Psd specifico in un'immagine|Errore|
|PSDJAVA-227|OverflowException durante il tentativo di aprire un file Psd specifico|Errore|

# **Modifiche all'API pubblica**
# **API Aggiunte:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFullPath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getRelativePath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setAdobeStockId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementRef(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileSize(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFullPath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setRelativePath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetLockedState
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetModTime
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getChildDocId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileCreator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.hasFileOpenDescriptor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.isLibraryLink
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetLockedState(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetModTime(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setChildDocId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileCreator(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileOpenDescriptor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileType(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setLibraryLink(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setUniqueId(java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getDataSourceCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.isEmpty
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.link2resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.linkdatasource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.link2resource.getkey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.linkeresource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.linkeresource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.linkdatasource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.linkeresource.getkey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.linkeresource.get_item(int)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.lifddatasource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.lifedatasource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.linkdatasource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.linkdatasourcetype
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.linkresource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.link2resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.linkeresource
## **API Rimossi:**
- M:com.aspose.psd.imageloadoptions.psdloadoptions.getdefaultreplacementfont
- M:com.aspose.psd.imageloadoptions.psdloadoptions.setdefaultreplacementfont(java.lang.string)
# **Esempi di Utilizzo:**

**PSDJAVA-216: Supporto di LnkEResource (Risorsa del Livello Smart Object)**

{{< highlight java >}}

 // Esempio di collegamento di diversi tipi di risorse (immagini raster, librerie CC) a PSD.

// Viene considerata anche l'API di LnkeResource.

// Classe che mantiene i metodi nello scope locale

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("L'esempio di supporto di LnkEResource non funziona correttamente.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // Questo esempio dimostra come ottenere e impostare le proprietà del Photoshop Psd LnkE

    // Resource che contiene informazioni su un file esterno collegato.

    void exampleOfLnkEResourceSupport(

            String fileName,

            int length,

            int length2,

            int length3,

            int length4,

            String fullPath,

            String date,

            double assetModTime,

            String childDocId,

            boolean locked,

            String uid,

            String name,

            String originalFileName,

            String fileType,

            long size)

    {

        String outputPath = "out_" + fileName;

        // Carica un PSD predefinito

        PsdImage image = (PsdImage)Image.load(fileName);

        try

        {

            // Cerca LnkeResource tra le risorse globali

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // Verifica le proprietà di LnkeResource

                    assertAreEqual(lnkeResource.getLength(), length);

                    assertAreEqual(lnkeResource.get_Item(0).getUniqueId(), UUID.fromString(uid));

                    assertAreEqual(lnkeResource.get_Item(0).getFullPath(), fullPath);

                    assertAreEqual(new SimpleDateFormat("dd/MM/yyyy HH:mm:ss").format(lnkeResource.get_Item(0).getDate()), date);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetModTime(), assetModTime);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetLockedState(), locked);

                    assertAreEqual(lnkeResource.get_Item(0).getFileName(), name);

                    assertAreEqual(lnkeResource.get_Item(0).getFileSize(), size);

                    assertAreEqual(lnkeResource.get_Item(0).getChildDocId(), childDocId);

                    assertAreEqual(lnkeResource.get_Item(0).getVersion(), 7);

                    assertAreEqual(lnkeResource.get_Item(0).getFileType().trim(), fileType);

                    assertAreEqual(lnkeResource.get_Item(0).getFileCreator().trim(), "");

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalFileName(), originalFileName);

                    assertAreEqual(lnkeReso...

{{< /highlight >}}

**PSDJAVA-219: Supporto di britResource (Risorsa del Livello di Regolazione Luminosità/Contrasto)**

{{< highlight java >}}

 // Questo Esempio dimostra come modificare programmaticamente il Livello di Regolazione Luminosità/Contrasto dell'immagine PSD. Questa è un'API Aspose.PSD a basso livello.

// È possibile utilizzare il Livello di Luminosità/Contrasto tramite la sua API, questrarà molto più semplice,

// ma la modifica diretta delle risorse di Photoshop ti offre più controllo sul contenuto del file PSD.

String srcPath = "BrightnessContrastPS6.psd";

String dstPath = "BrightnessContrastPS6_output.psd";

// Carica un documento Photoshop contenente un Livello di Regolazione Luminosità/Contrasto

PsdImage psdImage = (PsdImage)Image.load(srcPath);

try

{

    // Cerca BritResource

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof BrightnessContrastLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof BritResource)

                {

                    BritResource resource = (BritResource)layerResource;

                    // Verifica le proprietà della risorsa

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw new RuntimeException("La BritResource è stata letta in modo errato");

                    }

                    // Aggiorna le proprietà della risorsa

                    resource.setBrightness((short)25);

                    resource.setContrast((short)-14);

                    resource.setLabColor(true);

                    resource.setMeanValueForBrightnessAndContrast((short)200);

                    // Salva una copia del PSD aggiornato

                    psdImage.save(dstPath, new PsdOptions());

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-217: Il ridimensionamento dei file PSD non funziona correttamente se c'è una maschera nel livello di regolazione che ha limiti vuoti**

{{< highlight java >}}

 // Esempio di ridimensionamento di un'immagine contenente una maschera nel livello di regolazione che ha limiti vuoti.

// Il programma carica un PSD predefinito solo per verificare l'assenza di eccezioni.

final int scala = 2; // coefficiente arbitrario

String[] nomi = {

        "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

        "LevelsLayerWithLayerMaskRgb",

        "LevelsLayerWithLayerMaskCmyk",

};

for (String nome : nomi)

{

    String srcFilePath = nome + ".psd";

    String dstFilePath = "output_" + srcFilePath;

    String dstPngFilePath = "output_" + nome + ".png";

    // Carica un PSD predefinito contenente una maschera nel livello di regolazione con limiti vuoti

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();

    psdLoadOptions.setLoadEffectsResource(true);

    PsdImage image = (PsdImage)Image.load(srcFilePath, psdLoadOptions);

    try

    {

        // Ridimensiona l'immagine

        image.resize(image.getWidth() * scala, image.getHeight() * scala);

        // Salva una copia del PSD caricato

        image.save(dstFilePath, new PsdOptions());

        // Esporta PSD in formato file PNG (con canale alfa per la trasparenza)

        PngOptions pngOptions = new PngOptions();

        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        image.save(dstPngFilePath, pngOptions);

    }

    finally

    {

        image.dispose();

    }

}

{{< /highlight >}}