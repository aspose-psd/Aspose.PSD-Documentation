---
title: Notatki dotyczące wydania Aspose.PSD dla Python via .NET 24.2
type: docs
weight: 10
url: /pl/net/aspose-psd-dla-python-za-posrednictwem-net-24-2-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla Python via .NET 24.2](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Klucz**     | **Podsumowanie**                                                                  | **Kategoria** |
|:-------------|:-----------------------------------------------------------------------------|:------------|
| PSDPYTHON-28 | Obsługa właściwości kąta dla ustawień wypełnienia wzorem                     |   Funkcja   |
| PSDPYTHON-29 | Wsparcie dla skali pionowej i poziomej dla warstwy tekstowej                  |   Funkcja   |
| PSDPYTHON-33 | [Format AI] Wdrożenie poprawnego renderowania tła w formacie AI opartym na PDF.|   Funkcja   |
| PSDPYTHON-34 | Zmiana mechanizmu zniekształcania w deformacji                                | Udoskonalenie|
| PSDPYTHON-35 | Przyspieszenie deformacji                                                    | Udoskonalenie|
| PSDPYTHON-36 | Wyjątek "Wczytywanie obrazu nie powiodło się." przy otwieraniu dokumentu      |    Błąd     |
| PSDPYTHON-37 | Naprawa zapisywania plików PSD z wypełnieniem obrysu                          |    Błąd     |
| PSDPYTHON-38 | Styl tekstu jest niepoprawny w mądrym obiekcie podczas użycia ReplaceContents|    Błąd     |
| PSDPYTHON-39 | [Format AI] Naprawa renderowania Beziera kubicznego w pliku AI               |    Błąd     |



## **Zmiany w API publicznym**
# **Dodane API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **Usunięte API:**
- Brak


## **Przykłady użycia:**

## **Przykłady użycia:**

**PSDPYTHON-28. Obsługa właściwości kąta dla ustawień wypełnienia wzorem**

{{< highlight python >}}

	    fileName = "PatternFillLayerWide_0"
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

**PSDPYTHON-29. Wsparcie dla skali pionowej i poziomej dla warstwy tekstowej**

{{< highlight python >}}

           sourceFile = "1719_src.psd"
           outputFile = "output.png"

           # Dodaj kilka czcionek
           fontsFolder = "1719_Fonts"
           fontFolders = list(FontSettings.get_fonts_folders())
           fontFolders.append(fontsFolder)
           FontSettings.set_fonts_folders(fontFolders, True)

           with PsdImage.load(sourceFile) as image:
               image.save(outputFile, PngOptions())

{{< /highlight >}}

**PSDPYTHON-33. [Format AI] Wdrożenie poprawnego renderowania tła w formacie AI opartym na PDF**

{{< highlight python >}}

           sourceFile = "pineapples.ai"
           outputFile  = "pineapples.png"

           with AiImage.load(sourceFile) as image:
               image.save(outputFile, PngOptions())

{{< /highlight >}}

**PSDPYTHON-34. Zmiana mechanizmu zniekształcania w deformacji**

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

**PSDPYTHON-35. Przyspieszenie deformacji**

{{< highlight python >}}

        sourceFile = "output.psd"
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

        # stara wartość = 193300
        # nowa wartość =  55500
        time_in_sec = int(elapsed_time * 1000)
        if time_in_sec > 100000:
            raise Exception("Zbyt długi czas przetwarzania")        

{{< /highlight >}}

**PSDPYTHON-36. Wyjątek "Wczytywanie obrazu nie powiodło się." przy otwieraniu dokumentu**

{{< highlight python >}}
        sourceFile1 = "PRODUCT.ai"
        outputFile1 = "PRODUCT.png"

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

**PSDPYTHON-37. Naprawa zapisywania plików PSD z wypełnieniem obrysu**

{{< highlight python >}}
	    sourceFile = "StrokeShapePattern.psd"
        outputFile = "StrokeShapePattern_output.psd"

        newPatternBounds = Rectangle(0, 0, 4, 4)
        guid = str(uuid.uuid4())
        newPatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0"
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
                    patternItem = pattResource.patterns[0]  # Dane wzoru wewnętrznego obrysu

                    patternItem.pattern_id = guid
                    patternItem.name = newPatternName
                    patternItem.set_pattern(newPattern, newPatternBounds)
                    break


            strokeInternalFillSettings.pattern_name = newPatternName
            strokeInternalFillSettings.pattern_id = guid + "\0"

            shapeLayer.update()

            image.save(outputFile)

        # Sprawdź zmienione dane.
        with PsdImage.load(outputFile) as img:
            image = cast(PsdImage, img)
            shapeLayer = cast(ShapeLayer, image.layers[1])
            strokeInternalFillSettings = shapeLayer.fill

            assert guid.upper() == strokeInternalFillSettings.pattern_id
            assert newPatternName == strokeInternalFillSettings.pattern_name + "\0"
			
{{< /highlight >}}

**PSDPYTHON-38. Styl tekstu jest niepoprawny w mądrym obiekcie podczas użycia ReplaceContents**

{{< highlight python >}}
        inputFile = "source.psd"
        output2 = "output.png"

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

**PSDPYTHON-39. [Format AI] Naprawa renderowania Beziera kubicznego w pliku AI**

{{< highlight python >}}

        sourceFile = "Typography.ai"
        outputFilePath = "Typography.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())

{{< /highlight >}}
