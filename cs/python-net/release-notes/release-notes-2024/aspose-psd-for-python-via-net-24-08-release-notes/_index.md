---
title: Aspose.PSD pro Python via .NET 24.8 - Poznámky k vydání
type: docs
weight: 10
url: /cs/python-net/aspose-psd-pro-python-pres-net-24-8-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Python via .NET 24.8](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Klíč**      | **Souhrn**                                                                                                       | **Kategorie** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-81 | [Formát AI] Přidání zpracování skupin XObject                                                        | Vylepšení  |
| PSDPYTHON-82 | Vylepšení možností transformace zkreslování přidáním nastavení WarpSettings pro TextLayer a SmartObjectLayer | Funkce      |
| PSDPYTHON-83 | [Formát AI] Zpracování vrstev v operátorech proudů obsahu                                             | Funkce      |
| PSDPYTHON-84 | Výsledek vykreslování souboru AI se velmi liší ve srovnání s výsledky Illustratoru               | Chyba          |
| PSDPYTHON-85 | Přepojení chytrého objektu se nevztahuje na všechny chytré objekty v souboru PSD                                  | Chyba          |

## **Změny ve veřejném rozhraní API**
# **Přidaná rozhraní API:**

- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.WarpSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.WarpSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[],Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource)
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Rotate
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.MeshPoints
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Horizontal
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Vertical
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.None
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Custom
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arc
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcUpper
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcLower
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arch
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Bulge
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Flag
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Fish
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Rise
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Wave
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Twist
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Squeeze
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Inflate

# **Odebraná rozhraní API:**
- žádné

## **Příklady použití:**

**PSDPYTHON-81. [Formát AI] Přidání zpracování skupin XObject**
{{< highlight python >}}
#Bez příkladu. Jedná se o vnitřní vylepšení
{{< /highlight >}}

**PSDPYTHON-82. Vylepšení možností transformace zkreslování přidáním WarpSettings pro TextLayer a SmartObjectLayer**
{{< highlight python >}}
        sourceFile = "smart_without_warp.psd"

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True
        outputImageFile = [None] * 4
        outputPsdFile = [None] * 4
        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        for caseIndex in range(len(outputImageFile)):
            outputImageFile[caseIndex] = "export_" + str(caseIndex) + ".png"
            outputPsdFile[caseIndex] = "export_" + str(caseIndex) + ".psd"

            with PsdImage.load(sourceFile, opt) as image:
                img = cast(PsdImage, image)
                for layer in img.layers:
                    if is_assignable(layer, SmartObjectLayer):
                        smartLayer = cast(SmartObjectLayer, layer)
                        smartLayer.warp_settings = GetWarpSettingsByIndex(smartLayer.warp_settings, caseIndex)

                    if is_assignable(layer, TextLayer):
                        textLayer = cast(TextLayer, layer)
                        if caseIndex != 3:
                            textLayer.warp_settings = GetWarpSettingsByIndex(textLayer.warp_settings, caseIndex)

                img.save(outputPsdFile[caseIndex], PsdOptions())
                img.save(outputImageFile[caseIndex], PsdOptions())

            with PsdImage.load(outputPsdFile[caseIndex], opt) as img:
                img.save(outputImageFile[caseIndex], pngOpt)

        def GetWarpSettingsByIndex(warpParams, caseIndex):
            switcher = {
                0: {"Style": WarpStyles.RISE, "Rotate": WarpRotates.HORIZONTAL, "Value": 20},
                1: {"Style": WarpStyles.RISE, "Rotate": WarpRotates.VERTICAL, "Value": 10},
                2: {"Style": WarpStyles.FLAG, "Rotate": WarpRotates.HORIZONTAL, "Value": 30},
                3: {"Style": WarpStyles.CUSTOM}
            }
            params = switcher.get(caseIndex)
            if params:
                warpParams.style = params.get("Style")
                if params.get("Rotate") is not None:
                    warpParams.rotate = params.get("Rotate")
                if params.get("Value") is not None:
                    warpParams.value = params.get("Value")
                if caseIndex == 3:
                    warpParams.mesh_points[2].y += 70

            return warpParams
{{< /highlight >}}

**PSDPYTHON-83. [Formát AI] Zpracování vrstev v operátorech proudů obsahu**
{{< highlight python >}}
        sourceFile = "Layers-NoPen.ai"
        outputFile = "Layers-NoPen.output.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())    
{{< /highlight >}}

**PSDPYTHON-84. Vykreslení souboru AI se velmi liší ve srovnání s výsledky Illustratoru**
{{< highlight python >}}
        sourceFile = "4.ai"
        outputFile = "4_output.png"
        referenceFile = "4_ethalon.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-85. Přeřazení chytrého objektu se nevztahuje na všechny chytré objekty v souboru PSD**
{{< highlight python >}}
        files = ["simple_test", "w22"]
        change_file = "image(19).png"

        for file in files:
            source_file = file + ".psd"
            output_file = file + "_output.psd"
            with Image.load(source_file) as img:
                image = cast(PsdImage, img)
                for layer in image.layers:
                    if is_assignable(layer, SmartObjectLayer):
                        smart_layer = cast(SmartObjectLayer, layer)
                        smart_layer.replace_contents(change_file)
                image.save(output_file)           
{{< /highlight >}}
