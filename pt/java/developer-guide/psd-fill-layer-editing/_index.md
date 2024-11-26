---
title: Atualização da Camada de Preenchimento PSD usando Java
weight: 100
type: docs
description: Exemplos de uso de todos os tipos de camadas de ajuste, incluindo Color Fill, Gradient Fill e Pattern Fill
keywords: [camada de preenchimento, Color Fill, Gradient Fill, Pattern Fill, api psd, java, exemplo de código]
url: pt/java/psd-fill-layer-editing/
---

## **Visão Geral**

A criação de uma camada regular envolve o uso da função createRegularLayer, que requer parâmetros para definir a posição e o tamanho da camada. Essa função cria uma nova camada, define seus limites e preenche com uma cor especificada.

Para uma camada de preenchimento de cor, você utiliza o método FillLayer.createInstance com o parâmetro FillType.Color. Uma vez que a camada de preenchimento é criada, acesse suas configurações de preenchimento através da propriedade fill_settings e defina a cor desejada usando a propriedade color da classe ColorFillSettings. Neste contexto, a cor é definida com Color.getCoral(). Adicionalmente, a propriedade clipping da camada de preenchimento é definida como 1, fazendo com que ela funcione como uma máscara de recorte.

As camadas de preenchimento gradiente são criadas de forma semelhante usando o método FillLayer.create_instance, mas com o parâmetro FillType.Gradient. Assim como as camadas de preenchimento de cor, você acessa as configurações de preenchimento por meio de fill_settings e define os pontos de cor do gradiente e os pontos de transparência. Neste exemplo, os pontos de cor do gradiente são definidos com a classe GradientColorPoint, e os pontos de transparência com a classe GradientTransparencyPoint. A propriedade clipping da camada de preenchimento também é definida como 1.

As camadas de preenchimento de padrão são criadas usando FillLayer.createInstance com o parâmetro FillType.Pattern. Novamente, acesse as configurações de preenchimento através de fill_settings e defina os dados do padrão e outras propriedades. Neste código, os dados do padrão são definidos usando a classe PatternFillSettings, e a propriedade clipping é definida como 1.

Uma vez que as camadas de preenchimento são criadas, adicione-as à imagem PSD usando o método addLayer, especificando o nome a ser exibido e outras propriedades para cada camada de preenchimento.

Por fim, salve a imagem PSD e sua imagem PNG correspondente com o código fornecido. As opções PNG estão configuradas para usar true color com alpha para transparência.

Por favor, consulte o exemplo completo para mais detalhes.

## **Exemplo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-psd-fill-layer-editing.java" >}}
