---
title: Abrir arquivos PSD, PSB e AI e exportá-los para PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: Exemplo de exportação de arquivos PSD, PSB e AI para outros formatos
keywords: [abrir psd, abrir ai, abrir psb, exportar para png, exportar para pdf, exportar para jpeg, exportar para tiff, api psd, python, exemplo de código]
url: pt/python-net/abrir-exportar-psd-psb-ai-imagens-para-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **Visão Geral**
Para converter arquivos PSD, PSB e AI para diferentes formatos, você pode usar a biblioteca Aspose.PSD em Python. Esta biblioteca oferece várias opções e configurações para personalizar o processo de conversão.

Primeiramente, é necessário importar as classes e módulos necessários da biblioteca Aspose.PSD. Certifique-se de ter instalado a biblioteca antes de executar o código.

Neste código, definimos várias opções para diferentes formatos, como PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB e PSD. Essas opções permitem personalizar o arquivo de saída de acordo com seus requisitos.

Em seguida, definimos um dicionário chamado `formats` que mapeia as extensões de arquivos às suas respectivas opções de salvamento.

Para converter um arquivo PSD para outros formatos, é necessário carregar o arquivo PSD usando `PsdImage.load()` e depois iterar através do dicionário `formats`. Para cada formato, especifique o nome do arquivo de saída e salve a imagem usando o método `image.save()`.

Da mesma forma, para converter um arquivo AI para outros formatos, carregue o arquivo AI usando `AiImage.load()` e itere através do dicionário `formatos`. Especifique o nome do arquivo de saída e salve a imagem usando o método `image.save()`.

Certifique-se de fornecer os caminhos corretos dos arquivos PSD e AI de origem.

É isso! Agora você pode usar este código para converter arquivos PSD, PSB e AI para vários formatos usando o Aspose.PSD para Python.

Por favor, verifique o exemplo completo.

## **Exemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentação-Python-Aspose-Psd-open-export-psd-psb-ai-imagens-para-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}
