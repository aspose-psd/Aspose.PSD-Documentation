---
title: Trabalhando com máscaras no Aspose.PSD para Python
weight: 100
type: docs
description: Exemplos de como trabalhar com Máscaras de Recorte, Raster e Vetor dentro do Arquivo PSD
keywords: [máscaras, máscara de camada, máscara vetorial, máscara de recorte, psd, api psd, python, exemplo de código]
url: /pt/python-net/update-create-layer-mask/
---

## **Visão Geral**

**Visão Geral**

Existem 3 tipos de máscaras em arquivos PSD:
1. Máscaras de Recorte
2. Máscaras de Raster
3. Máscaras Vetoriais

Este artigo abrange todos os 3 tipos.

**Máscaras de Recorte**

Máscaras de recorte são um recurso poderoso em softwares de design gráfico e edição de imagem. Elas permitem controlar a visibilidade de uma camada com base na forma e conteúdo de outra camada. Em outras palavras, uma máscara de recorte restringe a visibilidade de uma camada à forma de outra camada abaixo dela.

Para criar uma máscara de recorte, você precisa de duas camadas: a camada base e a camada que deseja recortar. A camada base define a forma ou área que será visível, enquanto a camada que deseja recortar contém o conteúdo que será recortado para a forma da camada base.

Quando você aplica uma máscara de recorte, o conteúdo da camada recortada é visível apenas dentro dos limites da camada base. Qualquer conteúdo fora dos limites da camada base será ocultado ou recortado.

Máscaras de recorte são particularmente úteis quando você deseja aplicar um efeito, como uma textura ou padrão, a uma área específica de uma imagem ou obra de arte. Usando uma máscara de recorte, você pode confinar o efeito à área desejada sem afetar o restante da imagem.

Por favor, verifique o exemplo no final da página

**Máscaras de Raster**

As máscaras de raster em arquivos PSD são usadas para controlar a visibilidade de áreas específicas dentro de uma camada. Ao contrário das máscaras vetoriais, que usam formas matemáticas para definir as áreas mascaradas, as máscaras de raster utilizam informações baseadas em pixels para determinar quais partes de uma camada são visíveis ou ocultas.

Uma máscara de raster consiste em uma imagem em escala de cinzas que é aplicada a uma camada. As áreas brancas da máscara representam as porções visíveis, enquanto as áreas pretas representam as porções ocultas. Tons de cinza intermediários podem ser usados para criar áreas parcialmente transparentes ou semi-visíveis.

Por favor, verifique o exemplo no final da página

**Máscaras Vetoriais**

As máscaras vetoriais em arquivos PSD são uma ferramenta versátil usada para definir a visibilidade de áreas específicas dentro de uma camada com base em formas matemáticas. Ao contrário das máscaras de raster, que usam informações baseadas em pixels, as máscaras vetoriais utilizam caminhos e curvas para criar áreas mascaradas suaves e escalonáveis.

Uma máscara vetorial é essencialmente um caminho aplicado a uma camada. A forma do caminho determina quais partes da camada são visíveis e quais partes estão ocultas. Ao manipular os pontos de controle e curvas do caminho, você pode criar áreas mascaradas precisas e intrincadas.

Por favor, verifique a página [Máscaras Vetoriais](psd/pt/net/layer-vector-mask/) para obter informações sobre como as máscaras vetoriais podem ser adicionadas usando recursos.

## **Exemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentação-Python-Aspose-psd-update-create-layer-mask.py" >}}
