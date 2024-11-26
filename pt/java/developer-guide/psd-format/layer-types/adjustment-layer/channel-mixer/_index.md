---
title: Camada de Ajuste do Misturador de Canais
type: docs
weight: 30
url: /pt/java/layer-types/adjustment-layer/channel-mixer/
---

# Trabalhando com a camada de ajuste do misturador de canais do Photoshop em Java

Hoje vamos ver como misturar cores de canais em documentos do Photoshop programaticamente em Java. Como o editor do Photoshop não suporta scripts em Java, vamos usar uma biblioteca especial de manipulação de formato de arquivo PSD chamada Aspose.PSD para Java.

A biblioteca contém **API para trabalhar com canais de cores**. Existem várias formas de misturar as cores, mas, neste artigo, vamos focar na camada de ajuste do misturador de canais.

A API da camada de ajuste do misturador de canais **permite brincar com os canais de cores** para fazer imagens com tons específicos, criar diferentes efeitos de cores criativas ou até mesmo converter a imagem para preto e branco. Em seguida, veremos como aplicar a camada de ajuste do misturador de canais a um documento existente do Photoshop usando o Aspose.PSD para Java, mas primeiro precisamos falar sobre os recursos gerais da API.

## Visão geral da API

Não há nada de especial na criação da camada de ajuste do misturador de canais. Ela pode ser adicionada por meio [do método de fábrica padrão](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) que retorna uma instância da classe ChannelMixerLayer. Esta classe contém funcionalidades gerais como a opção Monocromático e um método para obter um canal de saída. Um canal de saída específico pode ser um dos dois tipos: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) ou [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). O tipo de [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) depende do [modo de cor](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) da imagem.

## Tornar a imagem monocromática

Agora, vamos considerar um exemplo de aplicação da camada de ajuste do misturador de canais a um documento existente do Photoshop. Como esse tipo de camada de ajuste ainda não suporta presets, vamos **recriar o preset do Photoshop Preto e Branco Infravermelho (RGB)** (a). O preset será aplicado à imagem de uma árvore em floração (b). Como resultado, queremos alcançar o efeito da fotografia infravermelha (c).

![Exemplo da Camada de Ajuste do Misturador de Canais](channel-mixer-adjustment-psd-layer-figure-1.png) Primeiro, para recriar o preset do Photoshop Preto e Branco Infravermelho (RGB), é necessário habilitar a flag de monocrômico e definir valores brutos apropriados para cada cor (vermelho, verde e azul) para o canal de saída Cinza:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **curto** )200);
    grayOutputChannel.setBlue(( **curto** )-30);

A imagem deve estar no modo de cor RGB para que o código funcione (devido à conversão para a classe RgbMixerChannel). O modo de cor CMYK também é suportado, mas apenas para imagens com o modo de cor correspondente.

Lembre-se de que o valor de cada cor e a propriedade Constant devem estar na faixa de -200 a 200.

## Conclusão

Neste artigo, consideramos como trabalhar com a API do Misturador de Canais do Aspose.PSD para Java para ajustar cores nos canais de cores e converter a imagem para preto e branco.
