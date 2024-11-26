---
title: Utilizando Camada de Ajuste para Melhorias em PSD
weight: 100
type: docs
description: Exemplos de uso da camada de ajuste via Aspose.PSD para Java
keywords: [camada de ajuste, aprimoramento de fotos, ajuste de curvas, aprimoramento de níveis, inverter, filtro de fotos, api psd, java, exemplo de código]
url: pt/java/adjustment-layer-enhancement/
---

## **Visão Geral**

Este artigo explora a edição de camadas de ajuste no Aspose.PSD para Java. As camadas de ajuste são um recurso poderoso na edição de imagens que permitem fazer alterações não destrutivas em suas imagens. O Aspose.PSD fornece um conjunto abrangente de classes de camadas de ajuste que você pode usar para modificar vários aspectos de suas imagens.

Para demonstrar a edição de camadas de ajuste, forneceremos um trecho de código de exemplo no final da página que carrega uma imagem PSD e aplica diferentes ajustes às suas camadas.

No trecho de código a seguir, começamos carregando a imagem PSD usando o método PsdImage.load(). Em seguida, configuramos as opções para salvar os arquivos PNG de saída. A classe PngOptions nos permite especificar o tipo de cor para a imagem de saída.

Em seguida, iteramos por cada camada na imagem PSD e verificamos seu tipo usando o método isAssignable(). Se a camada for de um tipo específico, a lançamos para esse tipo usando o método cast() e aplicamos o ajuste desejado. Por exemplo, ajustamos o brilho e contraste de uma BrightnessContrastLayer, modificamos os níveis de uma LevelsLayer, adicionamos um ponto de curva a uma CurvesLayer, e assim por diante.

Você pode adicionar código adicional para aplicar outros ajustes às suas respectivas camadas. O Aspose.PSD fornece uma ampla variedade de classes de camadas de ajuste, como [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), e mais.

Por fim, salvamos a imagem modificada usando o método save() da classe PsdImage.

Isso fornece uma visão geral básica de como editar camadas de ajuste no Aspose.PSD para Java. Você pode personalizar os ajustes de acordo com suas necessidades e explorar as várias opções disponíveis na documentação da API.

Por favor, verifique o exemplo completo abaixo.

## **Exemplo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}
