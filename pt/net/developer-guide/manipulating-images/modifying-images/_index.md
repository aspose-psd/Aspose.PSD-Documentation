---
title: Modificando Imagens
type: docs
weight: 50
url: /pt/net/modifying-images/
---

## **Dithering para Imagens de Raster**
O Dithering é uma técnica de criar a ilusão de novas cores e tons variando o padrão de pontos que realmente criam uma imagem. É o meio mais comum de reduzir a gama de cores das imagens para 256 (ou menos) cores. Aspose.PSD fornece o suporte de dithering para a classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) ao introduzir o método Dither que aceita dois parâmetros. O primeiro é do tipo DitheringMethod a ser aplicado com duas opções possíveis: FloydSteinbergDithering e ThresholdDithering. O segundo parâmetro para o método [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) é o BitCount em inteiro. O BitCount define o tamanho da amostragem para o resultado de dithering. O valor padrão é 1, que representa preto e branco, enquanto os valores permitidos são 1, 4, 8, gerando paletas com 2, 4 e 256 cores, respectivamente.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.cs" >}}

## **Ajustando Brilho, Contraste e Gama**
Os ajustes de cor em imagens digitais são uma das principais características fornecidas pela maioria das bibliotecas de processamento de imagens. Os ajustes de cor podem ser categorizados da seguinte forma.

1. Brilho refere-se à luminosidade ou escuridão de uma cor. Aumentar o brilho de uma imagem clareia todas as cores, enquanto diminuir o brilho escurece todas as cores.
1. Contraste refere-se a tornar os objetos ou detalhes dentro de uma imagem mais óbvios. Aumentar o contraste de uma imagem aumenta a diferença entre áreas claras e escuras, para que as áreas claras se tornem mais claras e as áreas escuras se tornem mais escuras. Diminuir o contraste fará com que áreas mais claras e mais escuras permaneçam aproximadamente iguais, mas a imagem como um todo se torna mais homogênea.
1. Gama otimiza o contraste e o brilho da iluminação indireta que está iluminando um objeto na imagem.
### **Ajustando Brilho**
A API Aspose.PSD for .NET fornece o método [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) para a classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) que pode ser usada para ajustar o brilho da imagem ao passar um valor inteiro como parâmetro. O maior valor de parâmetro denota uma imagem mais brilhante. Aqui está a imagem original e a imagem resultante para comparação.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.cs" >}}

### **Ajustando Contraste**
O método [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) exposto pela classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) pode ser usado para ajustar o contraste de uma imagem passando um valor flutuante como parâmetro.

O maior valor de parâmetro denota um contraste mais alto na imagem fornecida. Aqui está a imagem original e a imagem resultante para comparação.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.cs" >}}

### **Ajustando Gama**
O método [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) exposto pela classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) tem duas versões. Uma das sobrecargas aceita um valor flutuante e realiza a correção gama para os coeficientes do canal vermelho, azul e verde. Enquanto a outra sobrecarga aceita três parâmetros flutuantes representando cada coeficiente de cor separadamente. O exemplo de código a seguir demonstra como Ajustar Gama em uma imagem.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.cs" >}}

## **Desfocar uma Imagem**
Este artigo demonstra o uso do Aspose.PSD for .NET para realizar um efeito de Desfoque em uma imagem. As APIs do Aspose.PSD expuseram métodos eficientes e fáceis de usar para alcançar esse objetivo. O Aspose.PSD for .NET expôs a classe [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) para criar um efeito de desfoque em tempo real. A classe [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) precisa de valores de raio e sigma para criar um efeito de desfoque em uma imagem. Os passos para realizar o redimensionamento são simples, conforme abaixo:

1. Carregar uma imagem usando o método de fábrica Load exposto pela classe Image.
1. Converter a imagem em [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. Criar uma instância da classe [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) com o construtor padrão ou fornecer os valores de raio e sigma no construtor.
1. Chamar o método [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter enquanto especifica o retângulo como limites da imagem e a instância da classe [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions).
1. Salvar os resultados.

O exemplo de código a seguir demonstra como criar um efeito de desfoque em uma imagem.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-BluranImage-BluranImage.cs" >}}

## **Verificar Transparência da Imagem**
Este artigo demonstra o uso do Aspose.PSD for .NET para verificar a transparência da imagem. Os passos para verificar a transparência da imagem são tão simples quanto abaixo:

1. Carregar uma imagem usando o método de fábrica [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) exposto pela classe [Image](https://reference.aspose.com/psd/net/aspose.psd/image).
1. Verificar a opacidade da imagem - se a opacidade for zero, a imagem é transparente.
1. O exemplo de código a seguir demonstra como verificar se a imagem é transparente ou não.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.cs" >}}

## **Implementar Compressor GIF Lossy**
Usando o Aspose.PSD for .NET, os desenvolvedores podem definir uma diferença de pixel. A compressão do GIF baseia-se em um "dicionário" de strings de pixels vistos. O codificador normal procura no dicionário a string mais longa de pixels que corresponda exatamente aos pixels na imagem. O codificador lossy escolhe a string mais longa de pixels que é "suficientemente semelhante" aos pixels na imagem. Abaixo está a demonstração de código da funcionalidade mencionada.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.cs" >}}

## **Implementar Redimensionamento Bicúbico**
Redimensionar significa que você está alterando as dimensões de pixel de uma imagem. Ao reduzir a escala, você está eliminando pixels e, portanto, deletando informações e detalhes da sua imagem. Ao aumentar a escala, você está adicionando pixels. O Photoshop adiciona esses pixels usando interpolação. Este artigo demonstra como você pode realizar o Redimensionamento Bicúbico usando o Aspose.PSD for .NET.

Abaixo está a demonstração de código da funcionalidade mencionada.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.cs" >}}

## **Camada de Ajuste de Balanço de Cor**
Este artigo demonstra o uso do Aspose.PSD for .NET para realizar a **camada de ajuste de balanço de cor** em uma imagem. A camada de ajuste de balanço de cor dá a você a capacidade de fazer ajustes na coloração de suas imagens. Ele apresenta os três canais de cor e suas cores complementares e você pode ajustar o equilíbrio desses pares para alterar a aparência de uma foto.

Abaixo está a demonstração de código da funcionalidade mencionada.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ColorBalanceAdjustment-ColorBalanceAdjustment.cs" >}}

## **Camada de Ajuste de Inversão**
Este artigo demonstra como você pode realizar a **camada de ajuste de inversão** usando o Aspose.PSD for .NET. Uma camada de ajuste é um tipo especial de camada usado principalmente para correção de cor. Em vez de ter um conteúdo próprio, elas ajustam as informações nas camadas abaixo delas. A camada de ajuste de inversão faz um efeito de negativo de uma foto invertendo as cores de uma imagem.

Abaixo está a demonstração de código da funcionalidade mencionada.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.cs" >}}
