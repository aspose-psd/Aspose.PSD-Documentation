---
title: Notas de Lançamento Aspose.PSD para Python via .NET 24.4
type: docs
weight: 10
url: /pt/python-net/aspose-psd-for-python-via-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para o [Aspose.PSD para Python via .NET 24.4](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Chave**    | **Resumo**                                                         | **Categoria**|
|:------------ |:-------------------------------------------------------------------|:------------|
| PSDPYTHON-50 | [AI Format] Adicionar manipulação de recurso XObjectForm           | Recurso     |
| PSDPYTHON-51 | Adicionar Construtor para o ShapeLayer                             | Recurso     |
| PSDPYTHON-52 | Corrigir conversão de arquivo Psd de RGB para CMYK                 | Erro        |
| PSDPYTHON-53 | Arquivo PSD específico não pode ser exportado usando Aspose.PSD   | Erro        |



## **Alterações na API Pública**
# **APIs Adicionadas:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

**PSDPYTHON-50. [AI Format] Adicionar manipulação de recurso XObjectForm**

{{< highlight python >}}
        nomeArquivoFonte = "exemplo.ai"
        caminhoArquivoSaida = "exemplo_saida.png"

        with AiImage.load(nomeArquivoFonte) as imagem:
            imagem.save(caminhoArquivoSaida, PngOptions())
{{< /highlight >}}

**PSDPYTHON-51. Adicionar Construtor para o ShapeLayer**

{{< highlight python >}}
     def verificar ShapeLayerConstructor():
        arquivoSaida = "AddShapeLayer_output.psd"

        with PsdImage(600, 400) as novoPsd:
            shapeLayer = novoPsd.add_shape_layer()

            novaForma = gerar_nova_forma(novoPsd.size)
            novasFormas = [novaForma]
            shapeLayer.path.set_items(novasFormas)

            shapeLayer.update()

            novoPsd.save(arquivoSaida)

        with PsdImage.load(arquivoSaida) as img:
            imagem = cast(PsdImage, img)
            assert len(imagem.layers) == 2

            shapeLayer = cast(ShapeLayer, imagem.layers[1])
            preenchimentoInterno = shapeLayer.fill
            configuracoesContorno = shapeLayer.stroke
            preenchimentoContorno = shapeLayer.stroke.fill

            assert len(shapeLayer.path.get_items()) == 1
            assert len(shapeLayer.path.get_items()[0].get_items()) == 3

            assert preenchimentoInterno.color.to_argb() == -16127182

            assert configuracoesContorno.size == 7.41
            assert not configuracoesContorno.enabled
            assert configuracoesContorno.line_alignment == StrokePosition.CENTER
            assert configuracoesContorno.line_cap == LineCapType.BUTT_CAP
            assert configuracoesContorno.line_join == LineJoinType.MITER_JOIN
            assert preenchimentoContorno.color.to_argb() == -16777216
			
    def gerar_nova_forma(tamanhoImagem):
        novaForma = PathShape()

        ponto1 = PointF(20, 100)
        ponto2 = PointF(200, 100)
        ponto3 = PointF(300, 10)

        nodo1 = BezierKnotRecord()
        nodo1.is_linked = True
        nodo1.points = [
                    Release_24_04_Tests.PointFToResourcePoint(ponto1, tamanhoImagem),
                    Release_24_04_Tests.PointFToResourcePoint(ponto1, tamanhoImagem),
                    Release_24_04_Tests.PointFToResourcePoint(ponto1, tamanhoImagem)
                ]

        nodo2 = BezierKnotRecord()
        nodo2.is_linked = True
        nodo2.points = [
                    Release_24_04_Tests.PointFToResourcePoint(ponto2, tamanhoImagem),
                    Release_24_04_Tests.PointFToResourcePoint(ponto2, tamanhoImagem),
                    Release_24_04_Tests.PointFToResourcePoint(ponto2, tamanhoImagem)
                ]

        nodo3 = BezierKnotRecord()
        nodo3.is_linked = True
        nodo3.points = [
                    Release_24_04_Tests.PointFToResourcePoint(ponto3, tamanhoImagem),
                    Release_24_04_Tests.PointFToResourcePoint(ponto3, tamanhoImagem),
                    Release_24_04_Tests.PointFToResourcePoint(ponto3, tamanhoImagem)
                ]

        bezierKnots = [
            nodo1,
            nodo2,
            nodo3
        ]

        novaForma.set_items(bezierKnots)

        return novaForma
		
    def PointFToResourcePoint(ponto, tamanhoImagem):
        RazaoImgParaPsd = 256 * 65535
        return Point(
            int(round(ponto.y * (RazaoImgParaPsd / tamanhoImagem.height))),
            int(round(ponto.x * (RazaoImgParaPsd / tamanhoImagem.width)))
        )

    def assert_são_iguais(esperado, atual, mensagem=None):
        if esperado != atual:
            raise Exception(mensagem or "Os objetos não são iguais.")
			
{{< /highlight >}}

**PSDPYTHON-52. Corrigir conversão de arquivo Psd de RGB para CMYK**

{{< highlight python >}}
     def verificarConversaoDeRgbParaCmyk():
        arquivoFonte = "sapo_nosimb.psd"
        arquivoSaida = "sapo_nosimb_saida.psd"

        with PsdImage.load(arquivoFonte) as imagem:
            psdImagem = cast(PsdImage, imagem)
            psdImagem.has_transparency_data = False

            opcoesPsd = PsdOptions(psdImagem)
            opcoesPsd.color_mode = ColorModes.CMYK
            opcoesPsd.compression_method = CompressionMethod.RLE
            opcoesPsd.channels_count = 4

            psdImagem.save(arquivoSaida, opcoesPsd)

        with PsdImage.load(arquivoSaida) as imagem:
            psdImagem = cast(PsdImage, imagem)
            assert not psdImagem.has_transparency_data
            assert psdImagem.layers[0].channels_count == 4

        def assert_são_iguais(esperado, atual, mensagem=None):
            if esperado != atual:
                raise Exception(mensagem or "Os objetos não são iguais.")			

    def assert_são_iguais(esperado, atual, mensagem=None):
        if esperado != atual:
            raise Exception(mensagem or "Os objetos não são iguais.")
				
{{< /highlight >}}

**PSDPYTHON-53. Arquivo PSD específico não pode ser exportado usando Aspose.PSD**

{{< highlight python >}}
        arquivoFonte = "1966fonte.psd"
        pngSaida = "saida.png"

        opcoesCarga = PsdLoadOptions()
        opcoesCarga.load_effects_resource = True

        with PsdImage.load(arquivoFonte, opcoesCarga) as psdImagem:
            psdImagem.save(pngSaida, PngOptions())
			
{{< /highlight >}}
