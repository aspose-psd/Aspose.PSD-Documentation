---
title: Aplicando Filtros de Mediana e Wiener
type: docs
weight: 10
url: /pt/java/aplicando-filtros-de-mediana-e-wiener/
---

## **Aplicando Filtros de Mediana e Wiener**
O filtro de mediana é uma técnica de filtragem digital não linear, frequentemente utilizada para remover ruídos. Essa redução de ruído é um passo típico de pré-processamento para melhorar os resultados do processamento posterior. O filtro de Wiener é o filtro linear estacionário ótimo de erro quadrático médio (MSE) para imagens degradadas por ruído aditivo e desfoque. Usando a API Aspose.PSD para Java, os desenvolvedores podem aplicar o filtro de mediana para remover o ruído da imagem e podem aplicar o filtro Gaussiano de Wiener nas imagens. Este artigo demonstra como os filtros de mediana e de Wiener Gaussiano podem ser aplicados às imagens.
### **Aplicando Filtro de Mediana**
O Aspose.PSD fornece a classe MedianFilterOptions para aplicar o filtro em uma RasterImage. O trecho de código fornecido abaixo demonstra como aplicar o filtro de mediana em uma imagem raster.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **Aplicando Filtro de Wiener Gaussiano**
O Aspose.PSD fornece a classe GaussWienerFilterOptions para aplicar o filtro em uma RasterImage. O trecho de código fornecido abaixo demonstra como aplicar o filtro de Wiener Gaussiano em uma imagem raster.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **Aplicando Filtro de Wiener Gaussiano para Imagem Colorida**
O Aspose.PSD fornece GaussWienerFilterOptions também para imagens coloridas. O trecho de código fornecido abaixo demonstra como aplicar o filtro de Wiener Gaussiano em uma imagem colorida.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **Aplicando Filtro Wiener de Movimento**
O Aspose.PSD fornece a classe MotionWienerFilterOptions para aplicar o filtro em uma RasterImage. O trecho de código fornecido abaixo demonstra como aplicar o filtro de Wiener de movimento em uma imagem raster.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **Aplicar Filtro de Correção em uma Imagem**
Este artigo demonstra o uso do Aspose.PSD para Java para aplicar filtros de correção em uma imagem. As APIs do Aspose.PSD expuseram métodos eficientes e fáceis de usar para alcançar esse objetivo. O Aspose.PSD para Java expôs as classes BilateralSmoothingFilterOptions e SharpenFilterOptions para filtragem. A classe BilateralSmoothingFilterOptions precisa de um inteiro como tamanho. Os passos para realizar o Redimensionamento são simples como abaixo:


1. Carregar uma imagem usando o método de fábrica Load exposto pela classe Image.
1. Converter a imagem em RasterImage.
1. Criar instâncias das classes BilateralSmoothingFilterOptions e SharpenFilterOptions.
1. Chamar o método RasterImage.Filter enquanto especifica um retângulo como limites da imagem e uma instância da classe BilateralSmoothingFilterOptions.
1. Chamar o método RasterImage.Filter enquanto especifica um retângulo como limites da imagem e uma instância da classe SharpenFilterOptions.
1. Ajustar o contraste.
1. Definir o brilho.
1. Salvar os resultados.

O trecho de código a seguir mostra como aplicar o filtro de correção.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **Utilizar o Algoritmo de Limiar de Bradley**
A limiarização de imagem é usada em aplicações gráficas. O objetivo da limiarização de uma imagem é classificar pixels como "escuros" ou "claros". A API Aspose.PSD permite que você utilize a limiarização de Bradley ao converter imagens. O trecho de código a seguir mostra como definir o valor do limiar e, em seguida, invocar o algoritmo de limiar de Bradley.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
