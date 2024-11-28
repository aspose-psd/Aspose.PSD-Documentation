---
title: Aspose.PSD para Python via .NET 24.3 - Notas de Lançamento
type: docs
weight: 10
url: /pt/net/aspose-psd-para-python-via-net-24-3-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Chave**    | **Resumo**                                                          | **Categoria** |
|:------------ |:-------------------------------------------------------------------- |:------------- |
| PSDPYTHON-42 | [AI Format] Reduzir tempo de carregamento de imagens AI multipágina grandes | Melhoria      |
| PSDPYTHON-45 | Arquivo PSD após a conversão de 8 bits para 16 bits tornou-se ilegível | Bug           |
| PSDPYTHON-46 | Arquivo PSD após a conversão de 8 bits para 32 bits tornou-se ilegível | Bug           |
| PSDPYTHON-47 | [AI Format] Corrigir a renderização de Curvas Curtas em arquivo AI    | Bug           |



## **Alterações na API Pública**
# **APIs Adicionadas:**
- Nenhuma

# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

**PSDPYTHON-42. [AI Format] Reduzir tempo de carregamento de imagens AI multipágina grandes**

{{< highlight python >}}
   # Sem exemplo
{{< /highlight >}}

**PSDPYTHON-45. Arquivo PSD após conversão de 8 bits para 16 bits tornou-se ilegível**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # está correto
                pass
            else:
                raise Exception("Recurso global incorreto, o primeiro recurso deve ser Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. Arquivo PSD após a conversão de 8 bits para 32 bits tornou-se ilegível**


{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # está correto
                pass
            else:
                raise Exception("Recurso global incorreto, o primeiro recurso deve ser Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [AI Format] Corrigir a renderização de Curvas Curtas em arquivo AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}
