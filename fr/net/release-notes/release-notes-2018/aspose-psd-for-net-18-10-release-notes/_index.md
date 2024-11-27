---
title: Aspose.PSD pour .NET 18.10 - Notes de version
type: docs
weight: 30
url: /fr/net/aspose-psd-pour-net-18-10-notes-de-version/
---

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-14|Ajouter le support des modes de fusion autres que Normal|Fonctionnalité|
|PSDNET-69|Ajouter le support de l'effet de superposition de couleur|Fonctionnalité|
|PSDNET-70|Ajouter le support de l'effet d'ombre portée|Fonctionnalité|
|PSDNET-71|Rendu pour l'export de l'effet de superposition de couleur|Fonctionnalité|
|PSDNET-72|Rendu pour l'export de l'effet d'ombre portée|Fonctionnalité|
|PSDNET-74|Support de l'ajout des effets de calque à l'exécution|Fonctionnalité|
|PSDNET-73|Optimisation des performances de chargement des ressources contenant des osTypeStructures|Bogue|
|PSDNET-79|Refonte et corrections des fuites mémoire dans LayerAndMaskInfo|Amélioration|

## **Exemples d'utilisation :**
**PSDNET-14 Ajouter le support des modes de fusion autres que Normal**

{{< highlight java >}}

 var fichiers = new string[]

{

    "Normal",

    "Dissoudre",

    "Assombrir",

    "Multiplier",

    "CarburantCouleur",

    "BrûlageLinéaire",

    "CouleurPlusSombre",

    "Éclaircir",

    "Écran",

    "DodgeCouleur",

    "DodgeLinéaireAjouter",

    "ÉclaircirCouleur",

    "Superposition",

    "LumièreDouce",

    "LumièreDure",

    "LumièreVive",

    "LumièreLinéaire",

    "LumièreDirecte",

    "PoseDure",

    "Différence",

    "Exclusion",

    "Soustraire",

    "Diviser",

    "Teinte",

    "Saturation",

    "Couleur",

    "Luminosité",

};

foreach (var nomFichier in fichiers)

{

    using (var im = LoadFile(nomFichier + ".psd"))

    {

        // Exporter en PNG

        var optionsSauvegarde = new PngOptions();

        optionsSauvegarde.TypeCouleur = PngColorType.VraiesCouleursAvecAlpha;

        var cheminExportPng100 = "ModeFusion" + nomFichier + "_Test100.png";

        im.Save(cheminExportPng100, optionsSauvegarde);

        // Régler l'opacité à 50%

        im.Calques[1].Opacite = 127;

        var cheminExportPng50 = "ModeFusion" + nomFichier + "_Test50.png";

        im.Save(cheminExportPng50, optionsSauvegarde);

    }

}

{{< /highlight >}}

**PSDNET-69 Ajouter le support de l'effet de superposition de couleur**

{{< highlight java >}}

     // Edition de l'effet de superposition de couleur

    string nomFichierSource = "SuperpositionCouleur.psd";

    string cheminPsdApresModification = "SuperpositionCouleurModifiee.psd";

    using (var im = LoadFile(nomFichierSource))

    {

       var superpositionCouleur = (SuperpositionCouleur)(im.Calques[1].OptionsDeFusion.Effets[0]);



       Assert.AreEqual(Couleur.Rouge, superpositionCouleur.Couleur);

       Assert.AreEqual(153, superpositionCouleur.Opacite);

       superpositionCouleur.Couleur = Couleur.Vert;

       superpositionCouleur.Opacite = 128;

       im.Save(cheminPsdApresModification);

    }

{{< /highlight >}}

**PSDNET-70 Ajouter le support de l'effet d'ombre portée**

{{< highlight java >}}

     // Edition de l'effet d'ombre portée

    string nomFichierSource = "Ombre.psd";

    string cheminPsdApresModification = "OmbreModifiee.psd";

    using (var im = LoadFile(nomFichierSource))

    {

       var effetOmbre = (EffetOmbrePortee)(im.Calques[1].OptionsDeFusion.Effets[0]);



       Assert.AreEqual(Couleur.Noir, effetOmbre.Couleur);

       Assert.AreEqual(255, effetOmbre.Opacite);

       Assert.AreEqual(3, effetOmbre.Distance);

       Assert.AreEqual(7, effetOmbre.Taille);

       Assert.AreEqual(true, effetOmbre.UtiliserLumiereGlobale);

       Assert.AreEqual(90, effetOmbre.Angle);

       Assert.AreEqual(0, effetOmbre.Etalement);

       Assert.AreEqual(0, effetOmbre.Bruit);

       effetOmbre.Couleur = Couleur.Vert;

       effetOmbre.Opacite = 128;

       effetOmbre.Distance = 11;

       effetOmbre.UtiliserLumiereGlobale = false;

       effetOmbre.Taille = 9;

       effetOmbre.Angle = 45;

       effetOmbre.Etalement = 3;

       effetOmbre.Bruit = 50;

       im.Save(cheminPsdApresModification);

    }

{{< /highlight >}}

