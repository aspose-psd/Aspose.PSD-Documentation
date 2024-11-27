---
title: Note sulla versione di Aspose.PSD per Python via .NET 24.8
type: docs
weight: 10
url: /it/python-net/aspose-psd-per-python-tramite-net-24-8-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per Python via .NET 24.8](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Chiave**   | **Sommario**                                                                                          | **Categoria** |
|:-------------|:-------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-81 | [Formato AI] Aggiunta gestione per Gruppi XObject                                                       | Miglioramento |
| PSDPYTHON-82 | Migliorare le capacità di trasformazione Warp aggiungendo WarpSettings per TextLayer e SmartObjectLayer | Caratteristica |
| PSDPYTHON-83 | [Formato AI] Gestire i livelli negli operatori di flusso dei contenuti                                   | Caratteristica |
| PSDPYTHON-84 | Il risultato del rendering del file AI è molto diverso rispetto ai risultati di Illustrator            | Errore       |
| PSDPYTHON-85 | Il ricollegamento degli oggetti intelligenti non si applica a tutti gli oggetti intelligenti nel file PSD | Errore       |

## **Cambiamenti nell'API pubblica**
# **API aggiunte:**

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

# **API rimosse:**
- Nessuna

## **Esempi di utilizzo:**

**PSDPYTHON-81. [Formato AI] Aggiunta gestione per Gruppi XObject**
{{< highlight python >}}
#Nessun esempio. Si tratta di un miglioramento interno
{{< /highlight >}}

**PSDPYTHON-82. Migliorare le capacità di trasformazione Warp aggiungendo WarpSettings per TextLayer e SmartObjectLayer**
{{< highlight python >}}
        fileSorgente = "smart_without_warp.psd"
        
        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True
        outputImageFile = [None] * 4
        outputPsdFile = [None] * 4
        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        for indiceCaso in range(len(outputImageFile)):
            outputImageFile[indiceCaso] = "export_" + str(indiceCaso) + ".png"
            outputPsdFile[indiceCaso] = "export_" + str(indiceCaso) + ".psd"

            with PsdImage.load(fileSorgente, opt) as immagine:
                img = cast(PsdImage, immagine)
                for layer in img.layers:
                    if is_assignable(layer, SmartObjectLayer):
                        smartLayer = cast(SmartObjectLayer, layer)
                        smartLayer.warp_settings = GetWarpSettingsByIndex(smartLayer.warp_settings, indiceCaso)

                    if is_assignable(layer, TextLayer):
                        textLayer = cast(TextLayer, layer)
                        if indiceCaso != 3:
                            textLayer.warp_settings = GetWarpSettingsByIndex(textLayer.warp_settings, indiceCaso)

                img.save(outputPsdFile[indiceCaso], PsdOptions())
                img.save(outputImageFile[indiceCaso], PsdOptions())

            with PsdImage.load(outputPsdFile[indiceCaso], opt) as img:
                img.save(outputImageFile[indiceCaso], pngOpt)

        def GetWarpSettingsByIndex(warpParams, indiceCaso):
            switcher = {
                0: {"Style": WarpStyles.RISE, "Rotate": WarpRotates.HORIZONTAL, "Value": 20},
                1: {"Style": WarpStyles.RISE, "Rotate": WarpRotates.VERTICAL, "Value": 10},
                2: {"Style": WarpStyles.FLAG, "Rotate": WarpRotates.HORIZONTAL, "Value": 30},
                3: {"Style": WarpStyles.CUSTOM}
            }
            params = switcher.get(indiceCaso)
            if params:
                warpParams.style = params.get("Style")
                if params.get("Rotate") is not None:
                    warpParams.rotate = params.get("Rotate")
                if params.get("Value") is not None:
                    warpParams.value = params.get("Value")
                if indiceCaso == 3:
                    warpParams.mesh_points[2].y += 70

            return warpParams
{{< /highlight >}}

**PSDPYTHON-83. [Formato AI] Gestire i livelli negli operatori di flusso dei contenuti**
{{< highlight python >}}
        fileSorgente = "Layers-NoPen.ai"
        fileOutput = "Layers-NoPen.output.png"

        with AiImage.load(fileSorgente) as immagine:
            immagine.save(fileOutput, PngOptions())
{{< /highlight >}}

**PSDPYTHON-84. Il risultato del rendering del file AI è molto diverso rispetto ai risultati di Illustrator**
{{< highlight python >}}
        fileSorgente = "4.ai"
        fileOutput = "4_output.png"
        fileDiRiferimento = "4_ethalon.png"

        with AiImage.load(fileSorgente) as immagine:
            immagine.save(fileOutput, PngOptions())
{{< /highlight >}}

**PSDPYTHON-85. Il ricollegamento degli oggetti intelligenti non si applica a tutti gli oggetti intelligenti nel file PSD**
{{< highlight python >}}
        files = ["simple_test", "w22"]
        fileDaCambiare = "image(19).png"

        for file in files:
            fileSorgente = file + ".psd"
            fileOutput = file + "_output.psd"
            with Image.load(fileSorgente) as img:
                immagine = cast(PsdImage, img)
                for layer in immagine.layers:
                    if is_assignable(layer, SmartObjectLayer):
                        smartLayer = cast(SmartObjectLayer, layer)
                        smartLayer.replace_contents(fileDaCambiare)
                immagine.save(fileOutput)           
{{< /highlight >}}
