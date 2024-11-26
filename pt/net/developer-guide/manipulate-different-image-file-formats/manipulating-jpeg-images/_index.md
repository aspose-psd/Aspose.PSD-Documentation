---
title: Manipulação de Imagens JPEG
type: docs
weight: 30
url: /pt/net/manipulando-imagens-jpeg/
---

## **Usando a Classe ExifData para Ler e Modificar Tags EXIF JPEG**
Quase todas as câmeras digitais (incluindo smartphones), scanners e outros sistemas que lidam com imagens salvam imagens com informações EXIF (Exchangeable Image File). As configurações da câmera e informações da cena são registradas pela câmera no arquivo de imagem. Os dados EXIF também incluem velocidade do obturador, data e hora em que a foto foi tirada, comprimento focal, compensação de exposição, padrão de medição e se o flash foi usado. As APIs do Aspose.Imaging tornaram possível extrair as informações EXIF de uma imagem fornecida de maneira muito fácil e simples. Os desenvolvedores também podem escrever dados EXIF nas imagens ou modificar as informações existentes conforme sua necessidade. Aspose.PSD disponibilizou a classe [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) para ler, escrever e modificar os dados EXIF, enquanto o namespace [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) contém as enumerações relevantes usadas no processo.
### **Lendo Dados EXIF**
As APIs do Aspose.PSD fornecem meios para ler dados EXIF de uma imagem fornecida. Os passos fornecidos abaixo ilustram o uso da classe ExifData para ler as informações EXIF de uma imagem.

- Carregar a Imagem PSD usando o método de fábrica Load.
- Encontrar a miniatura Jpeg entre os recursos PSD.
- Extrair uma instância da classe ExifData.

Obtenha as informações necessárias e escreva-as no console.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-JPEG-LerTodasAsTagsEXIFLerTodasAsTagsEXIF.cs" >}}

Alternativamente, os desenvolvedores também podem obter as informações específicas usando o trecho de código a seguir.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-JPEG-LerInformacoesEspecificasDasTagsEXIFLerInformacoesEspecificasDasTagsEXIF.cs" >}}
### **Escrevendo e Modificando Dados EXIF**
Usando as APIs do Aspose.PSD, os desenvolvedores podem escrever novas informações EXIF e modificar os dados EXIF existentes de uma imagem. Ambos os processos (Escrita & Modificação) requerem o carregamento de uma imagem e a obtenção dos dados EXIF em uma instância da classe ExifData. Depois, pode-se acessar as propriedades expostas pela classe ExifData para defini-las adequadamente. Por favor, observe que as imagens para manipulação devem ser imagens Jpeg ou Tiff, que geralmente são miniaturas PSD. O código de exemplo que demonstra o uso é o seguinte:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-JPEG-EscreverEModificarDadosEXIFEscritaEModificarDadosEXIF.cs" >}}
## **Extraindo miniaturas dos recursos PSD**
Miniaturas são versões em tamanho reduzido de imagens, usadas para exibir parte significativa da imagem em vez do quadro completo. Alguns arquivos de imagem (especialmente os feitos com uma câmera digital) possuem uma miniatura incorporada no arquivo. A API do Aspose.PSD permite extrair miniaturas de recursos PSD e armazená-las separadamente no disco. Os recursos de miniatura contêm a propriedade [Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) do ExifData, que pode obter os dados da miniatura. O trecho de código fornecido abaixo demonstra como usá-lo.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-JPEG-ExtrairMiniaturaDoPSD-ExtrairMiniaturaDoPSD.cs" >}}

Use a abordagem discutida acima para armazenar a miniatura em outros formatos de arquivo suportados. Se deseja exportar os dados da miniatura para outros formatos de imagem, como BMP e PNG, por favor, utilize outras opções de exportação de imagem.
### **Extraindo miniaturas dos segmentos JFIF**
Também é possível extrair miniaturas do segmento ExifData ou JFIF dos recursos de miniatura PSD. O código a seguir mostra como realizar a extração dos dados de miniatura do segmento JFIF ou ExifData:
  
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-JPEG-ExtrairMiniaturaDoPSD-ExtrairMiniaturaDoPSD.cs" >}}


Use a abordagem discutida acima para armazenar a miniatura em outros formatos de arquivo suportados. Se deseja exportar os dados da miniatura para outros formatos de imagem, como BMP e PNG, por favor, utilize outras opções de exportação de imagem.
### **Adicionar Miniatura ao Segmento JFIF**
O trecho de código abaixo demonstra como usar a propriedade JFIF. Thumbnail para adicionar uma imagem de miniatura ao segmento JFIF de uma imagem PSD carregada.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-JPEG-AdicionarMiniaturaAoSegmentoJFIF-AdicionarMiniaturaAoSegmentoJFIF.cs" >}}

Imagens de miniatura com outros dados de segmento não podem ocupar mais do que 65.545 bytes devido às especificações do formato JPEG. Em casos em que imagens grandes devem ser definidas como miniatura, pode ocorrer uma exceção.
  
### **Adicionar Miniatura ao Segmento EXIF**
O trecho de código abaixo demonstra como usar a propriedade ExifData.Thumbnail para adicionar uma imagem de miniatura ao segmento EXIF de uma imagem PSD carregada.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-JPEG-AdicionarMiniaturaAoSegmentoEXIF-AdicionarMiniaturaAoSegmentoEXIF.cs" >}}

Neste caso, a API do Aspose.PSD não pode estimar o tamanho da imagem de miniatura, mas pode verificar o tamanho de todo o segmento de dados EXIF. Este tamanho não pode ser maior que 65.535 bytes.
## **Usando a Classe JpegExifData para Ler e Modificar Tags EXIF JPEG**
As APIs do Aspose.PSD fornecem a classe [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) que é exclusiva para formatos de imagem Jpeg para recuperar e atualizar informações EXIF. Este artigo demonstra o uso da classe JpegExifData para alcançar o mesmo. A classe Aspose.PSD.Exif.JpegExifData serve como contêiner de dados EXIF para imagens Jpeg e fornece meios para recuperar tags EXIF Jpeg padrão, como demonstrado abaixo:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-JPEG-AdicionarMiniaturaAoSegmentoEXIF-AdicionarMiniaturaAoSegmentoEXIF.cs" >}}
### **Lista Completa de Tags EXIF**
O trecho de código acima lê algumas tags EXIF usando as propriedades oferecidas pela classe Aspose.PSD.Exif.JpegExifData. A lista completa dessas propriedades está disponível aqui. O código a seguir irá ler todas as tags EXIF usando a classe [System.Reflection.PropertyInfo](https://docs.microsoft.com/pt-br/dotnet/api/system.reflection.propertyinfo?view=net-5.0).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-JPEG-LerTodasAsListasDeTagsEXIFLerTodasAsListasDeTagsEXIF.cs" >}}
## **Correção Automática de Orientação de Imagens JPEG**
  

As fotos podem ser tiradas com uma câmera rotacionada em 90°, 180°, 270° ou nenhuma (orientação normal). A maioria das câmeras digitais armazena a informação de orientação juntamente com os dados da imagem como tags EXIF das imagens JEPG. Esta informação pode ser usada para realizar a rotação automática nas imagens para corrigir a orientação. As APIs do Aspose.PSD fornecem o método AutoRotate para a classe JpegImage para corrigir automaticamente a orientação das imagens JPEG. Aqui está como você pode usar o método AutoRotate com a API Aspose.PSD para .NET.
  
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-JPEG-CorrigirAutomaticamenteOrientacaoDeImagensJPEG-CorrigirAutomaticamenteOrientacaoDeImagensJPEG.cs" >}}
## **Suporte para JPEG-LS com CMYK e YCCK**
As APIs do Aspose.PSD para .NET oferecem suporte para modelos de cores CMYK e YCCK com JPEG-LS. O trecho de código abaixo demonstra como usar esse suporte para JPEG-LS.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-JPEG-SuporteParaJPEG_LSComCMYK-SuporteParaJPEG_LSComCMYK.cs" >}}
## **Suporte para 2-7 bits por amostra em imagens JPEG-LS**
As APIs do Aspose.PSD para .NET oferecem suporte para imagens JPEG-LS com 2-7 bits por amostra. O trecho de código abaixo demonstra como usar esse suporte para JPEG-LS.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-JPEG-SuportePara2-7BitsJPEG-SuportePara2_7BitsJPEG.cs" >}}
## **Definindo ColorType e CompressionType para imagens JPEG**
As APIs do Aspose.PSD para .NET oferecem suporte para Color Type e Compression Type e definem-nos como escala de cinza e progressivo para imagens JPEG. O trecho de código abaixo demonstra como usar esse suporte.

{{< gist "aspose-com-gists" "8a4d34ce856d160ce974175c" "ExemplosCsharp-Aspose-ModificandoEConvertendoImagens-JPEG-TipoDeCorETipoDeCompressao-TipoDeCorETipoDeCompressao.cs" >}}

O trecho de código abaixo demonstra como usar a propriedade ExifData.Thumbnail para adicionar uma imagem de miniatura ao segmento EXIF de uma imagem PSD carregada.

{{< gist "aspose-com-gists" "8a4d34ce856d160ce974175c" "ExemplosCsharp-Aspose-ModificandoEConvertendoImagens-JPEG-AdicionarMiniaturaAoSegmentoEXIF-AdicionarMiniaturaAoSegmentoEXIF.cs" >}}

Neste caso, a API do Aspose.PSD não pode estimar o tamanho da imagem de miniatura, mas pode verificar o tamanho de todo o segmento de dados EXIF. Este tamanho não pode ser maior que 65.535 bytes.
