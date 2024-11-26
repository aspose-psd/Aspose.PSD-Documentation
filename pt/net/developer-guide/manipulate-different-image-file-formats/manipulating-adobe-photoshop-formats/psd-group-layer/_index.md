---
title: Exemplo de uso de camadas de grupo em Aspose.PSD para C#
weight: 100
type: docs
description: Utilização do grupo de camadas do arquivo PSD via C#
keywords: [camada de grupo, camada de grupo, adicionar camada a grupo, api psd, C#, csharp, exemplo de código]
url: pt/net/psd-group-layer/
---

## Visão geral

As camadas de grupo em Aspose.PSD para C# permitem a organização eficiente e manipulação das camadas em um arquivo PSD. Ao usar camadas de pasta, é possível agrupar várias camadas juntas e aplicar transformações ou efeitos a todo o grupo.

Este exemplo demonstra a criação de uma nova imagem PSD com `PsdImage.Create`. Em seguida, um novo objeto `LayerGroup` é criado usando o `AddLayerGroup` do objeto `PsdImage`. A camada do grupo é nomeada como "Pasta", inserida no índice 0 e definida como visível.

Em seguida, dois objetos `Layer` são criados com suas propriedades `DisplayName` definidas. Essas camadas são adicionadas ao grupo de camadas usando `AddLayer`.

As camadas dentro do grupo podem ser acessadas por meio da propriedade `Layers` do objeto `LayerGroup`. O exemplo afirma que os nomes de exibição das primeiras e segundas camadas no grupo são "Camada 1" e "Camada 2".

Após modificar as camadas do grupo, a imagem PSD atualizada é salva com o método `Save` do objeto `PsdImage`.

Este exemplo básico apresenta o trabalho com camadas de grupo usando Aspose.PSD para C#. A biblioteca oferece recursos avançados para manipular e transformar camadas em arquivos PSD. Consulte a documentação do Aspose.PSD para C# para obter exemplos e recursos mais detalhados.

Aqui está um código de exemplo demonstrando o uso de camadas de grupo em Aspose.PSD para C#:

## Exemplo

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

Para obter informações e exemplos mais detalhados, visite a [documentação do Aspose.PSD para C#](https://docs.aspose.com/psd/net/).

