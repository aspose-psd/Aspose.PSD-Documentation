---
title: Instalação
type: docs
weight: 50
url: /pt/net/instalacao/
description: Instale a biblioteca de formato de arquivo PSD usando NuGet ou Package Manager Console.
---

## **Instalando Aspose.PSD para .NET via NuGet**
NuGet é a maneira mais fácil de baixar e instalar APIs da Aspose para .NET. Abra o Microsoft Visual Studio e o gerenciador de pacotes NuGet. Procure por "aspose" para encontrar a API desejada. Clique em "Instalar", a API selecionada será baixada e referenciada em seu projeto.

![todo:image_alt_text](installation_1.png)
## **Instale ou Atualize o Aspose.PSD usando o Package Manager Console**
Você pode seguir os passos abaixo para referenciar a [API Aspose.PSD](https://www.nuget.org/packages/Aspose.psd/) usando o console do gerenciador de pacotes:

1. Abra sua solução/projeto no Visual Studio.
1. Selecione Ferramentas -> Gerenciador de Pacotes -> Console do Gerenciador de Pacotes no menu para abrir o console do gerenciador de pacotes.

![todo:image_alt_text](installation_2.png)

Digite o comando "**Install-Package Aspose.Psd**" e pressione enter para instalar a última versão completa em sua aplicação. Alternativamente, você pode adicionar o sufixo "**-prerelease**" ao comando para especificar que a última versão, incluindo correções, será instalada.

![todo:image_alt_text](installation_3.png)

Você verá a dica **"Instalando Aspose.PSD"** aparecer na parte inferior da janela, indicando que o download está em processo.

![todo:image_alt_text](installation_4.png)

Após o download, você verá as seguintes mensagens de confirmação. Se você não está familiarizado com a [EULA da Aspose](https://company.aspose.com/legal/eula), é uma boa ideia ler a licença referenciada na URL.

![todo:image_alt_text](installation_5.png)

Você deverá ver que o Aspose.PSD foi adicionado e referenciado com sucesso em sua aplicação.

![todo:image_alt_text](installation_6.png)

No console do gerenciador de pacotes, você também pode usar o comando “**Update-Package Aspose.Psd**” e pressionar enter para verificar se há alguma atualização para o pacote Aspose.Psd e instalá-la se houver. Você também pode adicionar o sufixo "-prerelease" para atualizar para a última versão.

## **Considerações ao Executar em um Ambiente de Servidor Compartilhado**
Todos os componentes .NET da Aspose são recomendados para serem executados com o conjunto de permissão de Confiança Total. Isso ocorre porque os componentes .NET da Aspose às vezes precisam acessar configurações de registro e arquivos localizados em locais diferentes do diretório virtual, por exemplo, para ler fontes etc. Além disso, os componentes Aspose.NET são baseados em classes do sistema central do .NET, algumas das quais também requerem permissão de Confiança Total para serem executadas em alguns casos.

Os provedores de serviços de Internet que hospedam várias aplicações de diferentes empresas geralmente aplicam um nível de segurança de Confiança Média. No caso do .NET 2.0, esse nível de segurança pode impor as seguintes restrições, que podem afetar a capacidade do Aspose.PSD de funcionar adequadamente:

- **Permissão de Registro** não está disponível. Isso significa que você não pode acessar o registro, o que é necessário para enumerar as fontes instaladas ao renderizar documentos.
- **Restrição de Permissão de E/S de Arquivos**. Isso significa que você só pode acessar arquivos na hierarquia do diretório virtual da sua aplicação. Isso potencialmente significa que as fontes não podem ser lidas durante a exportação.

Por esses motivos especificados acima, é recomendado que o Aspose.PSD seja executado em permissões de Confiança Total. Você pode perceber que algumas funcionalidades da biblioteca funcionarão ao realizar diferentes tarefas em Confiança Média, enquanto outras não (como a renderização), o que pode ser devido a chamadas para o processamento de imagens GDI+.

## **Trabalhando com DLLs do .NET Core instaladas via pacote MSI**

**Por favor, note:** se você usar a dll do .Net Standard instalada via pacote MSI, você deve adicionar as dependências necessárias para trabalhar com a versão .Net Standard.

|**Captura de tela de dependências do Visual Studio**|**Fragmento de arquivo CsProj:**|
| :- | :- |
|![todo:image_alt_text](installation_7.png)|<ItemGroup><p></p><p>`    `<PackageReference Include="System.Drawing.Common" Version="4.5.1" /></p><p>`    `<PackageReference Include="System.Text.Encoding.CodePages" Version="4.5.0" /></p><p></p></ItemGroup>|


## **Requisitos do Sistema**
### **Sistemas Operacionais Suportados:**
- Microsoft Windows 2000 Professional e Server (SP2 recomendado)
- Microsoft Windows XP Professional e Home Edition
- Microsoft Windows 2003 Server
- Microsoft Windows Vista
- Microsoft Windows 2008 Server
- Microsoft Windows 2008 Server R2
- Microsoft Windows 7
- Microsoft Windows 8
- Microsoft Windows 10
- Microsoft Windows 11

### **Plataformas Suportadas:**
- Forms do Windows
- Forms da Web
- Visual Studio 2005
- Visual Studio 2008
- Visual Studio 2010
- Visual Studio 2012
- Visual Studio 2013
- Visual Studio 2015
- Visual Studio 2017
- Visual Studio 2019
- Visual Studio 2022

Aspose.PSD funciona tanto para as versões x86 quanto x64 dos sistemas operacionais listados acima.
### **Frameworks Suportados:**
Aspose.PSD para .NET suporta o framework .NET conforme abaixo:

- Versão do .NET Framework 2.0 ou superior
- .NET Standard 2.0
