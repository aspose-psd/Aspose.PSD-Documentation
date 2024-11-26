---
title: Licenciamento
type: docs
weight: 60
url: /pt/java/licenciamento/
---

## **Limitações da Versão de Avaliação**
Você pode baixar uma versão de avaliação do Aspose.PSD para Java na [página de download](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). A versão de avaliação oferece os mesmos recursos da versão totalmente licenciada do componente, com algumas restrições. Ao comprar o Aspose.PSD, simplesmente aplicar a licença remove quaisquer restrições da versão de avaliação instalada.

A versão de avaliação do Aspose.PSD para Java oferece funcionalidade completa do produto, com apenas duas limitações:

- **Uma marca d'água em cada imagem**: Qualquer imagem que você salve, modifique ou exporte terá uma marca d'água com a leitura "Avaliação apenas. Criado com Aspose.PSD. Copyright 2018-2019 Aspose Pty Ltd.". Imagens pequenas, onde a marca d'água completa não cabe, possuem duas linhas diagonais através da imagem.
- **Sem suporte para funcionalidade de desenho principal**: No modo de avaliação, pixels de imagem não podem ser carregados ou salvos na imagem. Para desenhar imagens, utilize a funcionalidade de desenho avançada. Essa limitação afeta funcionalidades que dependem da funcionalidade de desenho principal. O Aspose.PSD para Java permite registrar seu próprio formato de arquivo. No entanto, essa funcionalidade depende da funcionalidade de desenho principal, então não faz sentido usá-la no modo de avaliação, pois você não pode alterar o conteúdo desses arquivos.

{{% alert color="primary" %}} 

Se você deseja testar o Aspose.PSD para Java sem as limitações da versão de avaliação, solicite uma licença temporária de 30 dias. Consulte [Como obter uma Licença Temporária?](https://purchase.aspose.com/temporary-license) para mais informações.

{{% /alert %}} 

## **Sobre o Arquivo de Licença**
Depois de testar o Aspose.PSD e ficar satisfeito, você pode adquirir uma licença no [site da Aspose](https://purchase.aspose.com/default.aspx). Familiarize-se com os diferentes tipos de assinaturas oferecidos. Se tiver alguma dúvida, não hesite em contatar a equipe de vendas da [Aspose](https://company.aspose.com/contact).

Cada licença da Aspose inclui uma assinatura de um ano para atualizações de software. Após o primeiro ano, renove suas assinaturas para continuar recebendo os recursos e correções mais recentes. O suporte técnico é gratuito e ilimitado e é fornecido tanto para usuários licenciados quanto para usuários de avaliação através de nossos [Fóruns de Suporte](https://forum.aspose.com/).

A licença é um arquivo XML que contém detalhes como o nome do produto, número de desenvolvedores licenciados, data de expiração da assinatura, entre outros. O arquivo é digitalmente assinado, então não o modifique: mesmo adicionar inadvertidamente uma quebra de linha extra invalidará o arquivo.

Após comprar o Aspose.PSD, você precisa aplicar a licença antes de criar, editar ou manipular imagens. Se esquecer de aplicar a licença, todas as imagens de saída terão uma marca d'água de avaliação. 
Você só precisa definir a licença uma vez por aplicativo ou processo que desenvolver.
## **Aplicando a Licença**
Você pode baixar uma versão de avaliação do **Aspose.PSD** para Java na [página de download](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). A versão de avaliação oferece exatamente as mesmas capacidades da versão licenciada do produto. Além disso, basta adicionar algumas linhas de código para aplicar a licença.

Depois de testar o **Aspose.PSD** e ficar satisfeito, você pode [adquirir uma licença](http://www.aspose.com/Purchase/Components/Default.aspx) no site da Aspose. Familiarize-se com os diferentes tipos de assinaturas oferecidos. Se tiver alguma dúvida, não hesite em contatar a equipe de vendas da Aspose.

Cada licença da Aspose inclui uma assinatura de um ano para atualizações gratuitas para quaisquer novas versões ou correções lançadas durante esse período. O suporte técnico é gratuito e ilimitado e é fornecido tanto para usuários licenciados quanto para usuários de avaliação.

{{% alert color="primary" %}} 

Se você deseja testar o **Aspose.PSD** sem as limitações da versão de avaliação, solicite uma licença temporária de 30 dias. Consulte [Como obter uma Licença Temporária?](http://www.aspose.com/corporate/how-to-get-temporary-license.aspx) para mais informações.

{{% /alert %}} 

### **Definindo uma Licença**
A licença é um arquivo XML de texto simples que contém detalhes como o nome do produto, número de desenvolvedores que a licença permite, data de expiração da assinatura, entre outros. O arquivo é digitalmente assinado, então não o modifique; mesmo a adição inadvertida de uma quebra de linha extra no arquivo o invalidará.

Você precisa definir uma licença antes de utilizar o **Aspose.PSD** se deseja evitar suas limitações de avaliação. Você só precisa definir uma licença uma vez por aplicativo ou processo.

A licença pode ser carregada de um fluxo ou arquivo nos seguintes locais:

1. Caminho explícito.
1. A pasta que contém o Aspose.PSD.jar.

Use o método [License](http://www.aspose.com/api/java/psd/com.aspose.psd/classes/License).setLicense para licenciar o componente. Muitas vezes, a maneira mais fácil de definir uma licença é colocar o arquivo de licença na mesma pasta que o Aspose.PSD.jar e especificar apenas o nome do arquivo sem path, conforme mostrado no seguinte exemplo:
#### **Exemplo 1**
Neste exemplo, o **Aspose.PSD** tentará encontrar o arquivo de licença na pasta que contém os JARs de sua aplicação.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense("Aspose.PSD.Java.lic");

{{< /highlight >}}
#### **Exemplo 2**
Inicializa uma licença de um fluxo.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense(new java.io.FileInputStream("Aspose.PSD.Java.lic"));

{{< /highlight >}}
### **Validar a Licença**
É possível validar se a licença foi definida corretamente ou não. A classe License possui o campo isLicensed que retornará true se a licença foi definida corretamente.

**Java**

{{< highlight csharp >}}

 License license = new License();

license.setLicense("Aspose.PSD.Java.lic");

if (License.isLicensed()) {

    System.out.println("Licença Definida!");

}

{{< /highlight >}}
## **Onde Aplicar uma Licença em seu Aplicativo**
O local onde você aplica uma licença depende do tipo de aplicativo que está desenvolvendo. Siga estas regras simples:

- A licença só precisa ser definida uma vez por domínio de aplicativo. Chamar License.setLicense várias vezes não é prejudicial, mas desperdiça tempo do processador.
- Aplique a licença antes de chamar qualquer classe Aspose.PSD.
- **Aplicativos Java**: chame License.SetLicense no código de inicialização.
- **Biblioteca de Classes**: chame License.setLicense de um construtor estático da classe que utiliza o Aspose.PSD. O construtor estático é executado antes de uma instância da sua classe ser criada, garantindo que a licença do Aspose.PSD seja definida corretamente.
## **Usando Múltiplos Produtos Aspose**
Se você utilizar mais de um produto Aspose em seu aplicativo, por exemplo o Aspose.PSD e o Aspose.Cells, veja algumas dicas úteis.

- **Aplique a licença para cada produto Aspose separadamente**. Mesmo que você tenha um único arquivo de licença para todos os componentes, por exemplo 'Aspose.Total.lic', ainda é necessário chamar License.setLicense separadamente para cada produto Aspose em seu aplicativo.
- **Use um nome de classe de licença completamente qualificado**. Cada produto Aspose possui uma classe License em seu namespace. Por exemplo, o Aspose.PSD tem com.aspose.psd.license.License e o Aspose.Cells tem com.aspose.cells.License. Utilizar um nome de classe totalmente qualificado evita qualquer confusão sobre qual licença é aplicada a qual produto.
