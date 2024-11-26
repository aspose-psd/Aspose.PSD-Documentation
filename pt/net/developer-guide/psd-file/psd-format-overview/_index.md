---
title: Visão Geral do Formato PSD
type: docs
weight: 60
url: /pt/net/visao-geral-do-formato-psd/
---

## **Descrição**
PSD, Documento Photoshop, representa o formato de arquivo nativo do Adobe Photoshop usado para design gráfico e desenvolvimento.
## **Especificações do Formato de Arquivo**
Os dados em um arquivo PSD são armazenados em ordem de bytes big-endian. Isso implica a troca de short e long integers ao ler ou escrever na plataforma Windows. O formato de arquivo do Photoshop é dividido em cinco partes principais. Possui muitos marcadores de comprimento que podem ser usados para mover-se de uma seção para a próxima. Os marcadores de comprimento geralmente são preenchidos com bytes para arredondar para o intervalo mais próximo de 2 ou 4 bytes. As cinco partes principais são:

- Cabeçalho do Arquivo
- Dados do Modo de Cor
- Recursos de Imagem
- Informações de Camadas e Máscaras
- Dados de Imagem

Para conformidade, os dados devem ser gravados em todos esses campos na seção, pois o Photoshop pode tentar ler toda a seção. Isso também implica que zeros sejam escritos nos campos pulados ao escrever em um arquivo. O campo de comprimento nas seções delimitadas por comprimento deve ser usado para decidir quando parar de ler. Na maioria dos casos, o campo de comprimento indica o número de bytes, não registros, a seguir. Os seguintes pontos precisam ser lembrados ao ler um arquivo.

- Os valores na coluna "Comprimento" em todas as tabelas estão em bytes.
- Todos os valores definidos como cadeia de caracteres Unicode consistem em:
- Um campo de comprimento de 4 bytes, representando o número de caracteres na cadeia (não bytes).
- A cadeia de valores Unicode, dois bytes por caractere.
## **Recursos do Formato**
Os arquivos PSD podem incluir camadas de imagem, camadas de ajuste, máscaras de camada, anotações, informações de arquivo, palavras-chave e outros elementos específicos do Photoshop. Os arquivos do Photoshop têm a extensão padrão.PSD e têm uma altura e largura máximas de 30.000 pixels e um limite de comprimento de dois gigabytes.
## **Como Pode Ser Usado**
1. Um instrumento para Fatiar PSD.
1. [Convertendo PSD](/psd/pt/net/converting-psd-image-to-raster-format/) para HTML
1. Usando [PSD como um Modelo](/psd/pt/net/using-psd-files-as-templates-for-automation-business-cards-case/) para Email
1. PSD para HTML CMS específico
1. Identificação em Arquivo PSD (Retrato Falado)
1. Criar imagens de visualização pseudo-3D usando Objetos Inteligentes para produtos como garrafas, copos, camisetas, etc.
1. Edição rápida de PSD: Auto-Tom, Predefinições, Objeto Inteligente, Recorte de Imagem de Camada de Texto

E muito mais. Se você fez algo ótimo com Aspose.PSD, compartilhe conosco o seu estudo de caso usando os [Fóruns Aspose](https://forum.aspose.com/).


Exemplos adicionais que você pode aprender com:

- [Estudos de Caso](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [Mostras](/psd/pt/net/showcases-html/)
