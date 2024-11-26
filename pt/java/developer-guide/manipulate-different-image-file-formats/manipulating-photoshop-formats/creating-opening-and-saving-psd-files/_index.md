---
title: Criar, Abrir e Salvar Arquivos PSD
type: docs
weight: 10
url: /pt/java/criar-abrir-e-salvar-arquivos-psd/
---

## **Exportando Imagem para PSD**
PSD, documento do PhotoShop, é o formato de arquivo padrão usado pelo Adobe PhotoShop para trabalhar com imagens. O Aspose.PSD permite que você carregue, edite e salve arquivos no formato PSD para que possam ser abertos e editados no PhotoShop. Este artigo mostra como salvar um arquivo no formato PSD com Aspose.PSD, e também discute algumas das configurações que podem ser utilizadas ao salvar nesse formato. PsdOptions é uma classe especializada no namespace ImageOptions usada para exportar imagens para PSD. Para exportar para PSD, crie uma instância da classe Image, seja carregada de um arquivo de imagem existente (por exemplo, miniaturas) ou criada do zero. Este artigo explica como. Nos exemplos abaixo, uma imagem é criada do zero. Assim que for criada e os dados de pixels forem populados, salve a imagem usando o método Save da classe Image e forneça um objeto PsdOptions como segundo argumento. Várias propriedades da classe PsdOptions podem ser definidas para conversões avançadas. Algumas das propriedades são ColorMode, CompressionMethod e Version. O Aspose.PSD suporta os seguintes métodos de compressão por meio da enumeração CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Os seguintes modos de cor são suportados por meio da enumeração ColorModes:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



Recursos adicionais podem ser adicionados, como recursos de miniaturas para PSD v4.0, v5.0 e superiores, ou recursos de grade e guia para PSD v4.0 e superiores. O código abaixo cria um arquivo BMP do zero, popula os pixels e o salva no PSD com compressão RLE e modo de cor em escala de cinza. O trecho de código a seguir mostra como exportar uma imagem para PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-PSD-ExportarImagemParaPSD-ExportarImagemParaPSD.java" >}}

## **Importando imagem para camada PSD**
Este artigo demonstra o uso do Aspose.PSD para adicionar ou importar uma imagem para uma camada PSD. As APIs do Aspose.PSD expuseram métodos eficientes e fáceis de usar para alcançar esse objetivo. O Aspose.PSD expôs o método DrawImage da classe Layer para adicionar/importar uma imagem em um arquivo PSD. O método DrawImage precisa de valores de localização e imagem para adicionar/importar uma imagem em um arquivo PSD. Os passos para importar uma imagem para a camada PSD são simples, como abaixo:

- Carregar um arquivo PSD como uma imagem usando o método de fábrica Load exposto pela classe Image.
- Criar uma instância da classe Layer e atribuir a camada de imagem PSD a ela.
- Carregar a imagem que precisa ser adicionada ou criar uma do zero.
- Chamar o método Layer.DrawImage especificando a localização e instância da imagem.
- Salvar os resultados.



O trecho de código a seguir mostra como importar a imagem para a camada PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-PSD-ImportarImagemParaCamadaPSD-ImportarImagemParaCamadaPSD.java" >}}


## **Criar Miniaturas a partir de Arquivos PSD**
PSD é o formato de documento nativo da aplicação Adobe Photoshop. O Adobe Photoshop (versão 5.0 e posterior) armazena informações de miniatura para exibição de pré-visualização em um bloco de recursos de imagem que consiste em um cabeçalho inicial de 28 bytes, seguido de uma miniatura JFIF na ordem RGB (vermelho, verde, azul). A API Aspose.PSD fornece um mecanismo fácil de usar para acessar os recursos de um arquivo PSD. Esses recursos incluem também a miniatura que, por sua vez, pode ser buscada e salva no disco de acordo com as necessidades da aplicação. O trecho de código a seguir mostra como criar miniaturas a partir de arquivos PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-PSD-CriarMiniaturasDeArquivosPSD-CriarMiniaturasDeArquivosPSD.java" >}}


## **Criar Arquivos PSD Indexados**
O Aspose.PSD para a API Java pode criar arquivos PSD indexados a partir do zero. Este artigo demonstra o uso das classes PsdOptions e PsdImage para criar um PSD indexado enquanto desenha algumas formas sobre o novo canvas criado. Os seguintes passos simples são necessários para criar um arquivo PSD indexado.

- Criar uma instância de PsdOptions e definir sua origem.
- Definir a propriedade ColorMode do PsdOptions para ColorModes.Indexed.
- Criar uma nova paleta de cores do espaço RGB e defini-la como propriedade Palette do PsdOptions.
- Definir a propriedade CompressionMethod para o algoritmo de compressão necessário.
- Criar uma nova imagem PSD chamando o método PsdImage.Create.
- Desenhar gráficos ou realizar outras operações conforme necessário.
- Chamar o método PsdImage.Save para confirmar todas as alterações.



O trecho de código a seguir mostra como criar arquivos PSD indexados.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-PSD-CriarArquivosPSDIndexados-CriarArquivosPSDIndexados.java" >}}
## **Exportar Camada PSD para Imagem Raster**
O Aspose.PSD para Java permite que você exporte camadas em um arquivo PSD para imagens raster. Utilize o método Save da classe Aspose.PSD.FileFormats.Psd.Layers.Layer para exportar a camada para a imagem. O seguinte código de exemplo carrega um arquivo PSD e exporta cada uma de suas camadas para uma imagem PNG usando o Layer.Save da classe Aspose.PSD.FileFormats.Psd.Layers.Layer. Uma vez que todas as camadas são exportadas para imagens PNG, você pode abri-las usando o seu visualizador de imagens favorito. O trecho de código a seguir mostra como exportar a camada PSD para imagem raster.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-PSD-ExportarCamadaPSDParaImagemRaster-ExportarCamadaPSDParaImagemRaster.java" >}}
