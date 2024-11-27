---
title: Note sulla versione di Aspose.PSD per Python via .NET 24.4
type: docs
weight: 10
url: /it/python-net/aspose-psd-per-python-tramite-net-24-4-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per Python via .NET 24.4](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Chiave**   | **Sommario**                                                            | **Categoria** |
|:------------|:------------------------------------------------------------------------|:-------------|
| PSDPYTHON-50 | [Formato AI] Aggiunta gestione delle risorse XObjectForm               | Funzionalità  |
| PSDPYTHON-51 | Aggiunta costruttore per il Layer Figura                                 | Funzionalità  |
| PSDPYTHON-52 | Risoluzione della conversione del file Psd da RGB a CMYK                | Errore        |
| PSDPYTHON-53 | Specifico file PSD non può essere esportato utilizzando Aspose.PSD      | Errore        |



## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **API Rimosse:**
- Nessuna


## **Esempi di utilizzo:**

**PSDPYTHON-50. [Formato AI] Aggiunta gestione delle risorse XObjectForm**

{{< highlight python >}}
        nomeFileSorgente = "esempio.ai"
        percorsoOutput = "output_esempio.png"

        with AiImage.load(nomeFileSorgente) as immagine:
            immagine.save(percorsoOutput, PngOptions())
{{< /highlight >}}

**PSDPYTHON-51. Aggiunta Costruttore per il Layer Figura**

{{< highlight python >}}
     def verificaCostruttoreLayerFigura():
        fileOutput = "output_aggiunta_layer.psd"

        with PsdImage(600, 400) as nuovoPsd:
            layerFigura = nuovoPsd.add_shape_layer()

            nuovaForma = genera_nuova_forma(nuovoPsd.size)
            nuoveForme = [nuovaForma]
            layerFigura.path.set_items(nuoveForme)

            layerFigura.update()

            nuovoPsd.save(fileOutput)

        with PsdImage.load(fileOutput) as img:
            immagine = cast(PsdImage, img)
            assert len(immagine.layers) == 2

            layerFigura = cast(ShapeLayer, immagine.layers[1])
            riempimentoInterno = layerFigura.fill
            impostazioniTratto = layerFigura.stroke
            riempimentoTratto = layerFigura.stroke.fill

            assert len(layerFigura.path.get_items()) == 1
            assert len(layerFigura.path.get_items()[0].get_items()) == 3

            assert riempimentoInterno.color.to_argb() == -16127182

            assert impostazioniTratto.size == 7.41
            assert not impostazioniTratto.enabled
            assert impostazioniTratto.line_alignment == StrokePosition.CENTER
            assert impostazioniTratto.line_cap == LineCapType.BUTT_CAP
            assert impostazioniTratto.line_join == LineJoinType.MITER_JOIN
            assert riempimentoTratto.color.to_argb() == -16777216
			
    def genera_nuova_forma(dimImmagine):
        nuovaForma = PathShape()

        punto1 = PointF(20, 100)
        punto2 = PointF(200, 100)
        punto3 = PointF(300, 10)

        nodo1 = BezierKnotRecord()
        nodo1.is_linked = True
        nodo1.points = [
                    Release_24_04_Tests.PointFToResourcePoint(punto1, dimImmagine),
                    Release_24_04_Tests.PointFToResourcePoint(punto1, dimImmagine),
                    Release_24_04_Tests.PointFToResourcePoint(punto1, dimImmagine)
                ]

        nodo2 = BezierKnotRecord()
        nodo2.is_linked = True
        nodo2.points = [
                    Release_24_04_Tests.PointFToResourcePoint(punto2, dimImmagine),
                    Release_24_04_Tests.PointFToResourcePoint(punto2, dimImmagine),
                    Release_24_04_Tests.PointFToResourcePoint(punto2, dimImmagine)
                ]

        nodo3 = BezierKnotRecord()
        nodo3.is_linked = True
        nodo3.points = [
                    Release_24_04_Tests.PointFToResourcePoint(punto3, dimImmagine),
                    Release_24_04_Tests.PointFToResourcePoint(punto3, dimImmagine),
                    Release_24_04_Tests.PointFToResourcePoint(punto3, dimImmagine)
                ]

        nodiBezier = [
            nodo1,
            nodo2,
            nodo3
        ]

        nuovaForma.set_items(nodiBezier)

        return nuovaForma
		
    def PointFToResourcePoint(punto, dimImmagine):
        RapportoImgPsd = 256 * 65535
        return Point(
            int(round(punto.y * (RapportoImgPsd / dimImmagine.height))),
            int(round(punto.x * (RapportoImgPsd / dimImmagine.width)))
        )

    def assert_sono_uguali(previsto, attuale, messaggio=None):
        if previsto != attuale:
            raise Exception(messaggio or "Gli oggetti non sono uguali.")
			
{{< /highlight >}}

**PSDPYTHON-52. Risoluzione della conversione del file Psd da RGB a CMYK**

{{< highlight python >}}
     def verificaConversioneDaRgbACmyk():
        fileSorgente = "rana_nosimb.psd"
        fileOutput = "rana_nosimb_output.psd"

        with PsdImage.load(fileSorgente) as immagine:
            immaginePsd = cast(PsdImage, immagine)
            immaginePsd.has_transparency_data = False

            opzioniPsd = PsdOptions(immaginePsd)
            opzioniPsd.color_mode = ColorModes.CMYK
            opzioniPsd.compression_method = CompressionMethod.RLE
            opzioniPsd.channels_count = 4

            immaginePsd.save(fileOutput, opzioniPsd)

        with PsdImage.load(fileOutput) as immagine:
            immaginePsd = cast(PsdImage, immagine)
            assert not immaginePsd.has_transparency_data
            assert immaginePsd.layers[0].channels_count == 4

        def assert_sono_uguali(previsto, attuale, messaggio=None):
            if previsto != attuale:
                raise Exception(messaggio or "Gli oggetti non sono uguali.")			

    def assert_sono_uguali(previsto, attuale, messaggio=None):
        if previsto != attuale:
            raise Exception(messaggio or "Gli oggetti non sono uguali.")
				
{{< /highlight >}}

**PSDPYTHON-53. Un file PSD specifico non può essere esportato utilizzando Aspose.PSD**

{{< highlight python >}}
        fileSorgente = "1966source.psd"
        outputPng = "output.png"

        optCaricamento = PsdLoadOptions()
        optCaricamento.load_effects_resource = True

        with PsdImage.load(fileSorgente, optCaricamento) as immaginePsd:
            immaginePsd.save(outputPng, PngOptions())
			
{{< /highlight >}}
