---
title: Aspose.PSD para Java 24.3 - Notas de Lançamento
type: docs
weight: 40
url: /pt/java/aspose-psd-para-java-24-3-notas-de-lancamento/
---

{{% alert color="primary" %}} Esta página contém notas de lançamento para [Aspose.PSD para Java 24.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.3/) {{% /alert %}}

| **Chave**   | **Resumo**                                                                 | **Categoria** |
|:------------|:--------------------------------------------------------------------------|:-------------|
| PSDJAVA-601 | [Formato AI] Reduzir tempo de carregamento de imagens AI multipágina grandes.| Melhoria     |
| PSDJAVA-604 | O arquivo PSD, após a conversão de 8 bits para 16 bits, tornou-se ilegível. | Bug          |
| PSDJAVA-605 | O arquivo PSD, após a conversão de 8 bits para 32 bits, tornou-se ilegível. | Bug          |
| PSDJAVA-606 | [Formato AI] Corrigir a renderização da Curva Curta no arquivo AI.         | Bug          |

## **Mudanças na API Pública**
# **APIs Adicionadas:**

- T:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.getFilters
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isEnabled 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskEnabled 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskExtendWithWhite 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskLinked 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isValidAtPosition 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.setFilters(com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter[])
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.updateResourceValues 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.#ctor 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.apply(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.applyToMask(com.aspose.psd.fileformats.psd.layers.Layer)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.deepClone 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getBlendMode 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getName 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getOpacity 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getSourceDescriptor 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setBlendMode(long)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setOpacity(double)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.isEnabled 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.#ctor 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.FilterType 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getAmountNoise 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getDistribution 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getName 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setAmountNoise(double)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setDistribution(int)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setMonochromatic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.isMonochromatic 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.rendering.ISmartFilterRenderer.render(com.aspose.psd.PixelsData)
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.#ctor 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.FilterType 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getName 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getRadius 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.setRadius(double)
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.rendering.ISmartFilterRenderer 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution.Gaussian 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution.Uniform 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter.getName

# **APIs Removidas:**

- Nenhuma

## **Exemplos de Uso:**

**PSDJAVA-604. O arquivo PSD, após a conversão de 8 bits para 16 bits, tornou-se ilegível**

{{< highlight java >}}

        String arquivoOrigem = "src/main/resources/test_smart_layer.psd";
        String arquivoDestino = "src/main/resources/export.psd";

        try (PsdImage imagemPsd8 = (PsdImage) Image.load(arquivoOrigem)) {
            PsdOptions opcoesPsd16 = new PsdOptions();
            opcoesPsd16.setChannelBitsCount((short) 16);

            imagemPsd8.save(arquivoDestino, opcoesPsd16);
        }

        try (PsdImage imagemPsd16 = (PsdImage) Image.load(arquivoDestino)) {
            if (imagemPsd16.getGlobalLayerResources()[0] instanceof Lr16Resource) {
                // está correto
            } else {
                throw new Exception("Recurso global incorreto, o primeiro recurso deveria ser Lr16Resource");
            }
        }

{{< /highlight >}}

**PSDJAVA-605. O arquivo PSD, após a conversão de 8 bits para 32 bits, tornou-se ilegível**

{{< highlight java >}}

        String arquivoOrigem = "src/main/resources/test_smart_layer.psd";
        String arquivoDestino = "src/main/resources/export.psd";

        try (PsdImage imagemPsd8 = (PsdImage) Image.load(arquivoOrigem)) {
            PsdOptions opcoesPsd32 = new PsdOptions();
            opcoesPsd32.setChannelBitsCount((short) 32);

            imagemPsd8.save(arquivoDestino, opcoesPsd32);
        }

        try (PsdImage imagemPsd8 = (PsdImage) Image.load(arquivoDestino)) {
            if (imagemPsd8.getGlobalLayerResources()[0] instanceof Lr32Resource) {
                // está correto
            } else {
                throw new Exception("Recurso global incorreto, o primeiro recurso deveria ser Lr16Resource");
            }
        }

{{< /highlight >}}

**PSDJAVA-606. [Formato AI] Corrigir a renderização da Curva Curta no arquivo AI**

{{< highlight java >}}

        String arquivoOrigem = "src/main/resources/shortCurve.ai";
        String caminhoArquivoSaida = "src/main/resources/shortCurve.png";

        try (AiImage imagem = (AiImage) Image.load(arquivoOrigem)) {
            imagem.save(caminhoArquivoSaida, new PngOptions());
        }

{{< /highlight >}}
