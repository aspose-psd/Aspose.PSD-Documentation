---
title: Convertendo Imagens
type: docs
weight: 20
url: /pt/net/converting-images/
---

## **Convertendo Imagens para Preto e Branco e Tons de Cinza**
Às vezes, pode ser necessário converter imagens coloridas para preto e branco ou tons de cinza para fins de impressão ou arquivamento. Este artigo demonstra o uso da API Aspose.PSD para .NET para alcançar isso usando dois métodos conforme descrito abaixo.

- Binarização
- Tons de cinza

### **Binarização**
Para entender o conceito de binarização, é importante definir uma Imagem Binária; que é uma imagem digital que pode ter apenas dois valores possíveis para cada pixel. Normalmente, as duas cores usadas para uma imagem binária são preto e branco, embora qualquer duas cores possam ser usadas. A binarização é o processo de converter uma imagem em bi-nível, o que significa que cada pixel é armazenado como um único bit (0 ou 1) onde 0 denota a ausência de cor e 1 significa presença de cor. A API Aspose.PSD para .NET atualmente suporta dois métodos de binarização.

#### **Binarização com Limiar Fixo**
O trecho de código a seguir mostra como usar a binarização com limiar fixo pode ser aplicado a uma imagem.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Binarização com Limiar de Otsu**
O trecho de código a seguir mostra como o limiar de binarização de Otsu pode ser aplicado a uma imagem.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}

### **Tons de Cinza**
Escalonamento de cinza é o processo de converter uma imagem de tons contínuos em uma imagem com tons de cinza descontínuos. O trecho de código a seguir mostra como usar o escalonamento de cinza.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversão-EscalaDeCinza-EscalaDeCinza.cs" >}}

## **Converter Camadas de Imagem GIF para Imagem TIFF**
Às vezes é necessário extrair e converter camadas de uma imagem PSD em outro formato de imagem raster para atender a uma necessidade de aplicativo. A API Aspose.PSD suporta o recurso de extrair e converter camadas de uma imagem PSD em outro formato de imagem raster. Primeiramente, criaremos uma instância de imagem e carregaremos a imagem PSD do disco local, então iteraremos cada camada na propriedade Layer. Então converteremos o bloco em uma imagem TIFF. O trecho de código a seguir mostra como converter camadas de imagem PSD em imagens TIFF.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversion-CamadasDeImagemGIFFparaTIFF-CamadasDeImagemGIFFparaTIFF.cs" >}}

## **Convertendo um PSD CMYK para TIFF CMYK**
Usando Aspose.PSD para .NET, os desenvolvedores podem converter um arquivo PSD CMYK para o formato de arquivo tiff CMYK. Este artigo mostra como exportar/converter um arquivo PSD CMYK para o formato de arquivo tiff CMYK com o Aspose.PSD. Usando o Aspose.PSD para .NET, você pode carregar imagens PSD e, em seguida, pode configurar várias propriedades usando [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) classe e salvar ou exportar a imagem. O trecho de código a seguir mostra como realizar este recurso.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversão-PSD-CMYKparaTIFF-CMYKPSDtoCMYKTiff.cs" >}}

## **Exportando Imagens**
Juntamente com um rico conjunto de rotinas de processamento de imagem, o Aspose.PSD fornece classes especializadas para converter formatos de arquivo PSD em outros formatos. Usando esta biblioteca, a conversão de imagens PSD é muito simples e intuitiva. Abaixo estão algumas classes especializadas para esse fim no espaço de nomes [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions).

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

É fácil exportar imagens PSD com o Aspose.PSD para .NET API. Tudo o que você precisa é um objeto da classe apropriada de [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions). Ao usar essas classes, você pode facilmente exportar qualquer imagem criada, editada ou simplesmente carregada com o Aspose.PSD para .NET para qualquer formato suportado.

## **Combinando Imagens**
Este exemplo usa a classe Graphics e mostra como combinar duas ou mais imagens em uma única imagem completa. Para demonstrar a operação, o exemplo cria uma nova PsdImage e desenha imagens na superfície do canvas usando o método Draw Image exposto pela classe Graphics. Usando a classe Graphics, duas ou mais imagens podem ser combinadas de tal forma que a imagem resultante parecerá uma imagem completa sem espaço entre as partes da imagem e sem páginas. O tamanho do canvas deve ser igual ao tamanho da imagem resultante. A seguir está a demonstração de código que mostra como usar o método [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) da classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para combinar imagens em uma única imagem.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-DesenhoeFormataçãoDeImagens-CombinandoImagens-CombinandoImagens.cs" >}}

## **Expandir e Cortar Imagens**
A API Aspose.PSD permite que você expanda ou corte uma imagem durante o processo de conversão de imagem. O desenvolvedor precisa criar um retângulo com coordenadas X e Y e especificar a largura e altura da caixa de retângulo. O X, Y e a Largura, Altura do retângulo vão descrever a expansão ou corte da imagem carregada. Se for necessário expandir ou cortar a imagem durante a conversão de imagem, siga as seguintes etapas:

1. Crie uma instância da classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) e carregue a imagem existente.
1. Crie uma instância da classe ImageOption.
1. Crie uma instância da classe [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) e inicialize o X, Y e a Largura, Altura do retângulo.
1. Chame o método [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) da classe RasterImage enquanto passa o nome do arquivo de saída, as opções de imagem e o objeto retângulo como parâmetros.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-DesenhoeFormataçãoDeImagens-ExpandireCortarImagens-ExpandireCortarImagens.cs" >}}

## **Ler e Escrever Dados XMP em Imagens**
XMP (Extensible Metadata Platform) é um padrão ISO. O XMP padroniza um modelo de dados, um formato de serialização e propriedades essenciais para a definição e o processamento de metadados extensíveis. Ele também fornece diretrizes para incorporar informações XMP em uma imagem popular, como JPEG, sem comprometer a legibilidade por aplicativos que não suportam XMP. Usando a API Aspose.PSD para .NET, os desenvolvedores podem ler ou escrever metadados XMP em imagens. Este artigo demonstra como os metadados XMP podem ser lidos de uma imagem e como escrever metadados XMP em imagens.
### **Criar Metadados XMP, Escrever e Ler de um Arquivo**
Com a ajuda do namespace Xmp, o desenvolvedor pode criar um objeto de metadados XMP e gravá-lo em uma imagem. O seguinte trecho de código mostra como usar os pacotes XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage e DublinCorePackage contidos no namespace [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-DesenhoeFormataçãoDeImagens-CriarMetadadosXMP-CriarMetadadosXMP.cs" >}}

## **Exportar Imagens em Ambiente Multithread**
O Aspose.PSD para .NET agora oferece suporte para a conversão de imagens em um ambiente multithread. O Aspose.PSD para .NET garante o desempenho otimizado das operações durante a execução de código em um ambiente multithread. Todas as classes de [opção de imagem](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) (por exemplo, BmpOptions, TiffOptions, JpegOptions, etc.) no Aspose.PSD para .NET implementam a interface IDisposable. Portanto, é essencial que o desenvolvedor descarte corretamente o objeto da classe de opções de imagem no caso da propriedade Source ser definida. O trecho de código a seguir demonstra essa funcionalidade.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversão-ExportarImagensEmAmbienteMultithread-ExportarImagensEmAmbienteMultithread.cs" >}}


O Aspose.PSD agora suporta a propriedade SyncRoot ao trabalhar em um ambiente multithread. O desenvolvedor pode usar essa propriedade para sincronizar o acesso ao fluxo de origem. O trecho de código a seguir demonstra como a propriedade SyncRoot pode ser usada.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversão-SyncRoot-SyncRoot.cs" >}}
