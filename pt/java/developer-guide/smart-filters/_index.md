---
title: Manipulação de Filtros Inteligentes no Aspose.PSD for Java
weight: 100
type: docs
description: Exemplos de como usar Filtros Inteligentes no Arquivo PSD
keywords: [filtro inteligente, adicionar ruído, desfoque gaussiano, afiar, filtro, filtro psd, api psd, java, exemplo de código]
url: pt/java/filtros-inteligentes/
---

## **Visão Geral**

Existem 3 métodos para aplicar filtros inteligentes no Aspose.PSD for Java.

## **Aplicação Direta de Filtros**

Este exemplo de código demonstra como aplicar filtros inteligentes diretamente no Aspose.PSD for Java.

Inicialmente, o código define o arquivo PSD de origem, o arquivo de saída para a imagem original e o arquivo de saída para a imagem atualizada.

Em seguida, o código carrega a imagem PSD usando o método Image.load() e converte-a em um objeto PsdImage.

A imagem original é salva usando o método save(), especificando o nome do arquivo de saída.

É instanciado um objeto SharpenSmartFilter para representar o filtro inteligente desejado.

Depois, o código obtém a camada regular da imagem PSD usando psdImage.getLayers()[1].

Um loop é utilizado para aplicar o sharpenFilter à camada regular três vezes.

Por fim, a imagem atualizada é salva usando o método save() com o nome do arquivo de saída fornecido.

Este código exemplifica a aplicação direta de filtros inteligentes no Aspose.PSD para Java. Ao utilizar objetos de filtro apropriados e aplicá-los a camadas desejadas, efeitos desejados podem ser alcançados nas imagens.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-direct-apply.java" >}}

## **Manipulação de Filtros Inteligentes nos Objetos Inteligentes**

Este trecho de código descreve como manipular filtros inteligentes dentro de objetos inteligentes no Aspose.PSD for Java.

Inicialmente, o código define o arquivo PSD de origem, o arquivo de saída para a imagem original e o arquivo de saída para a imagem atualizada.

A imagem PSD é carregada usando o método Image.load() e então convertida em um objeto PsdImage.

A imagem original é salva usando o método save(), especificando o nome do arquivo de saída.

Em seguida, o código converte a segunda camada da imagem PSD em um objeto SmartObjectLayer, representando a camada de objeto inteligente.

Posteriormente, o código demonstra a edição de filtros inteligentes, exibindo dois tipos: GaussianBlurSmartFilter e AddNoiseSmartFilter.

Para o GaussianBlurSmartFilter, o código atualiza valores do filtro, como raio, modo de mesclagem, opacidade e status de ativação.

Para o AddNoiseSmartFilter, o código define a distribuição de ruído como NoiseDistribution.Uniform.

Depois, o código adiciona dois novos itens de filtro à camada de objeto inteligente: outro GaussianBlurSmartFilter e um AddNoiseSmartFilter.

Após a adição de novos filtros, o código aplica as alterações usando o método updateResourceValues().

Por fim, o código demonstra aplicar filtros diretamente à camada e à sua máscara usando os métodos apply() e applyToMask(), respectivamente.

A imagem atualizada é então salva usando o método save() com o nome do arquivo de saída fornecido.

Seguindo este exemplo de código, você pode entender como manipular filtros inteligentes dentro de objetos inteligentes no Aspose.PSD for Java. A biblioteca oferece uma ampla gama de filtros inteligentes, cada um com seu próprio conjunto de propriedades e métodos que podem ser personalizados para alcançar efeitos desejados nas imagens.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-features.java" >}}

## **Aplicação de Filtros Inteligentes na Máscara de Camada**

Aplicação de Filtros Inteligentes em Máscaras: Uma Técnica Potente de Edição de Imagens

Filtros inteligentes, comuns em softwares de edição de imagem, permitem aos usuários aplicar diversos filtros e efeitos em suas imagens. Uma técnica intrigante habilitada pelos filtros inteligentes é sua aplicação em máscaras. Este artigo explora a aplicação de filtros inteligentes em máscaras e discute sua utilidade no campo da edição de imagens.

Compreendendo Máscaras: Antes de adentrar na aplicação de filtros inteligentes em máscaras, é crucial compreender o conceito de uma máscara. Na edição de imagens, uma máscara é uma imagem em escala de cinza que dita a transparência de áreas específicas dentro de uma imagem. Máscaras possibilitam a aplicação seletiva de filtros, ajustes ou efeitos a partes específicas de uma imagem, deixando outras áreas sem alterações.

Aplicando Filtros Inteligentes em Máscaras: Quando filtros inteligentes são aplicados em máscaras, eles afetam apenas as áreas especificadas pela máscara, oferecendo controle preciso sobre o impacto do filtro. Ao manipular a máscara, os usuários podem modular a intensidade e a extensão do efeito do filtro.

Por favor, consulte o exemplo anterior e o método: [Referência da API Aplicar Filtro Inteligente à Máscara](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)
