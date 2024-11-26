---
title: Manipulando Imagens TIFF
type: docs
weight: 50
url: /pt/net/manipulando-imagens-tiff/
---

## **Adicionar Quadros com Configurações Diferentes**
TIFF é um formato muito flexível e permite a adição de quadros diferentes, com dimensões diferentes, compressão e outras configurações. As APIs da Aspose.PSD permitem adicionar qualquer quadro TIFF de qualquer tamanho, o que ajuda na criação de documentos complexos. Se houver a necessidade de ajustar os quadros durante o processo de adição para torná-los todos iguais, siga as seguintes etapas:

- Crie um novo quadro em branco com as opções desejadas ou copie o quadro de origem com as opções de saída especificadas usando o método CreateFrameFrom.
- Redimensione o quadro/imagem de origem para as dimensões desejadas usando o método Resize.
- Adicione os pixels do quadro/imagem de origem ao novo quadro.
- Adicione o novo quadro à imagem TIFF de saída.

## **Exportar camadas de imagem PSD para o formato de arquivo TIFF de várias páginas**
Às vezes é necessário exportar camadas de imagem PSD para o formato de arquivo TIFF de várias páginas. Este artigo demonstrará como realizar essa tarefa usando a API Aspose.PSD para .NET. Primeiramente, iremos carregar a imagem PSD do disco. Em seguida, iremos iterar sobre as camadas de imagem PSD e criar o TiffFrame a partir das camadas correspondentes. Por fim, iremos salvar a imagem TIFF resultante em um único arquivo no disco.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}
## **Configuração de TiffOptions**

Os desenvolvedores podem ajustar diferentes propriedades da classe [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) para obter os resultados desejados. Neste documento, nos focaremos em 4 propriedades principais que controlam os atributos da imagem resultante.

Essas propriedades estão listadas abaixo.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

Ao inicializarmos uma estrutura TiffOptions vazia, cada opção é definida como seu valor padrão, por exemplo, a compressão é definida como Nenhuma, BitsPerSample é definido como 1 e Photometric como MinIsWhite. Salvar neste formato tornará a imagem final em preto e branco, e este é o comportamento esperado para essa combinação de opções. Para obter resultados coloridos, você precisa configurar todas as propriedades mencionadas acima com valores correspondentes ao espaço de cor desejado ou você pode inicializar a estrutura TiffOptions com configurações predefinidas conforme discutido posteriormente neste artigo. Abaixo está uma tabela descrevendo os valores de parâmetros esperados que você pode definir para obter os resultados desejados. Por favor, note que você deve configurar todas as 4 colunas através do TiffOptions para salvar qualquer imagem carregada/criada no formato de arquivo TIFF.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Paleta|LZW/Comprimido|1/4/8/16 (paleta, modo de cor) único canal apenas|Nenhum|
|MinIsWhite/MinIsBlack|LZW/Comprimido|1/4/8/16 (modo em escala de cinza) único canal apenas|Nenhum|
|Paleta|LZW/Comprimido|8 (paleta, modo de cor) único canal apenas|Horizontal (maior compressão alcançada para LZW pelos mesmos padrões)|
|MinIsWhite/MinIsBlack|LZW/Comprimido|8 (modo em escala de cinza) único canal apenas|Horizontal (maior compressão alcançada para LZW pelos mesmos padrões)|
|RGB|LZW/Comprimido|[8,8,8] (3 canais RGB)|Nenhum/Horizontal|
|RGB|LZW/Comprimido|[8,8,8,8] (3 canais RGB e canal alfa adicional pode ser definido através de TiffOptions.AlphaStorage) Na verdade, qualquer contagem de canais adicional é suportada, mas cada canal deve ter tamanho de 8 bits como [8,8,8,8,8,8]|Nenhum/Horizontal|
Todas as 4 propriedades devem ser configuradas através do TiffOptions para salvar qualquer formato de imagem no formato Tiff. Ao empregar combinações diferentes, alguns visualizadores (incluindo o Visualizador de Fotos do Windows) podem se recusar a renderizar a imagem resultante devido ao suporte limitado que eles oferecem. Nesse caso, por favor escolha um visualizador diferente para seus testes.
### **Configurações Predefinidas para a Classe TiffOptions**
A fim de facilitar os usuários e evitar a má configuração da instância TiffOptions, a API Aspose.PSD para .NET expôs outro construtor que aceita um parâmetro do tipo [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat). Com base no valor selecionado da enumeração TiffExpectedFormat, a API configura automaticamente todas as propriedades obrigatórias para a instância TiffOptions a fim de produzir os resultados desejados. Antes de avançarmos para o código de exemplo, aqui está a lista dos campos TiffExpectedFormat e seus detalhes para melhor entendimento do uso.



- TiffExpectedFormat.Default: Configurar o campo como Default age de forma semelhante ao construtor padrão da classe TiffOptions, sem compressão definida e BitsPerPixel configurado como 1 para produzir um resultado em preto e branco. É aconselhável usar esse campo quando outras propriedades específicas de formato precisam ser definidas manualmente de acordo com os resultados desejados.
- TiffExpectedFormat.TiffCcitRle: Específico para codificação RLE ao salvar o resultado no formato TIFF 1 BitsPerPixel (preto e branco).
- TiffExpectedFormat.TiffCcittFax3: Específico para codificação CCITT Fax3 ao salvar o resultado no formato TIFF 1 BitsPerPixel (preto e branco).
- TiffExpectedFormat.TiffCcittFax4: Específico para codificação CCITT Fax4 ao salvar o resultado no formato TIFF 1 BitsPerPixel (preto e branco).
- TiffExpectedFormat.TiffDeflateBW: Específico para compressão Deflate ao salvar o resultado no formato TIFF 1 BitsPerPixel (preto e branco).
- TiffExpectedFormat.TiffDeflateRGB: Específico para compressão Deflate ao salvar o resultado no formato TIFF RGB (cor).
- TiffExpectedFormat.TiffJpegRGB: Específico para compressão Jpeg ao salvar o resultado no formato TIFF RGB (cor).
- TiffExpectedFormat.TiffJpegYCBCR: Específico para compressão Deflate ao salvar o resultado no formato TIFF YCBCR (colorido).
- TiffExpectedFormat.TiffLzwBW: Específico para compressão LZW ao salvar o resultado no formato TIFF 1 BitsPerPixel (preto e branco).
- TiffExpectedFormat.TiffLzwRGB: Específico para compressão LZW ao salvar o resultado no formato TIFF RGB (cor).
- TiffExpectedFormat.TiffLzwRGBA: Específico para compressão LZW ao salvar o resultado no formato TIFF RGBA (cor com transparência).
- TiffExpectedFormat.TiffNoCompressionBW: Específico para formato TIFF sem compressão ao salvar o resultado em 1 BitsPerPixel (preto e branco).
- TiffExpectedFormat.TiffNoCompressionRGB: Específico para formato TIFF sem compressão ao salvar o resultado em RGB (cor).
- TiffExpectedFormat.TiffNoCompressionRGBA: Específico para formato TIFF sem compressão ao salvar o resultado em RGBA (cor com transparência).



O trecho de código a seguir ilustra o uso dos campos TiffExpectedFormat ao criar uma instância da classe TiffOptions.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}
## **Suporte para Compressão Deflate e Adobe Deflate**
O formato de arquivo TIFF (Tagged Image File Format) suporta vários tipos de compressão, sendo o tipo de compressão armazenado como uma marca (um valor inteiro) no arquivo. Um desses métodos de compressão é o Adobe Deflate (anteriormente conhecido como Deflate). A API da Aspose.PSD para .NET suporta esse método de compressão para exportar e criar imagens TIFF.
### **Salvando Imagem em TIFF com Compressão Deflate**
Converter as imagens carregadas em TIFF com compressão Deflate/Adobe Deflate é fácil conforme o abaixo.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}
### **Criando TiffImage com Compressão Adobe Deflate**
O exemplo fornecido abaixo demonstra o uso da API da Aspose.PSD para .NET para criar uma imagem do zero usando o método de compressão Adobe Deflate.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}
### **Comprimindo Imagens TIFF**
A API da Aspose.PSD para .NET pode ser utilizada para converter imagens PSD para o formato de imagem TIFF e até mesmo alterar a compressão da imagem TIFF resultante. A API também pode ser usada para armazenar diferentes imagens como quadros em uma imagem TIFF para fins de arquivamento, enquanto comprime as imagens para o menor tamanho de dados. A compressão da imagem deve ser realizada pela redução do tamanho dos dados de origem, independentemente do algoritmo de compressão usado. Para obter a melhor taxa de compressão, podemos usar espaços de cores indexados. O trecho de código fornecido abaixo realiza a melhor compressão usando 16 cores indexadas apenas e o algoritmo de compressão LZW, no entanto, as cores de origem são ligeiramente ditherizadas.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.cs" >}}
