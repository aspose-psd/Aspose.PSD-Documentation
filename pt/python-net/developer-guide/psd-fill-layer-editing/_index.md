---
title: Atualização da Camada de Preenchimento PSD usando Python
weight: 100
type: docs
description: Exemplos de uso de todos os tipos de camadas de ajuste, incluindo Preenchimento de Cor, Preenchimento de Gradiente e Preenchimento de Padrão
keywords: [camada de preenchimento, Preenchimento de Cor, Preenchimento de Gradiente, Preenchimento de Padrão, api psd, python, exemplo de código]
url: /pt/python-net/edicao-de-camada-de-preenchimento-psd/
---

## **Visão Geral**

Para criar uma camada regular, você pode usar a função create_regular_layer fornecida no código. Esta função recebe os parâmetros left, top, width e height para definir a posição e tamanho da camada. Ela cria uma nova camada, define seus limites e a preenche com uma cor especificada.

Para criar uma camada de preenchimento de cor, você pode usar o método FillLayer.create_instance com o parâmetro FillType.COLOR. Após criar a camada de preenchimento, você pode acessar suas configurações de preenchimento usando a propriedade fill_settings e definir a cor usando a propriedade color da classe ColorFillSettings. No código fornecido, a cor é definida como Color.coral. A propriedade clipping da camada de preenchimento é definida como 1, o que faz a camada atuar como uma máscara de corte.

Para criar uma camada de preenchimento de gradiente, você pode usar o método FillLayer.create_instance com o parâmetro FillType.GRADIENT. Semelhante à camada de preenchimento de cor, você pode acessar as configurações de preenchimento usando a propriedade fill_settings e definir os pontos de cor do gradiente e os pontos de transparência. No código fornecido, os pontos de cor do gradiente são definidos usando a classe GradientColorPoint e os pontos de transparência são definidos usando a classe GradientTransparencyPoint. A propriedade clipping da camada de preenchimento também é definida como 1.

Para criar uma camada de preenchimento de padrão, você pode usar o método FillLayer.create_instance com o parâmetro FillType.PATTERN. Novamente, você pode acessar as configurações de preenchimento usando a propriedade fill_settings e definir os dados do padrão e outras propriedades. No código fornecido, os dados do padrão são definidos usando a classe PatternFillSettings e a propriedade clipping é definida como 1.

Após criar as camadas de preenchimento, você pode adicioná-las à imagem PSD usando o método add_layer. Você também pode especificar o nome de exibição e outras propriedades para cada camada de preenchimento.

Por fim, você pode salvar a imagem PSD e a imagem PNG correspondente usando o código fornecido. As opções de PNG são definidas para usar verdadeira cor com alfa para transparência.

Por favor, verifique o exemplo completo.

## **Exemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentacao-Python-Aspose-edicao-de-camada-de-preenchimento-psd.py" >}}
