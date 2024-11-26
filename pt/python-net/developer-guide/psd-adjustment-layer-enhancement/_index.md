---
title: Usando Camada de Ajuste para Melhorias em PSD
weight: 100
type: docs
description: Exemplos de uso de camada de ajuste via Aspose.PSD para Python
keywords: [camada de ajuste, melhoria de foto, ajuste de curvas, melhoria de níveis, inverter, filtro de foto, api psd, python, exemplo de código]
url: pt/python-net/camada-de-ajuste-melhoria/
---

## **Visão Geral**

Neste artigo, exploraremos a edição de camadas de ajuste no Aspose.PSD para Python. As camadas de ajuste são um recurso poderoso na edição de imagens que permitem fazer alterações não destrutivas em suas imagens. O Aspose.PSD fornece um conjunto abrangente de classes de camadas de ajuste que você pode usar para modificar vários aspectos de suas imagens.

Para demonstrar a edição de camadas de ajuste, usaremos um trecho de código de exemplo no final da página que carrega uma imagem PSD e aplica diferentes ajustes às suas camadas.

No trecho de código abaixo, começamos carregando a imagem PSD usando o método PsdImage.load(). Em seguida, configuramos as opções para salvar os arquivos PNG de saída. A classe PngOptions nos permite especificar o tipo de cor para a imagem de saída.

Em seguida, iteramos por cada camada na imagem PSD e verificamos seu tipo usando o método is_assignable(). Se a camada for de um tipo específico, a convertemos para esse tipo usando o método cast() e aplicamos o ajuste desejado. Por exemplo, ajustamos o brilho e contraste de uma BrightnessContrastLayer, modificamos os níveis de uma LevelsLayer, adicionamos um ponto de curva a uma CurvesLayer, e assim por diante.

Você pode adicionar código adicional para aplicar outros ajustes em suas respectivas camadas. O Aspose.PSD fornece uma ampla variedade de classes de camadas de ajuste, como [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) e outros.

Por fim, salvamos a imagem modificada usando o método save() da classe PsdImage.

Este código fornece uma visão geral básica de como editar camadas de ajuste no Aspose.PSD para Python. Você pode personalizar os ajustes de acordo com seus requisitos e explorar as várias opções disponíveis na documentação da API.

Por favor, confira o exemplo completo.

## **Exemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentação-Python-Aspose-ajuste-camada-melhoria.py" >}}
