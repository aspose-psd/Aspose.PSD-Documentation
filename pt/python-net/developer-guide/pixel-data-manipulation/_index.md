---
title: Manipulação de dados de Pixel usando Aspose.PSD para Python
weight: 100
type: docs
description: Exemplo de como atualizar diretamente e rapidamente os dados brutos de pixel usando a API do Python PSD
keywords: [editar pixels, editar psd, editar camada, manipulação de dados brutos, editar dados psd, api psd, python, exemplo de código]
url: /pt/python-net/pixel-data-manipulation/
---

## **Introdução**
Aspose.PSD é uma biblioteca poderosa que permite trabalhar com arquivos do Adobe Photoshop (PSD) em Python. Neste artigo, vamos explorar como manipular os dados de pixel em um arquivo PSD usando o Aspose.PSD.

## **Visão Geral**
O código fornecido demonstra como criar um arquivo PSD, adicionar uma nova camada e depois manipular diretamente os dados de pixel e salvar a imagem modificada.

Importando os Módulos Necessários: O primeiro passo é importar os módulos necessários. Importamos o módulo BytesIO da biblioteca io, bem como as classes PsdImage e Layer dos módulos aspose.psd.fileformats.psd e aspose.psd.fileformats.psd.layers, respectivamente.

Em seguida, definimos os caminhos dos arquivos de entrada e saída.

Abrindo o Arquivo de Entrada como um Fluxo: Abrimos o arquivo de entrada como um fluxo usando a função open e o modo "rb". O argumento de buffer é definido como 0 para desativar o buffer. O conteúdo do arquivo é lido em um fluxo BytesIO e o fluxo é configurado para o início usando stream.seek(0).

Criamos um objeto de camada PSD passando o fluxo para o construtor da classe Layer.

Criamos uma nova imagem PSD usando o construtor da classe PsdImage e fornecemos a largura e altura da camada como argumentos.

Atribuímos a camada à propriedade layers da imagem PSD usando o operador de atribuição (=).

Para manipular os dados de pixel, primeiro carregamos os pixels ARGB32 da camada usando o método load_argb_32_pixels. Armazenamos o resultado na variável pixels.

Em seguida, definimos um intervalo de índices (pixelsRange) com base no comprimento do array de pixels. Iteramos sobre os índices e verificamos se um índice é divisível por 5. Se for, definimos o valor do pixel nesse índice como 500000. Assim, queremos criar um padrão repetitivo. Você pode alterar os dados dos pixels conforme desejar.

Em seguida, salvamos os dados de pixel modificados de volta para a camada usando o método save_argb_32_pixels.

Por fim, salvamos a imagem PSD no arquivo de saída usando o método save.

Neste artigo, exploramos como manipular os dados de pixel em um arquivo PSD usando Aspose.PSD para Python. Ao entender o código fornecido, você pode realizar várias operações ao nível do pixel, como modificar pixels com base em certas condições. Aspose.PSD oferece um conjunto abrangente de recursos para trabalhar com arquivos PSD programaticamente, tornando-o uma ferramenta valiosa para tarefas de manipulação de imagem em Python.

Observe que o código fornecido pressupõe que você já instalou a biblioteca Aspose.PSD e suas dependências. Você pode encontrar mais informações sobre como instalar e usar Aspose.PSD para Python na documentação oficial.

Por favor, confira o exemplo completo.

## **Exemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-pixel-data-manipulation.py" >}}
