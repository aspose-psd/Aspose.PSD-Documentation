---
title: Notes de version Aspose.PSD pour Java 23.8
type: docs
weight: 40
url: /fr/java/aspose-psd-pour-java-23-8-notes-de-version/
---

{{% alert color="primary" %}} Cette page contient les notes de version pour [Aspose.PSD pour Java 23.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.8/) {{% /alert %}}

| **Clé**     | **Résumé**                                                                                                                                      | **Catégorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-518 | Ajouter un nouveau type de distorsion (Drapeau)                                                                                                  |    Fonctionnalité   |
| PSDJAVA-519 | Ajouter de nouveaux types de distorsion : arc vers le haut, arc vers le bas, sphère                                                              |    Fonctionnalité   |
| PSDJAVA-520 | Implémenter une nouvelle méthode PsdImage.AddPosterizeAdjustmentLayer pour ajouter un nouveau calque Posterize                                    |    Fonctionnalité   |
| PSDJAVA-521 | Informations PSD perdues juste en ouvrant et en enregistrant                                                                                     |      Problème     |
| PSDJAVA-522 | Échec du chargement de l'image                                                                                                                  |      Problème     |
| PSDJAVA-523 | Échec du chargement de l'image : Impossible de convertir l'objet de type UnknownStructure en type DescriptorStructure                           |      Problème     |
| PSDJAVA-524 | Le fichier modifié dans la bibliothèque tierce corrompt le fichier PSD mais il peut être ouvert dans Photoshop                                  |      Problème     |

## **Changements de l'API publique**
# **APIs ajoutées :**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **APIs supprimées :**

- Aucune

## **Exemples d'utilisation :**

**PSDJAVA-518. Ajouter un nouveau type de distorsion (Drapeau)**

{{< highlight java >}}
    String fichierSource = "src/main/resources/flag_warp.psd";
    String fichierSortie = "src/main/resources/flag_export.png";

    PsdLoadOptions optionsChargementPsd = new PsdLoadOptions();
    optionsChargementPsd.setAllowWarpRepaint(true);
    optionsChargementPsd.setLoadEffectsResource(true);
    try (PsdImage imagePsd = (PsdImage) Image.load(fichierSource, optionsChargementPsd)) {
        PngOptions optionsPng = new PngOptions();
        optionsPng.setColorType(PngColorType.TruecolorWithAlpha);

        imagePsd.save(fichierSortie, optionsPng);
    }
{{< /highlight >}}

**PSDJAVA-519. Ajouter de nouveaux types de distorsion : arc vers le haut, arc vers le bas, sphère**

{{< highlight java >}}
    String fichierSourceArcHaut = "src/main/resources/arc_upper_warp.psd";
    String fichierSourceArcBas = "src/main/resources/arc_lower_warp.psd";
    String fichierSourceBosse = "src/main/resources/bulge_warp.psd";

    String fichierSortieArcHaut = "src/main/resources/ArcUpper_export.png";
    String fichierSortieArcBas = "src/main/resources/ArcLower_export.png";
    String fichierSortieBosse = "src/main/resources/Bulge_export.png";

    PsdLoadOptions optionsChargementPsd = new PsdLoadOptions();
    optionsChargementPsd.setAllowWarpRepaint(true);
    optionsChargementPsd.setLoadEffectsResource(true);

    PngOptions optionsPng = new PngOptions();
    optionsPng.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage imagePsd = (PsdImage) Image.load(fichierSourceArcHaut, optionsChargementPsd)) {
        imagePsd.save(fichierSortieArcHaut, optionsPng);
    }

    try (PsdImage imagePsd = (PsdImage) Image.load(fichierSourceArcBas, optionsChargementPsd)) {
        imagePsd.save(fichierSortieArcBas, optionsPng);
    }

    try (PsdImage imagePsd = (PsdImage) Image.load(fichierSourceBosse, optionsChargementPsd)) {
        imagePsd.save(fichierSortieBosse, optionsPng);
    }
{{< /highlight >}}

**PSDJAVA-520. Implémenter une nouvelle méthode PsdImage.AddPosterizeAdjustmentLayer pour ajouter un nouveau calque Posterize**

{{< highlight java >}}
public static void main(String[] args) {
    String fichierSrc = "src/main/resources/zendeya.psd";
    String fichierSortie = "src/main/resources/zendeya.psd.out.psd";

    try (PsdImage imagePsd = (PsdImage) Image.load(fichierSrc)) {
        imagePsd.addPosterizeAdjustmentLayer();
        imagePsd.save(fichierSortie);
    }

    PsdLoadOptions optionsChargementPsd = new PsdLoadOptions();
    optionsChargementPsd.setLoadEffectsResource(true);

    // Vérifier les modifications enregistrées
    try (PsdImage image = (PsdImage) Image.load(fichierSortie, optionsChargementPsd)) {
        assertAreEqual(2, image.getLayers().length);

        PosterizeLayer calquePosterize = (PosterizeLayer) image.getLayers()[1];

        assertAreEqual(true, calquePosterize instanceof PosterizeLayer);
    }
}

static void assertAreEqual(Object attendu, Object actuel) {
    assertAreEqual(attendu, actuel, "Les objets ne sont pas égaux.");
}

static void assertAreEqual(Object attendu, Object actuel, String message) {
    if (!attendu.equals(actuel)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-521. Informations PSD perdues juste en ouvrant et en enregistrant**

{{< highlight java >}}
    String src = "src/main/resources/Fichier original.psd";
    String outputPsd = "src/main/resources/out_Fichier original.psd";
    String outputPng = "src/main/resources/out_Fichier original.png";

    try (PsdImage imagePsd = (PsdImage) Image.load(src)) {
        PngOptions optionsPng = new PngOptions();
        optionsPng.setColorType(PngColorType.TruecolorWithAlpha);

        imagePsd.save(outputPsd);
        imagePsd.save(outputPng, optionsPng);
    }
{{< /highlight >}}

**PSDJAVA-522. Échec du chargement de l'image**

{{< highlight java >}}
    String fichierSrc1 = "src/main/resources/test_text.psd";
    String fichierSrc2 = "src/main/resources/test_smart_object.psd";

    try (PsdImage imagePsd = (PsdImage) Image.load(fichierSrc1)) {
    }

    try (PsdImage imagePsd = (PsdImage) Image.load(fichierSrc2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. Échec du chargement de l'image : Impossible de convertir l'objet de type UnknownStructure en type DescriptorStructure**

{{< highlight java >}}
   try (PsdImage nouveauPsd = new PsdImage(10, 10)) {
        nouveauPsd.addLayer(FillLayer.createInstance(FillType.Gradient));

        final MemoryStream memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000);
        try {
            nouveauPsd.save(memStream.toOutputStream());

            memStream.seek(DescriptorStructure.StructureKey, SeekOrigin.Current);
            memStream.write(new byte[1], 0, 0);
            memStream.setPosition(0);

            try (PsdImage imagePsd = (PsdImage) Image.load(memStream.toInputStream())) {
                // Devrait se charger correctement
            }
        } finally {
            memStream.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. Le fichier modifié dans la bibliothèque tierce corrompt le fichier PSD mais il peut être ouvert dans Photoshop**

{{< highlight java >}}
    String fichierSource = "src/main/resources/output.psd";
    String fichierSortie = "src/main/resources/export.png";

    PsdLoadOptions optionsChargementPsd = new PsdLoadOptions();
    optionsChargementPsd.setLoadEffectsResource(true);

    try (PsdImage imagePsd = (PsdImage) Image.load(fichierSource, optionsChargementPsd)) {
        PngOptions optionsPng = new PngOptions();
        optionsPng.setCompressionLevel(9);
        optionsPng.setColorType(PngColorType.TruecolorWithAlpha);

        imagePsd.save(fichierSortie, optionsPng);
    }
{{< /highlight >}}
