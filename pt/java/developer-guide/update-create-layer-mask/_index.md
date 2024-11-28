---
title: Trabalhando com máscaras no Aspose.PSD para Java
weight: 100
type: docs
description: Exemplos de como trabalhar com Máscaras de Recorte, Raster e Vetor dentro de um Arquivo PSD
keywords: [máscaras, máscara de camada, máscara vetorial, máscara de recorte, psd, api psd, java, exemplo de código]
url: pt/java/update-create-layer-mask/
---

## **Visão Geral**

**Visão Geral**
	
	Há 3 tipos de máscaras em arquivos PSD:
	1. Máscaras de Recorte
	2. Máscaras Raster
	3. Máscaras Vetoriais
	
	Este artigo abrange os 3 tipos.

** Máscaras de Recorte **

As máscaras de recorte são um recurso robusto em softwares de design gráfico e edição de imagens, especialmente em Java. Permitem um controle preciso sobre a visibilidade de uma camada com base na forma e conteúdo de outra camada. Essencialmente, uma máscara de recorte restringe a visibilidade de uma camada à forma de outra camada abaixo dela.

Para implementar uma máscara de recorte em Java, você precisará de duas camadas: a camada base e a camada que pretende recortar. A camada base define a forma ou área que permanecerá visível, enquanto a camada a ser recortada contém o conteúdo que se conformará à forma da camada base.

Quando uma máscara de recorte é aplicada em Java, o conteúdo da camada recortada é visível apenas dentro dos limites da camada base. Qualquer conteúdo fora desses limites será ocultado ou recortado.

As máscaras de recorte são especialmente valiosas ao aplicar efeitos, como texturas ou padrões, a áreas específicas de uma imagem ou arte. Ao empregar uma máscara de recorte, você pode restringir o efeito à área desejada sem afetar o restante da imagem.

Consulte o exemplo no final da página para mais esclarecimentos.

** Máscaras Raster ** 

As máscaras raster em arquivos Java são empregadas para gerenciar a visibilidade de áreas específicas dentro de uma camada. Ao contrário das máscaras vetoriais, que utilizam formas matemáticas para definir áreas mascaradas, as máscaras raster dependem de informações baseadas em pixels para determinar regiões visíveis ou ocultas.

Uma máscara raster consiste em uma imagem em tons de cinza aplicada a uma camada. As áreas brancas da máscara denotam visibilidade, enquanto as áreas pretas representam partes ocultas. Tons de cinza no meio podem criar regiões de transparência parcial ou semi-visíveis.

Consulte o exemplo no final da página para uma melhor compreensão.

** Máscaras Vetoriais **

As máscaras vetoriais em arquivos Java são ferramentas versáteis usadas para delinear a visibilidade de áreas específicas dentro de uma camada com base em formas matemáticas. Ao contrário das máscaras raster, que dependem de dados baseados em pixels, as máscaras vetoriais utilizam caminhos e curvas para criar áreas mascaradas suaves e escalonáveis.

Uma máscara vetorial consiste essencialmente em um caminho aplicado a uma camada. A forma deste caminho determina quais partes da camada são visíveis e quais estão ocultas. Ao manipular os pontos de controle e curvas do caminho, áreas mascaradas precisas e intrincadas podem ser criadas.

Consulte a [página de Máscaras Vetoriais](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/layermaskdatashort/) para informações sobre adição de máscaras vetoriais usando recursos.

## **Exemplo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentacao-Java-Aspose-psd-update-create-layer-mask.java" >}}
