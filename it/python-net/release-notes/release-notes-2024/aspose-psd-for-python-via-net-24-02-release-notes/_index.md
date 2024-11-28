---
title: Note sulla distribuzione di Aspose.PSD per Python via .NET 24.2
type: docs
weight: 10
url: /it/net/aspose-psd-for-python-via-net-24-2-release-notes/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla distribuzione di [Aspose.PSD per Python via .NET 24.2](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Chiave**   | **Riepilogo**                                                              | **Categoria** |
|:-------------|:--------------------------------------------------------------------------|:------------|
| PSDPYTHON-28 | Gestione della proprietà Angolo per le impostazioni di riempimento a pattern |   Funzionalità    |
| PSDPYTHON-29 | Supporto della scala verticale e orizzontale per il livello di testo        |   Funzionalità    |
| PSDPYTHON-33 | [Formato AI] Implementare il rendering corretto dello sfondo nel Formato AI basato su PDF |   Funzionalità    |
| PSDPYTHON-34 | Modifica del meccanismo di distorsione in deformazione                      | Miglioramento  |
| PSDPYTHON-35 | Accelerazione della deformazione                                           | Miglioramento  |
| PSDPYTHON-36 | Eccezione "Caricamento dell'immagine fallito." all'apertura del documento   |     Errore     |
| PSDPYTHON-37 | Correzione del salvataggio dei file psd con motivo di tratto                |     Errore     |
| PSDPYTHON-38 | Lo stile del testo è errato in un oggetto intelligente quando si utilizza ReplaceContents | Errore |
| PSDPYTHON-39 | [Formato AI] Correggere il rendering di Cubic Bezier nel file AI           |     Errore     |



## **Modifiche all'API pubblica**
# **API Aggiunte:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **API Rimosse:**
- Nessuna


## **Esempi di Utilizzo:**

## **Esempi di Utilizzo:**

**PSDPYTHON-28. Gestione della proprietà Angolo per le impostazioni di riempimento a pattern**

{{< highlight python >}}

	    nomefile = "PatternFillLayerWide_0"
        fileSorgente = nomefile + ".psd"
        fileOutput = nomefile + "_output.psd"

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        with PsdImage.load(fileSorgente, loadOpt) as img:
            immagine = cast(PsdImage, img)
            livelloRiempimento = cast(FillLayer, immagine.layers[1])
            impostazioniRiempimento = livelloRiempimento.fill_settings
            impostazioniRiempimento.angle = 70
            livelloRiempimento.update()
            immagine.save(fileOutput, PsdOptions())

        with PsdImage.load(fileOutput, loadOpt) as img:
            immagine = cast(PsdImage, img)
            livelloRiempimento = cast(FillLayer, immagine.layers[1])
            impostazioniRiempimento = livelloRiempimento.fill_settings

            assert impostazioniRiempimento.angle == 70

{{< /highlight >}}

**PSDPYTHON-29. Supporto della scala verticale e orizzontale per il livello di testo**

{{< highlight python >}}

           fileSorgente = "1719_src.psd"
           fileOutput = "output.png"

           # Aggiungi alcuni font
           cartellaFont = "1719_Fonts"
           cartelleFont = list(FontSettings.get_fonts_folders())
           cartelleFont.append(cartellaFont)
           FontSettings.set_fonts_folders(cartelleFont, True)

           with PsdImage.load(fileSorgente) as immagine:
               immagine.save(fileOutput, PngOptions())

{{< /highlight >}}

**PSDPYTHON-33. [Formato AI] Implementare il rendering corretto dello sfondo nel Formato AI basato su PDF**

{{< highlight python >}}

           fileSorgente = "pineapples.ai"
           fileOutput  = "pineapples.png"

           with AiImage.load(fileSorgente) as immagine:
               immagine.save(fileOutput, PngOptions())

{{< /highlight >}}

**PSDPYTHON-34. Modifica del meccanismo di distorsione in deformazione**

{{< highlight python >}}

        fileSorgente = "crow_grid.psd"       
        fileOutput = self.GetFileInOutputFolder("export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
        with PsdImage.load(fileSorgente, opt) as img:
            img.save(fileOutput, pngOpt)

{{< /highlight >}}

**PSDPYTHON-35. Accelerazione della deformazione**

{{< highlight python >}}

        fileSorgente = "output.psd"
        fileOutput = "export.png"

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        start_time = time.time()

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(fileSorgente, opt) as img:
            img.save(fileOutput, pngOpt)

        elapsed_time = time.time() - start_time

        # vecchio valore = 193300
        # nuovo valore =  55500
        tempo_in_sec = int(elapsed_time * 1000)
        if tempo_in_sec > 100000:
            raise Exception("Il tempo di elaborazione è troppo lungo")        
			
{{< /highlight >}}

**PSDPYTHON-36. Eccezione "Caricamento dell'immagine fallito." all'apertura del documento**

{{< highlight python >}}
        fileSorgente1 = "PRODUCT.ai"
        fileOutput1 = "PRODUCT.png"

        with AiImage.load(fileSorgente1) as immagine:
            immagine.save(fileOutput1, PngOptions())

        fileSorgente2 = "Dolota.ai"
        fileOutput2 = "Dolota.png"

        with AiImage.load(fileSorgente2) as immagine:
            immagine.save(fileOutput2, PngOptions())       

        fileSorgente3 = "ARS_novelty_
