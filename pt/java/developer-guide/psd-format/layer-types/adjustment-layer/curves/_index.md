---
title: Camada de Ajuste de Curvas
type: docs
weight: 30
url: /pt/java/layer-types/adjustment-layer/curves/
---

# Trabalhando com a camada de ajuste de curvas do Photoshop em Java

O objetivo deste artigo é demonstrar as capacidades da biblioteca Aspose.PSD para Java ao **trabalhar com camadas de ajuste de Curvas** em documentos do Adobe® Photoshop®. A biblioteca é totalmente autônoma. Portanto, funciona sem a necessidade de instalar o editor de fotos Photoshop. A [lista completa de recursos](https://docs.aspose.com/psd/java/features/) pode ser encontrada em nossa base de conhecimento. Bem, agora voltando para as Curvas.

## Visão geral da API

A ferramenta Curvas pode ser representada como uma linha diagonal (curva) em um gráfico com destaques no canto superior direito e sombras no canto inferior direito.

A biblioteca fornece uma API para trabalhar com a curva, especificamente, a classe [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer). No entanto, essa classe possui **dois enfoques completamente diferentes** para trabalhar com a curva. Portanto, ela pode ser editada em um dos dois modos a qualquer momento:

- Contínuo (a curva representada como um caminho com pontos nos locais de curvatura)
- Discreto (a curva representada como uma linha pontilhada)

Assim, a biblioteca tem duas maneiras de modificar a curva usando respectivamente o [gerenciador contínuo](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) e o [gerenciador discreto](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager). Em seguida, vamos explicar como usar cada um deles em um exemplo específico.

## Ajustar cor e tom usando o Gerenciador Contínuo de Curvas

O [Gerenciador Contínuo de Curvas](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **configura os pontos de curvatura de uma curva contínua** para o canal composto (RGB) e também para cada canal de cor específico. Para fins de demonstração, será aplicado um ajuste de Curvas (a) em uma imagem escurecida de uma orquestra (b) para obter uma imagem clareada com cores mais quentes (c):

![Figura 1 da Camada de Ajuste de Curvas](curves-psd-adjustment-layer-figure-1.png)

Como existem dois gerenciadores, é necessário selecionar explicitamente um deles (gerenciador contínuo, neste caso), antes de obtê-lo. Depois, podemos adicionar diretamente pontos de curva em certas coordenadas para os canais de cor desejados (RGB composto, vermelho e azul, respectivamente) para recriar a forma da curva:
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

A origem das coordenadas está no canto inferior esquerdo. O valor da coordenada máxima de um ponto é limitado ao tipo de dados (byte) e é igual a 255 (127 para o tipo assinado).

Existem também alguns [outros métodos](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) que você pode usar.

## Ajustar o tom usando o Gerenciador Discreto de Curvas

O Gerenciador Discreto de Curvas também permite posicionar pontos de curva (alterar cor e tom na realidade), mas a diferença é que eles o fazem de forma diferente. Primeiro, a **curva consiste em pontos** ou pontos (não uma linha sólida). Em segundo lugar, esse gerenciador **não coloca um ponto em qualquer lugar** no gráfico. Em vez disso, **move o ponto para cima ou para baixo** com uma faixa de valores entre 255 e 0, respectivamente. Por padrão, os valores dos pontos de curva aumentam incrementalmente para formar uma curva que está em um ângulo de 45 graus.

Portanto, com isso em mente, é fácil recriar o ajuste predefinido do Photoshop de "Negativo (RBG)" (a) e aplicá-lo a uma imagem em escala de cinza de um vale (b) para obter no final uma representação negativa do vale (c).

![Figura 2 da Camada de Ajuste de Curvas](curves-psd-adjustment-layer-figure-2.png) Em primeiro lugar, não se esqueça de selecionar o gerenciador correspondente para poder usá-lo e, em seguida, definir os valores dos pontos da curva em ordem decrescente começando de 255 até 0 para cada ponto da curva (255 no total):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

O gerenciador também fornece alguns [outros métodos](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) para gerenciar a curva.

## Conclusão

Neste artigo, aprendemos como trabalhar com camadas de ajuste de Curvas em documentos do Photoshop usando o Aspose.PSD para Java de duas formas completamente diferentes (gerenciadores contínuos e discretos).
