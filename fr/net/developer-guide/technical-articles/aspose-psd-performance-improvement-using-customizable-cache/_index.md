---
title: Amélioration des performances d'Aspose.PSD en utilisant un cache personnalisable
type: docs
weight: 20
url: /fr/net/amelioration-des-performances-daspose-psd-en-utilisant-un-cache-personnalisable/
---

## **Améliorer les performances avec un cache personnalisable**
[Aspose.PSD](https://products.aspose.com/psd/family) utilise le cache pour le stockage temporaire des données. Le mécanisme est simple à utiliser, personnalisable et transparent. Il garantit l'absence de problèmes de performances lors du traitement des images. Cet article explique comment personnaliser le cache avec l'API Aspose.PSD pour .NET.
### **Personnalisation du cache**
Lorsqu'un processus nécessite un stockage temporaire des données, cet espace est alloué dans le cache. Le cache peut être un espace en mémoire ou sur le disque et est défini par l'utilisateur. Lorsque les données temporaires ne sont plus nécessaires, l'espace est libéré. Les statistiques de l'espace alloué peuvent être consultées à tout moment. La façon dont Aspose.PSD alloue et utilise les caches peut être personnalisée. Cette section décrit les différents paramètres et leurs valeurs par défaut, et les extraits de code ci-dessous montrent comment ils peuvent être utilisés.
### **Définir l'emplacement de l'allocation du cache**
Pour personnaliser comment l'espace de cache est alloué, définissez la propriété [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype). Par défaut, le cache est alloué en mémoire et lorsqu'il n'y a plus d'espace disponible en mémoire, il est alloué au disque. Ce comportement est capturé par le mode Auto. Le mode Auto est flexible et maximise les performances. Il existe également d'autres modes:

- Mode CacheOnDiskOnly : allocation uniquement sur le disque.
- Mode CacheInMemoryOnly : allocation uniquement en mémoire.

Le choix du mode CacheOnDiskOnly peut entraîner de mauvaises performances.
### **Définir la taille du cache**
Définissez l'espace maximum (en octets) pouvant être alloué sur le disque ou en mémoire en définissant respectivement les propriétés [MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) et [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache). Par défaut, les deux valeurs sont définies à 0, ce qui signifie qu'il n'y a pas de limite supérieure.
### **Contrôler la réallocation du cache**
S'il n'y a pas assez d'espace disponible en mémoire (tel que spécifié par la propriété MaxMemoryForCache) lorsqu'un nouveau cache est alloué, le cache est alloué au disque. S'il n'y a pas assez d'espace sur le disque, une exception est levée. Le processus d'allocation du cache se déplace de la mémoire vers le disque, mais pas dans l'autre sens. La propriété [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) est utilisée pour contrôler la ré-allocation de la mémoire. La ré-allocation est la plus susceptible de se produire pour des caches pré-alloués. Elle peut se produire lorsque le système détermine que l'espace alloué ne sera pas suffisant. Si ExactReallocateOnly est réglé sur la valeur par défaut, False, l'espace est ré-alloué au même support. Lorsqu'il est réglé sur True, la ré-allocation ne peut pas dépasser l'espace maximum spécifié. Dans ce cas, le cache alloué en mémoire existant (qui nécessite une ré-allocation) est libéré et l'espace étendu est alloué sur le disque.
### **Exemples de programmes**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.cs" >}}
