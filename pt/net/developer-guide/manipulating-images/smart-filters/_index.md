---
title: Manipulação de Filtro Inteligente em Aspose.PSD para C#
weight: 100
type: docs
description: Exemplos de como usar Filtros Inteligentes em Arquivo PSD
keywords: [filtro inteligente, adicionar ruído, borrão gaussiano, nitidez, filtro, filtro psd, api psd, C#, csharp, exemplo de código]
url: pt/net/filtros-inteligentes/
---

## Visão Geral

Existem três maneiras de aplicar filtros inteligentes no Aspose.PSD para C#.

### Aplicação Direta de Filtro

Este exemplo demonstra como aplicar diretamente filtros inteligentes no Aspose.PSD para C#.

Primeiro, especifique o arquivo PSD de origem, o arquivo de saída para a imagem original e o arquivo de saída para a imagem atualizada.

Em seguida, carregue a imagem PSD usando o método `Image.Load` e converta-a para um objeto `PsdImage`.

Salve a imagem original usando o método `Save` com o nome do arquivo de saída especificado.

Crie um objeto `SharpenSmartFilter`, representando o filtro inteligente a ser aplicado.

Recupere a camada regular da imagem PSD usando `psdImage.Layers[1]`.

Aplique o `sharpenFilter` à camada regular três vezes em um loop.

Por fim, salve a imagem atualizada usando o método `Save` com o nome do arquivo de saída especificado.

Este código demonstra como aplicar filtros inteligentes diretamente no Aspose.PSD para C#. Ao usar os objetos de filtro apropriados e aplicá-los nas camadas desejadas, você pode alcançar os efeitos desejados em suas imagens.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "AplicarFiltroInteligenteDiretamente-AplicarFiltroInteligenteDiretamente.cs" >}}

### Manipulando Filtros Inteligentes em Objetos Inteligentes

Este exemplo mostra como manipular filtros inteligentes dentro de objetos inteligentes.

Primeiro, especifique o arquivo PSD de origem, o arquivo de saída para a imagem original e o arquivo de saída para a imagem atualizada.

Carregue a imagem PSD usando o método `Image.Load` e converta-a para um objeto `PsdImage`.

Salve a imagem original usando o método `Save` com o nome do arquivo de saída especificado.

Converta a segunda camada da imagem PSD para um objeto `SmartObjectLayer`.

Edite os filtros inteligentes. Este exemplo demonstra como trabalhar com `GaussianBlurSmartFilter` e `AddNoiseSmartFilter`.

Para `GaussianBlurSmartFilter`, atualize os valores do filtro, incluindo raio, modo de mistura, opacidade e estado habilitado.

Para `AddNoiseSmartFilter`, defina a distribuição de ruído para `NoiseDistribution.UNIFORM`.

Adicione novos itens de filtro à camada do objeto inteligente: outro `GaussianBlurSmartFilter` e `AddNoiseSmartFilter`.

Aplique as alterações usando o método `UpdateResourceValues`.

Aplique os filtros diretamente na camada e na máscara da camada usando os métodos `Apply` e `ApplyToMask`, respectivamente.

Salve a imagem atualizada usando o método `Save` com o nome do arquivo de saída especificado.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipularFiltrosInteligentesEmObjetosInteligentes-ManipularFiltrosInteligentesEmObjetosInteligentes.cs" >}}

### Aplicando Filtros Inteligentes na Máscara da Camada

Filtros inteligentes são uma poderosa ferramenta de edição de imagem que permite aos usuários aplicar vários filtros e efeitos. Uma técnica interessante é aplicá-los em máscaras, o que pode controlar precisamente as áreas afetadas pelo filtro.

Uma máscara é uma imagem em tons de cinza que determina a transparência de certas áreas da imagem, aplicando seletivamente filtros, ajustes ou efeitos.

Ao aplicar filtros inteligentes em máscaras, os filtros são aplicados apenas às áreas especificadas pela máscara. Esse controle preciso permite a manipulação da intensidade e extensão do filtro.

Para obter informações mais detalhadas e exemplos, consulte a [documentação do Aspose.PSD para C#](https://docs.aspose.com/psd/net/).
