---
title: Notes de version d'Aspose.PSD pour .NET 21.6
type: docs
weight: 70
url: /fr/net/aspose-psd-pour-net-21-6-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-546|Le masque de découpe pour un groupe ne se rend pas correctement|Erreur|
|PSDNET-547|Le masque régulier ou vectoriel pour un groupe de calques est ignoré lors du rendu|Erreur|
|PSDNET-647|L'image PSD avec des masques de calque vectoriels désactivés lors de l'enregistrement active les masques vectoriels|Erreur|
|PSDNET-786|Exception lors de la création d'un calque de texte avec un texte de plus de 255 caractères|Erreur|
|PSDNET-900|Le texte du calque de texte ne peut pas être rendu sur Linux|Amélioration|

## **Changements dans l'API publique**
# **APIs ajoutées:**
- Aucune

# **APIs supprimées:**
- Aucune

## **Exemples d'utilisation**

**PSDNET-546. Le masque de découpe pour un groupe ne se rend pas correctement**

{{< highlight csharp >}}
string nomFichierSource = "AppleClip.psd";
string nomFichierSortie = "result.png";

Utilisation de (PsdImage image = (PsdImage)Image.Load(nomFichierSource))
    {
        image.Save(nomFichierSortie, new PngOptions());
    }
{{< /highlight >}}

**PSDNET-547. Le masque régulier ou vectoriel pour un groupe de calques est ignoré lors du rendu**

{{< highlight csharp >}}
    string nomFichierSource = "Stripes3Mask.psd";
    string nomFichierSortie = "OutputStripes3Mask.png";
    Utilisation de (PsdImage image = (PsdImage)Image.Load(nomFichierSource))
    {
        image.Save(nomFichierSortie, new PngOptions());
    }
{{< /highlight >}}

**PSDNET-647. L'image PSD avec des masques de calque vectoriels désactivés lors de l'enregistrement active les masques vectoriels**

{{< highlight csharp >}}
    string nomFichierSource = "FourWithMasksVd.psd";
    string nomFichierSortie = "FourWithMasksVdOutput.psd";

    Utilisation de (PsdImage image = (PsdImage)Image.Load(nomFichierSource))
    {
        image.Save(nomFichierSortie);
    }
{{< /highlight >}}

**PSDNET-786. Exception lors de la création d'un calque de texte avec un texte de plus de 255 caractères**

{{< highlight csharp >}}
    string sortie = "output.psd";

    Utilisation de (var image = new PsdImage(100, 100))
    {
        string texte = new string('a', 256);
        image.AddTextLayer(texte, Rectangle.Empty);

        image.Save(sortie);
    }
{{< /highlight >}}
