---
title: Trabajando con Capas
type: docs
weight: 150
url: /es/net/trabajando-con-capas/
---

## **Crear un Grupo de Capas**
Un grupo de capas consta de una o más capas y ayuda a organizar capas similares o relacionadas. Utilizando Aspose.PSD para .NET puedes crear un grupo de capas. Para este propósito, se ha agregado un nuevo método [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) en la clase **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** para agregar el grupo de capas.

Los pasos para crear grupos de capas son tan simples como se muestra a continuación:

- Crea una instancia de una imagen utilizando la clase PsdImage con el ancho, alto y opciones de imagen especificados.
- Crea un [**LayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup) con el nombre de grupo y el índice especificados.
- Crea una instancia de la clase Layer y asígnale la imagen PSD.
- Agrega la capa creada al grupo de capas utilizando el método AddLayer expuesto por la clase LayerGroup.
- Guarda los resultados.

El siguiente fragmento de código te muestra cómo crear un grupo de capas.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **Renombrar una Capa**
Puedes usar cualquier nombre que desees, pero la práctica típica es usar una descripción general del objeto o elemento que se encuentra en esa capa. Este artículo demuestra cómo cambiar el nombre de una capa utilizando Aspose.PSD para .NET. Para este propósito, se ha agregado una nueva propiedad [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname) en la clase Layer para mostrar adecuadamente un nombre de capa. Se ha observado que cuando Photoshop guarda un nombre de capa utilizando la propiedad **Name**, entonces los caracteres coreanos se almacenan como byte 63'?' en ASCII. Por lo tanto, si deseas mostrar correctamente un nombre de capa, utiliza la propiedad **DisplayName** porque la propiedad **Name** no es compatible con caracteres coreanos.

El siguiente ejemplo de código muestra cómo puedes renombrar una capa.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}

## **Soporte de Capas Enlazadas**
Enlazar capas es como agrupar las capas. Si estás enlazando dos o más capas, te permitirá hacer ciertos cambios en ambas capas enlazadas. Por ejemplo, si aplicas transformaciones a una capa, estas se aplicarán a todas las otras capas enlazadas. Este artículo muestra cómo puedes obtener y desenlazar capas enlazadas utilizando [Aspose.PSD](https://products.aspose.com/psd).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
