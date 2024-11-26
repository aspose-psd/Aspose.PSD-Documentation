---
title: Como Executar os Exemplos
type: docs
weight: 90
url: /pt/net/como-executar-os-exemplos/
description: Aprenda como executar os exemplos relacionados à biblioteca de formato de arquivo PSD que estão hospedados no GitHub.
---

## **Requisitos de Software**
Certifique-se de atender aos seguintes requisitos antes de baixar e executar os exemplos.

1. Visual Studio 2010 ou superior
1. Gerenciador de Pacotes NuGet instalado no Visual Studio. Verifique se a versão mais recente da API do NuGet está instalada no Visual Studio. Para obter detalhes sobre como instalar o gerenciador de pacotes NuGet, consulte [http://docs.nuget.org/ndocs/guides/install-nuget](http://docs.nuget.org/ndocs/guides/install-nuget)
1. Vá para Ferramentas->Opções->Gerenciador de Pacotes NuGet->Fontes de Pacote e certifique-se de que a opção **nuget.org** esteja marcada
1. O projeto de exemplo usa a funcionalidade de Restauração de Pacotes Automática do NuGet, portanto é necessário ter uma conexão ativa com a internet. Se você não tiver uma conexão ativa com a internet na máquina onde os exemplos serão executados, consulte [Instalação](/psd/pt/net/installation/) para adicionar a referência ao Aspose.Imaging.dll no projeto de exemplo.
## **Baixar do GitHub**
Todos os exemplos do Aspose.PSD para .NET estão hospedados no [GitHub](https://github.com/aspose-psd/Aspose.PSD-for-.NET).

- Você pode clonar o repositório usando seu cliente GitHub favorito ou baixar o arquivo ZIP da [aqui](https://github.com/aspose-psd/Aspose.PSD-for-.NET/archive/master.zip).
- Extraia o conteúdo do arquivo ZIP para qualquer pasta em seu computador. Todos os exemplos estão localizados na pasta **Exemplos**.
- Há um arquivo de solução do Visual Studio para C#.
- Os projetos são criados no Visual Studio 2013, mas os arquivos de solução são compatíveis com o Visual Studio 2010 SP1 e posterior.
- Abra o arquivo de solução no Visual Studio e compile o projeto.
- Na primeira execução, as dependências serão baixadas automaticamente via NuGet.
- A pasta **Data** na pasta raiz de **Exemples** contém arquivos de entrada usados pelos exemplos em CSharp. É obrigatório que você baixe a pasta **Data** juntamente com o projeto de exemplos.
- Abra o arquivo RunExamples.cs, todos os exemplos são chamados a partir daqui.
- Descomente os exemplos que deseja executar dentro do projeto.

Sinta-se à vontade para nos contatar usando nossos Fóruns se tiver algum problema para configurar ou executar os exemplos.
## **Contribuir**
Se você deseja adicionar ou melhorar um exemplo, incentivamos que contribua para o projeto. Todos os exemplos e projetos de demonstração neste repositório são de código aberto e podem ser livremente usados em suas próprias aplicações.

Para contribuir, você pode bifurcar o repositório, editar o código fonte e criar uma solicitação de recebimento. Iremos revisar as mudanças e incluí-las no repositório se forem consideradas úteis.
