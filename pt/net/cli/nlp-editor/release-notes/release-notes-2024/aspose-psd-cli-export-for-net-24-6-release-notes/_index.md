---
title: Notas de Lançamento do Aspose.PSD CLI NLP Editor para .NET 24.6
type: docs
weight: 90
url: /pt/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

Esta página contém as notas de lançamento para [Aspose.PSD CLI NLP Editor para .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                   | **Categoria** |
|:------------|:----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Lançamento Inicial do Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export e Aspose.PSD.CLI.NLP.Editor |  Aprimoramento |


## **Exemplos de Uso:**

**PSDNET-2110. Lançamento inicial da Aplicação Aspose.PSD CLI NLP Editor**

## **Uso a partir da linha de comando:**

{{% alert color="primary" %}}
Primeiro, instale esta ferramenta dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Recomendamos que antes do primeiro uso execute o seguinte comando:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Após este comando, você poderá executar esta aplicação com o nome curto nlp.cli em vez de Aspose.PSD.CLI.NLP.Editor. Você pode especificar seu próprio nome curto.
{{% /alert %}}

**Exemplos de uso**

1. Este comando converterá o primeiro arquivo encontrado (que pode ser aberto com aspose.psd) da pasta atual e o salvará em formato png com transparência. Além disso, a licença será configurada. Você precisa especificar a licença apenas uma vez. Nas próximas execuções, a licença será usada a partir do caminho especificado. Este comando mostrará o log verbose do processamento NLP, se estiver disponível.
{{< highlight bash >}}nlp.cli Converta o arquivo desta pasta para png com alfa --license "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. Este comando encontra o arquivo com o nome mais similar a "smth.psd". Em seguida, ajustará o contraste e o salvará como jpeg com a melhor qualidade. O nome do arquivo de saída será exibido. Será smth.jpg 
{{< highlight bash >}}Ajustar o contraste em 10 da camada com o nome ellipse no arquivo smth.psd e salvá-lo em output.jpg com a melhor qualidade{{< /highlight >}}

3. Este comando irá girar o arquivo no caminho especificado e reduzirá seu tamanho em 25%. O arquivo de saída será exibido. Ele será salvo na pasta atual do console.
{{< highlight bash >}}Redimensionar o arquivo C:\Users\someuser\Desktop\input.psd em 25%{{< /highlight >}}

4. Este comando encontrará o arquivo input.psd em C:\Users\someuser\Desktop\. Em seguida, encontrará a camada com o índice 3 e a redimensionará para largura 50px e altura 100px. Em seguida, esta camada será salva como PDF em C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}Redimensionar a camada com o índice 3 de C:\Users\someuser\Desktop\input.psd para largura 50 e altura 100 e salvar em C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

5. Este comando irá abrir smth.psd na pasta atual, mas todos os efeitos serão desativados. E então esse arquivo será convertido para o formato BMP e salvo como output.bmp na pasta atual.
{{< highlight bash >}}Abrir smth.psd sem efeitos e salvar como output.bmp{{< /highlight >}}

**Aviso Legal**

Esta é uma aplicação experimental. Por favor, experimente e deixe feedback. Qualquer feedback é altamente apreciado. Queremos levar a aplicação Sem-Código ao próximo nível. A integração fácil em qualquer pipeline de compilação ou processo de negócios é o nosso objetivo.
