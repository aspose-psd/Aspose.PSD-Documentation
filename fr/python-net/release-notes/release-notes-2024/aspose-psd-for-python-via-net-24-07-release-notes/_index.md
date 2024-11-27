---
title: Notes de version d'Aspose.PSD pour Python via .NET 24.7
type: docs
weight: 10
url: /fr/python-net/aspose-psd-pour-python-via-net-24-7-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version d'Aspose.PSD pour Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clé**      | **Résumé**                                                                                                       | **Catégorie** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | Exception "Échec du chargement de l'image" lors de l'ouverture du document AI                                  | Bug      |
| PSDPYTHON-87 | Texte rendu de manière incorrecte dans les fichiers PDF de sortie                                             | Bug      |
| PSDPYTHON-88 | Correction de l'exception ImageSaveException: L'exportation de l'image a échoué pour le fichier donné sur Linux| Bug      |
| PSDPYTHON-89 | Correction du chargement des polices lors de l'utilisation d'Aspose.Drawing                                   | Bug      |
| PSDPYTHON-90 | 'L'opération arithmétique a donné lieu à un dépassement' lors de la création d'une couche de calque d'objet intelligent en utilisant une grande image JPEG | Bug      |
| PSDPYTHON-91 | Le fichier AI ne peut pas être converti en fichier JPG                                                         | Bug      |

## **Changements de l'API publique**

# **APIs ajoutées :**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**

**PSDPYTHON-86. Exception "Échec du chargement de l'image" lors de l'ouverture du document AI**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Texte rendu de manière incorrecte dans les fichiers PDF de sortie**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Correction de l'exception ImageSaveException: L'exportation de l'image a échoué pour le fichier donné sur Linux**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("Bed_Roll-Sticker4_1.psd")
        outputFile = self.GetFileInOutputFolder("output.jpg")

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        saveOpt = JpegOptions()
        saveOpt.quality = 70
        with PsdImage.load(sourceFile, loadOpt) as psdImage:
            psdImage.save(outputFile, saveOpt)
{{< /highlight >}}


**PSDPYTHON-89. Correction du chargement des polices lors de l'utilisation d'Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Avant la mise à jour. Nombre de polices installées : " + str(len(installedFonts.families)))
            print("- Rafraîchir le cache de polices en essayant d'obtenir le nom de police Adobe pour 'Arial' : ")
            FontSettings.get_adobe_font_name("Arial")
            print("- Après la mise à jour. Nombre de polices installées : " + str(len(installedFonts.families)))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'L'opération arithmétique a donné lieu à un dépassement' lors de la création d'une couche de calque d'objet intelligent en utilisant une grande image JPEG**
{{< highlight python >}}
        # La correction est apportée, mais il y a un autre problème dans Aspose.PSD pour Python qui limite ce test
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as image:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "Couche de test"
                #image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. Le fichier AI ne peut pas être converti en fichier JPG**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}
