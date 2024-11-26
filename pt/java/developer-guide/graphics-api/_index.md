---
title: Utilizando a API de Gráficos para editar Camadas em arquivos PSD
weight: 100
type: docs
description: Exemplo de uso da API de Gráficos no Aspose.PSD para Java
keywords: [atualizar camada, desenhar círculo, desenhar elipse, desenhar círculo preenchido, gráficos, api psd, java, exemplo de código]
url: pt/java/graphics-api/
---

## **Visão Geral**
Para começar, carregue o arquivo PSD usando o método Image.load() ou crie uma imagem Psd do zero. Use a variável inputFile para representar o caminho do seu arquivo PSD e especifique quaisquer opções de carregamento com loadOpt, se necessário.

Em seguida, acesse a primeira camada da imagem PSD usando a sintaxe psdImage.getLayers()[0] para obter uma referência ao objeto da camada para manipulação.

Para editar a camada, crie um objeto Graphics passando a camada como parâmetro. Esse objeto fornece vários métodos para desenhar formas e aplicar pincéis.

Um objeto Pen é usado para definir a cor e a espessura do contorno das formas. Da mesma forma, pincéis como LinearGradientBrush são usados para definir as cores de preenchimento.

Desenhe formas na camada usando métodos como graphics.drawEllipse() para delinear formas e graphics.fillEllipse() para preenchê-las.

Após fazer as alterações desejadas na camada, salve a imagem PSD modificada usando psdImage.save().

Além disso, você pode salvar a imagem modificada em outros formatos como PNG usando as opções apropriadas.

É isso! Você usou com sucesso a API de Gráficos do Aspose.PSD para Java para editar camadas em um arquivo PSD. Explore mais recursos e funcionalidades da biblioteca Aspose.PSD para aprimorar suas capacidades de edição de imagens.

Por favor, confira o exemplo completo.

## **Exemplo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-graphics-api.java" >}}
