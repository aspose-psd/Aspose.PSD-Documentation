---
title: Mejora del rendimiento de Aspose.PSD utilizando caché personalizable
type: docs
weight: 30
url: /es/java/mejora-del-rendimiento-de-aspose-psd-utilizando-cache-personalizable/
---

## **Mejora el rendimiento con caché personalizable**
Aspose.PSD utiliza la caché para el almacenamiento temporal de datos. El mecanismo es simple de usar, personalizable y transparente. Asegura que no haya problemas de rendimiento durante el procesamiento de imágenes. Este artículo explica cómo personalizar la caché con la API de Aspose.PSD para Java.
### **Personalización de la caché**
Cuando un proceso necesita almacenamiento temporal de datos, este se asigna en la caché. La caché puede ser espacio en memoria o en disco y es configurada por el usuario. Cuando los datos temporales ya no son necesarios, el espacio es liberado. Las estadísticas del espacio asignado pueden ser inspeccionadas en cualquier momento. Cómo Aspose.PSD asigna y utiliza las cachés puede ser personalizado. Esta sección describe varios ajustes y sus valores predeterminados, y los fragmentos de código a continuación muestran cómo pueden ser utilizados.
### **Configuración de dónde se asigna la caché**
Para personalizar cómo se asigna el espacio de la caché, se establece la propiedad CacheType. Por defecto, la caché se asigna en memoria y cuando ya no hay espacio disponible en memoria, se asigna a disco. Este comportamiento es capturado por el modo Auto. El modo Auto es flexible y maximiza el rendimiento. También existen otros modos:

- Modo CacheOnDiskOnly: asignación solo a disco.
- Modo CacheInMemoryOnly: asignación solo a memoria.

Seleccionar el modo CacheOnDiskOnly puede resultar en un mal rendimiento.
### **Configuración del tamaño de la caché**
Establezca el espacio máximo (en bytes) que puede ser asignado en disco o en memoria estableciendo las propiedades MaxDiskSpaceForCache y MaxMemoryForCache respectivamente. Por defecto, ambos valores están establecidos en 0, lo que significa que no hay límite superior.
### **Control de la realocación de la caché**
Si no hay suficiente espacio disponible en memoria (según lo especificado por la propiedad MaxMemoryForCache) cuando se asigna una nueva caché, la caché se asigna a disco. Si no hay suficiente espacio en disco, se lanza una excepción. El proceso de asignación de caché se mueve de memoria a disco pero no viceversa. La propiedad ExactReallocateOnly se utiliza para controlar la realocación de memoria. La realocación es más probable que ocurra para las cachés preasignadas. Puede ocurrir cuando el sistema determina que el espacio asignado no será suficiente. Si ExactReallocateOnly está configurado en el valor predeterminado, Falso, el espacio se realoca al mismo medio. Cuando se establece en Verdadero, la realocación no puede exceder el espacio máximo especificado. En este caso, la caché asignada en memoria (que requiere realocación) se libera y se asigna un espacio extendido en disco.
### **Ejemplos de programas**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.java" >}}
