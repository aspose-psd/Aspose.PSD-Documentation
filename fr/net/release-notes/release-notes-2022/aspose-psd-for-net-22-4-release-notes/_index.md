---
title: Notes de version d'Aspose.PSD pour .NET 22.4
type: docs
weight: 90
url: /fr/net/aspose-psd-for-net-22-4-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 22.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-261|Affichage de l'effet de contour externe|Fonctionnalité|
|PSDNET-1123|Ajout de la prise en charge de la licence Sha256|Amélioration|
|PSDNET-1107|Le positionnement du texte sur plusieurs lignes ne correspond pas au résultat dans Photoshop|Erreur|
|PSDNET-1113|Problème lors du chargement du fichier PSD sur l'analyse des données de ressource de texte|Erreur|
|PSDNET-1129|Position incorrecte du motif personnalisé après l'enregistrement en tant que PSD|Erreur|


## **Changements d'API publics**
# **APIs ajoutées :**
- T:Aspose.PSD.FileFormats.Psd.JustificationMode
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Gauche
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Droite
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Centre
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddOuterGlow
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.CouleurDeRemplissage
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.ModeDeMélange
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.EstVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Opacité
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Intensité
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.AntiCrénelage
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Etalement
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Taille
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Bruit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.EstFlouDouxD
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Portée
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Décalage


# **APIs supprimées :**
- Aucune


## **Exemples d'utilisation:**

**PSDNET-261. Affichage de l'effet de contour externe**
{{< highlight csharp >}}
string src = "CalqueVert.psd";
string output = "sortie261.png";

using (var image = (PsdImage)Image.Load(src))
{
    OuterGlowEffect effet = image.Layers[1].BlendingOptions.AddOuterGlow();
    effet.Portée = 10;
    effet.Etalement = 10;
    ((IColorFillSettings)effet.CouleurDeRemplissage).Couleur = Color.Red;
    effet.Opacité = 128;
    effet.ModeDeMélange = BlendMode.Normal;

    image.Save(output, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1107. Le positionnement du texte sur plusieurs lignes ne correspond pas au résultat dans Photoshop**

{{< highlight csharp >}}
string src = "source1107.psd";
string outputPsd = "sortie.psd";
string outputPng = "sortie.png";

using (var image = (PsdImage)Image.Load(src))
{ 
   var calqueTxt = image.AddTextLayer("Ligne de texte1\rLigne de texte2\rLigne de texte3", new Rectangle(200, 200, 500, 500));
   var portions = calqueTxt.DonnéesTexte.Items;

   portions[0].Paragraphe.Justification = JustificationMode.Gauche;
   portions[1].Paragraphe.Justification = JustificationMode.Droite;
   portions[2].Paragraphe.Justification = JustificationMode.Centre;

   calqueTxt.DonnéesTexte.MettreÀJourDonnéesCalque();

   image.Save(outputPsd);
   image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1113. Problème lors du chargement du fichier PSD sur l'analyse des données de ressource de texte**

{{< highlight csharp >}}
string fichierSource = "entrée.psd";

using (PsdImage image = (PsdImage) Image.Load(fichierSource))
{
    // Chargé avec succès.
}
{{< /highlight >}}

**PSDNET-1129. Position incorrecte du motif personnalisé après l'enregistrement en tant que PSD**

{{< highlight csharp >}}
string fichierSource = "entrée_1129.psd";
string outputPsd = "sortie_psdnet1129.psd";
string outputPng = "sortie_psdnet1129.png";

using (PsdImage image = (PsdImage) Image.Load(fichierSource))
{
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
