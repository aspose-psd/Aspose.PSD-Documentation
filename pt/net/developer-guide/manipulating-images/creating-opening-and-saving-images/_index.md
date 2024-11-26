---
title: Criando, Abrindo e Salvando Imagens
type: docs
weight: 30
url: /pt/net/criando-abrindo-e-salvando-imagens/
---

## **Criando Arquivos de Imagem**
O Aspose.PSD para .NET permite que os desenvolvedores criem suas próprias imagens. Use o método estático Create exposto pela classe Image para criar novas imagens. Tudo que você precisa fazer é fornecer o objeto apropriado de uma das classes do namespace ImageOptions para o formato de imagem de saída desejado. Para criar um arquivo de imagem, primeiro crie uma instância de uma das classes do namespace ImageOptions. Essas classes determinam o formato de imagem de saída. Abaixo estão algumas classes do namespace ImageOptions (observe que apenas os formatos de arquivo PSD são atualmente suportados para criação):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) define as opções para criar um arquivo PSD. Arquivos de imagem podem ser criados definindo um caminho de saída ou definindo um stream.
### **Criando Definindo um Caminho**
Crie PsdOptions a partir do [namespace ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) e defina as várias propriedades. A propriedade mais importante a ser definida é a propriedade Source. Esta propriedade especifica onde os dados da imagem estão localizados (em um arquivo ou em um stream). No exemplo abaixo, a origem é um arquivo. Após definir as propriedades, passe o objeto para um dos métodos estáticos [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) juntamente com os parâmetros de largura e altura. A largura e a altura são definidas em pixels.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-DrawingAndFormattingImages-CriandoDefinindoCaminho-CriandoDefinindoCaminho.cs" >}}
### **Criando Usando Stream**
O processo para criar uma imagem usando um stream é o mesmo que usar um caminho. A única diferença é que você precisa criar uma instância de [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) passando um objeto Stream para seu construtor e atribuindo-o à propriedade Source.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-DrawingAndFormattingImages-CriandoUsandoStream-CriandoUsandoStream.cs" >}}
## **Abrindo Arquivos de Imagem**
Os desenvolvedores podem usar a API Aspose.PSD para .NET para abrir arquivos de imagem PSD existentes para diferentes fins, como adicionar efeitos à imagem ou converter um arquivo existente para outro formato. Seja qual for o propósito, o Aspose.PSD fornece duas maneiras padrão de abrir arquivos existentes: por arquivo ou por um stream.
### **Abrindo do Disco**
Abra um arquivo de imagem passando o caminho e o nome do arquivo como parâmetro para o método estático Load exposto pela classe Image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversao-SalvandoemDisco-SalvandoemDisco.cs" >}}
### **Abrindo usando um Stream**
Às vezes, a imagem que precisamos abrir está armazenada como um stream. Nesses casos, use a versão sobrecarregada do método Load. Este método aceita um objeto Stream como argumento para abrir a imagem.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversao-CarregandoDoStream-CarregandoDoStream.cs" >}}
### **Carregar Imagem como Camada**
Este artigo demonstra o uso do Aspose.PSD para carregar uma imagem como uma camada. O Aspose.PSD expõe APIs eficientes e fáceis de usar para alcançar esse objetivo. O Aspose.PSD expôs o método AddLayer da classe PsdImage para adicionar uma imagem em um arquivo PSD como uma camada.

Os passos para carregar uma imagem no PSD como camada são simples como abaixo:

- Crie uma instância de uma imagem usando a classe PsdImage com uma largura e altura especificadas.
- Carregue um arquivo PSD como imagem usando o método de fábrica Load exposto pela classe Image.
- Crie uma instância da classe Layer e atribua a camada de imagem PSD a ela.
- Adicione a camada criada usando o método AddLayer exposto pela classe PsdImage
- Salve os resultados.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificacaoEConversaoImagens-PSD-CarregarImagemParaPSD-CarregarImagemParaPSD.cs" >}}
### **Carregar Imagem como Camada de um Stream**
Este artigo demonstra o uso do Aspose.PSD para carregar uma imagem como uma camada de um stream. Para carregar uma imagem de um stream, basta passar um objeto stream que contenha uma imagem para o construtor da classe Layer. Adicione a camada criada usando o método AddLayer exposto pela classe PsdImage e salve os resultados.


Aqui está o código de exemplo.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Abertura-CarregandoImagemDoStream-CarregandoImagemDoStream.cs" >}}
## **Salvando Arquivos de Imagem**
O Aspose.PSD permite que você crie arquivos de imagem do zero. Ele também fornece os meios para editar arquivos de imagem existentes. Uma vez que a imagem é criada ou modificada, o arquivo geralmente é salvo no disco. O Aspose.PSD fornece métodos para salvar imagens em um disco especificando um caminho ou usando um objeto Stream.
### **Salvando no Disco**
A classe Image representa um objeto de imagem, então essa classe fornece todas as ferramentas necessárias para criar, carregar e salvar um arquivo de imagem. Use o método Save da classe Image para salvar imagens. Uma versão sobrecarregada do método Save aceita a localização do arquivo como uma string.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversao-SalvandoemDisco-SalvandoemDisco.cs" >}}
### **Salvando em um Stream**
Outra versão sobrecarregada do método Save aceita o objeto Stream como argumento e salva o arquivo de imagem no stream.

Se a imagem for criada especificando qualquer uma das CreateOptions no construtor de Image, a imagem será automaticamente salva no caminho ou stream fornecido durante a inicialização da classe Image chamando o método Save que não aceita nenhum parâmetro.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversao-SalvandoEmStream-SalvandoEmStream.cs" >}}
### **Configuração para Substituir Fontes Ausentes**
Os desenvolvedores podem usar a API Aspose.PSD para .NET para carregar arquivos de imagem PSD existentes para diferentes fins, por exemplo, para definir um nome de fonte padrão ao salvar documentos PSD como uma imagem rasterizada (em formatos PNG, JPG e BMP). Esta fonte padrão deve ser usada como substituição para todas as fontes ausentes (fontes que não são encontradas no Sistema Operacional atual). Uma vez que a imagem é modificada, o arquivo será salvo no disco.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-Conversao-ConfiguracaoParaSubstituirFontesAusentes-ConfiguracaoParaSubstituirFontesAusentes.cs" >}}
