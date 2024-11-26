---
title: Trabalhando com Camadas de Texto
type: docs
weight: 170
url: /pt/trabalhando-com-camadas-de-texto/
---

## **Adicionar Camada de Texto**
Aspose.PSD para .NET permite adicionar camadas de texto em um arquivo PSD. Os passos para adicionar uma camada de texto em um arquivo PSD são tão simples quanto abaixo:

- Carregue um arquivo PSD como uma imagem usando o método de fábrica [**Load**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index) exposto pela classe [Image](https://reference.aspose.com/psd/net/aspose.psd/image)
- Chame o método [**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer) que aceita texto e uma instância da classe [**Rectangle**](https://reference.aspose.com/psd/net/aspose.psd/rectangle)
- Salve os resultados

O trecho de código abaixo mostra como adicionar uma camada de texto em um arquivo PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}

## **Definir Posição da Camada de Texto**
Aspose.PSD para .NET permite definir a posição de uma camada de texto em um arquivo PSD. Os passos para definir a posição de uma camada de texto em um arquivo PSD são tão simples quanto abaixo:

- Carregue um arquivo PSD como uma imagem usando o método de fábrica Load exposto pela classe Image
- Chame o método AddTextLayer especificando as posições esquerda e superior da camada de texto
- Salve os resultados

O trecho de código abaixo mostra como definir a posição de uma camada de texto em um arquivo PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}

## **Obter Propriedades de Texto de uma Camada de Texto**
Usando Aspose.PSD para .NET, você pode obter e atualizar as propriedades de texto de diferentes partes de texto disponíveis em uma camada de texto PSD. Este artigo demonstra como você pode obter Parágrafos, Estilos e Propriedades de Texto da camada de texto e atualizá-los.

O trecho de código abaixo mostra como realizar esse requisito.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}

Aqui está outro exemplo que demonstra como um desenvolvedor pode obter a formatação de texto de diferentes partes de texto do [TextLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/textlayer) usando [Aspose.PSD para .NET](https://products.aspose.com/psd/net).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}

## **Atualizar Camada de Texto no Arquivo PSD**
Aspose.PSD para .NET permite manipular o texto na camada de texto de um arquivo PSD. Por favor, use a classe Aspose.PSD.FileFormats.Psd.Layers.TextLayer para atualizar o texto na camada PSD. O trecho de código a seguir carrega um arquivo PSD, acessa a camada de texto, atualiza o texto e salva o arquivo PSD com um novo nome usando o método [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}

## **Suporte de Camadas de Texto em Tempo de Execução**
Este artigo mostra como adicionar camadas de texto em tempo de execução para imagens PSD. O trecho de código foi fornecido abaixo.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
