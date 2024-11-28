---
title: Manipulação de Imagens TIFF
type: docs
weight: 40
url: /pt/java/manipulando-imagens-tiff/
---

## **Adicionar Frames com Diferentes Configurações**
O TIFF é um formato muito flexível e permite que diferentes frames sejam adicionados, com diferentes dimensões, compressão e outras configurações. As APIs da Aspose.PSD permitem adicionar qualquer frame TIFF de qualquer tamanho, o que ajuda na criação de documentos complexos. Se houver a necessidade de ajustar os frames durante o processo de adição para torná-los todos iguais, siga as seguintes etapas:

- Crie um novo frame em branco com as opções desejadas ou copie o frame de origem com as opções de saída especificadas usando o método CreateFrameFrom.
- Redimensione o frame/imagem de origem para as dimensões desejadas usando o método Resize.
- Adicione os pixels do frame/imagem de origem ao novo frame.
- Adicione o novo frame à imagem TIFF de saída.
## **Exportar Camadas de Imagem PSD para Formato de Arquivo TIFF de Múltiplas Páginas**
Às vezes, é necessário exportar camadas de imagem PSD para o formato de arquivo TIFF de várias páginas. Este artigo demonstrará como podemos realizar essa tarefa usando a API Aspose.PSD para Java. Primeiramente, carregaremos a imagem PSD do disco. Em seguida, iteraremos sobre as camadas da imagem PSD e criaremos um TiffFrame a partir das camadas correspondentes. Por fim, salveremos a imagem TIFF resultante em um único arquivo no disco.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}
## **Configuração de TiffOptions**
Os desenvolvedores podem ajustar diferentes propriedades da classe TiffOptions para obter resultados desejados. Neste documento, vamos nos concentrar em 4 propriedades principais que controlam os atributos da imagem resultante.

Essas propriedades estão listadas abaixo.

1. ` `TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

Quando inicializamos uma estrutura vazia de TiffOptions, cada opção é definida com seu valor padrão, por exemplo, a compressão é definida como Nenhuma, BitsPerSample é definido como 1 e Photometric como MinIsWhite. Salvar nesse formato fará com que a imagem final seja em preto e branco e este é o comportamento esperado para essa combinação de opções. Para obter resultados coloridos, você deve definir todas as propriedades mencionadas acima para valores que correspondam ao espaço de cor desejado ou pode inicializar a estrutura TiffOptions com configurações pré-definidas conforme discutido mais adiante neste artigo. Abaixo está uma tabela descrevendo os valores dos parâmetros esperados que você pode definir para alcançar os resultados desejados. Observe que você deve definir as 4 colunas através de TiffOptions para salvar qualquer imagem carregada/criada no formato de arquivo TIFF.

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Não Comprimido|1/4/8/16 (paleta, modo de cor) apenas um canal|Nenhum|
|MinIsWhite/MinIsBlack|LZW/Não Comprimido|1/4/8/16 (modo de escala de cinza) apenas um canal|Nenhum|
|Paleta|LZW/Não Comprimido|8 (paleta, modo de cor) apenas um canal|Horizontal (melhor compressão alcançada para LZW mesmos padrões)|
|MinIsWhite/MinIsBlack|LZW/Não Comprimido|8 (modo de escala de cinza) apenas um canal|Horizontal (melhor compressão alcançada para LZW mesmos padrões)|
|RGB|LZW/Não Comprimido|[8,8,8] (3 canais RGB)|Nenhum/Horizontal|
|RGB|LZW/Não Comprimido|[8,8,8,8] (3 canais RGB e canal alfa adicional podem ser definidos através de TiffOptions.AlphaStorage) Na verdade, é suportada qualquer contagem adicional de canais, mas cada canal deve ter 8 bits de tamanho, como [8,8,8,8,8,8]|Nenhum/Horizontal|

Todas as 4 propriedades devem ser definidas através de TiffOptions para salvar qualquer formato de imagem no formato Tiff. Ao usar combinações diferentes, alguns visualizadores (incluindo o Visualizador de Fotos do Windows) podem se recusar a renderizar a imagem resultante devido ao suporte limitado que oferecem. Nesse caso, escolha um visualizador diferente para seus testes.
### **Configurações Pré-definidas para a Classe TiffOptions**
Para facilitar os usuários e evitar a má configuração da instância TiffOptions, a API Aspose.PSD para Java expôs outro construtor que aceita um parâmetro do tipo TiffExpectedFormat. Com base no valor selecionado da enumeração TiffExpectedFormat, a API configura automaticamente todas as propriedades obrigatórias para a instância de TiffOptions a fim de produzir os resultados desejados. Antes de avançarmos para o código de exemplo, aqui está a lista dos campos TiffExpectedFormat e seus detalhes para melhor entendimento do uso.



- TiffExpectedFormat.Default: Definir o campo como Default age de forma semelhante ao construtor padrão da classe TiffOptions, sem definição de compressão e BitsPerPixel definidos como 1 para produzir um resultado em preto e branco. É aconselhável usar este campo quando outras propriedades específicas de formato devem ser definidas manualmente conforme os resultados desejados.
- TiffExpectedFormat.TiffCcitRle: Específico para codificação RLE ao salvar o resultado no formato TIFF com 1 BitsPerPixel (preto e branco).
- TiffExpectedFormat.TiffCcittFax3: Específico para codificação CCITT Fax3 ao salvar o resultado no formato TIFF com 1 BitsPerPixel (preto e branco).
- TiffExpectedFormat.TiffCcittFax4: Específico para codificação CCITT Fax4 ao salvar o resultado no formato TIFF com 1 BitsPerPixel (preto e branco).
- TiffExpectedFormat.TiffDeflateBW: Específico para compressão Deflate ao salvar o resultado no formato TIFF com 1 BitsPerPixel (preto e branco).
- TiffExpectedFormat.TiffDeflateRGB: Específico para compressão Deflate ao salvar o resultado no formato TIFF RGB (colorido).
- TiffExpectedFormat.TiffJpegRGB: Específico para compressão Jpeg ao salvar o resultado no formato TIFF RGB (colorido).
- TiffExpectedFormat.TiffJpegYCBCR: Específico para compressão Deflate ao salvar o resultado no formato TIFF YCBCR (colorido).
- TiffExpectedFormat.TiffLzwBW: Específico para compressão LZW ao salvar o resultado no formato TIFF com 1 BitsPerPixel (preto e branco).
- TiffExpectedFormat.TiffLzwRGB: Específico para compressão LZW ao salvar o resultado no formato TIFF RGB (colorido).
- TiffExpectedFormat.TiffLzwRGBA: Específico para compressão LZW ao salvar o resultado no formato TIFF RGBA (colorido com transparência).
- TiffExpectedFormat.TiffNoCompressionBW: Específico para formato TIFF não comprimido ao salvar o resultado com 1 BitsPerPixel (preto e branco).
- TiffExpectedFormat.TiffNoCompressionRGB: Específico para formato TIFF não comprimido ao salvar o resultado em RGB (colorido).
- TiffExpectedFormat.TiffNoCompressionRGBA: Específico para formato TIFF não comprimido ao salvar o resultado em RGBA (colorido com transparência).



O trecho de código a seguir elabora o uso dos campos TiffExpectedFormat ao criar uma instância da classe TiffOptions.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}
## **Suporte para Compressão Deflate e Adobe Deflate**
O formato de arquivo TIFF (Tagged Image File Format) suporta vários tipos de compressão, enquanto o tipo de compressão é armazenado como uma tag (um valor inteiro) no arquivo. Um desses métodos de compressão é o Adobe Deflate (anteriormente conhecido como Deflate). A API Aspose.PSD para Java suporta esse método de compressão para exportar e criar imagens TIFF.
### **Salvando Imagem em TIFF com Compressão Deflate**
Converter imagens carregadas em TIFF com compressão Deflate/Adobe Deflate é fácil como segue.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFWithDeflateCompression-TIFFWithDeflateCompression.java" >}}
### **Criando TiffImage com Compressão Adobe Deflate**
O exemplo fornecido abaixo demonstra o uso da API Aspose.PSD para Java para criar uma imagem do zero usando o método de compressão Adobe Deflate.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.java" >}}
### **Comprimindo Imagens TIFF**
A API Aspose.PSD para Java pode ser usada para converter imagens PSD para o formato de imagem TIFF e até mesmo alterar a compressão da imagem TIFF resultante. A API também pode ser usada para armazenar diferentes imagens como frames em uma imagem TIFF para fins de arquivamento, enquanto comprime as imagens para o menor tamanho de dados. A compressão da imagem, em qualquer caso, deve ser realizada reduzindo o tamanho dos dados de origem, independentemente do algoritmo de compressão usado. Para obter a melhor taxa de compressão, podemos usar espaços de cores indexados. O trecho de código a seguir realiza a melhor compressão usando 16 cores indexadas apenas e algoritmo de compressão LZW, no entanto, as cores de origem são ligeiramente difundidas.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.java" >}}
