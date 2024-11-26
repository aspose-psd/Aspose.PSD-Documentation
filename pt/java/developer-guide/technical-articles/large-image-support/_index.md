---
title: Suporte a Imagens Grandes
type: docs
weight: 60
url: /pt/java/suporte-imagens-grandes/
---

## **Suporte a Imagens Grandes**
Como a biblioteca Java padrão possui algumas limitações quanto ao tamanho da imagem que pode processar, introduzimos um novo mecanismo para oferecer suporte a imagens grandes. A nova abordagem supera essas limitações, mas devido a limitações de tamanho de dados, as dimensões máximas suportadas para criação e carregamento são de 2.147.483.647 x 2.147.483.647 pixels.
### **Trabalhando com Imagens Grandes**
O Aspose.PSD melhorou o desempenho e o suporte para imagens grandes. Imagens com centenas de megabytes de tamanho já não são mais um problema, então você pode criar, carregar e desenhar sobre essas imagens. No entanto, devido ao processamento parcial e ao tratamento de exceções OutOfMemoryException, o desempenho pode ser muito baixo em imagens muito grandes. Isso ocorre porque o Aspose.PSD tenta realocar uma quantidade menor de dados para o processamento e cada etapa de realocação é muito custosa. Os benefícios da nova arquitetura são evidentes:

- Não há limitação para o tamanho da imagem.
- Você não está limitado à memória disponível no seu computador.

Se você perceber um processamento lento, é aconselhável aumentar a quantidade total de RAM para caber todos os seus pixels na memória. Caso contrário, o processamento ainda é possível, mas é mais lento. A abordagem é a seguinte:

- Chamar o método LoadPartialPixels com o retângulo desejado e um delegado para receber os pixels carregados especificados.

O Aspose.PSD tenta carregar todo o retângulo.

- Se houver memória suficiente para caber todos os pixels, então todos os pixels são simplesmente retornados ao chamador.
- Se não houver memória suficiente, o chamador recebe um subconjunto de pixels de dentro do retângulo especificado. Quando esses pixels forem processados, o chamador receberá o próximo retângulo. O processamento termina quando todo o retângulo é processado.

O Aspose.PSD tenta extrair o maior número possível de linhas. Se não houver memória suficiente para caber uma única linha de pixels, então uma única linha é dividida em partes conforme os retângulos tendo 1 de altura. Também é possível desenhar em imagens grandes. O processo de desenho tenta afetar todo o retângulo desejado. Se não houver memória suficiente, o desenho é realizado em retângulos parciais até que toda a área seja desenhada. Além disso, o Aspose.PSD oferece suporte para salvar e exportar imagens grandes. Salve a imagem de origem no disco ou exporte-a para outro formato de arquivo. O processo de salvamento ou exportação é realizado usando retângulos parciais se necessário.
### **Formatos de Imagem Suportados**
Os formatos a seguir são suportados para processamento de imagens grandes:

- BMP
- GIF
- TIFF
- PSD
- JPG
- PNG

Os formatos acima podem ser processados com segurança por meio de criação, modificação, aplicação de operações de desenho, salvamento no disco ou exportação, independentemente do tamanho da imagem.
.

