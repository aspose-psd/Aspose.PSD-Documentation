---
title: Camada de ajuste do filtro de foto
type: docs
weight: 30
url: /pt/java/layer-types/adjustment-layer/photo-filter/
---

# Trabalhando com a camada de ajuste do filtro de foto do Photoshop em Java

Hoje veremos como aplicar a camada de ajuste do filtro de foto a um documento existente do Photoshop usando o Aspose.PSD para Java, que é a biblioteca para manipular o formato de arquivo PSD.

**A API da camada de ajuste do filtro de foto** altera o equilíbrio de cor da imagem usando tonalidades. A imagem resultante terá a mesma aparência que após o uso de um filtro de câmera real. Observe que a API da camada de ajuste do filtro de foto da biblioteca difere ligeiramente da do Photoshop porque ainda não existem filtros predefinidos. No entanto, é o mesmo em todos os outros aspectos. Isso significa que você pode definir uma cor da tonalidade e alterar sua intensidade (densidade) e também usar a opção Preservar Luminosidade.

## Visão geral da API

A API da camada de ajuste do filtro de foto é bastante simples de usar. Há a classe principal [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer) que serve como ponto de entrada para essa camada de ajuste e contém apenas três propriedades públicas, a saber, cor, densidade e preservar a luminosidade por meio das quais ocorre o ajuste.

## Ajustar equilíbrio de cor

Como não há muito o que falar, vamos considerar **um exemplo de ajuste de equilíbrio de cor** usando o Filtro de Foto diretamente. Vamos adicionar um filtro de aquecimento (a) manualmente para a imagem da escultura de veado (b) para obter a imagem em tons quentes (c) que seja mais agradável de ver.

![Exemplo da camada de ajuste do filtro de foto](photo-filter-adjustment-layer-figure-1.png)

Antes de tudo, observe que [o método de fábrica](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-) difere dos para [outras camadas de ajuste](https://docs.aspose.com/display/psdjava/PSD+Adjustment+Layers) porque não há um método padrão (sem argumentos). Portanto, para adicionar uma camada de ajuste do filtro de foto em um documento do Photoshop carregado, um único argumento é necessário, que é [cor](https://reference.aspose.com/psd/java/com.aspose.psd/Color). Portanto, para recriar o efeito do filtro de aquecimento, basta passar laranja como argumento para o método de fábrica, em seguida, definir a densidade usando os métodos correspondentes:

    PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
    photoFilterLayer.setDensity(25);

Vale ressaltar que a propriedade de Densidade tem um valor padrão que é 100, bem como verdadeiro é o valor padrão para a propriedade de Preservar Luminosidade (é por isso que não habilitamos explicitamente esta opção).

## Conclusão

Neste artigo, consideramos o uso da API da camada de ajuste do filtro de foto do Aspose.PSD para Java. Essa ferramenta é simples de usar e permite adicionar uma tonalidade a uma imagem com densidade variável. É uma maneira rápida de ajustar o equilíbrio de cor de toda a imagem.
