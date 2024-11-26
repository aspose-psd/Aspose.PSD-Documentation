---
title: Processamento de Dados Brutos
type: docs
weight: 50
url: /pt/processamento-de-dados-brutos/
---

## **Processamento de Dados Brutos**
Para melhorar o desempenho da API Aspose.PSD, introduzimos um método para processamento de dados brutos na versão 2.4.0. O processamento de dados brutos agora é usado internamente e possui uma API externa para que possa ser utilizada fora da biblioteca para melhorar o desempenho geral. Às vezes, o processamento pode ficar um pouco complicado e precisar de alguma explicação. Atualmente, o processamento de dados brutos está disponível apenas para o formato BMP.

Para ajudar os desenvolvedores a obter o melhor desempenho, a API Aspose.PSD fornece um sistema de processamento de dados brutos que possui uma API externa para personalização. Os desenvolvedores chamam a família de métodos [LoadRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadrawdata/index) e [SaveRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/saverawdata) para usar o processamento de dados brutos. Esses métodos também exigem que o formato desejado de dados brutos seja definido usando a classe [RawDataSettings](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings). A classe RawDataSettings permite que os desenvolvedores especifiquem qualquer formato de dados brutos. No entanto, para obter o melhor desempenho, é necessário utilizar o formato de dados brutos no qual os dados são armazenados. As configurações de RawDataSettings definidas na classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) ajudam a determinar o formato de [dados brutos](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings/properties/pixeldataformat) da imagem. Ao passar a instância de RawDataSettings para o método LoadRawData, os dados são retornados como estão, sem aplicação de conversão, e pode melhorar o desempenho. Por outro lado, é necessário cuidar de todos os possíveis layouts de formatos de dados brutos, o que pode ser um pouco complicado às vezes.

Para simplificar o processo de manipulação, com um custo de penalidade de desempenho, você pode especificar as configurações desejadas de RawDataSettings instanciando e inicializando a classe com as configurações de dados brutos desejadas. Existem casos em que não é possível retornar os dados brutos no formato especificado (por exemplo, a conversão do espaço de cores CMYK para RGB não está disponível na versão 2.4.0). Além disso, pode haver cenários em que o processamento de dados brutos não está disponível para um determinado formato de imagem. Para determinar se é possível usar a família de métodos LoadRawData e SaveRawData, é necessário consultar a propriedade [IsRawDataAvailable](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/israwdataavailable).
### **Visão Geral**
Para o formato de [dados de pixel](https://reference.aspose.com/psd/net/aspose.psd/pixeldataformat) RGB, existem formatos de dados brutos indexados (baseados em paleta) e baseados em RGB disponíveis. Os formatos de dados brutos indexados contêm índices de entrada de paleta na faixa de 0 a (2^contagem de bits - 1). Os formatos de dados brutos indexados são de 1, 2, 4 e 8 bits por pixel. Os demais são formatos de dados brutos baseados em RGB. Ao carregar dados brutos, certifique-se de que haja bytes disponíveis para carregar os dados, caso contrário, será lançada uma exceção apropriada. Você pode simplesmente estimar o tamanho da matriz de bytes multiplicando o tamanho da linha pelas linhas necessárias. O tamanho da linha pode variar e depende do formato de armazenamento de dados brutos.

Para obter o melhor desempenho, sempre use um tamanho de linha de dados brutos igual ao valor da propriedade [RasterImage.RawLineSize](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawlinesize). No entanto, às vezes pode ser necessário adicionar preenchimento adicional às linhas de dados brutos, ou reduzi-lo, e, nesse caso, um tamanho de linha diferente pode ser usado. Se for necessário um subconjunto de um retângulo delimitador de imagem, leve em conta os deslocamentos de bits que podem ocorrer para os formatos de pixels RGB indexados. Por exemplo, vamos considerar uma imagem com dimensões de 100x100 pixels e um formato de dados brutos de 1 bit por pixel. Queremos carregar um retângulo de dados brutos com a localização (7,0) e dimensões (2,1), ou em outras palavras, você precisa de 2 pixels a partir de x=7 e y=0. Neste caso, você deve receber o seguinte layout de dados:



![todo:image_alt_text](raw-data-processing_1.png)

Isso significa que você recebe 2 bytes onde o primeiro byte contém 7 pixels indesejados, depois 1 pixel desejado, e o segundo byte contém 1 pixel desejado e depois 7 indesejados. Você pode perguntar por que não realizamos um deslocamento de dados e colocamos esses 2 pixels em um único byte? A resposta é simples: para manter o desempenho alto. Todo o processamento interno é tipicamente realizado com todos os dados a partir do primeiro pixel e terminando com o último pixel disponível. Existem situações raras em que um subconjunto de pixels é necessário. Além disso, não temos ideia de como esses pixels serão processados posteriormente, então o deslocamento diminuirá o desempenho e tornará o código desnecessariamente complexo. Sempre estime o bit correto (não é necessário determinar o byte correto, pois os dados sempre vêm com o primeiro byte preenchido) onde os pixels solicitados começarão. Para calcular o bit correto, uma fórmula simples pode ser usada: (ret.Left * contagem de bits) % 8.
### **Conversão de Cores RGB Indexadas**
Para obter o melhor desempenho possível, sempre use as mesmas configurações de dados brutos de origem e destino, formatos de pixels e tamanhos de linha. No entanto, às vezes pode ser necessário realizar a conversão de dados. Por exemplo, você pode carregar uma imagem RGB de 1 bit por pixel e salvá-la com 2 bits por pixel, ou carregar uma imagem RGB de 4 bits e diminuir sua escala de cores para 2 bits por pixel. Em qualquer caso, uma conversão de cor deve ser aplicada. Converter imagens RGB indexadas pode ser complicado às vezes e não pode ser realizado sem algumas configurações aplicadas. Precisamos determinar como o intervalo de cores de origem é mapeado para o espaço de cores de destino. Para realizar essa tarefa, temos [modos](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods) diferentes:

- Mapeamento de paleta (DitheringMethods.PaletteConversion)
- Mapeamento de dados brutos (DitheringMethods.PaletteIgnore)
- Conversor personalizado (DitheringMethods.CustomConverter)

Quando a conversão de paleta é usada, o espaço de cores de origem tenta corresponder ao espaço de cores de destino o mais próximo possível. Por exemplo, vamos assumir que temos uma imagem de 4 bits com as seguintes cores:
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
[3] RGB=51, 51, 51
[4] RGB=68, 68, 68
[5] RGB=85, 85, 85
[6] RGB=102, 102, 102
[7] RGB=119, 119, 119
[8] RGB=136, 136, 136
[9] RGB=153, 153, 153
[10] RGB=170, 170, 170
[11] RGB=187, 187, 187
[12] RGB=204, 204, 204
[13] RGB=221, 221, 221
[14] RGB=238, 238, 238
[15] RGB=255, 255, 255

A imagem de origem se parece com o seguinte:



![todo:image_alt_text](raw-data-processing_2.png)

E convertemos a imagem de 4 bits para a imagem de 1 bit com as seguintes cores de paleta definidas:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

No modo de conversão de paleta, o conversor lê a cor de origem e determina o índice de destino usando o método [GetNearestColorIndex](https://reference.aspose.com/psd/net/aspose.psd/icolorpalette/methods/getnearestcolorindex/index) da paleta de destino. O valor da propriedade [RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex) é usado no caso do método GetNearestColorIndex da paleta fornecer um índice fora do alcance. Isso converte as cores de origem para as cores de destino mais próximas em termos de valores de intensidade. A imagem de destino corresponde à imagem de origem o mais próximo possível. Você pode ver o seguinte resultado:


![todo:image_alt_text](raw-data-processing_3.png)

No modo de mapeamento de dados brutos, é usado um cenário diferente. As paletas de cores de origem e destino são simplesmente ignoradas e os índices de origem são mapeados nos índices de destino. Quando um valor é encontrado que não pode ser mapeado para o intervalo de destino (quando a contagem de bits é reduzida), então o valor da propriedade [RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex) é usado. O valor é 0 por padrão e será mapeado para a primeira cor na paleta de destino. Se o valor dessa propriedade estiver fora do alcance de destino, será lançada uma exceção apropriada. Isso leva a resultados menos previsíveis, que podem ser mostrados na imagem a seguir:


![todo:image_alt_text](raw-data-processing_4.png)

O modo de conversão de paleta é uma solução mais correta para o problema de mapeamento de cores, mas também demora um pouco mais para ser concluído, pois os cálculos precisam ser realizados para estimar a correspondência correta das paletas. (Tipicamente, há uma diferença de desempenho muito pequena entre os dois métodos.) Por outro lado, o modo de mapeamento de dados brutos é um pouco mais rápido e pode ser usado para conversões de cores mais grosseiras, quando a correspondência exata de cores não é tão importante. Por exemplo, existem casos em que a paleta de cores de origem é reduzida e pode ser convertida com segurança para contagens de bits menores, pois os bits extras não foram usados de qualquer maneira.

Para usar qualquer um desses métodos, utilize a propriedade RawDitheringMethod da classe RasterImage. Por padrão, ela é definida como o método de conversão de paleta para obter os melhores resultados de aparência. Você pode alterar essa propriedade antes que qualquer conversão aconteça (ao salvar a imagem em um fluxo, por exemplo). Observe que os métodos de mapeamento de paleta ignorada e conversão de paleta não serão aplicados se você carregar uma imagem e reescrever parte dos dados de pixel originais, pois os novos dados vão para o cache e o cache armazena os dados no formato máximo disponível 32ARGB (a partir da versão 2.4.0, sujeita a alterações). Este formato é usado para superar problemas com possíveis diferentes faixas de cores para imagens carregadas e salvas. Além disso, os métodos de mapeamento de paleta ignorada e conversão de paleta não serão considerados quando uma imagem for carregada no modo RGB e convertida para o modo indexado ou vice-versa.
### **Conversores de Cores Personalizados**
Às vezes, não é suficiente usar a abordagem padrão para conversão de cores. Você pode querer usar um algoritmo personalizado para obter total liberdade ao usar rotinas de conversão de cores. Quando os formatos de pixel de imagens de origem e destino são ambos formatos RGB indexados, uma interface mais simples, [IIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/iindexedcolorconverter), pode ser usada. É necessário definir a propriedade [RasterImage.RawIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawindexedcolorconverter) como uma instância da interface IIndexedColorConverter e usar o [DitheringMethods](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods).CustomConverter para o valor da propriedade RawDitheringMethod.
Quando essa combinação é usada, qualquer conversão de cor indexada passa por essa instância específica de IIndexedColorConverter. O conversor de cor indexada personalizado tem o método a seguir definido:



{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat formatoFonte, PixelDataFormat formatoDestino);

{{< /highlight >}}



O método FillIndexedtoIndexedMap é chamado quando a conversão é necessária de uma imagem RGB indexada para outra imagem RGB indexada (quando qualquer uma das contagens de bits de 1,2,4 ou 8 é convertida entre si). O array de mapeamento tem o comprimento de todas as possíveis contagens de entradas do formato de origem. Você precisa preencher esse array para mapear a entrada da paleta de cores de origem para a entrada da paleta de cores de destino. Certifique-se de que o valor do índice de destino esteja na faixa de 0 a (contagem de bits - 1), ou uma exceção apropriada será lançada.

Se o requisito for realizar um cenário de conversão de cores mais personalizado, então a propriedade [RasterImage.RawCustomColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawcustomcolorconverter) deve ser definida como uma instância da interface [IColorConverter](https://reference.aspose.com/psd/net/aspose.psd/icolorconverter). A propriedade RawCustomColorConverter sempre substitui a propriedade RawIndexedColorConverter se ambas forem definidas e um conversor de cores indexadas não será usado nesse caso. A IColorConverter possui um único método:



{{< highlight java >}}

 int Convert(PixelDataFormat formatoFonte, byte[] dados, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat formatoDestino, byte[] outputData, int outputOffset); 

{{< /highlight >}}


O método Convert é chamado sempre que a conversão de cor é necessária. O método recebe os dados brutos de origem no formato de origem e possui um buffer de saída para receber o formato de cor convertido para o destino. O buffer de destino deve ser suficiente para receber os dados convertidos (se a chamada da interface for feita internamente pela biblioteca Aspose.PSD) e deve conter os dados brutos convertidos após o retorno do método. O método Convert pode ser chamado várias vezes até que todos os dados de origem sejam tratados.
