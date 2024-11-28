---
title: Manipulação de Imagens JPEG
type: docs
weight: 20
url: /pt/java/manipulando-imagens-jpeg/
---

## **Utilizando a Classe ExifData para Ler e Modificar Tags EXIF de JPEG**

Quase todas as câmeras digitais (incluindo smartphones), scanners e outros sistemas que lidam com imagens salvam imagens com informações EXIF (Exchangeable Image File). As configurações da câmera e informações da cena são registradas pela câmera no arquivo de imagem. Os dados EXIF também incluem a velocidade do obturador, data e hora em que a foto foi tirada, distância focal, compensação de exposição, padrão de medição e se o flash foi usado. As APIs Aspose.Imaging tornaram possível extrair as informações EXIF de uma imagem fornecida de maneira muito fácil e simples. Os desenvolvedores também podem escrever dados EXIF nas imagens ou modificar as informações existentes conforme sua necessidade. A Aspose.Imaging forneceu a classe ExifData para ler, escrever e modificar os dados EXIF, enquanto o namespace Aspose.PSD.Exif.Enums contém as enumerações relevantes usadas no processo.
### **Lendo Dados EXIF**
As APIs Aspose.PSD fornecem meios para ler dados EXIF de uma imagem fornecida. As etapas fornecidas abaixo ilustram o uso da classe ExifData para ler as informações EXIF de uma imagem.

- Carregar a Imagem PSD usando o método factory Load.
- Encontrar a miniatura JPEG entre os recursos do PSD.
- Extrair uma instância da classe ExifData.

Obter as informações necessárias e escrevê-las no console.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-JPEG-LerTodasAsTagsEXIF-LerTodasAsTagsEXIF.java" >}}

Alternativamente, os desenvolvedores também podem obter informações específicas usando o trecho de código a seguir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-JPEG-LerInformacoesEspecificasDeTagsEXIF-LerInformacoesEspecificasDeTagsEXIF.java" >}}
### **Escrevendo e Modificando Dados EXIF**
Usando as APIs Aspose.PSD, os desenvolvedores podem escrever novas informações EXIF e modificar dados EXIF existentes de uma imagem. Ambos os processos (Escrita e Modificação) requerem o carregamento de uma imagem e a obtenção dos dados EXIF em uma instância da classe ExifData. Em seguida, pode-se acessar as propriedades expostas pela classe ExifData para configurá-las conforme necessário. Por favor, note que as imagens para manipulação devem ser imagens JPEG ou TIFF que geralmente são miniaturas PSD. O código de exemplo para demonstrar o uso é o seguinte:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-JPEG-EscreverEModificarDadosEXIF-EscreverEModificarDadosEXIF.java" >}}
## **Extraindo Miniaturas dos Recursos PSD**
Miniaturas são versões em tamanho reduzido de fotos, usadas para exibir uma parte significativa da imagem em vez da moldura completa. Alguns arquivos de imagem (especialmente os tirados com uma câmera digital) têm uma imagem miniatura incorporada no arquivo. A API Aspose.PSD permite extrair miniaturas de recursos PSD e armazená-las separadamente no disco. Os recursos de miniatura contêm a propriedade ExifData.Thumbnail que pode recuperar os dados da miniatura. O trecho de código fornecido abaixo demonstra como usar isso.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-JPEG-ExtrairMiniaturaDoPSD-ExtrairMiniaturaDoPSD.java" >}}

Utilize a abordagem discutida acima para armazenar a miniatura em outros formatos de arquivo suportados. Se deseja exportar os dados da miniatura para outros formatos de imagem como BMP e PNG, por favor, utilize outras opções de exportação de imagem.
### **Extraindo Miniaturas dos Segmentos JFIF**
Também é possível extrair miniaturas do segmento ExifData ou JFIF dos recursos de miniaturas PSD. O código a seguir mostra como realizar a extração dos dados da miniatura do segmento JFIF ou ExifData:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-JPEG-ExtrairMiniaturaDoPSD-ExtrairMiniaturaDoPSD.java" >}}

Utilize a abordagem discutida acima para armazenar a miniatura em outros formatos de arquivo suportados. Se deseja exportar os dados da miniatura para outros formatos de imagem como BMP e PNG, por favor, utilize outras opções de exportação de imagem.
### **Adicionar Miniatura ao Segmento JFIF**
O trecho de código abaixo demonstra como usar a propriedade JFIF.Thumbnail para adicionar uma imagem miniatura ao segmento JFIF de uma imagem PSD carregada:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-JPEG-AdicionarMiniaturaAoSegmentoJFIF-AdicionarMiniaturaAoSegmentoJFIF.java" >}}

Imagens de miniatura com outros dados de segmento não podem ocupar mais do que 65.545 bytes devido às especificações do formato JPEG. Em casos em que imagens grandes devem ser definidas como miniatura, uma exceção pode surgir.
### **Adicionar Miniatura ao Segmento EXIF**
O trecho de código abaixo demonstra como usar a propriedade ExifData.Thumbnail para adicionar uma imagem miniatura ao segmento EXIF de uma imagem PSD carregada:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-JPEG-AdicionarMiniaturaAoSegmentoEXIF-AdicionarMiniaturaAoSegmentoEXIF.java" >}}

Neste caso, a API Aspose.PSD não pode estimar o tamanho da imagem miniatura, mas pode verificar o tamanho de todo o segmento de dados EXIF. Este não pode ser maior do que 65.535 bytes.
## **Utilizando a Classe JpegExifData para Ler e Modificar Tags EXIF de JPEG**
As APIs Aspose.PSD fornecem a classe JpegExifData que é exclusiva para formatos de imagem JPEG para recuperar e atualizar informações EXIF. Este artigo demonstra o uso da classe JpegExifData para alcançar o mesmo. A classe Aspose.PSD.Exif.JpegExifData serve como contêiner de dados EXIF para imagens JPEG e fornece meios para recuperar tags EXIF padrão de JPEG conforme demonstrado abaixo:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-JPEG-AdicionarMiniaturaAoSegmentoEXIF-AdicionarMiniaturaAoSegmentoEXIF.java" >}}
### **Lista Completa de Tags EXIF**
O trecho de código acima lê algumas Tags EXIF usando as propriedades oferecidas pela classe Aspose.PSD.Exif.JpegExifData. A lista completa dessas propriedades está disponível aqui. O código a seguir lerá todas as tags EXIF usando a classe System.Reflection.PropertyInfo.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-JPEG-LerTodasAsListasDeTagsEXIF-LerTodasAsListasDeTagsEXIF.java" >}}
## **Correção Automática de Orientação de Imagens JPEG**
As fotos podem ser tiradas com uma câmera rotacionada em 90°, 180°, 270° ou nenhum (orientação normal). A maioria das câmeras digitais armazena a informação de orientação juntamente com os dados da imagem como tags EXIF das imagens JPEG. Esta informação pode ser usada para realizar a rotação automática nas imagens para corrigir a orientação. As APIs Aspose.PSD fornecem o método AutoRotate para a classe JpegImage para corrigir automaticamente a orientação das imagens JPEG. Veja como você pode usar o método AutoRotate com a API Aspose.PSD para Java.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-JPEG-CorrecaoAutomaticaDeOrientacaoDeImagensJPEG-CorrecaoAutomaticaDeOrientacaoDeImagensJPEG.java" >}}
## **Suporte para JPEG-LS com CMYK e YCCK**
A API Aspose.PSD para Java fornece suporte para modelos de cores CMYK e YCCK com JPEG-LS. O trecho de código abaixo demonstra como usar esse suporte para JPEG-LS.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-JPEG-SuporteParaJPEGLSComCMYK-SuporteParaJPEGLSComCMYK.java" >}}
## **Suporte para 2-7 bits por amostra em imagens JPEG-LS**


A API Aspose.PSD para Java fornece suporte para imagens JPEG-LS de 2-7 bits por amostra. O trecho de código abaixo demonstra como usar esse suporte para JPEG-LS.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-JPEG-SuportePara2E7BitsJPEG-SuportePara2E7BitsJPEG.java" >}}
## **Configurando ColorType e CompressionType para imagens JPEG**




A API Aspose.PSD para Java fornece suporte para Color Type e Compression Type e os configura como escala de cinza e progressivo para imagens JPEG. O trecho de código abaixo demonstra como usar esse suporte.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-JPEG-TipoDeCorECompressao-TipoDeCorECompressao.java" >}}




