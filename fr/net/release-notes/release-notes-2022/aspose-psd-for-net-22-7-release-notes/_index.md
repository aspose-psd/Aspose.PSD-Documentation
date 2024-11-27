---
title: Notes de version Aspose.PSD pour .NET 22.7
type: docs
weight: 60
url: /fr/net/aspose-psd-for-net-22-7-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 22.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-482|Support de la ressource de section d'image #4000-4999 Plug-In|Fonctionnalité|
|PSDNET-875|Une exception non gérée de type "System.OutOfMemoryException" se produit dans Aspose.PSD.dll|Erreur|
|PSDNET-1050|Après l'exportation du fichier PSD, le résultat est beaucoup plus grand que le fichier source|Erreur|
|PSDNET-1083|Analyse incorrecte des données pour XmpResource|Erreur|
|PSDNET-1205|Après l'exportation, la taille des fichiers PSD avec des sous-dossiers a augmenté|Erreur|


## **Changements dans l'API publique**
# **APIs ajoutées :**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Items
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.SaveData(Aspose.PSD.StreamContainer)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.KeyName
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.AnimatedDataSection
- M:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.SaveData(Aspose.PSD.StreamContainer)


# **APIs supprimées :**
- Aucune


## **Exemples d'utilisation :**

**PSDNET-482. Support de la ressource de section d'image #4000-4999 Plug-In**

{{< highlight csharp >}}
// Le code suivant démontre comment définir/mettre à jour le temps de délai dans la trame de ligne de temps de données animées.
string fichierSource = "3_animé.psd";
string sortiePsd = "sortie_3_animé.psd";

T TrouverStructure<T>(IEnumerable<OSTypeStructure> structures, string nomCle) where T : OSTypeStructure
{
    foreach (var structure in structures)
    {
        if (structure.KeyName.ClassName == nomCle)
        {
            return structure as T;
        }
    }

    return null;
}

OSTypeStructure[] AjouterOuRemplacerStructure(IEnumerable<OSTypeStructure> structures, OSTypeStructure nouvelleStructure)
{
    List<OSTypeStructure> listeStructures = new List<OSTypeStructure>(structures);

    for (int i = 0; i < listeStructures.Count; i++)
    {
        OSTypeStructure structure = listeStructures[i];
        if (structure.KeyName.ClassName == nouvelleStructure.KeyName.ClassName)
        {
            listeStructures.RemoveAt(i);
            break;
        }
    }

    listeStructures.Add(nouvelleStructure);

    return listeStructures.ToArray();
}

using (PsdImage image = (PsdImage)Image.Load(fichierSource))
{
    foreach (var ressourceImage in image.ImageResources)
    {
        if (ressourceImage is AnimatedDataSectionResource)
        {
            var donnéesAnimées =
            (AnimatedDataSectionStructure) (ressourceImage as AnimatedDataSectionResource).AnimatedDataSection;
            var listeTrames = TrouverStructure<ListStructure>(donnéesAnimées.Items, "FrIn");

            var trame1 = (DescriptorStructure)listeTrames.Types[1];

            // Crée l'enregistrement de délai de trame avec la valeur 100 centi-secondes, équivalente à 1 seconde.
            var délaiTrame = new IntegerStructure(new ClassID("FrDl"));
            délaiTrame.Value = 100; // définir le temps en centi-secondes.

            trame1.Structures = AjouterOuRemplacerStructure(trame1.Structures, délaiTrame);

            break;
        }
    }

    image.Save(sortiePsd);
}
{{< /highlight >}}

**PSDNET-875. Une exception non gérée de type "System.OutOfMemoryException" se produit dans Aspose.PSD.dll**

{{< highlight csharp >}}
string fichierSrc = "001-.psd";
string cheminJpg = "T_0003.jpg";
string cheminSortieFichier = "nouveau_outputPsd.psd";

using (var im = (PsdImage)Image.Load(fichierSrc))
{
    using (FileStream fs = new FileStream(cheminJpg, FileMode.Open))
    {
        var nouvelleCouche = new Aspose.PSD.FileFormats.Psd.Layers.Layer(fs);
        nouvelleCouche.DisplayName = "NouvelleCouche";

        im.AddLayer(nouvelleCouche);

        im.Save(cheminSortieFichier, true);   
    }
}
{{< /highlight >}}

**PSDNET-1050. Après l'exportation du fichier PSD, le résultat est beaucoup plus grand que le fichier source**

{{< highlight csharp >}}
string source = "ShimadzuLetterhead100.psd";
string sortie = "output.psd";
using (var img = (PsdImage)Image.Load(source))
{
    img.Save(sortie);
}

double tailleSortieMb = new FileInfo(sortie).Length / 1024d / 1024d;
if (tailleSortieMb > 6)
{
    throw new Exception("Le fichier de sortie est plus grand qu'il ne devrait l'être.");
}
{{< /highlight >}}

**PSDNET-1083. Analyse incorrecte des données pour XmpResource**

{{< highlight csharp >}}
string cheminImagePsdEntree = @"entrée.psd";
string cheminIamgePsdSauvé = @"sauvé.psd";

bool originalContient = false;
bool sauvegardéContient = false;

// Trouver la sous-clé XMP dans le fichier d'entrée
using (PsdImage img = (PsdImage)Image.Load(cheminImagePsdEntree))
{
    foreach (var package in img.XmpData.Packages)
    {
        foreach (var pack in package)
        {
            if (pack.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)pack.Value;

                string valeurXml = xmpArray.GetXmlValue();

                if (valeurXml.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    originalContient = true;
                    break;
                }
            }
        }

        if (originalContient)
        {
            break;
        }
    }
    img.Save(cheminIamgePsdSauvé);
}

// Trouver la sous-clé XMP dans le fichier sauvegardé
using (PsdImage img = (PsdImage)Image.Load(cheminIamgePsdSauvé))
{
    foreach (var package in img.XmpData.Packages)
    {
        foreach (var pack in package)
        {
            if (pack.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)pack.Value;

                string valeurXml = xmpArray.GetXmlValue();

                if (valeurXml.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    sauvegardéContient = true;
                    break;
                }
            }
        }

        if (sauvegardéContient)
        {
            break;
        }
    }
    img.Save(cheminIamgePsdSauvé);
}

if (originalContient && sauvegardéContient)
{
    // Tout fonctionne correctement !
}
else
{
    throw new Exception("Cela ne fonctionne pas.");
}
{{< /highlight >}}

**PSDNET-1205. Après l'exportation, la taille des fichiers PSD avec des sous-dossiers a augmenté**

{{< highlight csharp >}}
string[] fichiersSource = new string[] { "1lvlDossiersTest.psd", "5lvlDossiersTest.psd"};

foreach (var nomFichier in fichiersSource)
{
    string cheminFichierSource = nomFichier;
    string cheminFichierSortie = "output_" + nomFichier;

    using (PsdImage image = (PsdImage)Image.Load(cheminFichierSource))
    {
        image.Save(cheminFichierSortie);
    }

    double tailleSortieMb = new FileInfo(cheminFichierSortie).Length / 1024d / 1024d;
    if (tailleSortieMb > 1.9)
    {
        throw new Exception("Le fichier de sortie est plus grand qu'il ne devrait l'être.");
    }
}
{{< /highlight >}}
