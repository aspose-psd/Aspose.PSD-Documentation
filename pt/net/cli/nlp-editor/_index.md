---
title: Aplicativo de Edição NLP da Aspose.PSD para CLI no .NET
type: docs
weight: 10
url: /pt/net/cli/nlp-editor/
is_root: false
keywords: CLI Photoshop Tool NLP Processamento-de-Linguagem-Natural PSD Console Biblioteca C# API PSD
description: Aplicativo de edição baseado em NLP da Aspose.PSD para CLI para os formatos de arquivo PSD, PSB e AI. Automação CI/CD sem código. Suporta processamento de linguagem natural para edição de arquivos PSD. Basta escrever sua solicitação em linguagem natural para realizar diversas operações como conversão, ajuste, redimensionamento e mais. Não requer a instalação do Adobe Photoshop ou Adobe Illustrator e pode ser executado a partir do console sem código adicional.
---

**![Logotipo do Produto Aspose.PSD para .NET](home_1.png)**

**Bem-vindo ao Aplicativo de Edição NLP da Aspose.PSD para CLI no .NET**

O Aplicativo de Edição NLP da Aspose.PSD para CLI é uma utilidade de console leve para editar arquivos PSD usando comandos de linguagem natural. Fácil integração em Pipelines CI/CD.

**Aviso Legal**

Este é um aplicativo experimental. Por favor, teste e deixe um feedback. Qualquer retorno é muito apreciado. Queremos levar o aplicativo sem código para o próximo nível. A integração fácil em qualquer pipeline de compilação ou processo de negócios é o nosso objetivo.

**Funcionalidade principal do Aplicativo de Edição NLP da Aspose.PSD para CLI no .NET**

1. Realizar operações em arquivos PSD, PSB, AI usando comandos de linguagem natural.
2. Suporta várias operações como conversão, ajuste, redimensionamento e mais.
3. Automação CI/CD sem código.
4. Suporta escrever solicitações em linguagem natural para editar arquivos PSD.

## **Uso a partir da linha de comando:**

{{% alert color="primary" %}}
Primeiramente, instale esta ferramenta dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Recomendamos executar o seguinte comando antes do primeiro uso:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Após este comando, você poderá executar este aplicativo com o nome curto nlp.cli em vez de Aspose.PSD.CLI.NLP.Editor. Você pode especificar seu próprio nome curto.
{{% /alert %}}

**Parâmetros disponíveis para o Aplicativo de Recorte Aspose.PSD.CLI**

| **Argumento** | **Descrição**                         |
|:-------------|:----------------------------------------|
| qualquer texto     | Obrigatório. Seu comando em linguagem natural para atualizar um Arquivo PSD ou PSB      |
| licença      | Caminho para a licença.                    |
| verbose      | Exibir mais informações sobre um comando específico. |
| setup        | Cria um arquivo bat na pasta de ferramentas para chamada rápida a partir do console. Exemplo: --setup psd.nlp. Em seguida, você pode chamar a ferramenta com o comando psd.nlp |

**Exemplos de uso**

1. Este comando converterá o primeiro arquivo encontrado (que pode ser aberto com aspose.psd) da pasta atual e o salvará no formato png com transparência. Além disso, a licença será configurada. Você precisa especificar a licença apenas uma vez. Nas próximas execuções, a licença será usada a partir do caminho especificado. Este comando mostrará o log detalhado do processamento NLP, se estiver disponível.
{{< highlight bash >}}
  nlp.cli Converter arquivo desta pasta para o formato png com alfa --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. Este comando encontra o arquivo com nome mais semelhante a "smth.psd". Em seguida, ajustará o contraste e o salvará em jpeg com a melhor qualidade. O nome do arquivo de saída será impresso. Será smth.jpg
{{< highlight bash >}}
Ajustar contraste em 10 da camada com nome elipse no arquivo smth.psd e salvar em output.jpg com melhor qualidade
{{< /highlight >}}

3. Este comando encolherá o arquivo no caminho especificado e reduzirá seu tamanho em 25%. O arquivo de saída será impresso. Será salvo na pasta atual do console.
{{< highlight bash >}}
Redimensionar arquivo C:\Users\someuser\Desktop\input.psd para 25%
{{< /highlight >}}

4. Este comando encontrará o arquivo input.psd em  C:\Users\someuser\Desktop\. Em seguida, encontrará a camada com índice 3 e a redimensionará para largura 50px e altura 100px. Em seguida, essa camada será salva como PDF em C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}
 Redimensionar camada com índice 3 de C:\Users\someuser\Desktop\input.psd para largura 50 e altura 100 e salvar em C:\Users\someuser\Desktop\output.pdf
 {{< /highlight >}}

 5. Este comando abrirá smth.psd na pasta atual, mas todos os efeitos serão desativados. Em seguida, este arquivo será convertido para o formato BMP e salvo como output.bmp na pasta atual.
 {{< highlight bash >}}
 Abrir smth.psd sem efeitos e salvar como output.bmp
  {{< /highlight >}}

**Por favor, verifique outros [Aplicativos de CLI Aspose.PSD](https://docs.aspose.com/psd/net/cli) para .NET se você precisar adicionar suporte para os formatos PSD, PSB e AI ao seu fluxo de trabalho**

1. [Aspose.PSD CLI Converter](/psd/pt/net/cli/convert)
2. [Aspose.PSD CLI Recorte](/psd/pt/net/cli/crop)
3. [Aspose.PSD CLI Redimensionar](/psd/pt/net/cli/resize)
4. [Aspose.PSD CLI Exportar](/psd/pt/net/cli/export)
5. [Aspose.PSD CLI Editor NLP](/psd/pt/net/cli/nlp-editor)

**Por favor, verifique Aspose.PSD para .NET ou [outras plataformas]**

Os Aplicativos de CLI da Aspose.PSD são uma solução pronta para uso para operações populares. Se você precisa de uma solução flexível, por favor, verifique a versão completa do Aspose.PSD

1. [Aspose.PSD para .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD para Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD para Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Recursos da Aspose.PSD para .NET**

A seguir estão os links para alguns recursos úteis que você pode precisar para concluir suas tarefas.

- [Documentação Online dos Aplicativos de CLI Aspose.PSD para .NET](/psd/pt/net/cli/conversion)
- [Notas de Lançamento dos Aplicativos de CLI Aspose.PSD para .NET](/psd/pt/net/cli/conversion/release-notes/)
- [Página do Produto dos Aplicativos de CLI Aspose.PSD para .NET](https://products.aspose.com/psd/net/cli)
- [Guia de Referência da API Aspose.PSD para .NET](https://reference.aspose.com/net/psd)
- [Baixar Exemplos no Repositório do GitHub](https://github.com/aspose-psd/CLI-Applications)
- [Fórum de Suporte Gratuito da Aspose.PSD para .NET](https://forum.aspose.com/c/psd)
- [Central de Ajuda do Suporte Pago da Aspose.PSD para .NET](https://helpdesk.aspose.com/)

