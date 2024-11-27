---
title: Aspose.PSD pour Java 24.3 - Notes de version
type: docs
weight: 40
url: /fr/java/aspose-psd-pour-java-24-3-notes-de-version/
---

{{% alert color="primary" %}} Cette page contient les notes de version pour [Aspose.PSD pour Java 24.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.3/) {{% /alert %}}

| **Clé**     | **Résumé**                                                                 | **Catégorie** |
|:-----------|:--------------------------------------------------------------------------|:-------------|
| PSDJAVA-601 | [Format AI] Réduire le temps de chargement des grandes images AI multipages. | Amélioration  |
| PSDJAVA-604 | Le fichier PSD après la conversion de 8 bits en 16 bits est devenu illisible. | Problème      |
| PSDJAVA-605 | Le fichier PSD après la conversion de 8 bits en 32 bits est devenu illisible. | Problème      |
| PSDJAVA-606 | [Format AI] Corriger le rendu de la courbe courte dans le fichier AI.       | Problème      |

## **Changements de l'API publique**
# **APIs ajoutées :**

- T:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.getFilters
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isEnabled 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskEnabled 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskExtendWithWhite 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskLinked 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isValidAtPosition 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.setFilters(com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter[])
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.updateResourceValues 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.#ctor 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.apply(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.applyToMask(com.aspose.psd.fileformats.psd.layers.Layer)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.deepClone 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getBlendMode 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getName 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getOpacity 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getSourceDescriptor 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setBlendMode(long)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setOpacity(double)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.isEnabled 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.#ctor 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.FilterType 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getAmountNoise 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getDistribution 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getName 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setAmountNoise(double)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setDistribution(int)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setMonochromatic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.isMonochromatic 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.rendering.ISmartFilterRenderer.render(com.aspose.psd.PixelsData)
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.#ctor 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.FilterType 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getName 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getRadius 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.setRadius(double)
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.rendering.ISmartFilterRenderer 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution.Gaussian 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution.Uniform 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter.getName

# **APIs supprimées :**

- Aucune

## **Exemples d'utilisation :**

** PSDJAVA-604. Le fichier PSD après la conversion de 8 bits en 16 bits est devenu illisible **

{{< highlight java >}}

        String fichierSource = "src/main/resources/test_smart_layer.psd";
        String fichierSortie = "src/main/resources/export.psd";

        try (PsdImage imagePsd8 = (PsdImage) Image.load(fichierSource)) {
            PsdOptions optionsPsd16 = new PsdOptions();
            optionsPsd16.setChannelBitsCount((short) 16);

            imagePsd8.save(fichierSortie, optionsPsd16);
        }

        try (PsdImage imagePsd16 = (PsdImage) Image.load(fichierSortie)) {
            if (imagePsd16.getGlobalLayerResources()[0] instanceof Lr16Resource) {
                // est bon
            } else {
                throw new Exception("Mauvaise ressource globale, la première ressource doit être Lr16Resource");
            }
        }

{{< /highlight >}}

** PSDJAVA-605. Le fichier PSD après la conversion de 8 bits en 32 bits est devenu illisible **

{{< highlight java >}}

        String fichierSource = "src/main/resources/test_smart_layer.psd";
        String fichierSortie = "src/main/resources/export.psd";

        try (PsdImage imagePsd8 = (PsdImage) Image.load(fichierSource)) {
            PsdOptions optionsPsd32 = new PsdOptions();
            optionsPsd32.setChannelBitsCount((short) 32);

            imagePsd8.save(fichierSortie, optionsPsd32);
        }

        try (PsdImage imagePsd8 = (PsdImage) Image.load(fichierSortie)) {
            if (imagePsd8.getGlobalLayerResources()[0] instanceof Lr32Resource) {
                // est bon
            } else {
                throw new Exception("Mauvaise ressource globale, la première ressource doit être Lr16Resource");
            }
        }

{{< /highlight >}}

** PSDJAVA-606. [Format AI] Corriger le rendu de la courbe courte dans le fichier AI **

{{< highlight java >}}

        String fichierSource = "src/main/resources/shortCurve.ai";
        String cheminFichierSortie = "src/main/resources/shortCurve.png";

        try (AiImage image = (AiImage) Image.load(fichierSource)) {
            image.save(cheminFichierSortie, new PngOptions());
        }

{{< /highlight >}}
