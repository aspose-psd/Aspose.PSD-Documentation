---
title: Camada de Ajuste de Exposição
type: docs
weight: 30
url: /pt/java/layer-types/adjustment-layer/exposure/
---

# Trabalhando com a camada de ajuste de exposição do Photoshop em Java

Neste artigo, vamos adicionar uma camada de ajuste de exposição a um documento do Adobe® Photoshop® usando o Aspose.PSD para Java - uma biblioteca de manipulação de arquivos PSD. A biblioteca funciona sem o editor do Photoshop instalado, pois utiliza seus próprios algoritmos de processamento de imagem. Também aprendemos alguns detalhes relacionados à API de ajuste de exposição da biblioteca.

## Visão geral da API

A camada de ajuste de exposição é configurada por meio da classe [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer) que contém as seguintes propriedades para trabalhar com o ajuste de exposição:

- Define o quanto de luz a foto tem ao comprimir ou esticar todo o histograma em relação aos tons escuros. Portanto, afeta principalmente os realces.
- Ao contrário do deslocamento da exposição, que afeta principalmente as sombras.
- Correção gama. Corrige a luminância da imagem.

## Exposição correta

Corrigir a exposição e propriedades relacionadas é tão simples quanto alterar algumas propriedades da classe. Vamos aplicar alguns ajustes de exposição (a) a uma foto subexposta de uma biblioteca (b) para torná-la perceptível ao olho humano (c).

![Exemplo de Camada de Ajuste de Exposição](exposure-adjustment-layer-figure-1.png)

Todo o ajuste é feito principalmente usando a correção gama. No entanto, a exposição e o deslocamento também são ajustados um pouco. Tudo o que você precisa fazer é definir valores apropriados para as propriedades já mencionadas:

    ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
    exposureLayer.setExposure(-0.03f);
    exposureLayer.setOffset(-0.0005f);
    exposureLayer.setGammaCorrection(1.85f);

Observe que a exposição deve estar na faixa de -20.0 a 20.0, o valor do deslocamento deve estar na faixa de -0.5 a 0.5 e a faixa de valor da correção gama deve estar entre 9.99 e 0.01.

Consulte a [referência da API da camada de ajuste de exposição](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer) para mais detalhes.

## Conclusão

Neste artigo, aprendemos como adicionar uma camada de ajuste de exposição a um arquivo PSD para clarear a imagem, bem como consideramos alguns detalhes da API.
