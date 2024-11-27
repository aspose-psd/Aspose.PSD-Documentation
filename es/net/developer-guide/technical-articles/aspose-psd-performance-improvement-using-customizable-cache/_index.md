---
title: Mejora de rendimiento de Aspose.PSD usando un caché personalizable
type: docs
weight: 20
url: /es/net/mejora-de-rendimiento-de-aspose-psd-usando-un-cache-personalizable/
---

## **Mejora el rendimiento con un caché personalizable**
[Aspose.PSD](https://products.aspose.com/psd/family) utiliza almacenamiento en caché para datos temporales. El mecanismo es fácil de usar, personalizable y transparente. Garantiza que no haya problemas de rendimiento durante el procesamiento de imágenes. Este artículo explica cómo personalizar el caché con la API de Aspose.PSD para .NET.
### **Personalización del caché**
Cuando un proceso necesita almacenamiento de datos temporales, este almacenamiento se asigna en el caché. El caché puede ser espacio en memoria o en disco y es configurado por el usuario. Cuando los datos temporales ya no son necesarios, se libera el espacio. Las estadísticas del espacio asignado se pueden inspeccionar en cualquier momento. Cómo Aspose.PSD asigna y utiliza cachés puede ser personalizado. Esta sección describe los diversos ajustes y sus valores por defecto y los fragmentos de código a continuación muestran cómo se pueden utilizar.
### **Establecer dónde se asigna el caché**
Para personalizar cómo se asigna el espacio de caché, establezca la propiedad [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype). Por defecto, el caché se asigna en memoria y cuando ya no hay más espacio disponible en memoria, se asigna al disco. Este comportamiento está capturado por el modo Auto. El modo Auto es flexible y maximiza el rendimiento. También hay otros modos:

- Modo CacheOnDiskOnly: asignación solo al disco.
- Modo CacheInMemoryOnly: asignación solo a la memoria.

Seleccionar el modo CacheOnDiskOnly puede resultar en un mal rendimiento.
### **Establecer el tamaño del caché**
Establezca el espacio máximo (en bytes) que puede ser asignado en disco o memoria configurando las propiedades [MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) y [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache) respectivamente. Por defecto, ambos valores están establecidos en 0, lo que significa que no hay límite superior.
### **Controlar la reasignación de caché**
Si no hay suficiente espacio disponible en memoria (como se especifica en la propiedad MaxMemoryForCache) cuando se asigna un nuevo caché, el caché se asigna al disco. Si no hay suficiente espacio en disco, se genera una excepción. El proceso de asignación de caché se mueve de memoria a disco pero no al revés. La propiedad [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) se utiliza para controlar la reasignación de memoria. La reasignación es más probable que ocurra para cachés preasignados. Puede ocurrir cuando el sistema determina que el espacio asignado no será suficiente. Si ExactReallocateOnly está establecido en el valor predeterminado, Falso, el espacio se reasigna al mismo medio. Cuando se establece en Verdadero, la reasignación no puede exceder el espacio máximo especificado. En este caso, el caché en memoria existente asignado (que requiere reasignación) se libera y el espacio extendido se asigna en disco.
### **Ejemplos de programas**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ejemplos-CSharp-Aspose-ModificandoYConvirtiendoImágenes-PSD-ControlReasignaciónCaché-ControlReasignaciónCaché.cs" >}}
