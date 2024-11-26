---
title: Evite a Degradação de Desempenho ao Desenhar sobre Imagens Comprimidas
type: docs
weight: 10
url: /pt/net/avoid-performance-degradation-when-drawing-over-compressed-images/
---

## **Evite a Degradação de Desempenho ao Desenhar sobre Imagens Comprimidas**
Há momentos em que deseja realizar operações gráficas extremamente extensas sobre uma imagem comprimida. Quando o Aspose.PSD precisa comprimir e descomprimir imagens dinamicamente, pode ocorrer degradação de desempenho. Desenhar sobre imagens comprimidas também pode acarretar uma penalidade de desempenho.

### **Solução**
Para evitar a degradação de desempenho, recomendamos que converta a imagem para um formato não comprimido, ou raw, antes de realizar operações gráficas.

### **Usando o Caminho do Arquivo**
No exemplo a seguir, uma imagem PSD é convertida para o formato raw (sem compressão) e salva no disco. A imagem não comprimida é então carregada de volta antes que as operações gráficas sejam realizadas. A mesma técnica se aplica para arquivos BMP e GIF.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}

### **Usando um Objeto de Fluxo (Stream)**
O trecho de código a seguir mostra como uma imagem PSD é convertida para o formato raw (sem compressão) e salva no disco usando MemoryStream.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}
