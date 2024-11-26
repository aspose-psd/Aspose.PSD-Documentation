---
title: Manipulação de Imagens PNG
type: docs
weight: 30
url: /pt/java/manipulacao-imagens-png/
---

## **Especificar Transparência para Imagens PNG**
Uma das vantagens de salvar imagens no formato PNG é que o PNG pode ter fundo transparente. Aspose.PSD para Java fornece a funcionalidade para especificar transparência para as classes PngImage & RasterImage, como demonstrado na seção abaixo. Aspose.PSD para Java API pode ser usada para definir qualquer cor como transparente ao criar novas imagens PNG ou converter imagens existentes para o formato PNG. Para este propósito, a Aspose.PSD para Java API expôs a propriedade TransparentColor e a enumeração PngColorType que pode ser definida para especificar qualquer cor a ser renderizada como transparente na imagem PNG. O trecho de código fornecido abaixo demonstra como converter uma imagem PSD existente em uma imagem PNG usando o construtor sobrecarregado de PngImage e especificando a cor desejada como transparente.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.java" >}}
## **Definir Resolução para Imagens PNG**
Aspose.PSD para Java expõe a classe ResolutionSetting que pode ser usada para definir a resolução para todos os formatos de imagem, incluindo PNG. Este artigo demonstra o uso da Aspose.PSD para Java API para definir os parâmetros de resolução horizontal e vertical para o formato de imagem PNG. O trecho de código abaixo carrega uma imagem PSD existente e a converte para o formato PNG, alterando também a resolução.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.java" >}}
## **Comprimir Arquivos PNG**
O Formato Gráfico de Rede Portátil (PNG) é um formato de compressão sem perdas para transmitir um bitmap na rede. Ao salvar uma imagem como um arquivo PNG em qualquer programa, pode ser solicitado que você escolha um nível de compressão em uma faixa de 0 a um nível máximo. Definir esse valor na verdade comprime o tamanho do arquivo e não diminui a qualidade da imagem. Este artigo descreve como as APIs da Aspose.PSD permitem que você controle o tamanho do arquivo PNG. As APIs Aspose.PSD podem ser usadas para definir os Níveis de Compressão para o formato de arquivo PNG usando a classe PngOptions que possui a propriedade CompressionLevel do tipo int. Esta propriedade aceita um valor de 0 a 9, onde 9 é a compressão máxima. O trecho de código fornecido abaixo demonstra como definir os Níveis de Compressão usando a Aspose.PSD para Java API.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.java" >}}
## **Especificar Profundidade de Bits para Imagens PNG**
A profundidade de bits em imagens é o número de bits usados para indicar a cor de um único pixel em uma imagem de bitmap. Como todos os outros formatos de bitmap, a profundidade de cor do PNG também é representada em bits, como 1 bit (2 cores), 2 bits (4 cores), 4 bits (16 cores) e 8 bits (256 cores). Aspose.PSD para Java API pode ser usada para definir a profundidade de bits para imagens PNG usando a propriedade BitDepth exposta pela classe PngOptions. No momento, a propriedade BitDepth pode ser definida para 1, 2, 4 ou 8 bits para tipos de cor em tons de cinza e indexados. Para todos os outros tipos de cor, apenas 8 bits são suportados. O trecho de código fornecido abaixo demonstra como definir a Profundidade de Bits para uma imagem PNG.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.java" >}}
## **Aplicar Métodos de Filtro em Imagens PNG**
Aspose.PSD para Java expõe a enumeração PngFilterType que pode ser usada para definir o tipo de filtro para a imagem PNG. O trecho de código fornecido abaixo demonstra como aplicar um filtro em um arquivo PSD existente para uma imagem PNG usando PngFilterType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.java" >}}
## **Alterar a Cor de Fundo de uma Imagem PNG Transparente**
Imagens no formato PNG podem ter fundo transparente. Aspose.PSD para Java fornece a funcionalidade de alterar a cor de fundo de uma imagem PNG que possui fundo transparente. A Aspose.PSD para Java API pode ser usada para definir/alterar a cor de uma imagem PNG transparente. O trecho de código fornecido abaixo demonstra como definir/alterar a cor de fundo de uma imagem PNG transparente.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.java" >}}
