---
title: Exemplo de uso de camadas de grupo em Aspose.PSD para Java
weight: 100
type: docs
description: Uso de Camada de Grupo de Arquivo PSD via Java
keywords: [camada de grupo, camada de grupo, adicionar camada ao grupo, api psd, java, exemplo de código]
url: pt/java/psd-group-layer/
---

## **Visão Geral**

A utilização de camadas de grupo em Aspose.PSD para Java aprimora sua capacidade de gerenciar e organizar camadas dentro de uma imagem PSD de forma eficaz. As camadas de grupo, também conhecidas como camadas de pasta, permitem que você consolide múltiplas camadas e aplique transformações ou efeitos coletivamente.

Para começar, crie uma nova imagem PSD utilizando o método PsdImage.create(). Em seguida, inicialize um novo objeto LayerGroup através do método addLayerGroup do objeto PsdImage. Forneça o nome desejado para a camada de grupo ("Pasta"), especifique o índice de inserção (0) e defina um sinalizador booleano indicando sua visibilidade (Verdadeiro).

Posteriormente, crie dois objetos Layer e defina seus nomes de exibição utilizando o método setDisplayName. Adicione essas camadas à camada de grupo usando o método addLayer.

Para acessar as camadas dentro do grupo, utilize a propriedade layers do objeto LayerGroup. Confirme que os nomes de exibição da primeira e segunda camadas no grupo são "Camada 1" e "Camada 2", respectivamente.

Após manipular as camadas de grupo, salve a imagem PSD modificada utilizando o método save do objeto PsdImage.

Este exemplo fundamental serve para ajudá-lo a se familiarizar com o trabalho com camadas de grupo usando Aspose.PSD para Java. A biblioteca oferece uma infinidade de recursos avançados para manipulação de camadas e transformações dentro de imagens PSD. Para mais detalhes e exemplos sobre como aproveitar as camadas de grupo e outras funcionalidades da biblioteca, consulte a documentação do Aspose.PSD para Java.

Para trabalhar com camadas de grupo em Aspose.PSD para Java, utilize a classe LayerGroup. Abaixo está um trecho de código ilustrando como criar uma camada de grupo, adicionar camadas a ela e salvar a imagem PSD modificada.

Consulte o exemplo completo fornecido.

## **Exemplo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-psd-group-layer.java" >}}
