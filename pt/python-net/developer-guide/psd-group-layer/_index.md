---
title: Exemplo de uso de camadas de grupo em Aspose.PSD para Python
weight: 100
type: docs
description: Uso de Camada de Grupo de Arquivo PSD via Python
keywords: [grupo de camadas, camada de grupo, adicionar camada a grupo, api psd, python, exemplo de código]
url: pt/python-net/psd-group-layer/
---

## **Visão Geral**

Trabalhar com camadas de grupo em Aspose.PSD para Python é um recurso poderoso que permite organizar e manipular camadas dentro de uma imagem PSD. Camadas de grupo, também conhecidas como camadas de pasta, fornecem uma maneira de agrupar várias camadas juntas e aplicar transformações ou efeitos a todo o grupo.

Neste exemplo, primeiro criamos uma nova imagem PSD usando o método PsdImage.create. Em seguida, criamos um novo objeto LayerGroup usando o método add_layer_group do objeto PsdImage. Fornecemos o nome da camada do grupo ("Pasta"), o índice no qual deve ser inserido (0) e um sinalizador booleano indicando se a camada do grupo deve ser visível (True).

Em seguida, criamos dois objetos Layer e definimos seus nomes de exibição usando a propriedade display_name. Adicionamos essas camadas ao grupo usando o método add_layer.

Finalmente, podemos acessar as camadas dentro do grupo usando a propriedade layers do objeto LayerGroup. No exemplo, afirmamos que os nomes de exibição das primeira e segunda camadas no grupo são "Camada 1" e "Camada 2" respectivamente.

Após manipular as camadas de grupo, podemos salvar a imagem PSD modificada usando o método save do objeto PsdImage.

Este é apenas um exemplo básico para você começar a trabalhar com camadas de grupo usando Aspose.PSD para Python. A biblioteca oferece muitos recursos mais avançados para manipulação e transformação de camadas em imagens PSD. Você pode consultar a documentação do Aspose.PSD para Python para obter mais detalhes e exemplos sobre o trabalho com camadas de grupo e outros recursos da biblioteca.

Para trabalhar com camadas de grupo em Aspose.PSD para Python, você pode usar a classe LayerGroup. Aqui está um trecho de código de exemplo que demonstra como criar uma camada de grupo, adicionar camadas a ela e salvar a imagem PSD modificada.

Por favor, verifique o exemplo completo.

## **Exemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-group-layer.py" >}}
