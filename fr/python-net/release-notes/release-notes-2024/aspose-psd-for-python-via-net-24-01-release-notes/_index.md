---
title: Notes de publication d'Aspose.PSD pour Python via .NET 24.1
type: docs
weight: 10
url: /fr/net/aspose-psd-for-python-via-net-24-1-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD pour Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clé**      | **Résumé**                                                                                             | **Catégorie** |
|:--------------|:-------------------------------------------------------------------------------------------------------|:-------------|
|  PSDPYTHON-19 | [Format AI] Ajout d'une gestion basique pour les images AI multipages                                    |   Fonctionnalité   |
|  PSDPYTHON-22 | L'effet Texte de Déformation ne s'applique pas au texte                                                  |     Bug     |
|  PSDPYTHON-23 | Rendu incorrect du masque dans le fichier spécifique                                                     |     Bug     |
|  PSDPYTHON-24 | NullReferenceException dans Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor        |     Bug     |
|  PSDPYTHON-25 | [Format AI] Correction de l'utilisation de la mémoire dans AiExporterUtils                               |     Bug     |



## **Changements dans l'API publique**
# **APIs ajoutées :**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **APIs supprimées :**
- Aucune


## **Exemples d'utilisation :**

**PSDPYTHON-19. [Format AI] Ajout d'une gestion basique pour les images AI multipages**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Charger l'image AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # Par défaut, ActivePageIndex est 0.
            # Donc si vous sauvegardez l'image AI sans changer cette propriété, la première page sera rendue et sauvegardée.
            image.save(firstPageOutputPng, PngOptions())

            # Changer l'index de la page active pour la deuxième page.
            image.active_page_index = 1

            # Sauvegarder la deuxième page de l'image AI en tant qu'image PNG.
            image.save(secondPageOutputPng, PngOptions())

            # Changer l'index de la page active pour la troisième page.
            image.active_page_index = 2

            # Sauvegarder la troisième page de l'image AI en tant qu'image PNG.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. L'effet Texte de Déformation ne s'applique pas au texte**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("text_warp.psd")
        outputFile = self.GetFileInOutputFolder("export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)
{{< /highlight >}}

**PSDPYTHON-23. Rendu incorrect du masque dans le fichier spécifique**

{{< highlight python >}}
        sourceFile1 = self.GetFileInBaseFolder("mask_problem.psd")
        sourceFile2 = self.GetFileInBaseFolder("puh_softLight3_1.psd")
        outputFile1 = self.GetFileInOutputFolder("mask_export.png")
        outputFile2 = self.GetFileInOutputFolder("puh_export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile1, opt) as img:
            img.save(outputFile1, pngOpt)

        with PsdImage.load(sourceFile2, opt) as img:
            img.save(outputFile2, pngOpt)
{{< /highlight >}}

**PSDPYTHON-24. NullReferenceException dans Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

            with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [Format AI] Correction de l'utilisation de la mémoire dans AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # L'utilisation de la mémoire en C# est de 220, mais pour Python nous n'avons pas un accès direct aux activités du GC.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # Charger l'image AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Sauvegarder la première page de l'image AI en tant qu'image PNG.
            image.save(firstPageOutputPng, pngOpt)

            # Changer l'index de la page active pour la deuxième page.
            image.active_page_index = 1

            # Sauvegarder la deuxième page de l'image AI en tant qu'image PNG.
            image.save(secondPageOutputPng, pngOpt)

            # Changer l'index de la page active pour la troisième page.
            image.active_page_index = 2

            # Sauvegarder la troisième page de l'image AI en tant qu'image PNG.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("L'utilisation de la mémoire est trop importante. {} au lieu de {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}
