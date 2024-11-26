---
title: Combinação Suportada de Modos de Cor e Profundidade de Bits no PSD
type: docs
weight: 80
url: /pt/supported-combination-of-color-modes-and-bit-depth-in-psd/
---

## **Descrição**
Aspose.PSD suporta a abertura de arquivos PSD com qualquer combinação de Modo de Cor e Profundidade de Bits nos arquivos PSD do Adobe Photoshop. Você pode abrir esses arquivos e usar a API de Baixo Nível para modificar o conteúdo do arquivo. Mas para algumas combinações menos populares podem haver problemas específicos, alguns deles relacionados à Limitação dos Modos de Cor.

## **Combinação de exportação suportada de Modos de Cor e Profundidade de Bits no PSD no modo somente leitura**

| |Bitmap|Escala de Cinza|Indexado|RGB|CMYK|Multicanal|Duotone|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Profundidade 1|Sim[](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|-|
|Profundidade 8|-|Sim|Sim|Sim|Sim|Não Q3-Q4|Não Q3-Q4|Sim[](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|Profundidade 16|-|Sim|-|Sim|Sim|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|Não (Q3-Q4)|
|Profundidade 32|-|Sim*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|Sim*|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|

\* Problemas menores em alguns casos

## **Combinação de exportação suportada de Modos de Cor e Profundidade de Bits no PSD no modo editável**

| |Bitmap|Escala de Cinza|Indexado|RGB|CMYK|Multicanal|Duotone|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Profundidade 1|Sim|-|-|-|-|-|-|-|
|Profundidade 8|-|Sim|Não|Sim|Sim|Não Q3-Q4|Não Q3-Q4|Sim*|
|Profundidade 16|-|Sim|-|Sim|Sim*|-|-|Não (Q3-Q4)|
|Profundidade 32|-|Não (Q3-Q4)|-|Não (Q3-Q4)|-|-|-|-|

\* Problemas menores em alguns casos

Se você precisar do suporte para uma combinação específica de Modo de Cor / Profundidade de Bits, você pode postar nos [Fóruns da Aspose](https://forum.aspose.com/c/psd)
