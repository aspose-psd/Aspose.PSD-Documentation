---
title: Notes de publication Aspose.PSD pour Java 20.5
type: docs
weight: 40
url: /fr/java/aspose-psd-pour-java-20-5-notes-de-release/
---

{{% alert color="primary" %}} Cette page contient les notes de publication pour [Aspose.PSD pour Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) {{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDJAVA-188|Prise en charge de la progression de conversion de document|Fonctionnalité|
|PSDJAVA-197|Prise en charge de l'enregistrement de l'image PSD en mode de couleur niveaux de gris avec 16 bits par canal|Fonctionnalité|
|PSDJAVA-198|Prise en charge des ressources Nvrt (Calque d'ajustement d'inversion)|Fonctionnalité|
|PSDJAVA-200|Support des masques de calque pour les groupes de calques|Fonctionnalité|
|PSDJAVA-195|Correction de l'enregistrement de l'image PSD en mode de couleur niveaux de gris 16 bits par canal au format PSD RVB 16 bits par canal|Bogue|
|PSDJAVA-196|Correction de l'enregistrement de l'image PSD en mode de couleur niveaux de gris 16 bits par canal au format PSD niveaux de gris 8 bits par canal|Bogue|
|PSDJAVA-199|L'alignement du texte via ITextPortion ne fonctionne pas pour les langues de droite à gauche. Le fichier de sortie est endommagé.|Bogue|
|PSDJAVA-201|Exception lors de la tentative d'ouverture d'un fichier Psd particulier avec couleur Lab et 8 bits/canal|Bogue|
# **Modifications de l'API publique**
# **APIs ajoutées :**
- Aucune
## **APIs supprimées :**
- Aucune
# **Exemples d'utilisation:**

**PSDJAVA-188. Prise en charge de la progression de conversion de document**

{{< highlight java >}}

 // Un exemple d'utilisation du gestionnaire de progression pour les opérations de chargement et d'enregistrement.

// Le programme utilise différentes options d'enregistrement pour déclencher des événements de progression.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// Crée un gestionnaire de progression qui écrit des informations de progression dans la console

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s : %s sur %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Chargement d'Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Associe le gestionnaire de progression pour afficher la progression du chargement

loadOptions.setProgressEventHandler(localProgressEventHandler);

// Charge le PSD en utilisant des options de chargement spécifiques

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Enregistrement d'Apple.psd au format PNG ----------");

    PngOptions pngOptions = new PngOptions();

    // Rendre l'image de sortie en couleur et non transparente

    pngOptions.setColorType(PngColorType.Truecolor);

    // Associe le gestionnaire de progression pour afficher la progression de l'enregistrement

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // Convertit le PSD en PNG avec des caractéristiques spécifiques

    image.save(outputStream, pngOptions);

    System.out.println("---------- Enregistrement d'Apple.psd au format PSD ----------");

    PsdOptions psdOptions = new PsdOptions();

    // Rendre le PSD de sortie en couleur

    psdOptions.setColorMode(ColorModes.Rgb);

    // Définir un canal pour chaque couleur (rouge, vert et bleu) plus un canal composite

    psdOptions.setChannelsCount((short)4);

    // Associe le gestionnaire de progression pour afficher la progression de l'enregistrement

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // Enregistrer une copie du PSD avec des caractéristiques spécifiques

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Prise en charge de l'enregistrement de l'image PSD en mode de couleur niveaux de gris avec 16 bits par canal**

{{< highlight java >}}

 // Un exemple d'application de différentes combinaisons de modes de couleur, de bits par canal, de comptes de canaux et de compressions pour des calques spécifiques.

// Permet à une méthode d'être accessible à partir de la portée locale

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String file,

            short colorMode,

            short channelBitsCount,

            short channelsCount,

            short compression,

            int layerNumber)

    {

        String filePath = file + ".psd";

        String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +

                channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);

        String exportPath = file + postfix + ".psd";

        String pngExportPath = file + postfix + ".png";

        // Charge un PSD en niveaux de gris prédéfini sur 16 bits

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // Dessine une bordure interne grise autour du périmètre du calque

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // Enregistre une copie du PSD avec des caractéristiques spécifiques

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(colorMode);

            psdOptions.setChannelBitsCount(channelBitsCount);

            psdOptions.setChannelsCount(channelsCount);

            psdOptions.setCompressionMethod(compression);

            image.save(exportPath, psdOptions);

        }

        finally

        {

            image.dispose();

        }

        // Charge le PSD enregistré

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // Convertit le PSD enregistré en une image PNG en niveaux de gris

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // il ne devrait y avoir aucune exception ici

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. Prise en charge des ressources Nvrt (Calque d'ajustement d'inversion)**

{{< highlight java >}}

 // Un exemple de recherche de la ressource Nvrt d'un calque d'ajustement d'inversion.

String inPsdFilePath = "CalqueAjustementInversion.psd";

NvrtResource nvrtResource = null;

// Charge un PSD prédéfini contenant un calque d'ajustement d'inversion

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Tente de trouver une ressource du calque d'ajustement d'inversion

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // La ressource Nvrt est trouvée

                    nvrtResource = (NvrtResource)layerResource;

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

**PSDJAVA-200. Prise en charge des masques de calque pour les groupes de calques**

{{< highlight java >}}

 // Un exemple de prise en charge des masques de calque pour les groupes de calques. Le programme charge et enregistre dans des formats de sortie différents sans générer d'exceptions.

String srcFile = "psdnet595.psd";

String outputPng = "sortie.png";

String outputPsd = "sortie.psd";

// Charge un PSD prédéfini contenant des masques de calque pour les groupes de calques

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // Convertit le PSD chargé en PNG

    input.save(outputPng, new PngOptions());

    // Enregistre une copie du PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. Correction de l'enregistrement de l'image PSD en mode de couleur niveaux de gris 16 bits par canal au format PSD RVB 16 bits par canal**

{{< highlight java >}}

 // Un exemple de conversion d'un PSD en niveaux de gris 16 bits en un PSD RVB 16 bits, puis à nouveau en

// une image raster en niveaux de gris 16 bits.

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "sortie_rgb16bit5x5.psd";

String pngExportPath = "sortie_rgb16bit5x5.png";

// Charge un PSD prédéfini en niveaux de gris 16 bits

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Dessine une bordure interne grise autour du périmètre du calque

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Enregistre une copie du PSD avec le mode de couleur modifié en RVB

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Rgb);

    psdOptions.setChannelBitsCount((short)16);

    psdOptions.setChannelsCount((short)4);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// Charge le PSD enregistré

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Convertit le PSD enregistré en une image PNG en niveaux de gris

    image1.save(pngExportPath, pngOptions); // il ne devrait y avoir aucune exception ici

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. Correction de l'enregistrement de l'image PSD en mode de couleur niveaux de gris 16 bits par canal au format PSD niveaux de gris 8 bits par canal**

{{< highlight java >}}

 // Un exemple de conversion d'un PSD en niveaux de gris 16 bits en un PSD en niveaux de gris 8 bits, puis en

// une image raster en niveaux de gris 8 bits.

String sourceFilePath = "niveauxdegris16bit.psd";

String exportFilePath = "sortie_niveauxdegris16bit.psd";

String pngExportPath = "sortie_niveauxdegris16bit.png";

// Charge un PSD prédéfini en niveaux de gris 16 bits

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Dessine une bordure interne grise autour du périmètre du calque

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Enregistre une copie du PSD avec le nombre de canaux changé en 8 bits

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Grayscale);

    psdOptions.setChannelBitsCount((short)8);

    psdOptions.setChannelsCount((short)2);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// Charge le PSD enregistré

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Convertit le PSD enregistré en une image PNG en niveaux de gris

    image1.save(pngExportPath, pngOptions); // il ne devrait y avoir aucune exception ici

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. L'alignement du texte via ITextPortion ne fonctionne pas pour les langues de droite à gauche. Le fichier de sortie est endommagé.**

{{< highlight java >}}

 // Un exemple d'alignement d'un calque de texte de droite à gauche via ITextPortion. Le programme modifie

// un calque de texte RTL existant dans le PSD chargé et enregistre une copie du document modifié.

String sourceFileName = "bidi.psd";

String outputFileName = "bidiSortie.psd";

// Charge un PSD prédéfini contenant un calque de texte RTL

PsdImage image = (PsdImage)Image.load(sourceFileName);

try

{

    // Obtient les portions de texte du calque

    TextLayer layer = (TextLayer)image.getLayers()[2];

    ITextPortion[] portions = layer.getTextData().getItems();

    // Change l'alignement du texte

    portions[0].getParagraph().setJustification(2);

    // Applique les changements au calque

    layer.getTextData().updateLayerData();

    // Enregistre une copie modifiée du PSD

    image.save(outputFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-201. Exception lors de la tentative d'ouverture d'un fichier PSD particulier avec couleur Lab et 8 bits/canal**

{{< highlight java >}}

 // Un exemple de prise en charge d'un document Photoshop 8 bits en mode de couleur LAB.

String srcFile = "SansTitre-1.psd";

String outputFilePsd = "sortie.psd";

// Charge un PSD 8 bits prédéfini en mode de couleur LAB

PsdImage psdImage = (PsdImage)Image.load(srcFile);

try

{

    // Enregistre une copie du PSD chargé

    psdImage.save(outputFilePsd);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}