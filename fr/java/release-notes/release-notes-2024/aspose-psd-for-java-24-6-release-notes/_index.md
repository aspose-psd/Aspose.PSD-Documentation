---
title: Notes de publication Aspose.PSD pour Java 24.6
type: docs
weight: 40
url: /fr/java/aspose-psd-for-java-24-6-release-notes/
---

{{% alert color="primary" %}} Cette page contient les notes de publication pour [Aspose.PSD pour Java 24.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.6/) {{% /alert %}}

| **Clé**     | **Résumé**                                                                                                      | **Catégorie** |
|:------------|:-----------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-628 | Implémenter le support de la calque de carte de dégradé                                                              | Fonctionnalité|
| PSDJAVA-629 | [Format AI] Ajouter le support des métadonnées XPacket au format AI                                                | Fonctionnalité|
| PSDJAVA-630 | Implémenter les types de déformation Inflate, Squeeze et Twist                                                      | Fonctionnalité|
| PSDJAVA-631 | Les modes Rgb et Lab ne peuvent pas contenir moins de 3 canaux ni plus de 4 canaux dans le fichier avec des calques ArtBoard | Problème     |
| PSDJAVA-632 | La zone de traitement supérieure doit être positive. (Paramètre 'areaToProcess') lors du traitement d'un fichier spécifique     | Problème     |
| PSDJAVA-633 | L'image étendue sur le canevas est rognée après l'enregistrement. Les données sont perdues mais l'aperçu est correct        | Problème     |

## **Changements dans l'API publique**
# **APIs ajoutées :**

- M:com.aspose.psd.fileformats.ai.AiImage.getXmpData
- M:com.aspose.psd.fileformats.psd.PsdImage.addGradientMapAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GrdmResource.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GrdmResource.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- T:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.GradientMapLayer
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.GradientMapLayer.setGradientSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.GradientMapLayer.getGradientSettings
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getExpansionCount
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setExpansionCount(short) 
- T:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.gradientKindToStr(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.noiseColorModelToInt(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.noiseColorModelToStr(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.intToNoiseColorModel(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.strToGradientKind(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.strToNoiseColorModel(java.lang.String)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrGradientNoise
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrGradientSolid
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrModelHSB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrModelLAB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrModelRGB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.IntModelRGB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.IntModelLAB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.IntModelHSB
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getGradientName
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setGradientName(java.lang.String)

# **APIs supprimées :**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getGradientName
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setGradientName(java.lang.String)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.gradientKindToStr(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.noiseColorModelToStr(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.strToGradientKind(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.strToNoiseColorModel(java.lang.String)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrGradientNoise
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrGradientSolid
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelHSB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelLAB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelRGB

## **Exemples d'utilisation :**

**PSDJAVA-628. Implémenter le support de la calque de carte de dégradé**

{{< highlight java >}}

    public static void main(String[] args) {
        String fichierSource = "src/main/resources/gradient_map_src.psd";
        String fichierSortie = "src/main/resources/gradient_map_src_output.psd";

        try (PsdImage im = (PsdImage) Image.load(fichierSource)) {
            // Ajouter un calque d'ajustement de carte de dégradé.
            GradientMapLayer calque = im.addGradientMapAdjustmentLayer();
            calque.getGradientSettings().setReverse(true);

            im.save(fichierSortie);
        }

        // Vérifier les modifications enregistrées
        try (PsdImage im = (PsdImage) Image.load(fichierSortie)) {
            GradientMapLayer calqueCarteDegradé = (GradientMapLayer) im.getLayers()[1];
            GradientFillSettings paramètresGradient = (GradientFillSettings) calqueCarteDegradé.getGradientSettings();

            assertAreEqual(0.0, paramètresGradient.getAngle());
            assertAreEqual((short) 4096, paramètresGradient.getInterpolation());
            assertAreEqual(true, paramètresGradient.getReverse());
            assertAreEqual(false, paramètresGradient.getAlignWithLayer());
            assertAreEqual(false, paramètresGradient.getDither());
            assertAreEqual(GradientType.Linear, paramètresGradient.getGradientType());
            assertAreEqual(100, paramètresGradient.getScale());
            assertAreEqual(0.0, paramètresGradient.getHorizontalOffset());
            assertAreEqual(0.0, paramètresGradient.getVerticalOffset());
            assertAreEqual("Custom", paramètresGradient.getGradientName());
        }
    }

    static void assertAreEqual(Object attendu, Object réel) {
        assertAreEqual(attendu, réel, "Les objets ne sont pas égaux.");
    }

    static void assertAreEqual(Object attendu, Object réel, String message) {
        if (!attendu.equals(réel)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-629. [Format AI] Ajouter le support des métadonnées XPacket au format AI**

{{< highlight java >}}

    public static void main(String[] args) {
        String fichierSource = "src/main/resources/ai_one.ai";

        String cléOutilCréateur = ":CreatorTool";
        String cléNPages = "xmpTPg:NPages";
        String cléUnité = "stDim:unit";
        String cléHauteur = "stDim:h";
        String cléLargeur = "stDim:w";

        String outilCréateurAttendu = "Adobe Illustrator CC 22.1 (Windows)";
        String nPagesAttendu = "1";
        String unitéAttendue = "Pixels";
        double hauteurAttendue = 768;
        double largeurAttendue = 1366;

        try (AiImage image = (AiImage) Image.load(fichierSource)) {
            // Les métadonnées Xmp ont été ajoutées.
            var métadonnéesXmp = image.getXmpData();

            assertIsNotNull(métadonnéesXmp);

            // Maintenant, nous pouvons accéder aux paquets Xmp des fichiers AI.
            var packageBasique = (XmpBasicPackage) métadonnéesXmp.getPackage(Namespaces.XmpBasic);
            XmpPackage paquet_ = métadonnéesXmp.getPackages()[4];
            // Et nous avons accès au contenu de ces paquets.
            var outilCréateur = packageBasique.get_Item(cléOutilCréateur).toString();
            var nPages = paquet_.get_Item(cléNPages);
            var unité = paquet_.get_Item(cléUnité);
            var hauteur = Double.parseDouble(paquet_.get_Item(cléHauteur).toString());
            var largeur = Double.parseDouble(paquet_.get_Item(cléLargeur).toString());

            assertAreEqual(outilCréateur, outilCréateurAttendu);
            assertAreEqual(nPages, nPagesAttendu);
            assertAreEqual(unité, unitéAttendue);
            assertAreEqual(hauteur, hauteurAttendue);
            assertAreEqual(largeur, largeurAttendue);
        }
    }

    static void assertAreEqual(Object attendu, Object réel) {
        assertAreEqual(attendu, réel, "Les objets ne sont pas égaux.");
    }

    static void assertAreEqual(Object attendu, Object réel, String message) {
        if (!attendu.equals(réel)) {
            throw new IllegalArgumentException(message);
        }
    }

    static void assertIsNotNull(Object objetTest) {
        if (objetTest == null) {
            throw new RuntimeException("L'objet de test est nul.");
        }
    }

{{< /highlight >}}

**PSDJAVA-630. Implémenter les types de déformation Inflate, Squeeze et Twist**

{{< highlight java >}}

    String[] fichiers = {"Twist", "Squeeze", "Squeeze_vert", "Inflate"};

    for (String préfixe : fichiers) {
        String fichierSource = "src/main/resources/" + préfixe + ".psd";
        String fichierSortie = "src/main/resources/" + préfixe + "_export.png";

        PsdLoadOptions optionsChargementPsd = new PsdLoadOptions();
        optionsChargementPsd.setAllowWarpRepaint(true);
        optionsChargementPsd.setLoadEffectsResource(true);
        try (PsdImage imagePsd = (PsdImage) Image.load(fichierSource, optionsChargementPsd)) {
            PngOptions optionsPng = new PngOptions();
            optionsPng.setColorType(PngColorType.TruecolorWithAlpha);
            imagePsd.save(fichierSortie, optionsPng);
        }
    }

{{< /highlight >}}

**PSDJAVA-631. Les modes Rgb et Lab ne peuvent pas contenir moins de 3 canaux ni plus de 4 canaux dans le fichier avec des calques ArtBoard**

{{< highlight java >}}

    String fichierSource = "src/main/resources/Rgb5Channels.psb";
    String fichierSortie = "src/main/resources/Rgb5Channels_output.psd";

    try (PsdImage image = (PsdImage) Image.load(fichierSource)) {
        // Il ne devrait y avoir aucune exception ici
        image.save(fichierSortie);
    }

{{< /highlight >}}

**PSDJAVA-632. La zone de traitement supérieure doit être positive. (Paramètre 'areaToProcess') lors du traitement d'un fichier spécifique**

{{< highlight java >}}

    String fichierSource = "src/main/resources/BANNERS_2_Intel-Gamer_psak.psd";
    String fichierSortie = "src/main/resources/BANNERS_2_Intel-Gamer_psak_out.psd";
    PsdLoadOptions optionsChargementPsd = new PsdLoadOptions();
    optionsChargementPsd.setLoadEffectsResource(true);
    optionsChargementPsd.setAllowWarpRepaint(true);
    try (PsdImage image = (PsdImage) PsdImage.load(fichierSource, optionsChargementPsd)) {
        image.save(fichierSortie);
        // Ne devrait pas y avoir d'exception
    }

{{< /highlight >}}

**PSDJAVA-633. L'image étendue sur le canevas est rognée après l'enregistrement. Les données sont perdues mais l'aperçu est correct**

{{< highlight java >}}

    String fichierSource = "src/main/resources/bigfile.psd";

    String fichierSortie = "src/main/resources/bigfile_output.psd";
    String imageSortie = "src/main/resources/bigfile.png";

    PsdLoadOptions optionsChargement = new PsdLoadOptions();
    optionsChargement.setLoadEffectsResource(true);
    optionsChargement.setUseDiskForLoadEffectsResource(true);

    try (var imagePsd = (PsdImage) Image.load(fichierSource, optionsChargement)) {
        PsdOptions optionsPsd = new PsdOptions();
        optionsPsd.setCompressionMethod(CompressionMethod.RLE);
        // Il ne devrait y avoir aucune erreur ici
        imagePsd.save(fichierSortie, optionsPsd);
    }

    try (var imagePsd = (PsdImage) Image.load(fichierSortie, optionsChargement)) {
        imagePsd.resize(imagePsd.getWidth() / 10, imagePsd.getHeight() / 10);

        PngOptions optionsPng = new PngOptions();
        optionsPng.setColorType(PngColorType.TruecolorWithAlpha);
        // Il ne devrait y avoir aucune erreur ici
        imagePsd.save(imageSortie, optionsPng);
    }

{{< /highlight >}}