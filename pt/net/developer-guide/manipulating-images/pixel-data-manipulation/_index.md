---
title: Manipulação de Dados de Pixel usando Aspose.PSD para C#
weight: 100
type: docs
description: Exemplo de como atualizar rapidamente os dados brutos de pixel diretamente e de forma rápida usando a API C# do PSD
keywords: [editar pixels, editar psd, editar camada, manipulação de dados brutos, editar dados psd, api psd, C#, csharp, exemplo de código]
url: pt/manipulacao-de-dados-de-pixel/
---

## Introdução

Aspose.PSD é uma biblioteca poderosa que permite trabalhar com arquivos do Adobe Photoshop (PSD) em C#. Neste artigo, exploraremos como manipular dados de pixel em um arquivo PSD usando Aspose.PSD para C#.

## Visão Geral

O código fornecido demonstra como criar um arquivo PSD, adicionar uma nova camada, manipular os dados dos pixels diretamente e salvar a imagem modificada.

### Etapas para Manipular Dados de Pixel

1. **Importar Módulos Necessários**:
   Importe os módulos necessários. Você precisa importar as classes `PsdImage` e `Layer` da biblioteca Aspose.PSD.

2. **Definir os Caminhos dos Arquivos de Entrada e Saída**:
   Especifique os caminhos dos arquivos de entrada e saída.

3. **Abrir o Arquivo de Entrada como um Fluxo**:
   Abra o arquivo de entrada como um fluxo usando a classe `FileStream` em modo de leitura. Crie um objeto `PsdImage` carregando o fluxo.

4. **Criar uma Nova Imagem PSD**:
   Crie uma nova imagem PSD usando o construtor `PsdImage` e forneça a largura e altura da camada como argumentos.

5. **Atribuir a Camada à Imagem PSD**:
   Atribua a camada à propriedade `Layers` da imagem PSD.

6. **Manipular os Dados de Pixel**:
   Carregue os pixels ARGB32 da camada usando o método `LoadArgb32Pixels`. Defina um intervalo de índices com base no comprimento do array de pixels e modifique os valores dos pixels conforme necessário.

7. **Salvar os Dados de Pixel Modificados**:
   Salve os dados de pixel modificados de volta para a camada usando o método `SaveArgb32Pixels`.

8. **Salvar a Imagem PSD**:
   Salve a imagem PSD no arquivo de saída usando o método `Save`.

### Exemplo

Aqui está um exemplo de código que demonstra como manipular dados de pixel usando Aspose.PSD para C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulacaoDadosPixel-ManipulacaoDadosPixel.cs" >}}

### Resumo

Aspose.PSD para C# oferece um conjunto poderoso de recursos para manipular dados de pixel em arquivos PSD. Independentemente de você precisar modificar pixels com base em condições específicas ou criar padrões complexos, Aspose.PSD torna essas tarefas diretas e eficientes.

Para obter informações e exemplos mais detalhados, visite a [documentação do Aspose.PSD para C#](https://docs.aspose.com/psd/net/).
