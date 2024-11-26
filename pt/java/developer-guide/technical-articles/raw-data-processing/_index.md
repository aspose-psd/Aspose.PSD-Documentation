---
title: Processamento de Dados Brutos
type: docs
weight: 70
url: /pt/java/processamento-de-dados-brutos/
---

## **Processamento de Dados Brutos**
Para melhorar o desempenho da API Aspose.PSD, introduzimos um método para processamento de dados brutos na versão 2.4.0. O processamento de dados brutos agora é usado internamente e possui uma API externa para que possa ser utilizado fora da biblioteca, a fim de melhorar o desempenho geral. Às vezes, o processamento fica um pouco complicado e precisa de alguma explicação. Atualmente, o processamento de dados brutos está disponível apenas para o formato BMP.

Para ajudar os desenvolvedores a obter o melhor desempenho, a API Aspose.PSD fornece um sistema de processamento de dados brutos que possui uma API externa para customização. Os desenvolvedores chamam a família de métodos LoadRawData e SaveRawData para usar o processamento de dados brutos. Esses métodos também exigem que o formato de dados brutos desejado seja definido usando a classe RawDataSettings. A classe RawDataSettings permite que os desenvolvedores especifiquem qualquer formato de dados brutos. No entanto, para obter o melhor desempenho, é necessário usar o formato de dados brutos no qual os dados estão armazenados. As RawDataSettings definidas na classe RasterImage ajudam a determinar o formato de dados brutos da imagem. Ao passar a instância de RawDataSettings para o método LoadRawData, os dados são retornados como estão, sem que seja aplicada nenhuma conversão, o que pode melhorar o desempenho. Por outro lado, é necessário cuidar de todos os possíveis layouts de formatos de dados brutos, o que pode ser um pouco complicado às vezes.

Para simplificar o processo de manuseio, mesmo que haja uma penalidade de desempenho, você pode especificar as RawDataSettings desejadas instanciando e inicializando a classe com as configurações de dados brutos desejadas. Existem casos em que não é possível retornar os dados brutos no formato especificado (por exemplo, a conversão do espaço de cores CMYK para RGB não está disponível na versão 2.4.0). Além disso, pode haver cenários nos quais o processamento de dados brutos não está disponível para um determinado formato de imagem. Para determinar se pode usar a família de métodos LoadRawData and SaveRawData, é necessário consultar a propriedade IsRawDataAvailable.
### **Visão Geral**
Para o formato de dados de pixel RGB, há formatos de dados brutos indexados (baseados em paleta) e RGB disponíveis. Os formatos de dados brutos indexados contêm índices de entrada de paleta na faixa de 0..(2^bits count – 1). Os formatos de dados brutos indexados são de 1, 2, 4 e 8 bits por pixel. O restante são formatos de dados brutos RGB baseados. Ao carregar dados brutos, certifique-se de que há bytes suficientes disponíveis para carregar os dados, caso contrário, uma exceção apropriada será lançada. Você pode simplesmente estimar o tamanho da matriz de bytes multiplicando o tamanho da linha pelo número de linhas requerido. O tamanho da linha pode variar e depende do formato de armazenamento de dados brutos.

Para obter o melhor desempenho, sempre use um tamanho de linha de dados brutos igual ao valor da propriedade RasterImage.RawLineSize. No entanto, às vezes pode ser necessário adicionar preenchimento adicional às linhas de dados brutos, ou reduzi-lo, e, quando esse for o caso, um tamanho de linha diferente pode ser usado. Se for necessário um subconjunto de um retângulo delimitador de imagem, leve em consideração os deslocamentos de bits que podem ocorrer para formatos de pixel RGB indexado. Por exemplo, considere uma imagem com dimensões de 100x100 pixels e formato de dados brutos de 1 bit por pixel. Você deseja carregar um retângulo de dados brutos com a localização (7,0) e dimensões (2,1), ou em outras palavras, você precisa de 2 pixels começando em x=7 e y=0. Nesse caso, você deve receber o seguinte layout de dados:



![todo:image_alt_text](raw-data-processing_1.png)

Isso significa que você recebe 2 bytes, onde o primeiro byte contém 7 pixels indesejados, em seguida, 1 pixel desejado, e o segundo byte contém 1 pixel desejado e depois 7 indesejados. Você pode se perguntar por que não realizamos o deslocamento de dados e colocamos esses 2 pixels em um único byte? A resposta é simples: para manter o desempenho alto. Todo o processamento interno é tipicamente realizado com todos os dados começando do primeiro pixel e terminando com o último pixel disponível. Existem situações raras em que é necessário um subconjunto de pixels. Além disso, não temos ideia de como esses pixels serão processados posteriormente, então o deslocamento diminuirá o desempenho e tornará o código desnecessariamente complexo. Sempre estime o bit certo (não é necessário determinar o byte certo, uma vez que os dados sempre vêm com o primeiro byte preenchido) onde os pixels exigidos começarão. Para calcular o bit correto, pode ser usada uma fórmula simples: (rect.Left * bitsCount) % 8.
### **Conversão de Cores RGB Indexadas**
Para obter o melhor desempenho possível, sempre use as mesmas configurações de dados brutos de origem e destino, formatos de pixels e tamanhos de linha. No entanto, às vezes pode ser necessário realizar a conversão de dados. Por exemplo, você pode carregar uma imagem RGB com 1 bit por pixel e salvá-la com 2 bits por pixel, ou carregar uma imagem RGB de 4 bits e diminuir sua faixa de cores para 2 bits por pixel. Em ambos os casos, uma conversão de cores deve ser aplicada. A conversão de imagens RGB indexadas pode ser complicada e não pode ser realizada sem algumas configurações aplicadas. É necessário determinar como o intervalo de cores da origem é mapeado para o espaço de cores de destino. Para realizar essa tarefa, temos diferentes modos:

- Mapeamento de paleta (DitheringMethods.PaletteConversion)
- Mapeamento de dados brutos (DitheringMethods.PaletteIgnore)
- Conversor personalizado (DitheringMethods.CustomConverter)

Quando o modo de conversão de paleta é usado, o espaço de cores de origem tenta corresponder ao espaço de cores de destino o mais próximo possível. Por exemplo, vamos assumir que temos uma imagem de 4 bits com as seguintes cores:
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

A imagem de origem parece o seguinte:



![todo:image_alt_text](raw-data-processing_2.png)

E convertemos a imagem de 4 bits para a imagem de 1 bit com as seguintes cores de paleta definidas:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

No modo de conversão de paleta, o conversor lê a cor de origem e determina o índice de destino usando o método GetNearestColorIndex da paleta de destino. O valor da propriedade RasterImage.RawFallbackIndex é usado no caso de o método GetNearestColorIndex da paleta fornecer um índice fora do intervalo. Isso converte as cores de origem para as cores de destino mais próximas em termos de valores de intensidade. A imagem de destino corresponde à imagem de origem o mais próxima possível. Você pode ver o seguinte resultado:



![todo:image_alt_text](raw-data-processing_3.png)

No modo de mapeamento de dados brutos, é usado um cenário diferente. As paletas de cores de origem e destino são simplesmente ignoradas e os índices de origem são mapeados nos índices de destino. Quando um valor é encontrado que não pode ser mapeado para a faixa de destino (ao diminuir a contagem de bits), então o valor da propriedade RasterImage.RawFallbackIndex é usado. O valor é 0 por padrão e será mapeado para a primeira cor na paleta de destino. Caso o valor dessa propriedade esteja fora do intervalo de destino, uma exceção apropriada é lançada. Isso leva a resultados menos previsíveis, que podem ser mostrados na seguinte imagem:



![todo:image_alt_text](raw-data-processing_4.png)

O modo de conversão de paleta é uma solução mais correta para a questão do mapeamento de cores, mas também leva um pouco mais de tempo para ser concluído, já que cálculos precisam ser realizados para estimar o mapeamento de paletas correto. (Tipicamente, há uma diferença de desempenho muito pequena entre os dois métodos.) Por outro lado, o modo de mapeamento de dados brutos é um pouco mais rápido e pode ser usado para uma conversão de cores mais grosseira quando o mapeamento de cores exato não é tão importante. Por exemplo, há casos em que a paleta de cores de origem é reduzida e pode ser convertida com segurança para uma contagem de bits menor, uma vez que os bits extras não foram usados de qualquer maneira.

Para usar qualquer um desses enfoques, utilize a propriedade RawDitheringMethod da classe RasterImage. Por padrão, ela é definida como o método de conversão de paleta para obter os melhores resultados. Você pode alterar essa propriedade antes que qualquer conversão ocorra (ao salvar uma imagem em um fluxo, por exemplo). Observe que os métodos de mapeamento de dados brutos da paleta não serão aplicados se você tiver carregado uma imagem e reescrito alguns dos dados de pixel originais, já que os novos dados são colocados em cache e o cache armazena os dados no formato 32ARGB disponível (a partir da versão 2.4.0, sujeito a alteração). Esse formato é usado para superar problemas com possíveis diferentes faixas de cores para imagens carregadas e salvas. Além disso, os métodos de mapeamento de dados brutos da paleta não serão aplicados quando uma imagem é carregada no modo RGB e convertida para o modo indexado ou vice-versa.
### **Conversores de Cores Personalizados**
Às vezes, não é suficiente usar a abordagem padrão para a conversão de cores. Você pode desejar usar um algoritmo personalizado para obter total liberdade ao utilizar rotinas de conversão de cores. Quando os formatos de pixel de imagens de origem e destino são ambos formatos de cores RGB indexados, uma interface mais simples, IIndexedColorConverter, pode ser usada. Você precisa definir a propriedade RasterImage.RawIndexedColorConverter como uma instância da interface IIndexedColorConverter e usar o valor da propriedade RawDitheringMethod como DitheringMethods.CustomConverter. Quando essa combinação é usada, toda a conversão de cores indexadas passa por aquela instância de IIndexedColorConverter especificada. O conversor de cores indexadas personalizado tem o seguinte método definido:



{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



O método FillIndexedtoIndexedMap é chamado quando é necessária a conversão de uma imagem RGB indexada para outro formato de imagem RGB indexada (quando qualquer uma das contagens de 1,2,4 ou 8 bits são convertidas entre si). O array de mapa tem o comprimento de todas as possíveis entradas de formato de origem. Você precisa preencher esse array para mapear a entrada de paleta de cores de origem para a entrada de paleta de cores de destino. Certifique-se de que o valor do índice de destino esteja na faixa de 0..(número de bits - 1), ou uma exceção apropriada será lançada.

Se a necessidade for realizar um cenário de conversão de cores mais personalizado, a propriedade RasterImage.RawCustomColorConverter deve ser definida como uma instância da interface IColorConverter. A propriedade RawCustomColorConverter sempre substitui a propriedade RawIndexedColorConverter se ambas forem configuradas e um conversor de cores indexadas não será utilizado nesse caso. A interface IColorConverter possui um único método:



{{< highlight java >}}

 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 

{{< /highlight >}}



O método Convert é chamado sempre que é necessária uma conversão de cores. O método recebe os dados brutos de origem no formato de origem e possui um buffer de saída para receber o formato de cor convertido para o destino. O buffer de destino deve ser suficiente para receber os dados convertidos (se a chamada da interface for feita internamente pela biblioteca Aspose.PSD) e deve conter os dados brutos convertidos ao finalizar o método. O método Convert pode ser chamado várias vezes até que todos os dados de origem sejam cobertos.