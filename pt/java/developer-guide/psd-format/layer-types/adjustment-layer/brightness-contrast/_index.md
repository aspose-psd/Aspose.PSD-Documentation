---
title: Camada de Ajuste de Brilho e Contraste no Java
type: docs
weight: 30
url: /pt/java/layer-types/adjustment-layer/brightness-contrast/
---

# Trabalhando com a camada de ajuste de Brilho e Contraste do Photoshop em Java

Neste artigo, aplicaremos o ajuste de Brilho/Contraste a um documento do Adobe® Photoshop® usando a biblioteca Aspose.PSD para Java®. Além disso, aprenderemos mais sobre os recursos da biblioteca relacionados a esse tipo de camada de ajuste ao longo do caminho.

Mas primeiro um pouco de teoria.

A camada de ajuste de Brilho/Contraste altera o brilho e o contraste da imagem. Mas espere um minuto, o que isso realmente significa? Aumentar o brilho clareia o valor da cor até o branco e diminuir o brilho escurece o valor da cor até o preto. Aumentar o contraste, por sua vez, aumentará a diferença entre cores claras e escuras e diminuir o contraste diminuirá essa diferença; isso significa que cores claras ficam mais claras e cores escuras ficam mais escuras.

## Suporte ao modo de cor

A biblioteca permite adicionar camadas de ajuste de Brilho/Contraste a imagens nos modos de cor RGB, CMYK ou Lab.

## O comportamento atual e legado

A implementação atual da biblioteca (v20.6 no momento da redação) usa o algoritmo padrão do Photoshop que preserva a gama tonal completa das sombras aos realces, mas ainda não suporta o comportamento legado. Isso significa que a biblioteca suporta camadas de ajuste de Brilho/Contraste em documentos criados nas últimas versões do Photoshop (CS4 e superiores). No entanto, você pode [solicitar a implementação legada da camada de ajuste de Brilho/Contraste](https://forum.aspose.com/c/psd) em nosso fórum se precisar.

## Ajustar brilho e contraste

Agora, vamos descrever como o API de alto nível da camada de ajuste de Brilho/Contraste funciona (olhando adiante, o API é direto). A classe PsdImage contém um método de fábrica (addBrightnessContrastAdjustmentLayer) para instanciar a classe BrightnessContrastLayer que é o gateway para o ajuste de brilho e contraste. A classe BrightnessContrastLayer contém apenas um par de métodos de acesso e alteração de propriedades de brilho e contraste.

![|Exemplo de Camada de Ajuste de Brilho/Contraste em PSD](brightness-contrast-psd-adjustment-layer-figure-1.png)

Então, vamos pegar uma imagem de um cachorro (b), por exemplo, para ajustar seu brilho1 e contraste2 (a), usando apenas o método de fábrica com argumentos correspondentes, para eventualmente obter uma imagem (c) que pareça mais vívida:

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

Observações:

1. O valor de brilho deve estar na faixa de -150 a 150.
2. O valor de contraste deve estar na faixa de -50 a 100.

Consulte a documentação da [BrightnessContrastLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer) para mais detalhes.

## Conclusão

Neste artigo, tivemos uma rápida visão geral da camada de ajuste de Brilho/Contraste e aprendemos como ajustar o brilho e o contraste da imagem usando o método de fábrica.

Consulte nossa série de [artigos sobre APIs de camadas de ajuste](/psd/pt/java/layer-types/adjustment-layer/) do Aspose.PSD para Java para saber mais.
