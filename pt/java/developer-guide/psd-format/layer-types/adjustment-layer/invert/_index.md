---
title: Inverter Camada de Ajuste
type: docs
weight: 30
url: /pt/java/layer-types/adjustment-layer/invert/
---

# Trabalhando com a camada de ajuste Inverter do Photoshop em Java

Neste artigo, vamos mostrar como transformar uma imagem em um documento do Photoshop em uma imagem negativa programaticamente em Java. Para este propósito, vamos utilizar a biblioteca para manipulação de arquivos PSD chamada Aspose.PSD para Java.

A API de inversão de cor permite **adicionar um efeito negativo a uma imagem**. Você já pode ter visto como [inverter as cores da imagem usando a camada de ajuste Curvas](/pt/psd/java/layer-types/adjustment-layer/curves/). No entanto, hoje iremos considerar uma forma mais rápida e fácil de fazer o trabalho usando a camada de ajuste Inverter.

## Visão geral da API

**A API da camada de ajuste Inverter** consiste na própria classe da camada que é [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer). Esta classe não possui membros públicos próprios, pois herda todos os membros públicos da classe pai ([AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)). Isso simplifica o seu uso, pois tudo que você precisa fazer é adicioná-la a um arquivo PSD e a imagem se torna negativa.

## Inverter as cores da imagem

Portanto, mesmo que pareça óbvio, vamos demonstrar para maior clareza como **aplicar a camada de ajuste Inverter à imagem** de um astronauta (a) para criar o efeito negativo para essa imagem (b).

![Exemplo Antes e Depois da Camada de Ajuste Inverter](invert-adjustment-layer-figure-1.png)

Para **inverter as cores da imagem**, basta adicionar uma camada de ajuste Inverter ao PSD:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

É isso! Não há propriedades específicas a serem configuradas para este tipo de camada de ajuste.

## Conclusão

Neste artigo, aprendemos sobre a API da camada de ajuste Inverter do Aspose.PSD para Java. É uma ferramenta sem esforço para obter imagens negativas, pois a API desta camada de ajuste não declara membros públicos específicos.
