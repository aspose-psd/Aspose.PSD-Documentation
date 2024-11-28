---
title: Manipulação de Formatos do Adobe Photoshop
type: docs
weight: 20
url: /pt/net/manipulacao-de-formatos-adobe-photoshop/
---

## **Fundir camadas PSD em outras camadas**

## **Exportar Imagem para PSD**
PSD, documento do Photoshop, é o formato de arquivo padrão usado pelo Adobe Photoshop para trabalhar com imagens. Aspose.PSD permite que você carregue, edite e salve arquivos em PSD para que possam ser abertos e editados no Photoshop. Este artigo mostra como salvar um arquivo em PSD com Aspose.PSD e também discute algumas das configurações que podem ser usadas ao salvar neste formato. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) é uma classe especializada no namespace [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) usada para exportar imagens para PSD. Para exportar para PSD, crie uma instância da classe Image, carregada de um arquivo de imagem existente (miniaturas, por exemplo) ou criada do zero. Este artigo explica como fazer isso. Nos exemplos abaixo, uma imagem é criada do zero. Depois que ela é criada e os dados de pixel são populados, salve a imagem usando o método Save da classe Image e forneça um objeto PsdOptions como segundo argumento. Várias propriedades da classe PsdOptions podem ser configuradas para conversões avançadas. Algumas das propriedades são Modo de cor, [Método de compressão](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) e Versão. Aspose.PSD oferece suporte aos seguintes métodos de compressão por meio da enumeração CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Os seguintes modos de cor são suportados por meio da enumeração [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes):

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB


Recursos adicionais podem ser adicionados, como recursos de miniatura para PSD v4.0, v5.0 e superiores, ou recursos de grade e guia para PSD v4.0 e superiores. O código abaixo cria um arquivo de imagem do zero, popula os pixels e o salva em PSD com compressão RLE e modo de cor em escala de cinza. O trecho de código a seguir mostra como exportar uma imagem para PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-PSD-ExportarImagemParaPSD-ExportarImagemParaPSD.cs" >}}
## **Importando imagem para camada PSD**
Este artigo demonstra o uso do Aspose.PSD para adicionar ou importar uma imagem para uma camada PSD. As APIs do Aspose.PSD expõem métodos eficientes e fáceis de usar para alcançar esse objetivo. O Aspose.PSD expôs o método [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) da classe Layer para adicionar/importar uma imagem em um arquivo PSD. O método DrawImage precisa de valores de localização e imagem para adicionar/importar uma imagem em um arquivo PSD. Os passos para importar uma imagem para a camada PSD são simples como abaixo:

- Carregue um arquivo PSD como uma imagem usando o método de fabrica Load exposto pela classe Image.
- Crie uma instância da classe Layer com o stream com arquivo Png, Jpeg, Tiff, Gif, Bmp, Psd ou j2k
- Adicione a camada ao PSD usando o método AddLayer
- Salve os resultados.


O trecho de código a seguir mostra como importar a imagem para a camada PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Abertura-CarregandoImagemDoStream-CarregandoImagemDoSteam.cs" >}}
## **Substituição de cor em camadas PSD**
Este artigo demonstra o uso do Aspose.PSD para adicionar ou importar uma imagem para uma camada PSD. As APIs do Aspose.PSD expõem métodos eficientes e fáceis de usar para alcançar esse objetivo. O Aspose.PSD expôs o método DrawImage da classe Layer para adicionar/importar uma imagem em um arquivo PSD. O método DrawImage precisa de valores de localização e imagem para adicionar/importar uma imagem em um arquivo PSD. Os passos para importar uma imagem para a camada PSD são simples como abaixo:

- Carregue um arquivo PSD como uma imagem usando o método de fábrica Load exposto pela classe Image.
- Crie uma instância da classe Layer e atribua a camada de imagem PSD a ela.
- Carregue a imagem que precisa ser adicionada ou crie uma do zero.
- Chame o método Layer.DrawImage enquanto especifica localização e instância de imagem.
- Salve os resultados.


O trecho de código a seguir mostra como importar uma imagem para a camada PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-PSD-SubstituicaoDeCorEmPSD-SubstituicaoDeCorEmPSD.cs" >}}
## **Criando Miniaturas de Arquivos PSD**
PSD é o formato de documento nativo da aplicação Photoshop da Adobe. O Adobe Photoshop (versão 5.0 e posterior) armazena informações de miniatura para exibição de pré-visualização em um bloco de recursos de imagem que consiste em um cabeçalho inicial de 28 bytes, seguido de uma miniatura JFIF em ordem RGB (vermelho, verde, azul). A API Aspose.PSD fornece um mecanismo fácil de usar para acessar os recursos do arquivo PSD. Esses recursos também incluem o recurso de miniatura que, por sua vez, pode ser recuperado e salvo no disco conforme as necessidades da aplicação. O trecho de código a seguir mostra como criar miniaturas a partir de arquivos PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-PSD-CriarMiniaturasDeArquivosPSD-CriarMiniaturasDeArquivosPSD.cs" >}}
## **Criando Arquivos PSD Indexados**
A API do Aspose.PSD para .NET pode criar arquivos PSD indexados do zero. Este artigo demonstra o uso das classes PsdOptions e [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage) para criar um PSD indexado enquanto desenha algumas formas sobre o canvas recém-criado. Os seguintes passos simples são necessários para criar um arquivo PSD indexado:

- Criar uma instância de PsdOptions e definir sua fonte.
- Definir a propriedade ColorMode das PsdOptions para ColorModes.Indexed.
- Criar uma nova paleta de cores do espaço RGB e defini-la como propriedade Palette das PsdOptions.
- Definir a propriedade CompressionMethod para o algoritmo de compressão necessário.
- Criar uma nova imagem PSD chamando o método PsdImage.[Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create).
- Desenhar gráficos ou executar outras operações conforme necessário.
- Chamar o método PsdImage.Save para finalizar todas as alterações.


O trecho de código a seguir mostra como criar arquivos PSD indexados.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-PSD-CriarArquivosPSDIndexados-CriarArquivosPSDIndexados.cs" >}}
## **Exportar Camada PSD para Imagem Rasterizada**
O Aspose.PSD para .NET permite exportar camadas em um arquivo PSD para imagens rasterizadas. Use o método [Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) para exportar a camada para a imagem. O código de exemplo a seguir carrega um arquivo PSD e exporta cada uma de suas camadas para uma imagem PNG usando o método Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Quando todas as camadas são exportadas para imagens PNG, você pode abri-las usando o visualizador de imagens de sua preferência. O trecho de código a seguir mostra como exportar uma camada PSD para uma imagem rasterizada.


{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-PSD-ExportarCamadaPSDParaImagemRasterizada-ExportarCamadaPSDParaImagemRasterizada.cs" >}}
## **Atualizar Camada de Texto no Arquivo PSD**
O Aspose.PSD para .NET permite manipular o texto na camada de texto de um arquivo PSD. Use a classe [Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) para atualizar o texto na camada PSD. O trecho de código a seguir carrega um arquivo PSD, acessa a camada de texto, atualiza o texto e salva o arquivo PSD com um novo nome usando o método [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index).


{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-PSD-AtualizarCamadaDeTextoNoArquivoPSD-AtualizarCamadaDeTextoNoArquivoPSD.cs" >}}
## **Detectar PSD Achatado**
O Aspose.PSD para .NET permite detectar se um determinado arquivo PSD está achatado ou não. A propriedade IsFlatten foi introduzida na classe Aspose.PSD.FileFormats.Psd.PsdImage para alcançar essa funcionalidade. O trecho de código a seguir carrega um arquivo PSD e acessa a propriedade [IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/isflatten).


{{< gist "aspos-d34143c775c0c75c4cc4175c775c9" "Exa-CShar-Aspose-ModConImgs-PS-DetectFlattenedPSD-DetectFlattenedPSD.cs" >}}
## **Fundir camadas PSD**
Este artigo mostra como fundir camadas em um arquivo PSD ao converter um arquivo PSD para JPG com o Aspose.PSD. No exemplo abaixo, um arquivo PSD existente é carregado passando o caminho do arquivo para o método estático Load da classe Image. Depois de carregá-lo, converta/caste a imagem para PsdImage. Crie uma instância da classe JpegOptions e defina suas várias propriedades. Agora chame o método Save da instância PsdImage. O trecho de código a seguir mostra como fundir camadas PSD.


{{< gist "aspost384634c3c8347051" "Exa-CShar-Aspose-ModConImgs-PS-MergePSDlayers-MergePSDlayers.cs" >}}
## **Suporte em Escala de Cinza com Alfa para PSD**
Este artigo mostra como oferecer suporte em escala de cinza com alfa para um arquivo PSD ao converter um arquivo PSD para PNG com Aspose.PSD. No exemplo abaixo, um arquivo PSD existente é carregado passando o caminho do arquivo para o método estático Load da classe Image. Depois de carregá-lo, converta/caste a imagem para PsdImage. Crie uma instância da classe PngOptions e defina suas várias propriedades. Defina a propriedade [ColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) para TruecolorWithAlpha. Agora chame o método Save da instância PngOptions. O trecho de código a seguir mostra como converter para PNG em escala de cinza com alfa.


{{< gist "aspost3834c5c853175c" "Exa-CShar-Aspose-ModConImgs-PS-GrayScaleSupportForAlpha-GrayScaleSupportForAlpha.cs" >}}
## **Suporte para Efeitos de Camada para PSD**
Este artigo mostra como suportar diferentes efeitos como **Desfoque**, **Brilho Interno**, **Brilho Externo** para uma camada PSD. O trecho de código a seguir mostra como suportar efeitos de camada.


{{< gist "aspost349c7c9175" "Exa-CShar-Aspose-ModConImgs-PS-SupportLayerForPSD-SupportLayerForPSD.cs" >}}
## **Suporte para Data e Hora da Criação da Camada em PSD**
Este artigo mostra como suportar a criação da camada de data e hora para uma camada PSD. O trecho de código a seguir mostra como criar camadas.


{{< gist "aspost3c0ce9475c9" "Exa-CShar-Aspose-ModConImgs-PS-DLayerCreationDateTime-LayerCreationDateTime.cs" >}}
## **Suporte para Realce de Cor de Planilha**
Este artigo mostra como carregar imagens PSD, em seguida, alterar e destacar cores de planilhas e salvar isso como uma imagem. O trecho de código foi fornecido.

{{< gist "aspos3397c0c17c0c975c9e175c" "Exa-CShar-Aspose-ModConImgs-PS-SheetColoHightlighting-SheetColoHightlighting.cs" >}}
## **Suporte para Máscara de Camada**
Este artigo mostra como suportar a camada de máscara para imagens PSD e depois salvar essas imagens. O trecho de código foi fornecido abaixo.

{{< gist "asposta4c9d34ce8575c0ce974175c" "Exa-CShar-Aspose-ModConImgs-PS-SupptOfLayerMask-SupptOfLayerMask.cs" >}}
## **Suporte para Máscara Vetorial de Camada**
Este artigo mostra o suporte para máscaras vetoriais de camada para o Aspose.PSD. O trecho de código a seguir mostra como o Aspose.PSD suporta máscaras vetoriais de camada.

{{< gist "asposa4c9d34ce856c0ce974175" "Exa-CShar-Aspose-ModConImgs-PS-SupptOfLayerVectorMask-SupptOfLayerVectorMask.cs" >}}
## **Suporte para Camadas de Texto em Tempo de Execução**
Este artigo mostra como adicionar camadas de texto em tempo de execução para imagens PSD. O trecho de código foi fornecido abaixo.

{{< gist "aspost99d34ce8475c0ce974175c" "Exa-CShar-Aspose-DrawingAndFormattingImgs-AdEfecttAtRunTime-AdEfecttAtRunTime.cs" >}}
## **Suporte para Camadas de Ajuste**
Este artigo mostra como ajustar camadas e, em seguida, se a camada for nula, mesclar a camada e salvar como imagens PSD. O trecho de código foi fornecido abaixo.

{{< gist "aspose-psd" "c68d1f8aa6f2af15b98e4d34e14a504a" "Exemplos-CShar-Aspose-ModificandoEConvertendoImagens-PSD-SuporteDeCamadasDeAjuste-SuporteDeCamadasDeAjuste.cs" >}}
## **Gerenciando Brilho e Contraste em Camadas de Ajuste**
Este artigo mostra como iterar através de camadas e gerenciar brilho e contraste em camadas e, em seguida, salvar como imagens PSD. O trecho de código foi fornecido abaixo.

{{< gist "aspost9d34ce8575c0ce974175c" "Exa-CShar-Aspose-ModConImgs-PS-ManageBrightnessContrasAjustLayer-ManageBrightnessContrasAjustLayer.cs" >}}
## **Gerenciando Camadas de Exposição**
Este artigo mostra como adicionar e editar camadas de exposição e gerenciar camadas de exposição e, em seguida, salvar como imagens PSD. O trecho de código foi fornecido abaixo.

{{< gist "asposskd34ce856c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-PSD-ManageExposureAjustLayer-ManageExposureAjustLayer.cs" >}}
## **Gerenciando Camadas de Mistura de Canais**
Este artigo mostra como gerenciar camadas de ajuste de mistura de canais e definir diferentes cores e, em seguida, salvar como imagens PSD. O trecho de