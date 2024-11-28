---
title: Manipulação de Imagens PNG
type: docs
weight: 40
url: /pt/net/manipulacao-de-imagens-png/
---

## **Especificar Transparência para Imagens PNG**
Uma das vantagens de salvar imagens no formato PNG é que o PNG pode ter um fundo transparente. Aspose.PSD para .NET fornece a funcionalidade para especificar a transparência para as imagens PNG e imagens rasterizadas, como demonstrado na seção abaixo. Aspose.PSD para .NET API pode ser usado para definir qualquer cor como transparente ao criar novas imagens PNG ou converter imagens existentes para o formato PNG. Para este fim, a API Aspose.PSD para .NET expôs a propriedade [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) e a enumeração [PngColorType](https://reference.aspose.com/psd/net/aspose.psd/fileformats.png/pngcolortype) que podem ser definidas para especificar qualquer cor a ser renderizada como transparente na imagem PNG. O trecho de código abaixo demonstra como converter uma imagem PSD existente em uma imagem PNG especificando a cor desejada como transparente.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificacaoEConversaoImagens-PNG-EspecificarTransparencia-EspecificarTransparencia.cs" >}}
## **Definir Resolução para Imagens PNG**
Aspose.PSD para .NET expõe a classe ResolutionSetting que pode ser usada para definir a resolução para todos os formatos de imagem, incluindo PNG. Este artigo demonstra o uso da API Aspose.PSD para .NET para definir os parâmetros de resolução horizontal e vertical para o formato de imagem PNG. O trecho de código abaixo carrega uma imagem PSD existente e a converte para o formato PNG, alterando também a resolução.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificacaoEConversaoImagens-PNG-DefinirResolucao-DefinirResolucao.cs" >}}
## **Comprimir Arquivos PNG**
O Formato Gráfico de Rede Portátil (PNG) é um formato de compressão sem perdas para transmitir um bitmap pela rede. Ao salvar uma imagem como arquivo PNG em qualquer programa, você pode ser solicitado a escolher um nível de compressão em uma faixa de 0 a um nível máximo. Definir esse valor realmente comprime o tamanho do arquivo e não diminui a qualidade da imagem. Este artigo descreve como as APIs Aspose.PSD permitem controlar o tamanho do arquivo PNG. As APIs Aspose.PSD podem ser usadas para definir os Níveis de Compressão para o formato do arquivo PNG usando a classe PngOptions que possui uma propriedade [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel) do tipo int. Esta propriedade aceita um valor de 0 a 9, onde 9 é a compressão máxima. O trecho de código abaixo demonstra como definir os Níveis de Compressão usando a API Aspose.PSD para .NET.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificacaoEConversaoImagens-PNG-ComprimirArquivos-ComprimirArquivos.cs" >}}
## **Especificar Profundidade de Bits para Imagens PNG**
A profundidade de bits em imagens é o número de bits usados para indicar a cor de um único pixel em uma imagem de bitmap. Assim como todos os outros formatos de bitmap, a profundidade de cor do PNG também é representada em bits, como 1-bit (2 cores), 2-bit (4 cores), 4-bit (16 cores) e 8-bit (256 cores). Aspose.PSD para .NET API pode ser usada para definir a profundidade de bits para imagens PNG usando a propriedade [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) exposta pela classe PngOptions. Atualmente, a propriedade BitDepth pode ser definida para 1, 2, 4 ou 8 bits para os tipos de cor em tons de cinza e indexados. Para todos os outros tipos de cor, apenas 8 bits são suportados. O trecho de código abaixo demonstra como definir a Profundidade de Bits para uma imagem PNG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificacaoEConversaoImagens-PNG-EspecificarProfundidadeBits-EspecificarProfundidadeBits.cs" >}}
## **Aplicar Métodos de Filtro em Imagens PNG**
A profundidade de bits em imagens é o número de bits usados para indicar a cor de um único pixel em uma imagem de bitmap. Assim como todos os outros formatos de bitmap, a profundidade de cor do PNG também é representada em bits, como 1-bit (2 cores), 2-bit (4 cores), 4-bit (16 cores) e 8-bit (256 cores). Aspose.PSD para .NET API pode ser usada para definir a profundidade de bits para imagens PNG usando a propriedade BitDepth exposta pela classe PngOptions. Atualmente, a propriedade BitDepth pode ser definida para 1, 2, 4 ou 8 bits para os tipos de cor em tons de cinza e indexados. Para todos os outros tipos de cor, apenas 8 bits são suportados. O trecho de código abaixo demonstra como definir a Profundidade de Bits para uma imagem PNG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificacaoEConversaoImagens-PNG-AplicarMetodoFiltro-AplicarMetodoFiltro.cs" >}}
## **Alterar Cor de Fundo de uma Imagem PNG Transparente**
Imagens no formato PNG podem ter fundo transparente. Aspose.PSD para .NET oferece a funcionalidade de alterar a cor de fundo de uma imagem PNG que possui fundo transparente. Aspose.PSD para .NET API pode ser usada para definir/alterar a cor de uma imagem PNG transparente. O trecho de código abaixo demonstra como definir/alterar a cor de fundo de uma imagem PNG transparente.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificacaoEConversaoImagens-PNG-AlterarCorDeFundo-AlterarCorDeFundo.cs" >}}
