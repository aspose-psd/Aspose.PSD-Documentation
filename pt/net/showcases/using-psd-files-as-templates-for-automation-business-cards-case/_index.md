---
title: Usar arquivos PSD como modelos para automação - Caso de cartões de visita
type: docs
weight: 10
url: /pt/usar-arquivos-psd-como-modelos-para-automacao-caso-de-cartoes-de-visita/
---

### **Visão geral**
Este artigo descreve casos frequentemente usados quando é necessário atualizar algumas camadas em um [arquivo PSD](https://wiki.fileformat.com/image/psd/) programaticamente, onde o arquivo PSD/PSB tem uma estrutura semelhante a um modelo conhecido. Isso pode ser útil para criar um grande número de cartões de visita para pessoas diferentes (Caso de cartões de visita). Ou se precisar traduzir o arquivo PSD para diferentes idiomas com a substituição de algum material gráfico nele.

Após ler este artigo, você saberá como pode fazer isso:

![todo:image_alt_text](usar-arquivos-psd-como-modelos-para-automacao-caso-de-cartoes-de-visita_1.png)
## **Caso simples**
Por exemplo, você tem um Modelo de PSD com os Nomes das Camadas conhecidos. Então você precisa alterar, atualizar ou substituir a Camada PSD via C#. Primeiramente, você precisa abrir o arquivo do modelo com Aspose.PSD.

Como abrir um arquivo PSD via C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-CSharp-Aspose-PsdFileComoModelo-Snippet-1.cs" >}}

![todo:image_alt_text](usar-arquivos-psd-como-modelos-para-automacao-caso-de-cartoes-de-visita_2.png)

Depois, precisamos encontrar a camada que queremos substituir pelo seu nome. Aqui está uma implementação simples para isso.

Como encontrar a camada no arquivo PSD pelo nome dela

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-CSharp-Aspose-PsdFileComoModelo-Snippet-2.cs" >}}


Quando a camada é encontrada, podemos atualizá-la da maneira usual, usando [Gráficos](https://reference.aspose.com/psd/net/aspose.psd/graphics):

Como Desenhar na Camada PSD com Gráficos

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-CSharp-Aspose-PsdFileComoModelo-Snippet-3.cs" >}}

Neste caso, desenhamos uma imagem [PNG](https://wiki.fileformat.com/image/png/) recém-carregada na camada PSD existente, para que os dados antigos sejam perdidos no novo arquivo.

Mas e se também precisarmos atualizar texto? O processo será semelhante. Encontrar a [Camada de Texto](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) pelo nome e então atualizamos programaticamente [a Camada de Texto do arquivo do Photoshop](/psd/pt/net/renderizar-texto-com-diferentes-cores-em-camada-de-texto/).

Como atualizar a Camada de Texto no Photoshop usando C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-CSharp-Aspose-PsdFileComoModelo-Snippet-4.cs" >}}


No final, precisamos salvar nossas alterações:

Como salvar o arquivo PSD alterado usando o [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-CSharp-Aspose-PsdFileComoModelo-Snippet-5.cs" >}}


A imagem resultante:

![todo:image_alt_text](usar-arquivos-psd-como-modelos-para-automacao-caso-de-cartoes-de-visita_3.png)


## **Um caso complexo com recursos adicionais**
Acima mostramos a maneira mais simples de substituir uma imagem em uma camada de Arquivo PSD.

Mas o Aspose.PSD pode oferecer recursos adicionais mais complexos, como adicionar uma nova camada, remover camadas antigas e atualizar camadas de texto usando estilos diferentes em texto multi-linha.

Podemos encontrar a [Camada](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer) que queremos substituir, então encontramos seu índice na Lista de Camadas, removemos ele e inserimos uma nova Camada depois de criá-la a partir de um [Arquivo Jpeg](https://wiki.fileformat.com/image/jpeg/) no mesmo local.

Criar uma nova camada a partir de um arquivo e inseri-la na Imagem PSD usando [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-CSharp-Aspose-PsdFileComoModelo-Snippet-6.cs" >}}


No final deste trecho de código do arquivo, corrigimos a posição da camada e salvamos a nova matriz de Camadas na Imagem PSD.

Como copiar propriedades de Camada de [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-CSharp-Aspose-PsdFileComoModelo-Snippet-7.cs" >}}


E, por fim, precisamos atualizar camadas de texto na imagem PSD existente por C#. O Aspose.PSD suporta [a atualização de Camada de Texto por Porções](/psd/pt/net/trabalhando-com-camadas-de-texto/). Cada [porção de texto](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) possui uma combinação única de propriedades de Estilo e Parágrafo.

Como copiar propriedades de Camada de [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-CSharp-Aspose-PsdFileComoModelo-Snippet-8.cs" >}}


Como resultado, alteramos o modelo PSD via código com uma nova Camada de um arquivo Jpeg, Png, J2k, Bmp, Gif, ou TIFF e texto multi-linha com [diferentes estilos](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) em cada linha.

![todo:image_alt_text](usar-arquivos-psd-como-modelos-para-automacao-caso-de-cartoes-de-visita_4.png)
