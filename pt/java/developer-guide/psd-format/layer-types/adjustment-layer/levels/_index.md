---
title: Camada de Ajuste Preto e Branco
type: docs
weight: 30
url: /pt/java/layer-types/adjustment-layer/levels/
---

## Trabalhando com a camada de ajuste de níveis no Photoshop em Java

Neste artigo, aprenderemos como ajustar o alcance tonal e o equilíbrio de cor de uma foto no formato de arquivo [PSD](/psd/pt/java/psd-format/) programaticamente em Java. Não utilizamos o editor de fotos Adobe® Photoshop® em si. Em vez disso, utilizamos a biblioteca Aspose.PSD para Java, que funciona de forma independente para manipular o documento do Photoshop.

Embora o Aspose.PSD para Java suporte mais do que ferramentas suficientes para [editar a foto](/psd/pt/java/manipulating-images/) como desejamos, vamos **utilizar a API da camada de ajuste de níveis** que é uma das maneiras mais simples e rápidas de realizar o trabalho.

## Visão geral da API

A implementação atual (20.6 no momento da escrita) da API da camada de ajuste de níveis **suporta todos os recursos básicos dos Níveis do Photoshop**, ou seja, ajustar os Níveis de entrada e saída para o canal composto (RGB) assim como para cada canal de cor primária (vermelho, verde e azul).

A API da camada de ajuste de níveis é direta. A classe [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) é um ponto de entrada para o ajuste de níveis. Ela contém alguns métodos para acessar os canais de cor: getMasterChannel e getChannel(int). Ambos os métodos retornam [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel) que possui propriedades correspondentes para a manipulação dos Níveis de entrada e saída. A diferença está no fato de que getMasterChannel serve para ajustar o canal de cor composto (RGB) enquanto getChannel acessa um canal de cor específico (vermelho, verde ou azul) pelo seu índice.

## Compatibilidade com modos de cor

Vale ressaltar que a camada de ajuste de níveis **é compatível com a grande maioria dos modos de cor** de acordo com os Níveis do Photoshop. Portanto, é possível ajustar os Níveis para imagens em Escala de Cinza (canal cinza), RGB (canais RGB, vermelho, verde e azul), CMYK (canais CMYK, ciano, magenta, amarelo e preto), Duotone (canal monocromático) e LAB (luminosidade, a e b canais) modos de cor.

## Ajustar alcance tonal

Simplesmente falando, a correção tonal aplica-se a uma imagem para remodelar as sombras e os realces para uma melhor distribuição dos meios-tons. Geralmente, **faz a imagem parecer mais contrastada** , se feito corretamente. Por exemplo, vamos pegar uma foto de um cachorro (b) e ajustar seu alcance tonal (a – a captura de tela é feita a partir da janela de Níveis do Photoshop para clareza) para que a foto pareça mais contrastada (c).

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Figura 1 da Camada de Ajuste de Níveis](levels-adjustment-figure-1.png)|

Para **ajustar o alcance tonal geral** de uma imagem, os Níveis de entrada do canal mestre devem ser definidos:

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel(( **short** )229);

É necessário ter em mente que os Níveis de entrada devem estar no intervalo de 0 a 253 para sombras, de 9,99 a 0,01 para meios-tons e de 2 a 255 para realces. O intervalo dos Níveis de saída deve estar entre 0 e 255.

Precisa de mais exemplos? Você pode encontrá-los no [Github](https://github.com/aspose-psd/Aspose.PSD-for-Java) e na [base de conhecimento](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers).

## Conclusão

Para resumir, o Aspose.PSD para Java possui uma API útil e simples para alterar o alcance tonal e o equilíbrio de cor de uma imagem, que é compatível com quase todos os modos de cor. A API da camada de ajuste de níveis da biblioteca se assemelha aos Níveis do Photoshop, portanto, é fácil começar, mesmo se você nunca tiver trabalhado com a biblioteca anteriormente.
