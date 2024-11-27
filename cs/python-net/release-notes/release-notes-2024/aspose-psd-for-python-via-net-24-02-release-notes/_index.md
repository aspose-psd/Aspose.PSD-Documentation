---
title: Aspose.PSD pro Python via .NET 24.2 - Poznámky k vydání
type: docs
weight: 10
url: /cs/net/aspose-psd-pro-python-pres-net-24-2-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Python via .NET 24.2](https://pypi.org/project/aspose-psd/)

{{% /alert %}}


| **Klíč**     | **Souhrnně**                                                                  | **Kategorie** |
|:-------------|:-----------------------------------------------------------------------------|:------------|
| PSDPYTHON-28 | Ošetřit vlastnost Angle pro nastavení výplně vzoru (PatternFillSettings)                                |   Funkce   |
| PSDPYTHON-29 | Podpora vertikálního a horizontálního měřítka pro TextLayer                       |   Funkce   |
| PSDPYTHON-33 | [AI Formát] Implementace správného vykreslení pozadí v formátu AI založeném na PDF.|   Funkce   |
| PSDPYTHON-34 | Změna mechanismu zkreslení (Distort)                                             | Vylepšení |
| PSDPYTHON-35 | Zrychlení zkreslení                                                                | Vylepšení |
| PSDPYTHON-36 | Výjimka "Chyba při načítání obrázku." při otevření dokumentu                         |     Chyba     |
| PSDPYTHON-37 | Oprava ukládání souborů PSD s vyplněním tahu                                   |     Chyba     |
| PSDPYTHON-38 | Styl textu je nesprávný v chytrém objektu při použití ReplaceContents    |     Chyba     |
| PSDPYTHON-39 | [AI Formát] Oprava vykreslení Cubic Bezieru ve souboru AI                        |     Chyba     |



## **Změny ve veřejném rozhraní**
# **Přidané API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **Odstraněné API:**
- Žádné


## **Příklady použití:**


**PSDPYTHON-28. Ošetřit vlastnost Angle pro nastavení výplně vzoru (PatternFillSettings)**

{{< highlight python >}}

	    fileName = "VzorovaNáplňVrstvyŠiroká_0"
        sourceFile = fileName + ".psd"
        outputFile = fileName + "_output.psd"

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        with PsdImage.load(sourceFile, loadOpt) as img:
            image = cast(PsdImage, img)
            fillLayer = cast(FillLayer, image.layers[1])
            fillSettings = fillLayer.fill_settings
            fillSettings.angle = 70
            fillLayer.update()
            image.save(outputFile, PsdOptions())

        with PsdImage.load(outputFile, loadOpt) as img:
            image = cast(PsdImage, img)
            fillLayer = cast(FillLayer, image.layers[1])
            fillSettings = fillLayer.fill_settings

            assert fillSettings.angle == 70

{{< /highlight >}}


**PSDPYTHON-29. Podpora vertikálního a horizontálního měřítka pro TextLayer**

{{< highlight python >}}

           sourceFile = "1719_zdroj.psd"
           outputFile = "výstup.png"

           # Přidejte několik písem
           složkaSFonty = "1719_Fonts"
           fontFolders = list(FontSettings.get_fonts_folders())
           fontFolders.append(složkaSFonty)
           FontSettings.set_fonts_folders(fontFolders, True)

           with PsdImage.load(sourceFile) as image:
               image.save(outputFile, PngOptions())

{{< /highlight >}}


**PSDPYTHON-33. [AI Formát] Implementace správného vykreslení pozadí v formátu AI založeném na PDF**

{{< highlight python >}}

           sourceFile = "ananas.ai"
           outputFile  = "ananas.png"

           with AiImage.load(sourceFile) as image:
               image.save(outputFile, PngOptions())

{{< /highlight >}}


**PSDPYTHON-34. Změna mechanismu zkreslení (Distort)**

{{< highlight python >}}

        sourceFile = "crow_grid.psd"       
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


**PSDPYTHON-35. Zrychlení zkreslení**

{{< highlight python >}}

        sourceFile = "výstup.psd"
        outputFile = "export.png"

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        start_time = time.time()

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)

        elapsed_time = time.time() - start_time

        # stará hodnota = 193300
        # nová hodnota =  55500
        time_in_sec = int(elapsed_time * 1000)
        if time_in_sec > 100000:
            raise Exception("Čas zpracování je příliš dlouhý")        
			
{{< /highlight >}}


**PSDPYTHON-36. Výjimka "Chyba při načítání obrázku." při otevření dokumentu**

{{< highlight python >}}
        sourceFile1 = "PRODUKT.ai"
        outputFile1 = "PRODUKT.png"

        with AiImage.load(sourceFile1) as image:
            image.save(outputFile1, PngOptions())

        sourceFile2 = "Dolota.ai"
        outputFile2 = "Dolota.png"

        with AiImage.load(sourceFile2) as image:
            image.save(outputFile2, PngOptions())       
        
        sourceFile3 = "ARS_novelty_2108_out_01(1).ai"
        outputFile3 = "ARS_novelty_2108_out_01(1).png"

        with AiImage.load(sourceFile3) as image:
            image.save(outputFile3, PngOptions())

        sourceFile4 = "bit_gear.ai"      
        outputFile4 = "bit_gear.png"

        with AiImage.load(sourceFile4) as image:
            image.save(outputFile4, PngOptions())

        sourceFile5 = "test.ai"
        outputFile5 = "test.png"

        with AiImage.load(sourceFile5) as image:
            image.save(outputFile5, PngOptions())
{{< /highlight >}}


**PSDPYTHON-37. Oprava ukládání souborů PSD s vyplněním tahu**

{{< highlight python >}}
	    sourceFile = "VzorTvaruTahuVzorem.psd"
        outputFile = "VzorTvaruTahuVzorem_výstup.psd"

        newPatternBounds = Rectangle(0, 0, 4, 4)
        guid = str(uuid.uuid4())
        newPatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontální čára 9\0"
        newPattern = [
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
        ]

        with PsdImage.load(sourceFile) as img:
            image = cast(PsdImage, img)
            shapeLayer = cast(ShapeLayer, image.layers[1])
            strokeInternalFillSettings = shapeLayer.fill

            pattResource = None
            for globalLayerResource in image.global_layer_resources:


                pattResource = as_of(globalLayerResource, PattResource)
                if pattResource is not None:
                    patternItem = pattResource.patterns[0]  # Data vnitřního tahu tvaru (internal pattern data)

                    patternItem.pattern_id = guid
                    patternItem.name = newPatternName
                    patternItem.set_pattern(newPattern, newPatternBounds)
                    break


            strokeInternalFillSettings.pattern_name = newPatternName
            strokeInternalFillSettings.pattern_id = guid + "\0"

            shapeLayer.update()

            image.save(outputFile)

        # Zkontroluj změněná data.
        with PsdImage.load(outputFile) as img:
            image = cast(PsdImage, img)
            shapeLayer = cast(ShapeLayer, image.layers[1])
            strokeInternalFillSettings = shapeLayer.fill

            assert guid.upper() == strokeInternalFillSettings.pattern_id
            assert newPatternName == strokeInternalFillSettings.pattern_name + "\0"
			
{{< /highlight >}}


**PSDPYTHON-38. Styl textu je nesprávný v chytrém objektu při použití ReplaceContents**

{{< highlight python >}}
        inputFile = "zdroj.psd"
        output2 = "výstup.png"

        psdLoadOptions = PsdLoadOptions()
        psdLoadOptions.load_effects_resource = True

        with PsdImage.load(inputFile, psdLoadOptions) as image:
            psdImage = cast(PsdImage, image)
            smartObject = cast(SmartObjectLayer, psdImage.layers[1])

            smartObjectImage = cast(PsdImage, smartObject.load_contents(psdLoadOptions))

            with smartObjectImage:
                smartObject.replace_contents(smartObjectImage)

            pngOpt = PngOptions()
            pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
            psdImage.save(output2, pngOpt)

{{< /highlight >}}


**PSDPYTHON-39. [AI Formát] Oprava vykreslení Cubic Bezieru ve souboru AI**

{{< highlight python >}}

        sourceFile = "Typografie.ai"
        outputFilePath = "Typografie.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())

{{< /highlight >}}
