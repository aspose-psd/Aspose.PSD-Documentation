---
title: Modificar Imagens
type: docs
weight: 50
url: /pt/java/modificando-imagens/
---

## **Difusão para Imagens de Raster**
A difusão é uma técnica de criar a ilusão de novas cores e tons variando o padrão de pontos que realmente criam uma imagem. É o meio mais comum de reduzir a gama de cores das imagens para 256 (ou menos) cores. O Aspose.PSD oferece suporte à difusão para a classe RasterImage, introduzindo o método Dither que aceita dois parâmetros. O primeiro é do tipo DitheringMethod a ser aplicado com duas opções possíveis: FloydSteinbergDithering e ThresholdDithering. O segundo parâmetro para o método Dither é o BitCount como inteiro. BitCount define o tamanho da amostragem para o resultado de difusão. O valor padrão é 1, que representa preto e branco, enquanto os valores permitidos são 1, 4, 8, gerando paletas com 2, 4 e 256 cores, respectivamente.

## **Ajustando Brilho, Contraste e Gama**
Os ajustes de cores em imagens digitais são um dos recursos principais que a maioria das bibliotecas de processamento de imagens fornece. Os ajustes de cores podem ser categorizados da seguinte forma.

1. Brilho refere-se à claridade ou escuridão da cor. Aumentar o brilho de uma imagem ilumina todas as cores, enquanto diminuir o brilho escurece todas as cores.
1. Contraste refere-se a tornar os objetos ou detalhes dentro de uma imagem mais óbvios. Aumentar o contraste de uma imagem aumenta a diferença entre áreas claras e escuras, de modo que as áreas claras se tornam mais claras e as áreas escuras se tornam mais escuras. Diminuir o contraste fará com que as áreas mais claras e mais escuras permaneçam aproximadamente iguais, mas a imagem como um todo se torna mais homogênea.
1. Gama otimiza o contraste e o brilho das luzes indiretas que iluminam um objeto na imagem.
### **Ajustando Brilho**
O Aspose.PSD fornece o método AdjustBrightness para a classe RasterImage que pode ser usado para ajustar o brilho da imagem passando um valor inteiro como parâmetro. O maior valor do parâmetro denota uma imagem mais clara. Aqui está a imagem original e a imagem resultante para comparação.

### **Ajustando Contraste**
O método AdjustContrast exposto pela classe RasterImage pode ser usado para ajustar o Contraste de uma imagem passando um valor float como parâmetro.

O maior valor do parâmetro denota um maior contraste na imagem fornecida. Aqui está a imagem original e a imagem resultante para comparação.

### **Ajustando Gama**
O método AdjustGamma exposto pela classe RasterImage tem duas versões. Uma das sobrecargas aceita um valor float e realiza a correção gama para os coeficientes dos canais vermelho, azul e verde. Enquanto a outra sobrecarga aceita três parâmetros float representando cada coeficiente de cor separadamente. O exemplo de código a seguir demonstra como ajustar o Gama em uma imagem.

## **Desfocar uma Imagem**
Este artigo demonstra o uso do Aspose.PSD para Java para realizar um efeito de desfoque em uma imagem. As APIs do Aspose.PSD expuseram métodos eficientes e fáceis de usar para alcançar esse objetivo. O Aspose.PSD para Java expôs a classe GaussianBlurFilterOptions para criar um efeito de desfoque on-the-fly. A classe GaussianBlurFilterOptions precisa de valores de raio e sigma para criar um efeito de desfoque em uma imagem. Os passos para realizar o redimensionamento são simples como abaixo:

1. Carregar uma imagem usando o método de fábrica Load exposto pela classe Image.
1. Converter a imagem em RasterImage.
1. Criar uma instância da classe GaussianBlurFilterOptions com construtor padrão ou fornecer valores de raio e sigma no construtor.
1. Chamar o método RasterImage.Filter especificando um retângulo como limites da imagem e uma instância da classe GaussianBlurFilterOptions.
1. Salvar os resultados.

O exemplo de código a seguir demonstra como criar um efeito de desfoque em uma imagem.

## **Verificar Transparência da Imagem**
Este artigo demonstra o uso do Aspose.PSD para Java para verificar a transparência da imagem. Os passos para verificar a transparência da imagem são simples como abaixo:

1. Carregar uma imagem usando o método de fábrica Load exposto pela classe Image.
1. Verificar a opacidade da imagem. Se a opacidade for zero, a imagem é transparente.
1. O exemplo de código a seguir demonstra como verificar se a imagem é transparente ou não.

## **Implementar Compressor de GIF Lossy**
Usando o Aspose.PSD para Java, os desenvolvedores podem definir a diferença de pixels. A compressão do GIF é baseada em um "dicionário" de strings de pixels vistos. O codificador normal procura no dicionário a string mais longa de pixels que corresponde exatamente aos pixels na imagem. O codificador lossy escolhe a string mais longa de pixels que é "suficientemente similar" aos pixels na imagem. Abaixo está a demonstração de código da referida funcionalidade.

## **Implementar Redimensionamento Bicúbico**
O redimensionamento significa que você está mudando as dimensões de pixels de uma imagem. Quando você redimensiona para baixo, você está eliminando pixels e, portanto, excluindo informações e detalhes de sua imagem. Quando você redimensiona para cima, você está adicionando pixels. O Photoshop adiciona esses pixels usando interpolação. Este artigo demonstra como você pode realizar o Redimensionamento Bicúbico usando o Aspose.PSD para Java.

Abaixo está a demonstração de código da referida funcionalidade.

## **Camada de Ajuste de Inversão**
Este artigo demonstra como você pode realizar a camada de ajuste de Inversão usando o Aspose.PSD para Java. Uma camada de ajuste é um tipo especial de camada usado principalmente para correção de cores. Em vez de ter um conteúdo próprio, eles ajustam as informações nas camadas abaixo delas. A camada de ajuste de Inversão faz um efeito de negativo da foto invertendo as cores de uma imagem.

Abaixo está a demonstração de código da referida funcionalidade.
