---
title: Utilizando Camada de Ajuste para Aprimoramento de PSD
weight: 100
type: docs
description: Exemplos de utilização de camadas de ajuste via Aspose.PSD para C#
keywords: [camada de ajuste, aprimoramento de foto, ajuste de curvas, aprimoramento de níveis, inverter, filtro de foto, api psd, C#, csharp, exemplo de código]
url: pt/camada-de-ajuste-aprimoramento/
---

## Visão Geral

Neste artigo, exploraremos a edição de camadas de ajuste no Aspose.PSD para C#. As camadas de ajuste são um recurso poderoso na edição de imagens que permitem fazer alterações não destrutivas em suas imagens. O Aspose.PSD fornece um conjunto abrangente de classes de camada de ajuste que você pode utilizar para modificar vários aspectos de suas imagens.

Para demonstrar a edição das camadas de ajuste, utilizaremos um trecho de código de exemplo no final da página que carrega uma imagem PSD e aplica diferentes ajustes às suas camadas.

No trecho de código abaixo, começamos carregando a imagem PSD usando o método `PsdImage.Load()`. Em seguida, configuramos as opções para salvar os arquivos PNG de saída. A classe `PngOptions` nos permite especificar o tipo de cor para a imagem de saída.

Depois, iteramos por cada camada na imagem PSD e verificamos seu tipo usando o método `IsAssignable()`. Se a camada for de um tipo específico, a lançamos para esse tipo utilizando o método `Cast()` e aplicamos o ajuste desejado. Por exemplo, ajustamos o brilho e contraste de uma `BrightnessContrastLayer`, modificamos os níveis de uma `LevelsLayer`, adicionamos um ponto de curva a uma `CurvesLayer`, e assim por diante.

Você pode adicionar código adicional para aplicar outros ajustes às suas respectivas camadas. O Aspose.PSD fornece uma ampla gama de classes de camadas de ajuste, como [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer) e muito mais.

Por fim, salvamos a imagem modificada usando o método `Save()` da classe `PsdImage`.

Este código fornece uma visão geral básica de como editar camadas de ajuste no Aspose.PSD para C#. Você pode personalizar os ajustes de acordo com suas necessidades e explorar as diversas opções disponíveis na documentação da API.

## Exemplo

Segue um exemplo de código demonstrando como utilizar camadas de ajuste em Aspose.PSD para C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

Para informações mais detalhadas e exemplos, visite a [documentação do Aspose.PSD para C#](https://docs.aspose.com/psd/net/).
