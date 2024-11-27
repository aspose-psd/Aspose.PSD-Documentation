---
title: Note sulla versione di Aspose.PSD for Java 20.4
type: docs
weight: 30
url: /it/java/aspose-psd-per-java-20-4-note-sulla-versione/
---

{{% alert color="primary" %}} Questa pagina contiene le note sulla versione di [Aspose.PSD per Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) {{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-156|Supporto del 'Vector Origination Data' resource|Caratteristica|
|PSDJAVA-171|Supporto di lclrResource (Impostazioni di colore del foglio)|Caratteristica|
|PSDJAVA-157|Supporto delle proprietà dei dati di LengthRecord. (Operazioni sul percorso (operazioni booleane), indice della forma nel livello, conteggio dei record dei nodi di bezier)|Caratteristica|
|PSDJAVA-158|Supporto del Colore di sfondo dell'immagine della sezione di risorsa #1010|Caratteristica|
|PSDJAVA-161|Aggiunta di livelli di riempimento durante l'esecuzione|Caratteristica|
|PSDJAVA-168|Supporto delle informazioni sul bordo dell'immagine della sezione di risorsa #1009|Caratteristica|
|PSDJAVA-169|Supporto dei livelli nei file del formato AI|Caratteristica|
|PSDJAVA-163|Supporto Lettura e Modifica dell'Effetto del Livello Sovrimpressione Gradient|Caratteristica|
|PSDJAVA-164|Rendering dell'Effetto del Livello Sovrimpressione Gradient|Caratteristica|
|PSDJAVA-149|Aspose.PSD per java errore quando si ottiene la proprietà textData.items del livello di testo|Bug|
|PSDJAVA-166|Risoluzione del salvataggio dell'immagine PSD con ColorMode in Scala di grigi e 16 bit per canale nel formato PSD in scala di grigi|Bug|
|PSDJAVA-167|Risoluzione del salvataggio dell'immagine PSD con ColorMode in Scala di grigi e 16 bit per canale nel formato PNG|Bug|
|PSDJAVA-159|Le modifiche della proprietà GradientOverlayEffect.BlendMode non vengono visualizzate in Photoshop|Bug|
# **Cambianti nell'API pubblica**
# **API aggiunte:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.text.IText.producePortions(java.lang.String[],com.aspose.psd.fileformats.psd.layers.text.ITextStyle,com.aspose.psd.fileformats.psd.layers.text.ITextParagraph)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getBaselineShift
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxBold
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxItalic
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontBaseline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontCaps
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getStrikethrough
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getUnderline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setBaselineShift(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxBold(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxItalic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontBaseline(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontCaps(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setStrikethrough(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setUnderline(boolean)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Subscript
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Superscript
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.AllCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.SmallCaps
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream)
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream,boolean)
## **API Rimosse:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)
# **Esempi di utilizzo:**

**PSDJAVA-156. Supporto del 'Vector Origination Data' resource**

{{< highlight java >}}

 /*

Un esempio di lettura e modifica di una risorsa 'Vector Origination Data'.

*/

// Mantenere i metodi nello scope locale per semplificare

class LocalScopeExtension

{

    VogkResource findFirstVogkResource(LayerResource[] layerResources)

    {

        VogkResource vogkResource = null;

        for (LayerResource layerResource : layerResources)

        {

            if (layerResource instanceof VogkResource)

            {

                vogkResource = (VogkResource)layerResource;

                break;

            }

        }

        if (vogkResource == null)

        {

            throw new Exception("Risorsa Vogk non trovata.");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// Caricare un file PSD contenente una risorsa VOGK predefinita

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Trova la prima VogkResource nelle risorse del livello predefinito

    VogkResource vogkResource = $.findFirstVogkResource(

            psdImage.getLayers()[1].getResources());

    // Verifica le proprietà della risorsa predefinita

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("Risorsa Vogk non è stata letta correttamente.");

    }

    // Modifica alcune proprietà della risorsa Vogk

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // Salva una copia modificata del file PSD caricato sul percorso

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. Supporto di lclrResource (Impostazioni di colore del foglio)**

{{< highlight java >}}

 /*

Un esempio di utilizzo del Colore di livello per evidenziare visivamente i livelli. Per esempio è possibile

aggiornare alcuni livelli in PSD e quindi evidenziare con colore il livello a cui si vuole attirare

attenzione.

*/

class LocalScopeExtension

{

    void checkSheetColorsAndRerverse(Short[] sheetColors, PsdImage psdImage)

    {

        int layersCount = psdImage.getLayers().length;

        for (int layerIndex = 0; layerIndex < layersCount; layerIndex++)

        {

            Layer layer = psdImage.getLayers()[layerIndex];

            for (LayerResource layerResource : layer.getResources())

            {

                if (!(layerResource instanceof LclrResource))

                {

                    continue;

                }

                // Risorsa lcrl sempre presente nell'elenco delle risorse del file psd.

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("Il Colore del foglio è stato letto erroneamente");

                }

                // Stile inverso dei colori del foglio. Impostazione del colore del livello in evidenza.

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// Nell'archivio i colori dei livelli di evidenziazione sono in questo ordine

Short[] sheetColors = new Short[] {

        SheetColorHighlightEnum.Rosso,

        SheetColorHighlightEnum.Arancione,

        SheetColorHighlightEnum.Giallo,

        SheetColorHighlightEnum.Verde,

        SheetColorHighlightEnum.Azzurro,

        SheetColorHighlightEnum.Viola,

        SheetColorHighlightEnum.Grigio,

        SheetColorHighlightEnum.NessunColore

};

// Caricare un file PSD contenente una risorsa LclrResource predefinita

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    $.checkSheetColorsAndRerverse(sheetColors, psdImage);

    psdImage.save(outPsdFilePath, new PsdOptions());

}

finally

{

    psdImage.dispose();

}

// Carica un file PSD appena salvato

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // Colori invertiti

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. Supporto delle proprietà dei dati di LengthRecord. (Operazioni sul percorso (operazioni booleane), indice della forma nel livello, conteggio dei record dei nodi di bezier)**

{{< highlight java >}}

 /*

Un esempio di cambiamento delle operazioni sul percorso quando si lavora con le forme. Il programma legge

record di percorso vettoriale predefinito (LengthRecord) e cambia le loro operazioni sul percorso quindi salva

una copia modificata del documento come nuovo file PSD.

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// Carica un file PSD contenente una risorsa vsms predefinita

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Trova il primo VsmsResource tra le risorse del livello predefinito

    VsmsResource resource = null;

    for (LayerResource layerResource : psdImage.getLayers()[1].getResources())

    {

        if (layerResource instanceof VsmsResource)

        {

            resource = (VsmsResource)layerResource;

            break;

        }

    }

    LengthRecord lengthRecord0 = (LengthRecord)resource.getPaths()[2];

    LengthRecord lengthRecord1 = (LengthRecord)resource.getPaths()[7];

    LengthRecord lengthRecord2 = (LengthRecord)resource.getPaths()[11];

    // Cambiare il modo in cui le forme sono combinate

    lengthRecord0.setPathOperations(PathOperations.EscludiFormeSovrapposte);

    lengthRecord1.setPathOperations(PathOperations.IntersecaAreeForme);

    lengthRecord2.setPathOperations(PathOperations.SottraiFrontForma);

    // Salva una copia modificata del file PSD caricato sul percorso

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-158. Supporto del Colore di sfondo dell'immagine della sezione di risorsa #1010**

{{< highlight java >}}

 /*

Un esempio di lettura e modifica di una risorsa di colore di sfondo.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// Carica un file PSD contenente una risorsa di colore di sfondo predefinita

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    BackgroundColorResource backgroundColorResource = null;

    for (ResourceBlock imageResource : psdImage.getImageResources())

    {

        if (imageResource instanceof BackgroundColorResource)

        {

            backgroundColorResource = (BackgroundColorResource)imageResource;

            break;

        }

    }

    if (backgroundColorResource == null)

    {

        throw new Exception("Risorsa di colore di sfondo non trovata");

    }

    // Aggiorna il colore della risorsa di colore di sfondo

    backgroundColorResource.setColor(Color.getDarkerRed());

    // Salva una copia modificata del file PSD caricato sul percorso

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-161. Aggiunta di livelli di riempimento durante l'esecuzione**

{{< highlight java >}}

 /*

Un esempio di aggiunta di livelli di riempimento di tipi differenti a un documento Photoshop.

*/

String outPsdFilePath = "output.psd";

// Crea un documento Photoshop con una tela vuota

PsdImage psdImage = new PsdImage(100, 100);

try

{

    // Aggiungi livelli di riempimento di tipi diversi a PSD

    FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);

    colorFillLayer.setDisplayName("Livello di Riempimento a Colori");

    psdImage.addLayer(colorFillLayer);

    FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);

    gradientFillLayer.setDisplayName("Livello di Riempimento a Gradiente");

    psdImage.addLayer(gradientFillLayer);

    FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);

    patternFillLayer.setDisplayName("Livello di Riempimento con Motivo");

    patternFillLayer.setOpacity((byte)50);

    psdImage.addLayer(patternFillLayer);

    // Salva una copia modificata del file PSD caricato sul percorso

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-168. Supporto delle informazioni di bordo dell'immagine della sezione di risorsa #1009**

{{< highlight java >}}

 /*

Un esempio di lettura, modifica e salvataggio di un file PSD che contiene una risorsa di informazioni di bordo.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// Carica un file PSD contenente una risorsa di immagine predefinita

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    ResourceBlock[] imageResources = psdImage.getImageResources();

    // Trova prima risorsa di informazioni di bordo nelle ris