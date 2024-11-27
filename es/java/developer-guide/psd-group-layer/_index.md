---
title: Ejemplo de uso de capas de grupo en Aspose.PSD para Java
weight: 100
type: docs
description: Uso de la capa de grupo de archivo PSD a través de Java
keywords: [grupo de capas, capa de grupo, añadir capa a grupo, psd api, java, muestra de código]
url: es/java/psd-group-layer/
---

## **Resumen**

La utilización de capas de grupo en Aspose.PSD para Java mejora tu capacidad para gestionar y organizar capas dentro de una imagen PSD de manera efectiva. Las capas de grupo, también conocidas como capas de carpeta, te permiten consolidar múltiples capas y aplicar transformaciones o efectos de forma colectiva.

Para comenzar, crea una nueva imagen PSD utilizando el método PsdImage.create(). Luego, inicializa un nuevo objeto LayerGroup a través del método addLayerGroup del objeto PsdImage. Proporciona el nombre deseado para la capa de grupo ("Carpeta"), especifica el índice de inserción (0) y establece un indicador booleano que indique su visibilidad (Verdadero).

Posteriormente, crea dos objetos Layer y establece sus nombres de visualización utilizando el método setDisplayName. Agrega estas capas a la capa de grupo utilizando el método addLayer.

Para acceder a las capas dentro del grupo, utiliza la propiedad layers del objeto LayerGroup. Confirma que los nombres de visualización de las primeras dos capas del grupo sean "Capa 1" y "Capa 2" respectivamente.

Una vez que hayas manipulado las capas de grupo, guarda la imagen PSD modificada utilizando el método save del objeto PsdImage.

Esto sirve como un ejemplo fundamental para ayudarte a familiarizarte con el trabajo con capas de grupo utilizando Aspose.PSD para Java. La biblioteca ofrece una gran cantidad de funciones avanzadas para la manipulación de capas y transformaciones dentro de imágenes PSD. Para más detalles y ejemplos sobre cómo aprovechar las capas de grupo y otras funcionalidades de la biblioteca, consulta la documentación de Aspose.PSD para Java.

Para trabajar con capas de grupo en Aspose.PSD para Java, utiliza la clase LayerGroup. A continuación, se muestra un fragmento de código que ilustra cómo crear una capa de grupo, agregarle capas y guardar la imagen PSD modificada.

Consulta el ejemplo completo proporcionado.

## **Ejemplo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-group-layer.java" >}}
