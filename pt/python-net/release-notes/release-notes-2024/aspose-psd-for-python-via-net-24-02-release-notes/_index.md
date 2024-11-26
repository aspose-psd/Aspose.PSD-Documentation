---
title: Aspose.PSD para Python via .NET 24.2 - Notas de Lançamento
type: docs
weight: 10
url: /pt/net/aspose-psd-for-python-via-net-24-2-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para Python via .NET 24.2](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Chave**    | **Resumo**                                                                     | **Categoria** |
|:-------------|:-------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-28 | Manipular a propriedade de Ângulo para PatternFillSettings                     | Recurso      |
| PSDPYTHON-29 | Suporte à escala vertical e horizontal para TextLayer                         | Recurso      |
| PSDPYTHON-33 | [Formato AI] Implementar renderização correta do plano de fundo no Formato AI baseado em PDF. | Recurso      |
| PSDPYTHON-34 | Alterar mecanismo de deformação em warp                                        | Aprimoramento|
| PSDPYTHON-35 | Acelerar warp                                                                 | Aprimoramento|
| PSDPYTHON-36 | Exceção "Falha ao carregar imagem." ao abrir um documento                      | Erro         |
| PSDPYTHON-37 | Corrigir salvamento de arquivos psd com Padrão de Traço                         | Erro         |
| PSDPYTHON-38 | O estilo de texto está incorreto em um objeto inteligente ao usar ReplaceContents | Erro         |
| PSDPYTHON-39 | [Formato AI] Corrigir a renderização de Bezier Cúbico no arquivo AI             | Erro         |



## **Mudanças na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

## **Exemplos de Uso:**

**PSDPYTHON-28. Manipular a propriedade de Ângulo para PatternFillSettings**

{{< highlight python >}}

	    nomeArquivo = "PadraoPreenchimentoLargo_0"
        arquivoFonte = nomeArquivo + ".psd"
        arquivoSaida = nomeArquivo + "_output.psd"

        carregarOpts = PsdLoadOptions()
        carregarOpts.load_effects_resource = True
        with PsdImage.load(arquivoFonte, carregarOpts) as img:
            imagem = cast(PsdImage, img)
            camadaPreenchimento = cast(FillLayer, imagem.layers[1])
            configuracoesPreenchimento = camadaPreenchimento.fill_settings
            configuracoesPreenchimento.angle = 70
            camadaPreenchimento.update()
            imagem.save(arquivoSaida, PsdOptions())

        with PsdImage.load(arquivoSaida, carregarOpts) as img:
            imagem = cast(PsdImage, img)
            camadaPreenchimento = cast(FillLayer, imagem.layers[1])
            configuracoesPreenchimento = camadaPreenchimento.fill_settings

            assert configuracoesPreenchimento.angle == 70

{{< /highlight >}}

**PSDPYTHON-29. Suporte à escala vertical e horizontal para TextLayer**

{{< highlight python >}}

           arquivoFonte = "1719_src.psd"
           arquivoSaida = "output.png"

           # Adicionar algumas fontes
           pastaFontes = "1719_Fonts"
           pastasFontes = list(FontSettings.get_fonts_folders())
           pastasFontes.append(pastaFontes)
           FontSettings.set_fonts_folders(pastasFontes, True)

           with PsdImage.load(arquivoFonte) as imagem:
               imagem.save(arquivoSaida, PngOptions())

{{< /highlight >}}

**PSDPYTHON-33. [Formato AI] Implementar renderização correta do plano de fundo no Formato AI baseado em PDF**

{{< highlight python >}}

           arquivoFonte = "abacaxis.ai"
           arquivoSaida = "abacaxis.png"

           with AiImage.load(arquivoFonte) as imagem:
               imagem.save(arquivoSaida, PngOptions())

{{< /highlight >}}

**PSDPYTHON-34. Alterar mecanismo de deformação em warp**

{{< highlight python >}}

        arquivoFonte = "grade_corvo.psd"       
        arquivoSaida = self.ObterArquivoNaPastaSaida("exportar.png")

        opts = PsdLoadOptions()
        opts.load_effects_resource = True
        opts.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
        with PsdImage.load(arquivoFonte, opts) as img:
            img.save(arquivoSaida, pngOpt)

{{< /highlight >}}

**PSDPYTHON-35. Acelerar warp**

{{< highlight python >}}

        arquivoFonte = "saida.psd"
        arquivoSaida = "exportar.png"

        opts = PsdLoadOptions()
        opts.load_effects_resource = True
        opts.allow_warp_repaint = True

        tempo_inicio = time.time()

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(arquivoFonte, opts) as img:
            img.save(arquivoSaida, pngOpt)

        tempo_decorrido = time.time() - tempo_inicio

        # valor antigo = 193300
        # novo valor =  55500
        tempo_em_seg = int(tempo_decorrido * 1000)
        if tempo_em_seg > 100000:
            raise Exception("O tempo de processamento é muito longo")

{{< /highlight >}}

**PSDPYTHON-36. Exceção "Falha ao carregar imagem." ao abrir um documento**

{{< highlight python >}}
        arquivoFonte1 = "PRODUTO.ai"
        arquivoSaida1 = "PRODUTO.png"

        with AiImage.load(arquivoFonte1) as imagem:
            imagem.save(arquivoSaida1, PngOptions())

        arquivoFonte2 = "Dolota.ai"
        arquivoSaida2 = "Dolota.png"

        with AiImage.load(arquivoFonte2) as imagem:
            imagem.save(arquivoSaida2, PngOptions())       

        arquivoFonte3 = "ARS_novelty_2108_out_01(1).ai"
        arquivoSaida3 = "ARS_novelty_2108_out_01(1).png"

        with AiImage.load(arquivoFonte3) as imagem:
            imagem.save(arquivoSaida3, PngOptions())

        arquivoFonte4 = "engrenagem.bit.ai"      
        arquivoSaida4 = "engrenagem.bit.png"

        with AiImage.load(arquivoFonte4) as imagem:
            imagem.save(arquivoSaida4, PngOptions())

        arquivoFonte5 = "teste.ai"
        arquivoSaida5 = "teste.png"

        with AiImage.load(arquivoFonte5) as imagem:
            imagem.save(arquivoSaida5, PngOptions())
{{< /highlight >}}

**PSDPYTHON-37. Corrigir salvamento de arquivos psd com Padrão de Traço**

{{< highlight python >}}
	    arquivoFonte = "PadraoFormaTraço.psd"
        arquivoSaida = "PadraoFormaTraço_saida.psd"

        novosLimitesPadrao = Rectangle(0, 0, 4, 4)
        guid = str(uuid.uuid4())
        novoNomePadrao = "$$$/Presets/Patterns/LinhaHorizontal1=Linha Horizontal 9\0"
        novoPadrao = [
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
        ]

        with PsdImage.load(arquivoFonte) as img:
            imagem = cast(PsdImage, img)
            camadaForma = cast(ShapeLayer, imagem.layers[1])
            configPreenchimentoInterno = camadaForma.fill

            recursoPadrao = None
            for recursoGlobalCamada in imagem.global_layer_resources:


                recursoPadrao = as_of(recursoGlobalCamada, PattResource)
                if recursoPadrao is not None:
                    itemPadrao = recursoPadrao.patterns[0]  # Dados do padrão interno de traço
                    
                    itemPadrao.pattern_id = guid
                    itemPadrao.name = novoNomePadrao
                    itemPadrao.set_pattern(novoPadrao, novosLimitesPadrao)
                    break


            configPreenchimentoInterno.pattern_name = novoNomePadrao
            configPreenchimentoInterno.pattern_id = guid + "\0"

            camadaForma.update()

            imagem.save(arquivoSaida)

        # Verificar dados alterados.
        with PsdImage.load(arquivoSaida) as img:
            imagem = cast(PsdImage, img)
            camadaForma = cast(ShapeLayer, imagem.layers[1])
            configPreenchimentoInterno = camadaForma.fill

            assert guid.upper() == configPreenchimentoInterno.pattern_id
            assert novoNomePadrao == configPreenchimentoInterno.pattern_name + "\0"
			
{{< /highlight >}}

**PSDPYTHON-38. O estilo de texto está incorreto em um objeto inteligente ao usar ReplaceContents**

{{< highlight python >}}
        arquivoEntrada = "origem.psd"
        saida2 = "saida.png"

        opcoesCarregarPsd = PsdLoadOptions()
        opcoesCarregarPsd.load_effects_resource = True

        with PsdImage.load(arquivoEntrada, opcoesCarregarPsd) as imagem:
            imagemPsd = cast(PsdImage, imagem)
            objetoInteligente = cast(SmartObjectLayer, imagemPsd.layers[1])

            imagemObjetoInteligente = cast(PsdImage, objetoInteligente.load_contents(opcoesCarregarPsd))

            with imagemObjetoInteligente:
                objetoInteligente.replace_contents(imagemObjetoInteligente)

            pngOpt = PngOptions()
            pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
            imagemPsd.save(saida2, pngOpt)

{{< /highlight >}}

**PSDPYTHON-39. [Formato AI] Corrigir a renderização de Bezier Cúbico no arquivo AI**

{{< highlight python >}}

        arquivoFonte = "Tipografia.ai"
        caminhoSaida = "Tipografia.png"

        with AiImage.load(arquivoFonte) as imagem:
            imagem.save(caminhoSaida, PngOptions())

{{< /highlight >}}
