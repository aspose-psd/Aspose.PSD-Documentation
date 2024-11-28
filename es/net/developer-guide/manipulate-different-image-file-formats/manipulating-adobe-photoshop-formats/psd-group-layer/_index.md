---
title: Ejemplo de uso de capas de grupo en Aspose.PSD para C#
weight: 100
type: docs
description: Uso de Capa de Grupo de Archivo PSD a través de C#
keywords: [capa de grupo, capa de grupo, agregar capa a grupo, api de psd, C#, csharp, muestra de código]
url: es/net/psd-capas-de-grupo/
---

## Descripción general

Las capas de grupo en Aspose.PSD para C# permiten una organización y manipulación eficientes de las capas en un archivo PSD. Al utilizar capas de carpeta, puedes agrupar múltiples capas y aplicar transformaciones o efectos a todo el grupo.

Este ejemplo muestra cómo crear una nueva imagen PSD con `PsdImage.Create`. Luego, se crea un objeto `LayerGroup` nuevo utilizando `AddLayerGroup` del objeto `PsdImage`. La capa de grupo se nombra "Carpeta", se inserta en el índice 0 y se establece como visible.

A continuación, se crean dos objetos `Layer` con sus propiedades `DisplayName` establecidas. Estas capas se agregan a la capa de grupo usando `AddLayer`.

Las capas dentro del grupo se pueden acceder a través de la propiedad `Layers` del objeto `LayerGroup`. El ejemplo verifica que los nombres visibles de las capas primero y segundo en el grupo son "Capa 1" y "Capa 2".

Después de modificar las capas de grupo, la imagen PSD actualizada se guarda con el método `Save` del objeto `PsdImage`.

Este ejemplo básico presenta el trabajo con capas de grupo utilizando Aspose.PSD para C#. La biblioteca ofrece funciones avanzadas para manipular y transformar capas en archivos PSD. Consulta la documentación de Aspose.PSD para C# para obtener ejemplos y funciones más detalladas.

Aquí tienes un código de muestra que demuestra el uso de capas de grupo en Aspose.PSD para C#:

## Ejemplo

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

Para obtener más información detallada y ejemplos, visita la [documentación de Aspose.PSD para C#](https://docs.aspose.com/psd/net/).
