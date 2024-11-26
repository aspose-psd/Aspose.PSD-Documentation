---
title: Manipulação inteligente de filtros no Aspose.PSD para Python
weight: 100
type: docs
description: Exemplos de como usar Filtros Inteligentes no Arquivo PSD
keywords: [filtro inteligente, adicionar ruído, desfoque gaussiano, afiar, filtro, filtro psd, api psd, python, exemplo de código]
url: pt/python-net/filtros-inteligentes/
---

## **Visão Geral**

Existem 3 maneiras de aplicar filtros inteligentes no Aspose.PSD para Python.

## **Aplicação Direta do Filtro**

Neste exemplo de código, podemos ver um exemplo de como aplicar filtros inteligentes diretamente no Aspose.PSD para Python.

Primeiramente, o código especifica o arquivo PSD de origem, o arquivo de saída para a imagem original e o arquivo de saída para a imagem atualizada.

Em seguida, o código carrega a imagem PSD usando o método Image.load() e a converte em um objeto PsdImage.

A imagem original é então salva usando o método save(), com o nome do arquivo de saída especificado.

Um objeto SharpenSmartFilter é criado, o qual representa o filtro inteligente a ser aplicado.

O código então recupera a camada regular da imagem PSD usando im.layers[1].

Um loop é então utilizado para aplicar o sharpenFilter à camada regular três vezes.

Por fim, a imagem atualizada é salva usando o método save() e o nome do arquivo de saída especificado.

Este código demonstra como aplicar filtros inteligentes diretamente no Aspose.PSD para Python. Ao utilizar os objetos de filtro apropriados e aplicá-los às camadas desejadas, você pode alcançar os efeitos desejados em suas imagens.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentação-Python-Aspose-psd-smart-filter-direct-apply.py" >}}

## **Manipulação de Filtros Inteligentes nos Objetos Inteligentes**

Primeiramente, o código especifica o arquivo PSD de origem, o arquivo de saída para a imagem original e o arquivo de saída para a imagem atualizada.

A imagem PSD é carregada usando o método Image.load() e então convertida em um objeto PsdImage.

A imagem original é salva usando o método save(), com o nome do arquivo de saída especificado.

O código então converte a segunda camada da imagem PSD em um objeto SmartObjectLayer, representando a camada de objeto inteligente.

O código então procede para editar os filtros inteligentes. Neste exemplo, ele demonstra como trabalhar com dois tipos de filtros inteligentes: GaussianBlurSmartFilter e AddNoiseSmartFilter.

Para o GaussianBlurSmartFilter, o código atualiza os valores do filtro, incluindo o raio, modo de mesclagem, opacidade e se está habilitado ou não.

Para o AddNoiseSmartFilter, o código define a distribuição de ruído como NoiseDistribution.UNIFORM.

Em seguida, o código adiciona dois novos itens de filtro à camada de objeto inteligente: outro GaussianBlurSmartFilter e um AddNoiseSmartFilter.

Após adicionar os novos filtros, o código aplica as alterações usando o método update_resource_values().

Por fim, o código demonstra como aplicar diretamente os filtros à camada e à máscara da camada usando os métodos apply() e apply_to_mask(), respectivamente.

A imagem atualizada é então salva usando o método save() e o nome do arquivo de saída especificado.

Ao seguir este exemplo de código, você pode aprender como trabalhar com filtros inteligentes no Aspose.PSD para Python. A biblioteca fornece uma ampla gama de filtros inteligentes, cada um com seu próprio conjunto de propriedades e métodos que podem ser personalizados para alcançar os efeitos desejados em suas imagens.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentação-Python-Aspose-psd-smart-filter-features.py" >}}

## **Aplicando Filtros Inteligentes à Máscara de Camada**

Aplicando Filtros Inteligentes em Máscaras: Uma Técnica Poderosa de Edição de Imagens

Filtros inteligentes são um recurso popular em software de edição de imagens que permitem aos usuários aplicar vários filtros e efeitos em suas imagens. Uma técnica interessante que pode ser alcançada usando filtros inteligentes é aplicá-los em máscaras. Neste artigo, exploraremos como aplicar filtros inteligentes em máscaras e discutiremos seu uso no mundo da edição de imagens.

O que é uma Máscara? Antes de mergulharmos na aplicação de filtros inteligentes em máscaras, primeiro vamos entender o que é uma máscara. Na edição de imagens, uma máscara é uma imagem em tons de cinza que determina a transparência de certas áreas de uma imagem. Uma máscara pode ser usada para aplicar seletivamente filtros, ajustes ou efeitos em partes específicas de uma imagem, enquanto deixa outras áreas inalteradas.

Aplicando Filtros Inteligentes em Máscaras: Ao aplicar filtros inteligentes em máscaras, os filtros são aplicados apenas às áreas especificadas pela máscara. Isso permite um controle preciso sobre quais partes da imagem são afetadas pelo filtro. Ao manipular a máscara, você pode determinar a intensidade e extensão do efeito do filtro.

Por favor, consulte o exemplo anterior e o método: [Referência da API Aplicando Filtro Inteligente na Máscara](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)
