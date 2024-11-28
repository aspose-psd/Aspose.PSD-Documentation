---
title: Convertendo Imagens
type: docs
weight: 20
url: /pt/java/convertendo-imagens/
---

## **Convertendo Imagens para Preto e Branco e Escala de Cinza**
Às vezes, pode ser necessário converter imagens coloridas para preto e branco ou escala de cinza para fins de impressão ou arquivamento. Este artigo demonstra o uso da API Aspose.PSD para Java para alcançar isso usando dois métodos conforme indicado abaixo.

- Binarização
- Escalonamento de Cinza
### **Binarização**
Para entender o conceito de Binarização, é importante definir uma Imagem Binária; ou seja, uma imagem digital que pode ter apenas dois valores possíveis para cada pixel. Normalmente, as duas cores usadas para uma imagem binária são preto e branco, embora qualquer duas cores possam ser usadas. Binarização é o processo de converter uma imagem em bi-nível, ou seja, cada pixel é armazenado como um único bit (0 ou 1), onde 0 denota a ausência de cor e 1 significa presença de cor. A API Aspose.PSD para Java atualmente suporta dois métodos de binarização.
#### **Binarização com Limiar Fixo**
O trecho de código a seguir mostra como aplicar a binarização com limiar fixo a uma imagem.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **Binarização com Limiar de Otsu**
O trecho de código a seguir mostra como aplicar a binarização com limiar de Otsu a uma imagem.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **Escala de Cinza**
Escalonamento de cinza é o processo de converter uma imagem de tons contínuos em uma imagem com tons de cinza descontínuos. O trecho de código a seguir mostra como usar o escalonamento de cinza.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **Converter Camadas de Imagem GIF para Imagem TIFF**
Às vezes é necessário extrair e converter camadas de uma imagem PSD em outro formato de imagem raster para atender a uma necessidade do aplicativo. A API Aspose.PSD suporta a funcionalidade de extrair e converter camadas de uma imagem PSD em outro formato de imagem raster. Primeiramente, criaremos uma instância de imagem e carregaremos a imagem PSD do disco local, então iteraremos cada camada na propriedade Layer. Em seguida, converteremos o bloco em imagem TIFF. O trecho de código a seguir mostra como converter camadas de imagem PSD em imagens TIFF.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **Convertendo PSD CMYK para TIFF CMYK**
Usando Aspose.PSD para Java, os desenvolvedores podem converter arquivos PSD CMYK para o formato TIFF CMYK. Este artigo mostra como exportar / converter arquivos PSD CMYK para o formato de imagem TIFF CMYK com o Aspose.PSD. Usando Aspose.PSD para Java, você pode carregar imagens PSD e então pode definir várias propriedades usando a classe TiffOptions e salvar ou exportar a imagem. O trecho de código a seguir mostra como alcançar essa funcionalidade.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **Exportando Imagens**
Junto com um extenso conjunto de rotinas de processamento de imagem, o Aspose.PSD fornece classes especializadas para converter formatos de arquivo PSD para outros formatos. Usando esta biblioteca, a conversão de imagens PSD é muito simples e intuitiva. Abaixo estão algumas classes especializadas para este fim no espaço de nome ImageOptions.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

É fácil exportar imagens PSD com a API Aspose.PSD para Java. Tudo o que você precisa é de um objeto da classe apropriada do espaço de nome ImageOptions. Usando essas classes, você pode facilmente exportar qualquer imagem criada, editada ou simplesmente carregada com o Aspose.PSD para Java para qualquer formato suportado.
## **Combinando Imagens**
Este exemplo usa a classe Graphics e mostra como combinar duas ou mais imagens em uma única imagem completa. Para demonstrar a operação, o exemplo cria uma nova PsdImage e desenha imagens na superfície do canvas usando o método DrawImage exposto pela classe Graphics. Usando a classe Graphics, duas ou mais imagens podem ser combinadas de tal forma que a imagem resultante parecerá uma imagem completa, sem espaço entre as partes da imagem e sem páginas. O tamanho do canvas deve ser igual ao tamanho da imagem resultante. A seguir está a demonstração de código que mostra como usar o método DrawImage da classe Graphics para combinar imagens em uma única imagem.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **Expandir e Cortar Imagens**
A API Aspose.PSD permite que você expanda ou corte uma imagem durante o processo de conversão de imagem. O desenvolvedor precisa criar um retângulo com as coordenadas X e Y e especificar a largura e altura da caixa do retângulo. As coordenadas X, Y e Largura, Altura do retângulo irão representar a expansão ou o corte da imagem carregada. Se for necessário expandir ou cortar a imagem durante a conversão de imagem, siga as etapas abaixo:

1. Crie uma instância da classe RasterImage e carregue a imagem existente.
1. Crie uma instância da classe ImageOption.
1. Crie uma instância da classe Rectangle e inicialize as coordenadas X, Y e Largura, Altura do retângulo.
1. Chame o método Save da classe RasterImage enquanto passa o nome do arquivo de saída, as opções de imagem e o objeto retângulo como parâmetros.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **Ler e Escrever Dados XMP nas Imagens**
XMP (Plataforma de Metadados Extensíveis) é um padrão ISO. O XMP padroniza um modelo de dados, um formato de serialização e propriedades centrais para definição e processamento de metadados extensíveis. Também fornece diretrizes para embutir informações XMP em imagens populares, como JPEG, sem comprometer a legibilidade por aplicativos que não suportam XMP. Usando a API Aspose.PSD para Java, os desenvolvedores podem ler ou escrever metadados XMP em imagens. Este artigo demonstra como os metadados XMP podem ser lidos de uma imagem e como os metadados XMP podem ser escritos nas imagens.
### **Criar Metadados XMP, Escrevê-los e Ler de um Arquivo**
Com a ajuda do espaço de nomes XMP, o desenvolvedor pode criar um objeto de metadados XMP e escrevê-lo em uma imagem. O trecho de código a seguir mostra como usar os pacotes XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage e DublinCorePackage contidos no espaço de nomes XMP.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **Exportar Imagens em Ambiente de Múltiplas Threads**
O Aspose.PSD para Java agora suporta a conversão de imagens em um ambiente de várias threads. O Aspose.PSD para Java garante o desempenho otimizado das operações durante a execução de código em um ambiente de várias threads. Todas as classes de opção de imagem (por exemplo, BmpOptions, TiffOptions, JpegOptions, etc.) no Aspose.PSD para Java implementam a interface IDisposable. Portanto, é obrigatório que o desenvolvedor libere adequadamente o objeto da classe de opções de imagem no caso de a propriedade Source ser definida. O trecho de código a seguir demonstra essa funcionalidade.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}



O Aspose.PSD agora suporta a propriedade SyncRoot ao trabalhar em um ambiente de várias threads. O desenvolvedor pode usar essa propriedade para sincronizar o acesso ao fluxo de origem. O trecho de código a seguir demonstra como a propriedade SyncRoot pode ser usada.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}

