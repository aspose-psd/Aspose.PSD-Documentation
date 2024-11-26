---
title: Notas da Versão de Aspose.PSD para Python via .NET 24.7
type: docs
weight: 10
url: /pt/python-net/aspose-psd-for-python-via-net-24-7-release-notes/
---

{{% alert color="primary" %}}

Esta página contém as notas de versão para o [Aspose.PSD para Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Chave**    | **Resumo**                                                                                                     | **Categoria** |
|:------------|:-----------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | Exceção "Falha ao carregar imagem" ao abrir documento AI                                                       | Bug      |
| PSDPYTHON-87 | Texto renderizado incorretamente em arquivos PDF de saída                                                     | Bug      |
| PSDPYTHON-88 | Corrigir ImageSaveException: Falha na exportação da imagem para o arquivo fornecido no Linux                  | Bug      |
| PSDPYTHON-89 | Corrigir carregamento de fontes ao usar Aspose.Drawing                                                        | Bug      |
| PSDPYTHON-90 | 'Operação aritmética resultou em um estouro' ao criar camada de objeto inteligente usando JPEG grande        | Bug      |
| PSDPYTHON-91 | O arquivo AI não pode ser convertido em um arquivo JPG                                                       | Bug      |

## **Alterações na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDPYTHON-86. Exceção "Falha ao carregar imagem" ao abrir documento AI**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Texto renderizado incorretamente em arquivos PDF de saída**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Corrigir ImageSaveException: Falha na exportação da imagem para o arquivo fornecido no Linux**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("Bed_Roll-Sticker4_1.psd")
        outputFile = self.GetFileInOutputFolder("output.jpg")

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        saveOpt = JpegOptions()
        saveOpt.quality = 70
        with PsdImage.load(sourceFile, loadOpt) as psdImage:
            psdImage.save(outputFile, saveOpt)
{{< /highlight >}}


**PSDPYTHON-89. Corrigir carregamento de fontes ao usar Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Antes da atualização. Contagem de fontes instaladas: " + str(len(installedFonts.families)))
            print("- Atualize o cache de fontes tentando obter o nome da fonte Adobe para 'Arial': ")
            FontSettings.get_adobe_font_name("Arial")
            print("- Após a atualização. Contagem de fontes instaladas: " + str(len(installedFonts.families))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'Operação aritmética resultou em um estouro' ao criar camada de objeto inteligente usando JPEG grande**
{{< highlight python >}}
        # A correção foi feita, mas há outro problema no Aspose.PSD para Python que restringe este teste
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as image:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "Camada de Teste"
                #image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. O arquivo AI não pode ser convertido em um arquivo JPG**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}
