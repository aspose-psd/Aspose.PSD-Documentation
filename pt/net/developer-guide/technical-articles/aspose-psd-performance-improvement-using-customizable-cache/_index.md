---
title: Melhoria de Desempenho Aspose.PSD usando Cache Customizável
type: docs
weight: 20
url: /pt/net/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Melhora o Desempenho com Cache Customizável**
[Aspose.PSD](https://products.aspose.com/psd/family) utiliza caching para armazenamento temporário de dados. O mecanismo é simples de usar, customizável e transparente. Garante que não haja problemas de desempenho durante o processamento de imagens. Este artigo explica como personalizar o cache com a API Aspose.PSD para .NET.
### **Personalizando o Cache**
Quando um processo precisa de armazenamento temporário de dados, este armazenamento é alocado no cache. O cache pode ser espaço em memória ou em disco e é configurado pelo usuário. Quando os dados temporários não são mais necessários, o espaço é liberado. As estatísticas do espaço alocado podem ser inspecionadas a qualquer momento. Como o Aspose.PSD aloca e utiliza caches pode ser customizado. Esta seção descreve as várias configurações e seus padrões e os trechos de código abaixo mostram como podem ser utilizados.
### **Definindo onde o Cache é Alocado**
Para personalizar como o espaço do cache é alocado, defina a propriedade [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype). Por padrão, o cache é alocado na memória e quando não há mais espaço disponível na memória, ele é alocado no disco. Esse comportamento é capturado pelo modo Automático. O modo Automático é flexível e maximiza o desempenho. Existem também outros modos:

- Modo CacheOnDiskOnly: alocação apenas no disco.
- Modo CacheInMemoryOnly: alocação apenas na memória.

Selecionar o modo CacheOnDiskOnly pode resultar em desempenho ruim.
### **Definindo o Tamanho do Cache**
Defina o espaço máximo (em bytes) que pode ser alocado no disco ou na memória configurando as propriedades [MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) e [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache) respectivamente. Por padrão, ambos os valores são definidos como 0, o que significa que não há limite superior.
### **Controlando o Realocação do Cache**
Se não houver espaço suficiente disponível na memória (conforme especificado pela propriedade MaxMemoryForCache) quando um novo cache é alocado, o cache é alocado no disco. Se não houver espaço suficiente no disco, uma exceção é lançada. O processo de alocação de cache passa da memória para o disco, mas não vice-versa. A propriedade [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) é usada para controlar a realocação de memória. A realocação é mais provável de ocorrer para caches pré-alocados. Pode acontecer quando o sistema percebe que o espaço alocado não será suficiente. Se ExactReallocateOnly estiver definido como o valor padrão, Falso, o espaço é realocado para o mesmo meio. Quando definido como Verdadeiro, a realocação não pode exceder o espaço máximo especificado. Neste caso, o cache existente alocado na memória (que requer realocação) é liberado e o espaço estendido é alocado no disco.
### **Amostras do Programa**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.cs" >}}

