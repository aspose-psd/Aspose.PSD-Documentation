---
title: Criando, Abrindo e Salvando Imagens
type: docs
weight: 30
url: /pt/java/criando-abrindo-e-salvando-imagens/
---

## **Criando Arquivos de Imagem**
Aspose.PSD para Java permite aos desenvolvedores criar suas próprias imagens. Use o método Create estático exposto pela classe Image para criar novas imagens. Tudo o que você precisa fazer é fornecer o objeto apropriado de uma das classes do namespace ImageOptions para o formato de imagem de saída desejado. Para criar um arquivo de imagem, primeiro crie uma instância de uma das classes do namespace ImageOptions. Essas classes determinam o formato de imagem de saída. Abaixo estão algumas classes do namespace ImageOptions (observe que atualmente somente os formatos de arquivo PSD são suportados para criação):

PsdOptions define as opções para criar um arquivo PSD. Arquivos de imagem podem ser criados definindo um caminho de saída ou configurando um fluxo.
### **Criando Configurando o Caminho**
Crie PsdOptions a partir do namespace ImageOptions e defina as várias propriedades. A propriedade mais importante a ser definida é a propriedade Source. Esta propriedade especifica onde os dados da imagem estão localizados (em um arquivo ou em um fluxo). No exemplo abaixo, a fonte é um arquivo. Após definir as propriedades, passe o objeto para um dos métodos estáticos Create juntamente com os parâmetros de largura e altura. A largura e altura são definidas em pixels.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **Criando Usando Fluxo**
O processo de criação de uma imagem usando um fluxo é o mesmo que o uso de um caminho. A única diferença é que você precisa criar uma instância de StreamSource passando um objeto Stream para o seu construtor e atribuindo-o à propriedade Source.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **Abrindo Arquivos de Imagem**
Os desenvolvedores podem usar a API Aspose.PSD para Java para abrir arquivos de imagem PSD existentes para diferentes fins, como adicionar efeitos à imagem ou converter um arquivo existente em outro formato. Seja qual for o propósito, o Aspose.PSD fornece duas formas padrão de abrir arquivos existentes: a partir de um arquivo ou a partir de um fluxo.
### **Abrindo do Disco**
Abra um arquivo de imagem passando o caminho e o nome do arquivo como parâmetro para o método estático Load exposto pela classe Image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Abrindo Usando um Fluxo**
Às vezes, a imagem que precisamos abrir está armazenada como um fluxo. Nesses casos, use a versão sobrecarregada do método Load. Isso aceita um objeto Stream como argumento para abrir a imagem.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **Carregar Imagem como Camada**
Este artigo demonstra o uso do Aspose.PSD para carregar uma imagem como uma camada. As APIs do Aspose.PSD expuseram métodos eficientes e fáceis de usar para alcançar esse objetivo. O Aspose.PSD expôs o método AddLayer da classe PsdImage para adicionar uma imagem a um arquivo PSD como camada.

Os passos para carregar uma imagem no PSD como camada são simples como abaixo:

- Crie uma instância de imagem usando a classe PsdImage com a largura e altura especificadas.
- Carregue um arquivo PSD como uma imagem usando o método de fábrica Load exposto pela classe Image.
- Crie uma instância da classe Layer e atribua a camada de imagem do PSD a ela.
- Adicione a camada criada usando o método AddLayer exposto pela classe PsdImage
- Salve os resultados.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **Salvando Arquivos de Imagem**
O Aspose.PSD permite que você crie arquivos de imagem do zero. Ele também fornece meios para editar arquivos de imagem existentes. Após a criação ou modificação da imagem, o arquivo geralmente é salvo no disco. O Aspose.PSD fornece métodos para salvar imagens em um disco especificando um caminho ou usando um objeto Stream.
### **Salvando no Disco**
A classe Image representa um objeto de imagem, portanto, esta classe fornece todas as ferramentas necessárias para criar, carregar e salvar um arquivo de imagem. Use o método Save da classe Image para salvar imagens. Uma versão sobrecarregada do método Save aceita a localização do arquivo como uma string.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Salvando em um Fluxo**
Outra versão sobrecarregada do método Save aceita o objeto Stream como argumento e salva o arquivo de imagem no fluxo.

Se a imagem for criada especificando qualquer um dos CreateOptions no construtor da Image, a imagem é automaticamente salva no caminho ou fluxo fornecido durante a inicialização da classe Image chamando o método Save que não aceita nenhum parâmetro.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **Configuração para Substituir Fontes Ausentes**
Os desenvolvedores podem usar a API Aspose.PSD para Java para carregar arquivos de imagem PSD existentes para diferentes fins, por exemplo, para definir o nome da fonte padrão ao salvar documentos PSD como imagem rasterizada (em formatos PNG, JPG e BMP). Esta fonte padrão deve ser usada como uma substituição para todas as fontes ausentes (fontes que não são encontradas no Sistema Operacional atual). Uma vez que a imagem é modificada, o arquivo será salvo no disco.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}
