---
title: Notes de publication d'Aspose.PSD pour Python via .NET 24.2
type: docs
weight: 10
url: /fr/net/aspose-psd-for-python-via-net-24-2-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD pour Python via .NET 24.2](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                    | **Catégorie** |
|:-------------|:-------------------------------------------------------------------------------|:------------|
| PSDPYTHON-28 | Gérer la propriété Angle pour PatternFillSettings                               |   Fonctionnalité   |
| PSDPYTHON-29 | Prise en charge de l'échelle verticale et horizontale pour TextLayer           |   Fonctionnalité   |
| PSDPYTHON-33 | [Format AI] Implémenter le rendu correct de l'arrière-plan dans le format AI basé sur PDF. |   Fonctionnalité   |
| PSDPYTHON-34 | Changer le mécanisme Distort dans warp                                         | Amélioration |
| PSDPYTHON-35 | Accélérer le warp                                                             | Amélioration |
| PSDPYTHON-36 | Exception "Échec du chargement de l'image" lors de l'ouverture du document      |     Problème     |
| PSDPYTHON-37 | Corriger la sauvegarde des fichiers psd avec le motif de trait                 |     Problème     |
| PSDPYTHON-38 | Le style de texte est incorrect dans un objet intelligent lorsque nous utilisons ReplaceContents    |     Problème     |
| PSDPYTHON-39 | [Format AI] Corriger le rendu des courbes de Bézier cubiques dans le fichier AI |     Problème     |



## **Changements d'API publics**
# **APIs ajoutées:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **APIs supprimées:**
- Aucune


## **Exemples d'utilisation:**

**PSDPYTHON-28. Gérer la propriété Angle pour PatternFillSettings**

{{< highlight python >}}

	    nomFichier = "PatternFillLayerWide_0"
        fichierSource = nomFichier + ".psd"
        fichierSortie = nomFichier + "_output.psd"

        optionsChargement = PsdLoadOptions()
        optionsChargement.load_effects_resource = True
        with PsdImage.load(fichierSource, optionsChargement) as img:
            image = cast(PsdImage, img)
            fillLayer = cast(FillLayer, image.layers[1])
            fillSettings = fillLayer.fill_settings
            fillSettings.angle = 70
            fillLayer.update()
            image.save(fichierSortie, PsdOptions())

        with PsdImage.load(fichierSortie, optionsChargement) as img:
            image = cast(PsdImage, img)
            fillLayer = cast(FillLayer, image.layers[1])
            fillSettings = fillLayer.fill_settings

            assert fillSettings.angle == 70

{{< /highlight >}}

**PSDPYTHON-29. Prise en charge de l'échelle verticale et horizontale pour TextLayer**

{{< highlight python >}}

           fichierSource = "1719_src.psd"
           fichierSortie = "output.png"

           # Ajouter quelques polices
           dossierFonts = "1719_Fonts"
           fontFolders = list(FontSettings.get_fonts_folders())
           fontFolders.append(dossierFonts)
           FontSettings.set_fonts_folders(fontFolders, True)

           with PsdImage.load(fichierSource) as image:
               image.save(fichierSortie, PngOptions())

{{< /highlight >}}

**PSDPYTHON-33. [Format AI] Implémenter le rendu correct de l'arrière-plan dans le format AI basé sur PDF**

{{< highlight python >}}

           fichierSource = "pineapples.ai"
           fichierSortie  = "pineapples.png"

           with AiImage.load(fichierSource) as image:
               image.save(fichierSortie, PngOptions())

{{< /highlight >}}

**PSDPYTHON-34. Changer le mécanisme Distort dans warp**

{{< highlight python >}}

        fichierSource = "crow_grid.psd"       
        fichierSortie = self.GetFileInOutputFolder("export.png")

        options = PsdLoadOptions()
        options.load_effects_resource = True
        options.allow_warp_repaint = True

        optionsPng = PngOptions()
        optionsPng.compression_level = 9
        optionsPng.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
        with PsdImage.load(fichierSource, options) as img:
            img.save(fichierSortie, optionsPng)

{{< /highlight >}}

**PSDPYTHON-35. Accélérer le warp**

{{< highlight python >}}

        fichierSource = "output.psd"
        fichierSortie = "export.png"

        options = PsdLoadOptions()
        options.load_effects_resource = True
        options.allow_warp_repaint = True

        start_time = time.time()

        optionsPng = PngOptions()
        optionsPng.compression_level = 9
        optionsPng.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(fichierSource, options) as img:
            img.save(fichierSortie, optionsPng)

        elapsed_time = time.time() - start_time

        # ancienne valeur = 193300
        # nouvelle valeur =  55500
        time_in_sec = int(elapsed_time * 1000)
        if time_in_sec > 100000:
            raise Exception("Le temps de traitement est trop long")        
			
{{< /highlight >}}

**PSDPYTHON-36. Exception "Échec du chargement de l'image" lors de l'ouverture du document**

{{< highlight python >}}
        fichierSource1 = "PRODUCT.ai"
        fichierSortie1 = "PRODUCT.png"

        with AiImage.load(fichierSource1) as image:
            image.save(fichierSortie1, PngOptions())

        fichierSource2 = "Dolota.ai"
        fichierSortie2 = "Dolota.png"

        with AiImage.load(fichierSource2) as image:
            image.save(fichierSortie2, PngOptions())       
        
        fichierSource3 = "ARS_novelty_2108_out_01(1).ai"
        fichierSortie3 = "ARS_novelty_2108_out_01(1).png"

        with AiImage.load(fichierSource3) as image:
            image.save(fichierSortie3, PngOptions())

        fichierSource4 = "bit_gear.ai"      
        fichierSortie4 = "bit_gear.png"

        with AiImage.load(fichierSource4) as image:
            image.save(fichierSortie4, PngOptions())

        fichierSource5 = "test.ai"
        fichierSortie5 = "test.png"

        with AiImage.load(fichierSource5) as image:
            image.save(fichierSortie5, PngOptions())
{{< /highlight >}}

**PSDPYTHON-37. Corriger la sauvegarde des fichiers psd avec le motif de trait**

{{< highlight python >}}
	    fichierSource = "StrokeShapePattern.psd"
        fichierSortie = "StrokeShapePattern_output.psd"

        nouveauxLimitsPattern = Rectangle(0, 0, 4, 4)
        id = str(uuid.uuid4())
        nouveauNomPattern = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0"
        nouveauPattern = [
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
        ]

        with PsdImage.load(fichierSource) as img:
            image = cast(PsdImage, img)
            shapeLayer = cast(ShapeLayer, image.layers[1])
            strokeInternalFillSettings = shapeLayer.fill

            pattResource = None
            for globalLayerResource in image.global_layer_resources:


                pattResource = as_of(globalLayerResource, PattResource)
                if pattResource is not None:
                    patternItem = pattResource.patterns[0]  # Données de motif interne de trait

                    patternItem.pattern_id = id
                    patternItem.name = nouveauNomPattern
                    patternItem.set_pattern(nouveauPattern, nouveauxLimitsPattern)
                    break


            strokeInternalFillSettings.pattern_name = nouveauNomPattern
            strokeInternalFillSettings.pattern_id = id + "\0"

            shapeLayer.update()

            image.save(fichierSortie)

        # Vérifier les données modifiées.
        with PsdImage.load(fichierSortie) as img:
            image = cast(PsdImage, img)
            shapeLayer = cast(ShapeLayer, image.layers[1])
            strokeInternalFillSettings = shapeLayer.fill

            assert id.upper() == strokeInternalFillSettings.pattern_id
            assert nouveauNomPattern == strokeInternalFillSettings.pattern_name + "\0"
			
{{< /highlight >}}

**PSDPYTHON-38. Le style de texte est incorrect dans un objet intelligent lorsque nous utilisons ReplaceContents**

{{< highlight python >}}
        fichierEntree = "source.psd"
        fichierSortie = "output.png"

        optionsChargementPsd = PsdLoadOptions()
        optionsChargementPsd.load_effects_resource = True

        with PsdImage.load(fichierEntree, optionsChargementPsd) as image:
            psdImage = cast(PsdImage, image)
            smartObject = cast(SmartObjectLayer, psdImage.layers[1])

            smartObjectImage = cast(PsdImage, smartObject.load_contents(optionsChargementPsd))

            with smartObjectImage:
                smartObject.replace_contents(smartObjectImage)

            optionsPng = PngOptions()
            optionsPng.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
            psdImage.save(fichierSortie, optionsPng)

{{< /highlight >}}

**PSDPYTHON-39. [Format AI] Corriger le rendu des courbes de Bézier cubiques dans le fichier AI**

{{< highlight python >}}

        fichierSource = "Typography.ai"
        cheminFichierSortie = "Typography.png"

        with AiImage.load(fichierSource) as image:
            image.save(cheminFichierSortie, PngOptions())

{{< /highlight >}}
