---
title: Aplicando Filtros de Mediana e Wiener
type: docs
weight: 10
url: /pt/aplicando-filtros-de-mediana-e-wiener/
---

## **Aplicando Filtros de Mediana e Wiener**
O filtro de mediana é uma técnica de filtragem digital não-linear, frequentemente utilizada para remover ruído. Essa redução de ruído é uma etapa de pré-processamento típica para melhorar os resultados de processamentos posteriores. O filtro de Wiener é o filtro linear estacionário ótimo de erro médio quadrático (MSE) para imagens degradadas por ruído aditivo e desfoque. Usando o Aspose.PSD para desenvolvedores de API .NET, é possível aplicar um filtro de mediana para desentranhar a imagem e aplicar um filtro gaussiano Wiener nas imagens. Este artigo demonstra como o filtro de mediana e o filtro gaussiano Wiener podem ser aplicados em imagens.
### **Aplicando Filtro de Mediana**
O Aspose.PSD fornece a classe [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) para aplicar um filtro em um [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). O trecho de código abaixo demonstra como aplicar o filtro de mediana a uma imagem rasterizada.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversao-AplicarFiltrosMedianaWiener-AplicarFiltrosMedianaWiener.cs" >}}


### **Aplicando Filtro Gaussiano Wiener**
O Aspose.PSD fornece a classe [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) para aplicar um filtro em um [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). O trecho de código abaixo demonstra como aplicar o filtro gaussiano Wiener a uma imagem rasterizada.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversao-AplicarFiltrosGaussWiener-AplicarFiltrosGaussWiener.cs" >}}


### **Aplicando Filtro Gaussiano Wiener para Imagem Colorida**
O Aspose.PSD fornece [GaussWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) para imagens coloridas também. O trecho de código abaixo demonstra como aplicar o filtro gaussiano Wiener a uma imagem colorida.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversao-AplicarFiltrosGaussWienerParaImagemColorida-AplicarFiltrosGaussWienerParaImagemColorida.cs" >}}


### **Aplicando Filtro Wiener de Movimento**
O Aspose.PSD fornece a classe [MotionWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) para aplicar um filtro em um [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). O trecho de código abaixo demonstra como aplicar um filtro Wiener de movimento a uma imagem rasterizada.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversao-AplicarFiltrosWienerMovimento-AplicarFiltrosWienerMovimento.cs" >}}


## **Aplicar Filtro de Correção em uma Imagem**
Este artigo demonstra o uso do Aspose.PSD para .NET para realizar filtros de correção em uma imagem. As APIs do Aspose.PSD expõem métodos eficientes e fáceis de usar para atingir esse objetivo. Aspose.PSD for .NET expôs as classes [BilateralSmoothingFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions) e [SharpenFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) para a filtragem. A classe BilateralSmoothingFilterOptions requer um número inteiro como tamanho. Os passos para realizar o redimensionamento são tão simples quanto abaixo:

1. Carregar uma imagem usando o método de fábrica Load exposto pela classe Image.
1. Converter a imagem em RasterImage.
1. Criar uma instância das classes BilateralSmoothingFilterOptions e SharpenFilterOptions.
1. Chamar o método [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) especificando o retângulo como limites da imagem e a instância da classe BilateralSmoothingFilterOptions.
1. Chamar o método [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) especificando o retângulo como limites da imagem e a instância da classe SharpenFilterOptions.
1. Ajustar o contraste.
1. Definir o brilho.
1. Salvar os resultados.


## **Usar o algoritmo de limiar Bradley**
A limiarização de imagem é usada em aplicações gráficas. O objetivo da limiarização de uma imagem é classificar os pixels como "escuros" ou "claros". A API do Aspose.PSD permite usar a limiarização de Bradley ao converter imagens. O trecho de código a seguir mostra como definir o valor de limiar e, em seguida, invocar o algoritmo de limiar de Bradley.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversao-LimiarBradley-LimiarBradley.cs" >}}
