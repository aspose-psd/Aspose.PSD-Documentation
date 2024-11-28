---
title: Manual Completo do Aspose.PSD Adapters para .NET
type: docs
weight: 10
url: /pt/net/adapters/manual-completo
keywords: Adapters Manual Completo PSD PSB AI WebP SVG PNG JPEG TIFF GIF BMP guia de início rápido
description: Manual Completo do Aspose.PSD Adapters.
---

## Visão Geral

Este é um manual completo sobre como trabalhar com os adaptadores Aspose.PSD para ampliar as capacidades do Aspose.PSD. Os adaptadores são pacotes Nuget especiais que permitem a integração perfeita do Aspose.PSD com outros produtos Aspose, permitindo que você exporte seus arquivos para vários formatos não suportados sem esforço, sem a necessidade de escrever código adicional de integração.

## Aplicação de Licenças

Por favor, verifique o [artigo completo sobre aplicação de licenças](/psd/pt/net/adapters/license) para adaptadores.

{{% alert color="primary" %}} 
Por favor, observe que para usar os Adaptadores você precisa das Licenças tanto do Aspose.PSD quanto dos adaptadores.
{{% /alert %}} 

A licença pode ser aplicada usando este exemplo:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapters-CSharp-License.cs" >}}

É melhor aplicar a licença uma vez no módulo de inicialização do seu projeto.

## Referência dos Aspose.PSD Adapters

Primeiramente, você precisa referenciar o Aspose.PSD.Adapters.Imaging do [Nuget](https://www.nuget.org/aspose.psd.adapters.imaging) ou fazer o download deles da [Página de Lançamento da Aspose](https://releases.aspose.com/psd/net/) (Os adaptadores estão incluídos no artefato de lançamento principal neste momento como um binário separado) para o seu projeto.

![Referências necessárias](references.png)

Pode ser necessário também fazer referência a outros pacotes adicionais.

## Habilitação de Carregadores e Exportadores dos Adaptees

### Habilitação de adaptadores
Quando você precisa usar adaptadores, basta usar o seguinte código:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Enable-Adapters.cs" >}}

### Desabilitação de adaptadores
No processo de desenvolvimento, você pode se deparar com uma situação em que os Adaptadores devem ser desativados. Isso é comum se, em uma parte do código, você precisa usar os carregadores do Aspose.PSD e em outra parte precisa usar os carregadores dos Adaptees. Nesse caso, basta utilizar o seguinte código:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Disable-Adapters.cs " >}}

## Carregamento de Imagens usando Adaptadores

Com os adaptadores, você pode [carregar formatos populares não suportados pelo Aspose.PSD]((/pt/net/adapters/load-unsupported-formats)) como SVG ou WebP.

### Uso simples
Apenas utilize o código a seguir para carregar:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Add-Imaging-Adapters-Loading-Unsupported-Formats.cs" >}}

### Uso intermediário para o Processamento Complexo de Imagens
Se você precisa especificar opções adicionais fornecidas pelo Adaptee, verifique o exemplo a seguir:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapters-CSharp-Full-Manual-Complex-Loading.cs" >}}

Você pode trabalhar com imagens SVG usando todos os recursos de Imagem e, em seguida, exportá-la com uma chamada de método.

## Exportação de Imagens usando Adaptadores

Existem muitas situações em que você não precisa [abrir um formato não suportado](/pt/net/adapters/load-unsupported-formats), mas sim [exportar para ele](/pt/net/adapters/export-to-unsupported-formats). Nestes casos, você deve habilitar os exportadores e usar o código a seguir:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Add-Imaging-Adapters-Exporting-to-Unsupported-Formats.cs" >}}

## Conclusão

O uso dos Aspose.PSD Adapters para carregar e exportar arquivos é um divisor de águas para os desenvolvedores. Esses poderosos Pacotes Nuget permitem a integração perfeita do Aspose.PSD com outros produtos Aspose, tornando mais fácil do que nunca abrir e trabalhar com formatos de arquivo não suportados sem a necessidade de escrever código adicional de integração. Com os Adapters Aspose.PSD, você pode economizar tempo e esforço eliminando a necessidade de código extra e processos de conversão manual. Seja para carregar ou exportar arquivos, os Adapters Aspose.PSD oferecem uma solução conveniente e eficiente que abre novas possibilidades para seus projetos. Experimente o poder dos Adapters Aspose.PSD e leve seu processo de desenvolvimento para o próximo nível.
