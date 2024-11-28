---
title: Melhora de Desempenho do Aspose.PSD usando Cache Personalizável
type: docs
weight: 30
url: /pt/java/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Melhora o Desempenho com Cache Personalizável**
O Aspose.PSD usa o cache para armazenamento temporário de dados. O mecanismo é simples de usar, personalizável e transparente. Ele garante que não haja problemas de desempenho durante o processamento de imagens. Este artigo explica como personalizar o cache com a API do Aspose.PSD para Java.
### **Personalizando o Cache**
Quando um processo precisa de armazenamento temporário de dados, esse armazenamento é alocado no cache. O cache pode ser espaço na memória ou no disco e é definido pelo usuário. Quando os dados temporários não são mais necessários, o espaço é liberado. As estatísticas do espaço alocado podem ser inspecionadas a qualquer momento. Como o Aspose.PSD aloca e utiliza caches pode ser personalizado. Esta seção descreve as várias configurações e seus padrões e os trechos de código abaixo mostram como eles podem ser usados.
### **Definindo onde o Cache é Alocado**
Para personalizar como o espaço do cache é alocado, defina a propriedade CacheType. Por padrão, o cache é alocado na memória e quando não há mais espaço disponível na memória, ele é alocado no disco. Esse comportamento é capturado pelo modo Auto. O modo Auto é flexível e maximiza o desempenho. Existem também outros modos:

- Modo CacheOnDiskOnly: alocação apenas no disco.
- Modo CacheInMemoryOnly: alocação apenas na memória.

Selecionar o modo CacheOnDiskOnly pode resultar em baixo desempenho.
### **Definindo o Tamanho do Cache**
Defina o espaço máximo (em bytes) que pode ser alocado no disco ou na memória, definindo as propriedades MaxDiskSpaceForCache e MaxMemoryForCache, respectivamente. Por padrão, ambos os valores são definidos como 0, significando que não há limite superior.
### **Controlando Realocação do Cache**
Se não houver espaço disponível na memória (conforme especificado pela propriedade MaxMemoryForCache) quando um novo cache for alocado, o cache é alocado no disco. Se não houver espaço no disco, uma exceção é lançada. O processo de alocação de cache passa da memória para o disco, mas não o contrário. A propriedade ExactReallocateOnly é usada para controlar a realocação de memória. A realocação é mais provável de ocorrer para caches pré-alocados. Pode acontecer quando o sistema percebe que o espaço alocado não será suficiente. Se ExactReallocateOnly estiver definido como o valor padrão, Falso, o espaço é realocado para o mesmo meio. Quando definido como Verdadeiro, a realocação não pode exceder o espaço máximo especificado. Nesse caso, o cache alocado na memória (que requer realocação) é liberado e um espaço estendido é alocado no disco.
### **Exemplos de Programa**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.java" >}}
