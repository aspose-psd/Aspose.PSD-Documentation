---
title: Manipulação de Formatos do Photoshop
type: docs
weight: 10
url: /java/manipulando-formatos-do-photoshop/
---

## **Substituição de Cor em Camadas PSD**
O Aspose.PSD para Java permite que você altere a cor de fundo de cada camada de um arquivo PSD. Por favor, utilize a classe Aspose.PSD.FileFormats.Psd.Layers.BackgroundColor para alterar a cor de fundo da camada no PSD. O trecho de código a seguir carrega um arquivo PSD, acessa a camada, atualiza a cor de fundo e salva o arquivo PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-PSD-SubstituicaoDeCorNaCamadaPSD-SubstituicaoDeCorNaCamadaPSD.java" >}}

## **Atualizar Camada de Texto no Arquivo PSD**
O Aspose.PSD para Java permite que você manipule o texto na camada de texto de um arquivo PSD. Por favor, utilize a classe Aspose.PSD.FileFormats.Psd.Layers.TextLayer para atualizar o texto na camada PSD. O trecho de código abaixo carrega um arquivo PSD, acessa a camada de texto, atualiza o texto e salva o arquivo PSD com um novo nome usando o método TextLayer.UpdateText da classe TextLayer.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.java" >}}

## **Detectando PSD Achatados**
O Aspose.PSD para Java permite que você detecte se um arquivo PSD fornecido está achatado ou não. A propriedade IsFlatten foi introduzida na classe Aspose.PSD.FileFormats.Psd.PsdImage para alcançar essa funcionalidade. O trecho de código abaixo carrega um arquivo PSD e acessa a propriedade IsFlatten.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-PSD-DetectFlattenedPSD-DetectFlattenedPSD.java" >}}

## **Mesclar Camadas PSD**
Esse artigo mostra como mesclar camadas em um arquivo PSD ao converter um PSD para JPG com o Aspose.PSD. No exemplo abaixo, um arquivo PSD existente é carregado passando o caminho do arquivo para o método estático Load da classe Image. Após carregá-lo, converta a imagem para PsdImage. Crie uma instância da classe JpegOptions e defina várias propriedades. Agora, chame o método Save da instância de PsdImage. O trecho de código abaixo mostra como mesclar camadas PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-PSD-MergePSDLayers-MergePSDLayers.java" >}}

## **Suporte a Escala de Cinza com Alfa para PSD**
Esse artigo mostra como suportar a escala de cinza com alfa para um arquivo PSD ao converter um PSD para PNG com o Aspose.PSD. No exemplo abaixo, um arquivo PSD existente é carregado passando o caminho do arquivo para o método estático Load da classe Image. Após carregá-lo, converta a imagem para PsdImage. Crie uma instância da classe PngOptions e defina suas várias propriedades. Configure a propriedade ColorType para TruecolorWithAlpha. Agora, chame o método Save da instância PngOptions. O trecho de código abaixo mostra como converter para PNG em escala de cinza com alfa.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-ModificandoEConvertendoImagens-PSD-GrayScaleSupportForAlpha-GrayScaleSupportForAlpha.java" >}}

Restante do artigo não foi traduzido.