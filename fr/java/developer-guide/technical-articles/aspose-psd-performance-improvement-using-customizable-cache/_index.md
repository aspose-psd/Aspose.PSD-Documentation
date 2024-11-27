---
title: Amélioration des performances d'Aspose.PSD en utilisant un cache personnalisable
type: docs
weight: 30
url: /fr/java/aspose-psd-amelioration-des-performances-en-utilisant-un-cache-personnalisable/
---

## **Améliore les performances avec un cache personnalisable**
Aspose.PSD utilise la mise en cache pour le stockage temporaire des données. Le mécanisme est simple à utiliser, personnalisable et transparent. Il garantit qu'il n'y a pas de problèmes de performance lors du traitement des images. Cet article explique comment personnaliser le cache avec l'API Aspose.PSD pour Java.
### **Personnalisation du cache**
Lorsqu'un processus a besoin de stockage temporaire des données, ce stockage est alloué dans le cache. Le cache peut être de l'espace en mémoire ou sur disque et est défini par l'utilisateur. Lorsque les données temporaires ne sont plus nécessaires, l'espace est libéré. Les statistiques de l'espace alloué peuvent être inspectées à tout moment. Comment Aspose.PSD alloue et utilise les caches peut être personnalisé. Cette section décrit les différents paramètres et leurs valeurs par défaut, et les extraits de code ci-dessous montrent comment ils peuvent être utilisés.
### **Définition de l'emplacement de l'allocation du cache**
Pour personnaliser la manière dont l'espace de cache est alloué, définissez la propriété CacheType. Par défaut, le cache est alloué en mémoire et lorsqu'il n'y a plus d'espace disponible en mémoire, il est alloué sur le disque. Ce comportement est capturé par le mode Auto. Le mode Auto est flexible et maximise les performances. Il existe également d'autres modes :

- Mode CacheOnDiskOnly : allocation sur le disque uniquement.
- Mode CacheInMemoryOnly : allocation en mémoire uniquement.

Le choix du mode CacheOnDiskOnly peut entraîner de mauvaises performances.
### **Définition de la taille du cache**
Définissez l'espace maximal (en octets) pouvant être alloué sur le disque ou en mémoire en définissant respectivement les propriétés MaxDiskSpaceForCache et MaxMemoryForCache. Par défaut, les deux valeurs sont définies à 0, ce qui signifie qu'il n'y a pas de limite supérieure.
### **Contrôle de la réallocation du cache**
S'il n'y a pas suffisamment d'espace disponible en mémoire (tel que spécifié par la propriété MaxMemoryForCache) lorsqu'un nouveau cache est alloué, le cache est alloué sur le disque. S'il n'y a pas suffisamment d'espace sur le disque, une exception est lancée. Le processus d'allocation du cache passe de la mémoire au disque mais pas dans le sens inverse. La propriété ExactReallocateOnly est utilisée pour contrôler la réaffectation de la mémoire. La réaffectation est la plus susceptible de se produire pour des caches pré-alloués. Elle peut se produire lorsque le système réalise que l'espace alloué ne sera pas suffisant. Si ExactReallocateOnly est défini sur la valeur par défaut, False, l'espace est ré-alloué au même support. Lorsqu'il est défini sur True, la réaffectation ne peut pas dépasser l'espace maximum spécifié. Dans ce cas, le cache alloué en mémoire (qui nécessite une réaffectation) est libéré et l'espace supplémentaire est alloué sur le disque.
### **Exemples de programmes**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.java" >}}

