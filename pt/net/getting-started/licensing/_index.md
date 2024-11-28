---
title: Licenciamento
type: docs
weight: 70
url: /pt/net/licenciamento/
description: Avalie a Biblioteca C# do Photoshop PSD do NuGet e aplique a licença usando arquivo ou fluxo para remover quaisquer restrições da avaliação instalada.
---

## **Limitações da Versão de Avaliação**
Você pode baixar uma versão de avaliação do Aspose.PSD para .NET no [NuGet](https://www.nuget.org/packages/Aspose.psd/). A versão de avaliação fornece os mesmos recursos da versão totalmente licenciada do componente com algumas restrições. Quando você compra o Aspose.PSD, simplesmente aplicar a licença remove quaisquer restrições da avaliação instalada. A versão de avaliação do Aspose.PSD para .NET fornece funcionalidades completas do produto, com apenas duas limitações:

- **Uma marca d'água em cada imagem**: Qualquer imagem que você salve, modifique ou exporte tem uma marca d'água com a leitura "Avaliação Apenas. Criado com Aspose.PSD. Direitos autorais 2010-2018 Aspose Pty Ltd.". Imagens pequenas, onde a marca d'água completa não se encaixa, possuem duas linhas diagonais através da imagem em vez disso.
- **Sem suporte para funcionalidades centrais de desenho**: Em modo de avaliação, os pixels da imagem não podem ser carregados ou salvos na imagem. Para desenhar imagens, use a funcionalidade de desenho avançada em vez disso. Essa limitação afeta funcionalidades que dependem das funcionalidades centrais de desenho. O Aspose.PSD para .NET permite que você registre seu próprio formato de arquivo. No entanto, essa funcionalidade depende das funcionalidades centrais de desenho, então não faz sentido usá-la em modo de avaliação porque você não pode alterar o conteúdo desses arquivos.

Se você quiser testar o Aspose.PSD para .NET sem as limitações da avaliação, solicite uma licença temporária de 30 dias. Consulte [Como obter uma Licença Temporária?](https://purchase.aspose.com/temporary-license) para mais informações.
## **Sobre o Arquivo de Licença**
Depois de estar satisfeito com a sua avaliação do Aspose.PSD, você pode comprar uma licença no [site da Aspose](https://purchase.aspose.com/default.aspx). Familiarize-se com os diferentes tipos de assinatura oferecidos. Se tiver alguma dúvida, não hesite em contatar a equipe de vendas da [Aspose](https://company.aspose.com/contact). Toda licença da Aspose vem com uma assinatura de um ano para atualizações de software. Após o primeiro ano, renove suas assinaturas para continuar obtendo as últimas funcionalidades e correções. O suporte técnico é gratuito e ilimitado e é fornecido tanto para usuários licenciados quanto para usuários em avaliação através dos nossos [Fóruns de Suporte](https://forum.aspose.com/). A licença é um arquivo XML que contém detalhes como o nome do produto, número de desenvolvedores licenciados, data de expiração da assinatura, entre outros. O arquivo é assinado digitalmente, portanto, não o modifique: mesmo adicionar inadvertidamente uma quebra de linha extra invalidará o arquivo. Após comprar o Aspose.PSD, você precisa aplicar a licença antes de criar, editar ou manipular imagens de outra forma. Se esquecer de aplicar a licença, quaisquer imagens de saída terão uma marca d'água de avaliação. Você só precisa definir a licença uma vez por aplicativo ou processo que você desenvolver.
## **Onde Aplicar uma Licença em seu Aplicativo**
O local onde você aplica uma licença depende do tipo de aplicativo que está desenvolvendo. Siga estas regras simples:

- Aplique a licença apenas uma vez por domínio de aplicativo. Chamar License.SetLicense várias vezes não é prejudicial, mas desperdiça o tempo do processador.
- Aplique a licença antes de chamar quaisquer classes Aspose.PSD para .NET.
- **Aplicativos do Windows Forms ou Console**: chame License.SetLicense no código de inicialização, antes de usar quaisquer classes Aspose.PSD para .NET.
- **Aplicativos ASP.NET**: chame License.SetLicense do arquivo Global.asax.cs (Global.asax.vb), no método protegido Application_Start. Dessa forma, ela é chamada uma vez quando o aplicativo inicia. Não chame License.SetLicense dentro dos métodos Page_Load ou a licença será carregada toda vez que uma página da web for carregada.
- **Aplicativos Silverlight**: chame License.SetLicense no evento Application_Startup no arquivo App.xaml.cs (App.xaml.vb).
- **Biblioteca de classes**: chame License.SetLicense de um construtor estático da classe que usa o Aspose.PSD. O construtor estático executa antes de uma instância da sua classe ser criada, garantindo que a licença do Aspose.PSD seja configurada corretamente.
## **Aplicando uma Licença**
Você pode facilmente baixar uma versão de avaliação do Aspose.PSD no NuGet [página de download](https://www.nuget.org/packages/Aspose.psd/). A versão de avaliação oferece absolutamente as mesmas capacidades da versão licenciada do Aspose.PSD. Além disso, a versão de avaliação simplesmente se torna licenciada quando você adquire uma licença e adiciona algumas linhas de código para aplicar a licença.
### **Usando um Arquivo ou um Fluxo**
Se você deseja evitar trabalhar com limitações de avaliação, precisa definir uma licença antes de usar o Aspose.PSD. Você só precisa definir uma licença uma vez por aplicativo (ou processo).
### **Aplicando uma licença de um arquivo**
A maneira mais fácil de aplicar uma licença é colocar o arquivo de licença na mesma pasta que o Aspose.PSD.dll. Então você pode especificar o nome do arquivo no código em vez de um caminho completo.



{{< highlight java >}}

 // Instancie uma instância de licença e aplique a licença usando um caminho completo

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense("Aspose.PSD.lic");



{{< /highlight >}}



Ao chamar o método SetLicense, o nome da licença deve ser o mesmo que o nome do seu arquivo de licença. Por exemplo, se você alterar o nome do arquivo de licença para "Aspose.PSD.lic.xml", você deve usar este nome de licença para o método SetLicense.
### **Aplicando uma licença usando um fluxo**
Também é possível carregar uma licença de um fluxo, como demonstrado abaixo.



{{< highlight java >}}



// Instancie uma instância de licença e aplique a licença usando um fluxo

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense(meuFluxo);



{{< /highlight >}}
### **Verificando o status da licença**
A classe Aspose.PSD.License tem a propriedade IsLicensed que retornará true se a licença tiver sido configurada corretamente.



{{< highlight java >}}

 License license = new License();

license.SetLicense(caminhoLicença);

if (license.IsLicensed)

{

    Console.WriteLine("Licença configurada!");

}

{{< /highlight >}}
### **Usando um Recurso Embutido**
Uma maneira prática de empacotar a licença com seu aplicativo e garantir que ela não seja perdida, é incluí-la como um recurso embutido em uma das assembleias que chama o Aspose.PSD. Para incluir o arquivo de licença como um recurso embutido:

1. No Visual Studio .NET, clique no menu **Arquivo** e selecione **Adicionar Item Existente**.
1. Inclua o arquivo de licença (extensão .lic) no projeto.
1. Selecione o arquivo no Explorador de Soluções.
1. Na janela Propriedades, defina **Ação de Compilação** para **Recurso Embutido**.

Não é necessário chamar os métodos GetExecutingAssembly ou GetManifestResourceStream da System.Reflection.Assembly no Framework .NET da Microsoft para acessar uma licença embutida. Em vez disso, incorpore o arquivo como um recurso no projeto e, em seguida, passe o nome do arquivo de licença para o método SetLicense. A classe de licença encontra automaticamente o arquivo de licença nos recursos embutidos. O exemplo abaixo mostra como incluir a licença como um recurso embutido e aplicá-lo ao seu aplicativo.



{{< highlight java >}}

 // Instancie a classe License

Aspose.PSD.License license = new Aspose.PSD.License();



// Passe o nome do arquivo de licença embutida

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}


### **Verificando o status da licença**
A classe Aspose.PSD.License tem a propriedade IsLicensed que retornará true se a licença tiver sido configurada corretamente.



{{< highlight java >}}

 License license = new License();

license.SetLicense(caminhoLicença);

if (license.IsLicensed)

{

    Console.WriteLine("Licença configurada!");

}

{{< /highlight >}}
