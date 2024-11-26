---
title: Camada de Ajuste de Equilíbrio de Cores
type: docs
weight: 30
url: /pt/java/layer-types/adjustment-layer/color-balance/
---

# Trabalhando com a camada de ajuste de equilíbrio de cores do Photoshop em Java

Neste artigo, vamos **ajustar o equilíbrio de cores da imagem** no formato de arquivo PSD em Java. Vamos usar uma biblioteca especial chamada Aspose.PSD para Java, que é uma caixa de ferramentas para manipulação de documentos do Photoshop.

Como a biblioteca trabalha com o formato de arquivo PSD, ela contém quase [todos os recursos](https://docs.aspose.com/psd/java/features/) disponíveis no editor do Photoshope a **camada de ajuste de equilíbrio de cores**, que é absolutamente adequada para esta tarefa, não é uma exceção.

A camada de ajuste de equilíbrio de cores torna possível mudar o equilíbrio entre as cores primárias (RGB) e subtrativas (CMY) para sombras, tons médios e destaques de forma simples e rápida.

## Ajustar o Equilíbrio de Cores

Como mencionado anteriormente, a camada de ajuste de equilíbrio de cores no Aspose.PSD para Java é exatamente o que é **um balanceador entre cores primárias e subtrativas**. Isso significa que há três escalas para cada par de cores (ciano/vermelho, magenta/verde, amarelo/azul). A intensidade de uma cor específica no par irá aumentar se o valor se mover em sua direção e vice-versa. Além disso, esses três pares são inerentes a cada área da faixa tonal (sombras, tons médios e destaques) o que aumenta a flexibilidade desse tipo de ajuste.

Então, vamos aplicar esse conhecimento na prática. Por exemplo, escolhemos uma foto avermelhada do rosto de uma mulher (b). O rosto está muito avermelhado e vamos corrigir isso **adicionando uma camada de ajuste de equilíbrio de cores** para diminuir o vermelho e aumentar o ciano basicamente (a) para obter um rosto que pareça mais natural (c). Novamente, há muito trabalho a ser feito com esta imagem, mas dentro deste artigo é tudo o que faremos.

![Exemplo de camada de ajuste de equilíbrio de cores](color-balance-adjustment-layer-example-figure-1.png) A API da camada de ajuste de equilíbrio de cores tem um design simples. Portanto, a [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) classe é tudo o que você precisa. Primeiramente, preserve a luminosidade porque ela é desativada por padrão. Depois, adicione um pouco de verde e mais amarelo para sombras usando os métodos correspondentes (cujo nome consiste no nome da área da faixa tonal particular e nos nomes das cores no par de cores), em seguida, adicione mais ciano e um pouco de azul para os tons médios, e finalmente adicione mais ciano além de um pouco de magenta e azul:

    ColorBalance
