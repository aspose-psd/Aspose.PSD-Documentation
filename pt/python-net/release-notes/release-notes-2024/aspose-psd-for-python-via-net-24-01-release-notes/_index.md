---
title: Notas de Lançamento do Aspose.PSD para Python via .NET 24.1
type: docs
weight: 10
url: /pt/net/aspose-psd-para-python-via-net-24-1-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                                | **Categoria** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | [Formato AI] Adicionar tratamento básico para imagens AI multipágina                                       |   Recurso   |
|  PSDPYTHON-22 | Efeito de Texto Distorcido não se aplica ao texto                                                          |     Erro    |
|  PSDPYTHON-23 | Renderização incorreta da máscara em arquivo específico                                                   |     Erro    |
|  PSDPYTHON-24 | NullReferenceException em Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor           |     Erro    |
|  PSDPYTHON-25 | [Formato AI] Corrigir uso de memória em AiExporterUtils                                                    |     Erro    |



## **Alterações na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

**PSDPYTHON-19. [Formato AI] Adicionar tratamento básico para imagens AI multipágina**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Carregar a imagem AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # Por padrão, o ActivePageIndex é 0.
            # Portanto, se você salvar a imagem AI sem alterar essa propriedade, a primeira página será renderizada e salva.
            image.save(firstPageOutputPng, PngOptions())

            # Altere o índice da página ativa para a segunda página.
            image.active_page_index = 1

            # Salve a segunda página da imagem AI como uma imagem PNG.
            image.save(secondPageOutputPng, PngOptions())

            # Altere o índice da página ativa para a terceira página.
            image.active_page_index = 2

            # Salve a terceira página da imagem AI como uma imagem PNG.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. O efeito de texto distorcido não se aplica ao texto**

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

**PSDPYTHON-23. Renderização incorreta da máscara em arquivo específico**

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

**PSDPYTHON-24. NullReferenceException em Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [Formato AI] Corrigir o uso de memória em AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # O uso de memória em C# é de 220, mas para Python não temos acesso direto às atividades de GC.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # Carregar a imagem AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Salve a primeira página da imagem AI como uma imagem PNG.
            image.save(firstPageOutputPng, pngOpt)

            # Altere o índice da página ativa para a segunda página.
            image.active_page_index = 1

            # Salve a segunda página da imagem AI como uma imagem PNG.
            image.save(secondPageOutputPng, pngOpt)

            # Altere o índice da página ativa para a terceira página.
            image.active_page_index = 2

            # Salve a terceira página da imagem AI como uma imagem PNG.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("Uso de memória é muito grande. {} em vez de {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}
