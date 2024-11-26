---
title: Suporte a Imagens Grandes
type: docs
weight: 40
url: /pt/net/suporte-imagens-grandes/
---

## **Suporte a Imagens Grandes**
Uma vez que a biblioteca padrão .NET possui algumas limitações quanto ao tamanho de imagem que pode processar, introduzimos um novo mecanismo para suporte a imagens grandes. A nova abordagem supera as limitações, mas devido às limitações de tamanho de dados, as dimensões máximas suportadas para criação e carregamento são de 2.147.483.647 x 2.147.483.647 pixels.
### **Trabalhando com Imagens Grandes**
O Aspose.PSD melhorou o desempenho e o suporte para imagens grandes. Imagens com centenas de megabytes de tamanho já não são mais um problema, então você pode criar, carregar e desenhar sobre essas imagens. No entanto, devido ao processamento parcial e ao tratamento de exceções OutOfMemoryException, o desempenho pode ser muito baixo em imagens muito grandes. Isso se deve ao fato de que o Aspose.PSD tenta reatribuir uma quantidade menor de dados para processamento e cada etapa de realocação é muito custosa. Os benefícios da nova arquitetura são óbvios:

- Não há limitação quanto ao tamanho da imagem.
- Você não está limitado à memória disponível em seu PC.

Se você perceber um processamento lento, é aconselhável aumentar a quantidade total de RAM para acomodar todos os seus pixels na memória. Caso contrário, o processamento ainda é possível, mas é mais lento. A abordagem é a seguinte:

- Chame o método [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) com o retângulo desejado e um delegado para receber os pixels carregados especificados.

O Aspose.PSD tenta carregar todo o retângulo.

- Se houver memória suficiente para acomodar todos os pixels, então todos os pixels são simplesmente retornados ao chamador.
- Se não houver memória suficiente, o chamador recebe um subconjunto de pixels de dentro do retângulo especificado. Quando esses pixels forem processados, o chamador recebe o próximo retângulo. O processamento termina quando todo o retângulo é processado.

O Aspose.PSD tenta extrair o máximo de linhas possível. Se não houver memória suficiente para acomodar uma única linha de pixels, então uma única linha é dividida em partes conformes aos retângulos com uma altura de 1. Você também pode desenhar em imagens grandes. O processo de desenho tenta afetar todo o retângulo desejado. Se não houver memória suficiente, o desenho é realizado em retângulos parciais até que toda a área seja desenhada. Além disso, o Aspose.PSD suporta salvar e exportar imagens grandes. Salve a imagem de origem no disco ou exporte para outro formato de arquivo. O processo de salvamento ou exportação é realizado usando retângulos parciais, se necessário.
### **Formatos de Imagem Suportados**
Os seguintes formatos são suportados para o processamento de imagens grandes:

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Os formatos acima podem ser processados com segurança através da criação, modificação, aplicação de operações de desenho, salvamento no disco ou exportação, independentemente do tamanho da imagem.
