---
title: Notes de version d'Aspose.PSD pour Java 24.7
type: docs
weight: 40
url: /fr/java/aspose-psd-for-java-24-7-release-notes/
---

{{% alert color="primary" %}} Cette page contient les notes de version pour [Aspose.PSD pour Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}}

| **Clé**     | **Résumé**                                                                                      | **Catégorie** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | Exception "Échec du chargement de l'image." lors de l'ouverture du document AI                   | Bug          |
| PSDJAVA-636 | Texte incorrectement rendu dans les fichiers PDF de sortie                                      | Bug          |
| PSDJAVA-637 | Correction de ImageSaveException : échec de l'exportation d'image pour le fichier donné sur Linux | Bug          |
| PSDJAVA-638 | Correction du chargement des polices lors de l'utilisation d'Aspose.Drawing                      | Bug          |
| PSDJAVA-639 | 'L'opération arithmétique a entraîné un dépassement' lors de la création d'une couche d'objet intelligent en utilisant une grande image JPEG | Bug          |
| PSDJAVA-640 | Le fichier AI ne peut pas être converti en un fichier JPG                                         | Bug          |

## **Changements d'API publics**
# **APIs ajoutées :**

- Aucune

# **APIs supprimées :**

- Aucune 

## **Exemples d'utilisation :**

**PSDJAVA-635. Exception "Échec du chargement de l'image." lors de l'ouverture du document AI**

{{< highlight java >}}

    String fichierSource = "src/main/resources/[SA]_ID_card_template.ai";
    String fichierSortie = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(fichierSource)) {
        image.save(fichierSortie, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. Texte incorrectement rendu dans les fichiers PDF de sortie**

{{< highlight java >}}

    String source = "src/main/resources/CVFlor.psd";
    String sortie = "src/main/resources/sortie.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(source)) {
        PdfOptions optionsDeSauvegarde = new PdfOptions();
        optionsDeSauvegarde.setOptionsDeBasePdf(new OptionsDeBasePdf());

        psdImage.save(sortie, optionsDeSauvegarde);
    }

{{< /highlight >}}

**PSDJAVA-637. Correction de ImageSaveException : échec de l'exportation d'image pour le fichier donné sur Linux**

{{< highlight java >}}

    String fichierSource = "src/main/resources/Bed_Roll-Sticker4_1.psd";
    String fichierSortie = "src/main/resources/sortie.jpg";

    PsdLoadOptions optionsDeChargementPsd = new PsdLoadOptions();
    optionsDeChargementPsd.setChargerRessourcesEffets(true);

    try (var imagePsd = (PsdImage) Image.load(fichierSource, optionsDeChargementPsd)) {
        JpegOptions optionsDeSauvegarde = new JpegOptions();
        optionsDeSauvegarde.setQualite(70);
        imagePsd.save(fichierSortie, optionsDeSauvegarde);
    }

{{< /highlight >}}

**PSDJAVA-638. Correction du chargement des polices lors de l'utilisation d'Aspose.Drawing**

{{< highlight java >}}

    final var collectionPolicesInstallees = new InstalledFontCollection();
    try {
        System.out.println("- Avant la mise à jour. Nombre de polices installées : " + collectionPolicesInstallees.getFamilles().length);
        System.out.println("- Plateforme : " + Environment.get_VersionSystèmeExploitation().get_Plateforme());
        System.out.println("- Actualiser le cache des polices en essayant d'obtenir le nom de police Adobe pour 'Arial' : "
            + FontSettings.get_NomPoliceAdobe("Arial"));

        System.out.println("- Après la mise à jour. Nombre de polices installées : " + collectionPolicesInstallees.getFamilles().length);

        assertEgal(collectionPolicesInstallees.getFamilles().length, 1);
    } finally {
        collectionPolicesInstallees.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'L'opération arithmétique a entraîné un dépassement' lors de la création d'une couche d'objet intelligent en utilisant une grande image JPEG**

{{< highlight java >}}

    String fichierSource = "src/main/resources/source.psd";
    String imageJpg = "src/main/resources/test.jpg";

    PsdLoadOptions optionsDeChargementPsd = new PsdLoadOptions();
    optionsDeChargementPsd.setModeRécupDonnées(ModeRécupDonnées.RécupMaximale);
    try (var image = (PsdImage) Image.load(fichierSource, optionsDeChargementPsd)) {
        final FileStream flux = new FileStream(imageJpg, FileMode.Ouvrir);
        try {
            var coucheAjoutée = new SmartObjectLayer(flux);
            coucheAjoutée.setNom("Couche de test");
            image.ajouterCouche(coucheAjoutée);
        } finally {
            flux.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. Le fichier AI ne peut pas être converti en un fichier JPG**

{{< highlight java >}}

    String fichierSource = "src/main/resources/aaa.ai";
    String fichierSortie = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(fichierSource)) {
        image.save(fichierSortie, new PngOptions());
    }

{{< /highlight >}}
