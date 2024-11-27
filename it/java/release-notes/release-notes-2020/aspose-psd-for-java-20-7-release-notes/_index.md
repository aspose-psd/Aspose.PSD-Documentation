---
title: Note sulla versione di rilascio di Aspose.PSD per Java 20.7
type: docs
weight: 50
url: /it/java/aspose-psd-per-java-20-7-note-di-rilascio/
---

{{% alert color="primary" %}} Questa pagina contiene le note di rilascio per [Aspose.PSD per Java 20.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.7/) {{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-231|Supporto dell'aggiunta dell'Effetto di Contorno durante l'esecuzione|Caratteristica|
|PSDJAVA-249|Supporto di lnk2 / lnk3 Risorse (Risorse dello Strato Oggetto Intelligente)|Caratteristica|
|PSDJAVA-247|Cambio del Messaggio di Eccezione nel tentativo di aprire formati non supportati come immagine|Potenziamento|
|PSDJAVA-235|Se salviamo il file PSD dopo aver creato un nuovo Gruppo di Livelli otteniamo un avviso di Photoshop all'apertura del file.|Errore|
|PSDJAVA-236|Impossibile salvare la Maschera di Livello|Errore|
|PSDJAVA-237|La maschera di ritaglio non si applica alla cartella|Errore|
|PSDJAVA-238|Impossibile aprire il file con Aspose.PSD per Java|Errore|
|PSDJAVA-239|Eccezione di salvataggio immagine fallito durante la conversione di PSD in PDF|Errore|
|PSDJAVA-240|L'operazione di ritaglio rende il percorso di ritaglio non valido nell'immagine PSD|Errore|
|PSDJAVA-241|Eccezione di NullReference durante il tentativo di salvare uno specifico file PSD con Effetto Ombra|Errore|
|PSDJAVA-243|Aspose.PSD restituisce true su Image.CanLoad(pdfStream)|Errore|
|PSDJAVA-244|Livelli non renderizzati nel PNG generato|Errore|
|PSDJAVA-245|Eccezione nell'accesso ai dati del Testo|Errore|
|PSDJAVA-246|Eccezione ImageSaveException durante il salvataggio del PSD|Errore|

# **Modifiche alle API pubbliche**
# **API Aggiunte:**
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Center
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Inside
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Outside
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.TypeToolKey
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions.addStroke(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getOverprint
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getPosition
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getSize
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setOverprint(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setPosition(short)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setSize(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.getData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.setData(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.get_Item(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getMinimalVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getPaths
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isDisabled
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isInverted
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isNotLinked
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.saveData(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setVersion(int)
- T:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData

## **API Rimosse:**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.DescriptorVersion
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.UnexpectedLinkResourceTypeValue
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.ZeroChar
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureLayer(float,float,float)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])

# **Esempi di utilizzo:**

**PSDJAVA-231. Supporto dell'aggiunta dell'Effetto di Contorno durante l'esecuzione**
{{< highlight java >}}
// Questo esempio mostra come aggiungere un effetto di contorno (bordo) a livelli esistenti di un file PSD in Java.
// Ci sono tre tipi di tratto: colore, sfumatura e modello. Ognuno dei tipi ha
// tre modi (posizioni) in cui il tratto viene renderizzato: all'interno, al centro e all'esterno.
// Questo esempio dimostra l'utilizzo di tutti questi casi.

String srcPsdPath = "StrokeEffectsSource.psd";
String dstPngPath = "output.png";

PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);
PsdImage psdImage = (PsdImage)Image.load(srcPsdPath, psdLoadOptions);
try
{
    StrokeEffect strokeEffect;
    IColorFillSettings colorFillSettings;
    IGradientFillSettings gradientFillSettings;
    IPatternFillSettings patternFillSettings;

    // 1. Aggiunge Color fill, alla posizione Inside
    strokeEffect = psdImage.getLayers()[1].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Inside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 2. Aggiunge Color fill, alla posizione Outside
    strokeEffect = psdImage.getLayers()[2].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Outside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 3. Aggiunge Color fill, alla posizione Center
    strokeEffect = psdImage.getLayers()[3].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Center);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 4. Aggiunge Gradient fill, alla posizione Inside
    strokeEffect = psdImage.getLayers()[4].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Inside);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(false);
    gradientFillSettings.setAngle(90);

    // 5. Aggiunge Gradient fill, alla posizione Outside
    strokeEffect = psdImage.getLayers()[5].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Outside);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(true);
    gradientFillSettings.setAngle(90);

    // 6. Aggiunge Gradient fill, alla posizione Center
    strokeEffect = psdImage.getLayers()[6].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Center);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(true);
    gradientFillSettings.setAngle(0);

    // 7. Aggiunge Pattern fill, alla posizione Inside
    strokeEffect = psdImage.getLayers()[7].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Inside);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(200);

    // 8. Aggiunge Pattern fill, alla posizione Outside
    strokeEffect = psdImage.getLayers()[8].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(10);
    strokeEffect.setPosition(StrokePosition.Outside);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(100);

    // 9. Aggiunge Pattern fill, alla posizione Center
    strokeEffect = psdImage.getLayers()[9].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(10);
    strokeEffect.setPosition(StrokePosition.Center);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(75);

    psdImage.save(dstPngPath, new PngOptions());
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}

**PSDJAVA-249. Supporto di lnk2 / lnk3 Risorse (Risorse dello Strato Oggetto Intelligente)**
{{< highlight java >}}
// Questo esempio dimostra come lavorare con risorse oggetto intelligente (in pratica Lnk2Resource).
// Il programma carica diversi documenti Photoshop ed esporta i loro oggetti intelligenti
// in formati di file raster. Inoltre, il codice dimostra l'utilizzo dei metodi pubblici di Lnk2Resource.

class LocalScopeExtension
{
    void assertAreEqual(Object expected, Object actual)
    {
        if (!actual.equals(expected))
        {
            throw new FormatException(String.format("Il valore effettivo %s non corrisponde al previsto %s.", actual, expected));
        }
    }

    // Salva i dati di un oggetto intelligente in un file PSD
    void saveSmartObjectData(String filePath, byte[] data)
    {
        FileStreamContainer container = FileStreamContainer.createFileStream(filePath, false);
        try
        {
            container.write(data);
        }
        finally
        {
            container.dispose();
        }
    }

    // Carica i nuovi dati per un oggetto intelligente da un file
    byte[] loadNewData(String filePath)
    {
        FileStreamContainer container = FileStreamContainer.openFileStream(filePath);
        try
        {
            return container.toBytes();
        }
        finally
        {
            container.dispose();
        }
    }

    // Ottiene e imposta le proprietà della risorsa PSD Lnk2 / Lnk3 e le sue sorgenti dati LiFD nell'immagine PSD
    void exampleOfLnk2ResourceSupport(
            String fileName,
            int dataSourceCount,
            int length,
            int newLength,
            Object[] dataSourceExpectedValues)
    {
        String srcPsdPath = fileName;
        String dstPsdPath = "out_" + fileName;

        PsdImage image = (PsdImage)Image.load(srcPsdPath);
        try
        {
            // Cerca Lnk2Resource
            Lnk2Resource lnk2Resource = null;
            for (LayerResource resource : image.getGlobalLayerResources())
            {
                if (resource instanceof Lnk2Resource)
                {
                    lnk2Resource = (Lnk2Resource)resource;

                    // Verifica le proprietà di Lnk2Resource
                    assertAreEqual(lnk2Resource.getDataSourceCount(), dataSourceCount);
                    assertAreEqual(lnk2Resource.getLength(), length);
                    assertAreEqual(lnk2Resource.isEmpty(), false);

                    for (int i = 0; i < lnk2Resource.getDataSourceCount(); i++)
                    {
                        // Verifica e modifica le proprietà di LiFdDataSource
                        LiFdDataSource lifdSource = lnk2Resource.get_Item(i);
                        Object[] expected = (Object[])dataSourceExpectedValues[i];
                        assertAreEqual(LinkDataSourceType.liFD, lifdSource.getType());
                        assertAreEqual(expected[0], lifdSource.getUniqueId().toString());
                        assertAreEqual(expected[1], lifdSource.getOriginalFileName());
                        assertAreEqual(expected[2], lifdSource.getFileType().trim());
                        assertAreEqual(expected[3], lifdSource.getFileCreator().trim());
                        assertAreEqual(expected[4], lifdSource.getData().length);
                        assertAreEqual(expected[5], lifdSource.getAssetModTime());
                        assertAreEqual(expected[6], lifdSource.getChildDocId());
                        assertAreEqual(expected[7], lifdSource.getVersion());
                        assertAreEqual(expected[8], lifdSource.hasFileOpenDescriptor());
                        assertAreEqual(expected[9], lifdSource.getLength());

                        if (lifdSource.hasFileOpenDescriptor())
                        {
                            assertAreEqual(-1, lifdSource.getCompId());
                            assertAreEqual(-1, lifdSource.getOriginalCompId());
                            lifdSource.setCompId(Integer.MAX_VALUE);
                        }

                        saveSmartObjectData(
                                fileName + "_" + lifdSource.getOriginalFileName(),
                                lifdSource.getData());
                        lifdSource.setData(loadNewData("new_" + lifdSource.getOriginalFileName()));
                        assertAreEqual(expected[10], lifdSource.getLength());

                        lifdSource.setChildDocId(UUID.randomUUID().toString());
                        lifdSource.setAssetModTime(Double.MAX_VALUE);
                        lifdSource.setFileType("test");
                        lifdSource.setFileCreator("me");
                    }

                    assertAreEqual(newLength, lnk2Resource.getLength());
                    break;
                }
            }

            // Assicurati che Lnk2Resource sia stato trovato
            assertAreEqual(true, lnk2Resource != null);

            // Crea una copia della PSD caricata
            if (image.getBitsPerChannel() < 32) // Il salvataggio a 32 bit per canale non è ancora supportato
            {
                image.save(dstPsdPath, new PsdOptions(image));
            }
        }
        finally
        {
            image.dispose();
        }
    }
}
LocalScopeExtension $ = new LocalScopeExtension();


Object[] Lnk2ResourceSupportCases = new Object[]
        {
                new Object[]
                        {
                                "00af34a0-a90b-674d-a821-73ee508c5479",
                                "rgb8_2x2.png",
                                "png",
                                "",
                                0x53,
                                0d,
                                "",
                                7,
                                true,
                                0x124L,
                                0x74cL
                        }
        };

Object[] LayeredLnk2ResourceSupportCases = new Object[]
        {
                new Object[]
                        {
                                "69ac1c0d-1b74-fd49-9c7e-34a7aa6299ef",
                                "huset.jpg",
                                "JPEG",
                                "",
                                0x9d46,
                                0d,
                                "xmp.did:0F94B342065B11E395B1FD506DED6B07",
                                7,
                                true,
                                0x9E60L,
                                0xc60cL
                        },
                new Object[]
                        {
                                "5a7d1965-0eae-b24e-a82f-98c7646424c2",
                                "panama-papers.jpg",
                                "JPEG",
                                "",
                                0xF56B,
                                0d,
                                "xmp.did:BDE940CBF51B11E59D759CDA690663E3",
                                7,
                                true,
                                0xF694L,
                                0x10dd4L
                        },
        };

Object[] LayeredLnk3ResourceSupportCases = new Object[]
        {
                new Object[]
                        {
                                "2fd7ba52-0221-de4c-bdc4-1210580c6caa",
                                "panama-papers.jpg",
                                "JPEG",
                                "",
                                0xF56B,
                                0d,
                                "xmp.did:BDE940CBF51B11E59D759CDA690663E3",
                                7,
                                true,
                                0xF694l,
                                0x10dd4L
                        },
                new Object[]
                        {
                                "372d52eb-5825-8743-81a7-b6f32d51323d",
                                "huset.jpg",
                                "JPEG",
                                "",
                                0x9d46,
                                0d,
                                "xmp.did:0F94B342065B11E395B1FD506DED6B07",
                                7,
                                true,
                                0x9E60L,
                                0xc60cL
                        },
        };

// Questo esempio dimostra come ottenere e impostare le proprietà di una risorsa PSD Lnk2 Resource e delle sue sorgenti dati LiFD per 8 bit per canale.
$.exampleOfLnk2ResourceSupport("rgb8_2x2_embedded_png.psd", 1, 0x12C, 0x0000079c, Lnk2ResourceSupportCases);

// Questo esempio dimostra come ottenere e impostare le proprietà della risorsa PSD Lnk3 Resource e delle sue sorgenti dati LiFD per 32 bit per canale.
$.exampleOfLnk2ResourceSupport("Layered PSD file smart objects.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk3ResourceSupportCases);

// Questo esempio dimostra come ottenere e impostare le proprietà della risorsa PSD Lnk2 Resource e delle sue sorgenti dati LiFD per 16 bit per canale.
$.exampleOfLnk2ResourceSupport("LayeredSmartObjects16bit.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk2ResourceSupportCases);

{{< /highlight >}}

**PSDJAVA-247. Cambio del Messaggio di Eccezione nel tentativo di aprire formati non supportati come immagine**
{{< highlight java >}}
// Questo esempio mostra che viene generata un'eccezione con un messaggio nuovo e più descrittivo durante il caricamento
// delle immagini raster in un modo non supportato (le immagini raster possono essere caricate solo come livelli).

String[] filesPaths = new String[]
        {
                "BmpExample.bmp",
                "GifExample.gif",
                "Jpeg2000Example.jpf",
                "JpegExample.jpg",
                "PngExample.png",
                "TiffExample.tif",
        };

String expectedExceptionMessage = "Impossibile aprire un'immagine. Il formato del file immagine potrebbe non essere supportato al momento o non può essere aperto in questo modo. Se si tenta di aggiungere un Livello, si prega di Aprire il File come Stream e utilizzare invece il metodo AddLayer. Consultare la documentazione https://docs.aspose.com/display/psdnet/Add+Layer+to+PSD";

for (String filePath : filesPaths)
{
    try
    {
        Image image = Image.load(filePath);
        image.dispose();
    }
    catch (Exception e)
    {
        // Verifica se l'eccezione generata ha un messaggio nuovo e più descrittivo
        if (e.getInnerException() == null ||
                !e.getInnerException().getMessage().equals(expectedExceptionMessage))
        {
            throw e;
        }
    }
}
{{< /highlight >}}

**PSDJAVA-235. Se salviamo il file PSD dopo aver creato un nuovo Gruppo di Livelli otteniamo un avviso di Photoshop all'apertura del file.**
{{< highlight java >}}
// Questo esempio dimostra che non viene generata alcuna eccezione durante il salvataggio di un file PSD generato
// che contiene gruppi di livelli interni.

String dstPsdPath = "psdnet_test_out.psd";

// Definisci regole particolari per la creazione dell'immagine PSD
PsdOptions createOptions = new PsdOptions();
createOptions.setSource(new FileCreateSource(dstPsdPath, false));
createOptions.setPalette(new PsdColorPalette(new Color[] { Color.getRed(), Color.getGreen(), Color.getBlue() }));
PsdImage psdImage = (PsdImage)Image.create(createOptions, 500, 500);
try
{
    // Aggiunge una gerarchia di gruppi di livelli e un livello nel PSD
    LayerGroup group1 = psdImage.addLayerGroup("Gruppo 1", 0, true);

    Layer layer1 = new Layer(psdImage);
    layer1.setName("Livello 1");
    group1.addLayer(layer1);

    LayerGroup group2 = group1.addLayerGroup("Gruppo 2", 1);

    // Salva il PSD generato in un file fisico e assicurati che non ci siano eccezioni
    psdImage.save(dstPsdPath);
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}

**PSDJAVA-236. Impossibile salvare la Maschera di Livello**
{{< highlight java >}}
// Questo esempio dimostra la capacità di salvare e renderizzare le maschere di livello per
// Gruppi di Livelli quando i livelli vengono aggiunti da un'altra immagine PSD.

String srcPsdPath = "MaskTest.psd";
String dstPsdPath = "MaskTest_output.psd";
String dstJpgPath = "MaskTest_output.jpg";
String dstPngPath = "MaskTest_output.png";
String dstPngPath1 = "MaskTest_output_indirect.png";

PsdImage srcPsdImage = (PsdImage)Image.load(srcPsdPath);
try
{
    PsdImage dstPsdImage = new PsdImage(srcPsdImage.getWidth(), srcPsdImage.getHeight());
    try
    {
        LayerGroup openingLayerGroupTag = null;
        LayerGroup closingLayerGroupTag = null;

        // Clonazione manuale dei livelli dalla PSD di origine a una PSD di destinazione
        for (Layer layer : srcPsdImage.getLayers())
        {
            if (layer instanceof LayerGroup)
            {
                LayerGroup srcGroup = (LayerGroup)layer;

                if (closingLayerGroupTag == null)
                {
                    int insertAt = dstPsdImage.getLayers().length;
                    // Poiché il gruppo di livelli è implementato internamente come due livelli (tag di apertura
                    // e chiusura) per definire i bordi del gruppo di livelli, il seguente
                    // statement restituisce un tag di chiusura (livello)...
                    closingLayerGroupTag = dstPsdImage.addLayerGroup("Gruppo Mascherato", insertAt, true);
                    // ...ma questo statement restituisce un tag di apertura che viene memorizzato per ulteriori elaborazioni
                    openingLayerGroupTag = (LayerGroup)dstPsdImage.getLayers()[insertAt + 1];
                }

                if (srcGroup.getLayerMaskData() != null)
                {
                    // Lo statement commentato di seguito non funziona poiché se viene aggiunta una maschera di livello
                    // a un tag di chiusura di un gruppo di livelli non avrebbe senso
                    // poiché il tag di chiusura non mantiene alcun livello (funge solo da
                    // marcatore) inoltre non viene renderizzato (visibile) nell'editor
                    // closingLayerGroupTag.addLayerMask(oldGroup.getLayerMaskData());

                    openingLayerGroupTag.addLayerMask(srcGroup.getLayerMaskData()); // Funziona!
                }
            }
            else
            {
                // Attenzione: Aggiungere un livello a un'altra immagine senza copiarlo o rimuoverlo
                // dall'immagine originale potrebbe influire sul rendering dell'immagine originale perché
                // cambia la proprietà Container del livello.
                if (layer.getName().equals("Carta"))
                {
                    dstPsdImage.addLayer(layer);
                }
                else
                {
                    closingLayerGroupTag.addLayer(layer);
                }
            }
        }

        // Esporta il risultato PSD in vari formati di file per assicurarti che una maschera di livello
        // sia stata aggiunta a un gruppo di livelli e che sia resa correttamente per quei formati di file
        dstPsdImage.save(dstPsdPath);

        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
        dstPsdImage.save(dstPngPath, pngOptions);

        JpegOptions jpegOptions = new JpegOptions();
        jpegOptions.setColorType(JpegCompressionColorMode.Rgb);
        dstPsdImage.save(dstJpgPath, jpegOptions);

        // Usa un'immagine PSD di controllo per assicurarti che Graphics renda correttamente la maschera di livello, anche
        PsdImage controlPsdImage = new PsdImage(dstPsdImage.getWidth(), dstPsdImage.getHeight());
        try
        {
            Graphics graphics = new Graphics(controlPsdImage);
            graphics.drawImageUnscaled(dstPsdImage, 0, 0);

            controlPsdImage.save(dstPngPath1, new PngOptions());
        }
        finally
        {
            controlPsdImage.dispose();
        }
    }
    finally
    {
        dstPsdImage.dispose();
    }
}
finally
{
    srcPsdImage.dispose();
}
{{< /highlight >}}

**PSDJAVA-237. La maschera di ritaglio non si applica alla cartella**
{{< highlight java >}}
// Questo esempio verifica che le maschere di ritaglio legate ai gruppi di livelli siano esportate
// correttamente per un file PSD predefinito.

String srcPsdPath = "cartelleEFigure.psd";
String dstPngPath = "output.png";

PsdImage psdImage = (PsdImage)Image.load(srcPsdPath);
try
{
    // Esporta il PSD caricato in un file PNG per garantire che le maschere di ritaglio siano
    // esportate correttamente, cioè che siano visibili nell'immagine di output
    psdImage.save(dstPngPath, new PngOptions());
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}

**PSDJAVA-238. Impossibile aprire il file con Aspose.PSD per Java**
{{< highlight java >}}
// Questo esempio carica e salva un particolare file PSD senza generare eccezioni.

String srcPsdPath = "campione.psd";
String dstPngPath = "output.png";

PsdImage psdImage = (PsdImage)Image.load(srcPsdPath);
try
{
    psdImage.save(dstPngPath, new PngOptions());
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}

**PSDJAVA-239. Eccezione di salvataggio immagine fallito durante la conversione di PSD in PDF**
{{< highlight java >}}
// Questo esempio esporta un particolare file PSD nel formato di file PDF con la modalità di sola lettura attivata
// e disattivata per garantire che non vengano generati errori e che il file di output sia corretto.

class LocalScopeExtension
{
    void exportPsdToPdf(String srcFilePath, String dstFilePath, boolean readOnlyMode)
            throws IOException
    {
        FileInputStream fileStream = new FileInputStream(srcFilePath);
        try
        {
            PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
            psdLoadOptions.setReadOnlyMode(readOnlyMode);
            Image image = Image.load(fileStream, psdLoadOptions);
            try
            {
                image.save(dstFilePath, new PdfOptions());
            }
            finally
            {
                image.dispose();
            }
        }
        finally
        {
            fileStream.close();
        }
    }
}
LocalScopeExtension $ = new LocalScopeExtension();

String srcPsdPath = "campione.psd";
String dstPdfPath = "output-ReadOnlyMode-On.pdf";
String dstPdfPath1 = "output-ReadOnlyMode-Off.pdf";

$.exportPsdToPdf(srcPsdPath, dstPdfPath, true);
$.exportPsdToPdf(srcPsdPath, dstPdfPath1, false);
{{< /highlight >}}

**PSDJAVA-240. L'operazione di ritaglio rende il percorso di ritaglio non valido nell'immagine PSD**
{{< highlight java >}}
// Questo esempio dimostra che l'operazione di ritaglio non rende un percorso di ritaglio non valido.
// Il programma carica un particolare file PSD e quindi lo ritaglia e salva il file. Dopo che il programma
// apre il file salvato e verifica che l'operazione di ritaglio sia stata eseguita come previsto.

String srcPsdPath = "originale.psd";
String dstPsdPath = "output.psd";

// Carica, ritaglia e salva l'immagine
PsdImage psdImage = (PsdImage)Image.load(srcPsdPath);
try
{
    // Cerca una risorsa WorkingPathResource
    ResourceBlock[] imageResources = psdImage.getImageResources();
    WorkingPathResource workingPathResource = null;
   