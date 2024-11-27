---
title: Notes de version Aspose.PSD pour .NET 20.6
type: docs
weight: 70
url: /fr/net/aspose-psd-for-net-20-6-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 20.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-606 |Support de la ressource LnkE|Fonctionnalité|
|PSDNET-386 |Support de britResource (Ressource de calque d'ajustement de luminosité/contraste)|Fonctionnalité|
|PSDNET-219|Déplacer le paramètre DefaultReplacementFont dans la classe ImageOptionsBase|Amélioration|
|PSDNET-596|Le groupe de calques avec un mode de fusion autre que PassThrough n'est pas rendu|Bogue|
|PSDNET-610|Exception NullReference lors de la tentative de conversion d'un fichier Psd particulier en image|Bogue|
|PSDNET-636|Les fichiers PSD redimensionnés fonctionnent de manière incorrecte s'il existe un masque dans le calque d'ajustement dont les limites sont vides|Bogue|
|PSDNET-611|Exception Overflow lors de la tentative d'ouverture d'un fichier Psd particulier|Bogue|
|PSDNET-565|L'image Psd en mode RVB 16 bits/canal met à jour les calques uniquement en aperçu|Bogue|
|PSDNET-652|Exception lors du chargement d'un fichier PSD spécifique avec la ressource LnkE composée et la propriété adobeStockLicenseState|Bogue|
|PSDNET-640|Les modifications du masque de calque PSD sont ignorées à l'enregistrement|Bogue|
|PSDNET-593|L'enregistrement d'un fichier AI au format Jpeg2000 ne fonctionne pas|Bogue|
|PSDNET-638|Ordre de calque incorrect après avoir ajouté un groupe de calques à un groupe de calques vide|Bogue|

## **Changements d'API publique**
# **APIs ajoutées :**
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
# **APIs supprimées :**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.DefaultReplacementFont

## **Exemples d'utilisation :**
**PSDNET-606. Support de la ressource LnkE**

{{< highlight java >}}

string message = "L'exemple de support de la ressource LnkE ne fonctionne pas correctement.";

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

// Cet exemple montre comment obtenir et définir les propriétés de la ressource LnkE de Photoshop Psd qui contient des informations sur un fichier externe lié.

void ExampleOfLnkEResourceSupport(

    string cheminFichier,

    int longueur,

    int longueur2,

    int longueur3,

    int longueur4,

    string cheminComplet,

    string date,

    double tempsModifActif,

    string idDocEnfant,

    bool verrouillé,

    string uid,

    string nom,

    string nomFichierOriginal,

    string typeFichier,

    long taille)

{

    string nomFichier = Path.GetFileName(cheminFichier);

    string cheminSortie = @"Output\" + nomFichier;

    using (PsdImage image = (PsdImage)Image.Load(cheminFichier))

    {

        LnkeResource ressourceLnke = null;

        foreach (var ressource in image.GlobalLayerResources)

        {

            ressourceLnke = ressource as LnkeResource;

            if (ressourceLnke != null)

            {

                AssertAreEqual(ressourceLnke.Longueur, longueur);

                AssertAreEqual(ressourceLnke.UniqueId, new Guid(uid));

                AssertAreEqual(ressourceLnke.CheminComplet, cheminComplet);

                AssertAreEqual(ressourceLnke.Date.ToString(CultureInfo.InvariantCulture), date);

                AssertAreEqual(ressourceLnke.TempsModifActif, tempsModifActif);

                AssertAreEqual(ressourceLnke.Verrouillé, verrouillé);

                AssertAreEqual(ressourceLnke.NomFichier, nom);

                AssertAreEqual(ressourceLnke.TailleFichier, taille);

                AssertAreEqual(ressourceLnke.IdDocEnfant, idDocEnfant);

                AssertAreEqual(ressourceLnke.Version, 7);

                AssertAreEqual(ressourceLnke.TypeFichier, typeFichier);

                AssertAreEqual(ressourceLnke.CréateurFichier, string.Empty);

                AssertAreEqual(ressourceLnke.NomFichierOriginal, nomFichierOriginal);

                AssertAreEqual(ressourceLnke.CompId, -1);

                AssertAreEqual(ressourceLnke.OriginalCompId, -1);

                AssertIsTrue(ressourceLnke.PossèdeDescripteurFichierOuvert);

                AssertIsTrue(!ressourceLnke.IsEmpty);

                AssertIsTrue(ressourceLnke.Type == LinkResourceType.liFE);

                ressourceLnke.CheminComplet =

                    @"file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png";

                AssertAreEqual(ressourceLnke.Longueur, longueur2);

                ressourceLnke.NomFichier = "rgb8_2x23.png";

                AssertAreEqual(ressourceLnke.Longueur, longueur3);

                ressourceLnke.IdDocEnfant = Guid.NewGuid().ToString();

                AssertAreEqual(ressourceLnke.Longueur, longueur4);

                ressourceLnke.Date = DateTime.Now;

                ressourceLnke.TempsModifActif = double.MaxValue;

                ressourceLnke.TailleFichier = long.MaxValue;

                ressourceLnke.TypeFichier = "test";

                ressourceLnke.CréateurFichier = "file";

                ressourceLnke.CompId = int.MaxValue;

                break;

            }

        }

        AssertIsTrue(ressourceLnke != null);

        image.Save(cheminSortie, new PsdOptions(image));

    }

    using (PsdImage image = (PsdImage)Image.Load(cheminSortie))

    {

        image.Save(

            Path.ChangeExtension(cheminSortie, "png"),

            new PngOptions

            {

                ColorType = PngColorType.TruecolorWithAlpha

            });

    }

}

// Cet exemple montre comment obtenir et définir les propriétés de la ressource LnkE de Psd qui contient des informations sur une image JPEG externe liée.

this.ExampleOfLnkEResourceSupport(

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

// Cet exemple montre comment obtenir et définir les propriétés de la ressource LnkE de Psd qui contient des informations sur une image PNG externe liée.

this.ExampleOfLnkEResourceSupport(

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

// Cet exemple montre comment obtenir et définir les propriétés de la ressource LnkE de Photoshop Psd qui contient des informations sur un actif de bibliothèque CC.

this.ExampleOfLnkEResourceSupport(

    "rgb8_2x2_asset_linked.psd",

    0x398,

    0x38c,

    0x388,

    0x3d0,

    @"CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (Fonctionnalité disponible dans Photoshop CC 2015)",

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

**PSDNET-201. Support de la progression de conversion de document**

{{< highlight java >}}

string cheminFichierSource = "Apple.psd";

Stream fluxSortie = new MemoryStream();

ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo infosProgression)

{

      string message = string.Format(

           "{0} {1} : {2} sur {3}",

           infosProgression.Description,

           infosProgression.EventType,

           infosProgression.Value,

           infosProgression.MaxValue);

      Console.WriteLine(message);

};

Console.WriteLine("---------- Chargement de Apple.psd ----------");

var optionsChargement = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };

using (PsdImage image = (PsdImage)Image.Load(cheminFichierSource, optionsChargement))

{

      Console.WriteLine("---------- Enregistrement de Apple.psd au format PNG ----------");

      image.Save(

           fluxSortie,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler

           });

      Console.WriteLine("---------- Enregistrement de Apple.psd au format PSD ----------");

      image.Save(

           fluxSortie,

           new PsdOptions()

           {

                 ColorMode = ColorModes.Rgb,

                 ChannelsCount = 4,

                 ProgressEventHandler = localProgressEventHandler

           });

}

{{< /highlight >}}

**PSDNET-386. Support de britResource (Ressource de calque d'ajustement de luminosité/contraste)**

{{< highlight java >}}

 /* Cet exemple montre comment vous pouvez modifier de manière programmatique la ressource Brightness/Contrast Layer d'une image PSD

   Il s'agit d'une API Aspose.PSD de niveau inférieur. Vous pouvez utiliser le calque de luminosité/contraste via son API, ce qui sera beaucoup plus facile, 

   mais l'édition directe de ressources Photoshop vous donne plus de contrôle sur le contenu du fichier PSD.  */

string chemin = @"BrightnessContrastPS6.psd";

string cheminSortie = @"BrightnessContrastPS6_output.psd";

using (PsdImage im = (PsdImage)Image.Load(chemin))

{

    foreach (var calque in im.Layers)

    {

        if (calque is BrightnessContrastLayer)

        {

            foreach (var ressourceCalque in calque.Resources)

            {

                if (ressourceCalque is BritResource)

                {

                    var ressource = (BritResource)ressourceCalque;

                    isRequiredResourceFound = true;

                    if (ressource.Luminosité != -40 ||

                        ressource.Contraste != 10 ||

                        ressource.LabColor != false ||

                        ressource.ValeurMoyennePourLuminositéEtContraste != 127)

                    {

                        throw new Exception("La ressource BritResource a été lue de manière incorrecte");

                    }

                    // Test modification et enregistrement

                    ressource.Luminosité = 25;

                    ressource.Contraste = -14;

                    ressource.LabColor = true;

                    ressource.ValeurMoyennePourLuminositéEtContraste = 200;

                    im.Save(cheminSortie, new PsdOptions());

                    break;

                }

            }

        }

    }

}

{{