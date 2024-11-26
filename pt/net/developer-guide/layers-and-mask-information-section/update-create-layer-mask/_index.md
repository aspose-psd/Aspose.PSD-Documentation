---
title: Trabalhando com máscaras em Aspose.PSD para C#
weight: 100
type: docs
description: Exemplos de como trabalhar com Máscaras de Recorte, Raster e Vetor dentro de um Arquivo PSD
keywords: [máscaras, máscara de camada, máscara de vetor, máscara de recorte, psd, api psd, C#, csharp, exemplo de código]
url: pt/net/atualizar-criar-mascara-de-camada/
---

## Visão Geral

Existem três tipos de máscaras em arquivos PSD:
1. Máscaras de Recorte
2. Máscaras Raster
3. Máscaras de Vetor

Este artigo aborda todos os três tipos.

### Máscaras de Recorte

Máscaras de recorte são um recurso poderoso em softwares de design gráfico e edição de imagens que permitem controlar a visibilidade de uma camada com base na forma e conteúdo de outra camada. Basicamente, uma máscara de recorte restringe a visibilidade de uma camada à forma definida por outra camada abaixo dela.

Para criar uma máscara de recorte, você precisa de duas camadas: a camada base e a camada de recorte. A camada base define a forma ou área que será visível, enquanto a camada de recorte contém o conteúdo que será limitado à forma da camada base.

Ao aplicar uma máscara de recorte, o conteúdo da camada de recorte só é visível dentro dos limites da camada base. Qualquer conteúdo fora dos limites da camada base é oculto ou cortado.

As máscaras de recorte são particularmente úteis para aplicar efeitos, como texturas ou padrões, a áreas específicas de uma imagem ou de uma obra de arte. Ao usar uma máscara de recorte, você pode garantir que o efeito seja limitado à área desejada sem afetar o restante da imagem.

### Máscaras Raster

Máscaras raster em arquivos PSD são essenciais para controlar a visibilidade de áreas específicas dentro de uma camada. Ao contrário de máscaras de vetor, que usam formas matemáticas para definir áreas mascaradas, máscaras raster usam informações baseadas em pixels para determinar quais partes de uma camada são visíveis ou ocultas.

Uma máscara raster consiste em uma imagem em tons de cinza aplicada a uma camada. As áreas brancas da máscara representam as partes visíveis, enquanto as áreas pretas representam as partes ocultas. Tons de cinza no meio criam transparência parcial ou áreas semi-visíveis.

Usando máscaras raster, é possível obter efeitos de mascaramento intrincados, permitindo controle preciso sobre a visibilidade da camada com base em detalhes de nível de pixel. Esse recurso é particularmente útil para tarefas que exigem edição detalhada e mistura dentro de uma imagem.

### Máscaras de Vetor

Máscaras de vetor em arquivos PSD são uma ferramenta versátil usada para definir a visibilidade de áreas específicas dentro de uma camada com base em formas matemáticas. Ao contrário de máscaras raster, que usam informações baseadas em pixels, máscaras de vetor utilizam trajetórias e curvas para criar áreas mascaradas suaves e escaláveis.

Uma máscara de vetor é essencialmente uma trajetória aplicada a uma camada. A forma da trajetória determina quais partes da camada são visíveis e quais estão ocultas. Manipulando os pontos de controle e curvas da trajetória, é possível criar áreas mascaradas precisas e intrincadas.

Máscaras de vetor são particularmente úteis para criar máscaras limpas e escaláveis que podem ser facilmente ajustadas sem perda de qualidade. Esse recurso é ideal para tarefas que requerem alta precisão e flexibilidade na definição de áreas visíveis dentro de uma camada.

Para obter mais informações sobre adicionar máscaras de vetor, visite a [página de Máscaras de Vetor](psd/pt/camada-mascara-de-vetor/).

## Exemplo
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "TrabalhandoComMascaras-TrabalhandoComMascaras.cs" >}}

Para obter informações e exemplos mais detalhados, visite a [documentação do Aspose.PSD para C#](https://docs.aspose.com/psd/net/).
