---
title: Evite a Degradação de Desempenho ao Desenhar sobre Imagens Comprimidas
type: docs
weight: 40
url: /pt/java/evite-a-degradacao-de-desempenho-ao-desenhar-sobre-imagens-comprimidas/
---

## **Evite a Degradação de Desempenho ao Desenhar sobre Imagens Comprimidas**
Há momentos em que você deseja realizar operações gráficas extremamente extensas em uma imagem comprimida. Quando o Aspose.PSD precisa comprimir e descomprimir imagens dinamicamente, a degradação de desempenho pode ocorrer. Desenhar sobre imagens comprimidas também pode acarretar uma penalidade de desempenho.
### **Solução**
Para evitar a degradação de desempenho, recomendamos que você converta a imagem para um formato não comprimido, ou RAW, antes de realizar operações gráficas.
### **Usando o Caminho do Arquivo**
No exemplo a seguir, uma imagem PSD é convertida para o formato RAW (sem compressão) e salva no disco. A imagem não comprimida é então carregada de volta antes que as operações gráficas sejam realizadas nela. A mesma técnica se aplica a arquivos BMP e GIF.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **Usando um Objeto Stream**
O trecho de código a seguir mostra como a imagem PSD é convertida para o formato RAW (sem compressão) e salva no disco usando Stream.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}
