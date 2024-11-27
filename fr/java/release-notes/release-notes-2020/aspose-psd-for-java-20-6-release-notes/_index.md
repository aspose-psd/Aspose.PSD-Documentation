---
title: Notes de version Aspose.PSD pour Java 20.6
type: docs
weight: 50
url: /fr/java/aspose-psd-for-java-20-6-release-notes/
---

{{% alert color="primary" %}} Cette page contient les notes de version pour [Aspose.PSD pour Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) {{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDJAVA-216|Support de LnkEResource (Ressource de la couche d'objet intelligent)|Fonctionnalité|
|PSDJAVA-219|Prise en charge de britResource (Ressource de la couche d'ajustement luminosité/contraste)|Fonctionnalité|
|PSDJAVA-222|Déplacer le paramètre DefaultReplacementFont dans la classe ImageOptionsBase|Amélioration|
|PSDJAVA-217|Le redimensionnement des fichiers PSD ne fonctionne pas correctement s'il y a un masque dans la couche d'ajustement qui a des limites vides|Bogue|
|PSDJAVA-218|L'image Psd en mode RVB 16 bits/canal ne met à jour que les calques en mode aperçu|Bogue|
|PSDJAVA-220|Les modifications du masque de calque PSD sont ignorées lors de l'enregistrement|Bogue|
|PSDJAVA-221|Ordre de calque incorrect après avoir ajouté un groupe de calques vide à un groupe de calques vide|Bogue|
|PSDJAVA-223|Exception lors du chargement d'un fichier PSD spécifique avec la ressource LnkE composite et la propriété adobeStockLicenseState|Bogue|
|PSDJAVA-224|L'enregistrement d'un fichier AI au format Jpeg2000 ne fonctionne pas|Bogue|
|PSDJAVA-225|Le groupe de calques avec un mode de fusion non Passthrough n'est pas rendu|Bogue|
|PSDJAVA-226|Exception NullReference lors de la tentative de conversion d'un fichier Psd particulier en image|Bogue|
|PSDJAVA-227|OverflowException lors de la tentative d'ouverture d'un fichier Psd particulier|Bogue|

# **Modifications de l'API publique**
# **APIs ajoutées:**
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
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.get_Item(int)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSourceType
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource
## **APIs supprimées:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)
# **Exemples d'utilisation:**

**PSDJAVA-216: Support de LnkEResource (Ressource de la couche d'objet intelligent)**

{{< highlight java >}}

 // Un exemple de liaison de différents types de ressources (images matricielles, bibliothèques CC) à un PSD.

// Également considérer l'API de LnkeResource.

// Une classe qui contient des méthodes dans la portée locale

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("ExampleOfLnkEResourceSupport fonctionne incorrectement.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // Cet exemple montre comment obtenir et définir les propriétés de la ressource LnkE du Psd Photoshop

    // qui contient des informations sur un fichier lié externe.

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

        // Charger un PSD prédéfini

        PsdImage image = (PsdImage)Image.load(fileName);

        try

        {

            // Rechercher LnkeResource parmi les ressources globales

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // Vérification des propriétés de LnkeResource

                    assertAreEqual(lnkeResource.getLength(), length);

                    assertAreEqual(lnkeResource.get_Item(0).getUniqueId(), UUID.fromString(uid));

                    assertAreEqual(lnkeResource.get_Item(0).getFullPath(), fullPath);

                    assertAreEqual(new SimpleDateFormat("MM/dd/yyyy HH:mm:ss").format(lnkeResource.get_Item(0).getDate()), date);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetModTime(), assetModTime);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetLockedState(), locked);

                    assertAreEqual(lnkeResource.get_Item(0).getFileName(), name);

                    assertAreEqual(lnkeResource.get_Item(0).getFileSize(), size);

                    assertAreEqual(lnkeResource.get_Item(0).getChildDocId(), childDocId);

                    assertAreEqual(lnkeResource.get_Item(0).getVersion(), 7);

                    assertAreEqual(lnkeResource.get_Item(0).getFileType().trim(), fileType);

                    assertAreEqual(lnkeResource.get_Item(0).getFileCreator().trim(), "");

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalFileName(), originalFileName);

                    assertAreEqual(lnkeResource.get_Item(0).getCompId(), -1);

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalCompId(), -1);

                    assertIsTrue(lnkeResource.get_Item(0).hasFileOpenDescriptor());

                    assertIsTrue(!lnkeResource.isEmpty());

                    assertIsTrue(lnkeResource.get_Item(0).getType() == LinkDataSourceType.liFE);

                    // Mettre à jour les propriétés de LnkeResource

                    lnkeResource.get_Item(0).setFullPath("file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png");

                    assertAreEqual(lnkeResource.getLength(), length2);

                    lnkeResource.get_Item(0).setFileName("rgb8_2x23.png");

                    assertAreEqual(lnkeResource.getLength(), length3);

                    lnkeResource.get_Item(0).setChildDocId(UUID.randomUUID().toString());

                    assertAreEqual(lnkeResource.getLength(), length4);

                    lnkeResource.get_Item(0).setDate(new Date());

                    lnkeResource.get_Item(0).setAssetModTime(Double.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileSize(Long.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileType("test");

                    lnkeResource.get_Item(0).setFileCreator("file");

                    lnkeResource.get_Item(0).setCompId(Integer.MAX_VALUE);

                    break;

                }

            }

            // Assurez-vous que LnkeResource est pris en charge

            assertIsTrue(lnkeResource != null);

            // Enregistrer une copie du PSD chargé

            image.save(outputPath, new PsdOptions(image));

        }

        finally

        {

            image.dispose();

        }

        // Charger la copie enregistrée

        PsdImage image1 = (PsdImage)Image.load(outputPath);

        try

        {

            // Convertir PSD en format de fichier PNG (avec canal alpha pour la transparence)

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            image1.save(Path.changeExtension(outputPath, "png"), pngOptions);

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Cet exemple montre comment obtenir et définir les propriétés de la ressource LnkE Psd qui

// contient des informations sur un fichier JPEG externe lié.

$.exampleOfLnkEResourceSupport(

        "photooverlay_5_new.psd",

        0x21c,

        0x26c,

        0x274,

        0x27c,

        "file:///C:/Users/cvallejo/Desktop/photo.jpg",

        "05/09/2017 22:24:51",

        0,

        "F062B9DB73E8D124167A4186E54664B0",

        false,

        "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

        "photo.jpg",

        "photo.jpg",

        "JPEG",

        0x1520d);

// Cet exemple montre comment obtenir et définir les propriétés de la ressource LnkE Psd

// qui contient des informations sur un fichier PNG externe lié.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_linked.psd",

        0x284,

        0x290,

        0x294,

        0x2dc,

        "file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

        "04/14/2020 14:23:44",

        0,

        "",

        false,

        "5867318f-3174-9f41-abca-22f56a75247e",

        "rgb8_2x2.png",

        "rgb8_2x2.png",

        "png",

        0x53);

// Cet exemple montre comment obtenir et définir les propriétés de la ressource LnkE Photoshop Psd

// qui contient des informations sur un actif de bibliothèque CC lié.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_asset_linked.psd",

        0x398,

        0x38c,

        0x388,

        0x3d0,

        "CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (La fonctionnalité est disponible dans Photoshop CC 2015)",

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

**PSDJAVA-219: Support de britResource (Ressource de la couche d'ajustement luminosité/contraste)**

{{< highlight java >}}

 // Cet exemple montre comment vous pouvez modifier de manière programmatique la ressource de calque luminosité/contraste de l'image PSD. Il s'agit d'une API de bas niveau Aspose.PSD. Vous pouvez utiliser la couche de luminosité/contraste à travers son API, ce qui sera beaucoup plus facile, mais l'édition directe des ressources Photoshop vous donne plus de contrôle sur le contenu du fichier PSD.

String srcPath = "BrightnessContrastPS6.psd";

String dstPath = "BrightnessContrastPS6_output.psd";

// Charger un document Photoshop contenant une couche d'ajustement luminosité/contraste

PsdImage psdImage = (PsdImage)Image.load(srcPath);

try

{

    // Recherche de BritResource

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof BrightnessContrastLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof BritResource)

                {

                    BritResource resource = (BritResource)layerResource;

                    // Vérifier les propriétés de la ressource

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throwune RuntimeException("BritResource a été lu incorrectement");

                    }

                    // Mettre à jour les propriétés de la ressource

                    resource.setBrightness((short)25);

                    resource.setContrast((short)-14);

                    resource.setLabColor(true);

                    resource.setMeanValueForBrightnessAndContrast((short)200);

                    // Enregistrer une copie du PSD mis à jour

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


**PSDJAVA-217: Le redimensionnement des fichiers PSD ne fonctionne pas correctement s'il y a un masque dans la couche d'ajustement qui a des limites vides**

{{< highlight java >}}

 // Un exemple de redimensionnement d'une image contenant un masque de calque d'ajustement avec des limites vides. Le programme charge un PSD prédéfini juste pour vérifier s'il n'y a pas d'exceptions.

final int échelle = 2; // coefficient arbitraire

String[] noms = {

        "UneRegulièreEtUneAvecVecteurEtMasqueDeCalque",

        "CalqueDeNiveauxAvecMasqueDeCalqueRgb",

        "CalqueDeNiveauxAvecMasqueDeCalqueCmyk",

};

for (String nom : noms)

{

    String cheminFichierSrc = nom + ".psd";

    String cheminFichierDst = "sortie_" + cheminFichierSrc;

    String cheminFichierPngDst = "sortie_" + nom + ".png";

    // Charger un PSD prédéfini contenant un masque de calque d'ajustement avec des limites vides

    PsdLoadOptions optionsPsd = new PsdLoadOptions();

    optionsPsd.setLoadEffectsResource(true);

    PsdImage image = (PsdImage)Image.load(cheminFichierSrc, optionsPsd);

    try

    {

        // Redimensionner l'image

        image.resize(image.getWidth() * échelle, image.getHeight() * échelle);

        // Enregistrer une copie du PSD chargé

        image.save(cheminFichierDst, new PsdOptions());

        // Exporter le PSD au format de fichier PNG (avec canal alpha pour la transparence)

        PngOptions optionsPng = new PngOptions();

        optionsPng.setColorType(PngColorType.TruecolorWithAlpha);

        image.save(cheminFichierPngDst, optionsPng);

    }

    finally

    {

        image.dispose();

    }

}

{{< /highlight >}}


**PSDJAVA-218: L'image Psd en mode RVB 16 bits/canal ne met à jour que les calques en mode aperçu**

{{< highlight java >}}

 // Un exemple de mise à jour des calques réguliers pour une image RVB 16 bits. Le programme dessine quelque chose

// sur chaque calque juste pour s'assurer que le calque entier est mis à jour correctement.

String cheminFichierSource = "in.psd";

String cheminFichierSortie = "output.psd";

// Charger un PSD prédéfini en mode RVB 16 bits

PsdImage image = (PsdImage)Image.load(cheminFichierSource);

try

{

    for (Layer calque : image.getLayers())

    {

        // Dessiner le nom du calque et une bordure intérieure pour le calque régulier

        if (!(calque instanceof LayerGroup) && !(calque instanceof AdjustmentLayer) &&

                (calque.getWidth() > 100) && (calque.getHeight() > 100))

        {

            Graphics graphiques = new Graphics(calque);

            graphiques.drawString(calque.getName(), new Font("Arial", 10),

                    new SolidBrush(Color.getRed()), 15, 45);

            graphiques.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

        }

    }

    // Enregistrer une copie du PSD chargé

    image.save(cheminFichierSortie, new PsdOptions(image));

}

finally

{

    image.dispose();

}

{{< /highlight >}}


**PSDJAVA-220: Les modifications du masque de calque PSD sont ignorées lors de l'enregistrement**

{{< highlight java >}}

 // Une classe qui contient des méthodes dans la portée locale

class LocalScopeExtension

{

    void assertAreEqual(Object actual, Object expected)

    {

        if (!(actual != null && actual.equals(expected)))

        {

            throw new FormatException("L'exemple fonctionne incorrectement.");

        }

    }

    // Obtient la valeur int convertie en octets big-endians.

    byte[] getBigEndianBytesInt32(int valeur)

    {

        byte[] octets = new byte[4];

        octets[0] = (byte)((valeur >> 24) & 0x000000FF);

        octets[1] = (byte)((valeur >> 16) & 0x000000FF);

        octets[2] = (byte)((valeur >> 8) & 0x000000FF);

        octets[3] = (byte)valeur;

        return octets;

    }

    // Obtient la valeur convertie du big-endian en Int32.

    int fromBigEndianToInt32(byte[] octets, int index)

    {

        if (octets == null)

        {

            throw new ArgumentNullException("octets");

        }

        if (index < 0 || index + 4 > octets.length)

        {

            throw new ArgumentOutOfRangeException("index", "L'index est hors du tableau d'octets.");

        }

        return ((octets[index] & 0xff) << 24) | ((octets[index + 1] & 0xff) << 16) |

                ((octets[index + 2] & 0xff) << 8) | (octets[index + 3] & 0xff);

    }

    // Obtient un masque de trame du calque d'une image PSD et l'enregistre dans un fichier

    void saveRasterMask(String cheminFichierMasque, Layer calque)

    {

        LayerMaskDataShort donneesMasque = (LayerMaskDataShort)calque.getLayerMaskData();

        FileStreamContainer conteneur = FileStreamContainer.createFileStream(cheminFichierMasque, false);

        try

        {

            conteneur.write(getBigEndianBytesInt32(donneesMasque.getTop()));

            conteneur.write(getBigEndianBytesInt32(donneesMasque.getLeft()));

            conteneur.write(getBigEndianBytesInt32(donneesMasque.getBottom()));

            conteneur.write(getBigEndianBytesInt32(donneesMasque.getRight()));

            conteneur.writeByte(donneesMasque.getDefaultColor());

            conteneur.writeByte((byte)donneesMasque.getFlags());

            conteneur.write(getBigEndianBytesInt32(donneesMasque.getImageData().length));

            conteneur.write(donneesMasque.getImageData(), 0, donneesMasque.getImageData().length);

        }

        finally

        {

            conteneur.dispose();

        }

    }

    // Ajoute un masque de trame à partir du fichier au calque et enregistre l'image au format Psd

    void addRasterMask(Layer calque, String cheminSourceMasque)

    {

        LayerMaskDataShort donneesMasque = new LayerMaskDataShort();

        FileStreamContainer conteneur = FileStreamContainer.openFileStream(cheminSourceMasque);

        try

        {

            byte[] octets = new byte[22];

            assertAreEqual(conteneur.read(octets), 22);

            donneesMasque.setTop(fromBigEndianToInt32(octets, 0));

            donneesMasque.setLeft(fromBigEndianToInt32(octets, 4));

            donneesMasque.setBottom(fromBigEndianToInt32(octets, 8));

            donneesMasque.setRight(fromBigEndianToInt32(octets, 12));

            donneesMasque.setDefaultColor(octets[16]);

            donneesMasque.setFlags(octets[17]);

            int longueurDonneesImage = fromBigEndianToInt32(octets, 18);

            byte[] donnees = new byte[longueurDonneesImage];

            assertAreEqual(donneesMasque.getMaskRectangle().getWidth() *

                    donneesMasque.getMaskRectangle().getHeight(), longueurDonneesImage);

            assertAreEqual(conteneur.read(donnees), longueurDonneesImage);

            donneesMasque.setImageData(donnees);

        }

        finally

        {

            conteneur.dispose();

        }

        // Ajouter uniquement LayerMaskData ne suffit pas pour l'enregistrement correct car les canaux ne sont pas mis à jour;

        // layer.setLayerMaskData(mask); // Cela n'ajoute pas le canal de masque

        // Ajouter (ou mettre à jour) le masque

        calque.addLayerMask(donneesMasque); // Mais cela ajoute / met à jour à la fois le masque et les canaux!

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Cet exemple montre comment obtenir, mettre à jour, supprimer et ajouter des masques de trame dans le fichier Photoshop® de manière programmatique.

PngOptions optionsPng = new PngOptions();

optionsPng.setColorType(PngColorType.TruecolorWithAlpha);

String cheminFichierSource = "FourWithMasks.psd";

PsdImage image = (PsdImage)Image.load(cheminFichierSource);

try

{

    Layer calque = image.getLayers()[2];

    // Obtenir un masque de trame à partir du calque et l'enregistrer dans un fichier

    $.saveRasterMask("FourWithMasks2.msk", calque);

    // Changer le masque de calque (inverser) et enregistrer l'image

    LayerMaskData masque = calque.getLayerMaskData();

    byte[] donneesMasque = masque.getImageData();

    for (int i = 0; i < donneesMasque.length; i++)

    {

        donneesMasque[i] = (byte)~donneesMasque[i];

    }

    // Changer simplement le LayerMaskData suffit pour l'effet de rendu

    image.save("FourWithMasksUpdated2.png", optionsPng);

    // Mais changer simplement LayerMaskData ne suffit pas pour l'enregistrement correct car les canaux ne sont pas mis à jour;

    calque.setLayerMaskData(masque); 

    calque.addLayerMask(masque); 

    image.save("FourWithMasksUpdated2.psd");

    // Retirer un masque de trame du calque et enregistrer l'image

    calque.setLayerMaskData(null); 

    image.save("FourWithMasksRemoved2.png", optionsPng);

    calque.addLayerMask(null); 

    image.save("FourWithMasksRemoved2.psd");

    // Ajouter un masque de trame à partir du fichier au calque et enregistrer l'image

    $.addRasterMask(calque, "raster.msk");

    image.save("FourWithMasksAdded2.png", optionsPng);

    image.save("FourWithMasksAdded2.psd");

}

finally

{

    image.dispose();

}

{{< /highlight >}}


**PSDJAVA-221: Ordre de calque incorrect après avoir ajouté un groupe de calques vide à un groupe de calques vide**

{{< highlight java >}}

 // Cet exemple montre comment ajouter un groupe de calques imbriqué à un PSD de manière programmatique.

String cheminPsdDst = "output.psd";

// Créer une image avec une taille de 1x1 pixels pour travailler

PsdImage psdImage = new PsdImage(1, 1);

try

{

    // Ajouter un groupe de calques parent ("true" signifie ouvrir le groupe de calques au démarrage)

    LayerGroup groupe1 = psdImage.addLayerGroup("Groupe 1", 0, true);

    // Ajouter un groupe de calques imbriqué

    LayerGroup groupe2 = groupe1.addLayerGroup("Groupe 2", 0);

    if (groupe1.getLayers().length != 2)

    {

        throw new RuntimeException("Le Groupe 1 doit contenir deux calques de Groupe 2.");

    }

    // Vérifier qu'il n'y a pas d'exceptions lors de l'enregistrement des groupes de calques créés

    psdImage.save(cheminPsd