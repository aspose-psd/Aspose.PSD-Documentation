---
title: Usar archivos PSD como plantillas para automatización - Caso de tarjetas de presentación
type: docs
weight: 10
url: /es/net/usar-archivos-psd-como-plantillas-para-automatizacion-caso-de-tarjetas-de-presentacion/
---

### **Resumen**
Este artículo describe casos de uso frecuentes cuando se necesita actualizar algunas capas en un [archivo PSD](https://wiki.fileformat.com/image/psd/) de forma programática, donde el archivo PSD/PSB tiene una estructura de plantilla conocida. Esto se puede utilizar para crear una gran cantidad de tarjetas de presentación para diferentes personas (Caso de tarjetas de presentación). O puede ser necesario realizar una traducción del archivo PSD a diferentes idiomas con la sustitución de algunos materiales gráficos.

Después de leer este artículo sabrás cómo puedes hacer esto:

![todo:image_alt_text](usar-archivos-psd-como-plantillas-para-automatizacion-caso-de-tarjetas-de-presentacion_1.png)

## **Caso simple**
Por ejemplo, tienes una Plantilla PSD con los Nombres de Capa conocidos. Por lo tanto, necesitas cambiar, actualizar o reemplazar la Capa PSD a través de C#. En primer lugar, debes abrir el archivo de plantilla con Aspose.PSD.

¿Cómo abrir un archivo PSD a través de C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:image_alt_text](usar-archivos-psd-como-plantillas-para-automatizacion-caso-de-tarjetas-de-presentacion_2.png)

Luego debemos encontrar la capa que queremos reemplazar por su nombre. Aquí hay una implementación simple para esto.

¿Cómo encontrar la capa en un archivo PSD por su nombre?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}


Cuando se encuentra la capa, podemos actualizarla de manera común, utilizando [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics):

Cómo dibujar en la Capa PSD Graphics

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

En este caso, dibujamos una nueva imagen en formato [PNG](https://wiki.fileformat.com/image/png/) en la capa PSD existente, por lo que los datos antiguos se perderán en el nuevo archivo.

Pero, ¿qué pasa si también necesitamos actualizar texto? El proceso será similar. Encontramos la [Capa de Texto](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) por su nombre y luego actualizamos programáticamente la Capa de Texto del Archivo de Photoshop.

Cómo actualizar la Capa de Texto en Photoshop usando C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}


Al final, necesitamos guardar nuestros cambios:

Cómo guardar un archivo PSD modificado utilizando [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}


La imagen resultante:

![todo:image_alt_text](usar-archivos-psd-como-plantillas-para-automatizacion-caso-de-tarjetas-de-presentacion_3.png)


## **Un caso complejo con características adicionales**
Anteriormente mostramos la forma más sencilla de reemplazar una imagen en una capa de un archivo PSD.

Pero Aspose.PSD puede ofrecer características adicionales más complejas como añadir una nueva capa, eliminar capas antiguas y actualizar la capa de texto utilizando estilos diferentes en texto de varias líneas.

Podemos encontrar la [Capa](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer) que queremos reemplazar, luego encontramos su índice en la Lista de Capas, lo eliminamos e insertamos una nueva Capa después de crearla a partir de un archivo [Jpeg](https://wiki.fileformat.com/image/jpeg/) en el mismo lugar.

Crear una nueva capa a partir de un archivo e insertarla en la Imagen PSD utilizando [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}


Al final de este archivo de código, corregimos la posición de la capa y guardamos el nuevo arreglo de capas en la Imagen Psd.

Cómo copiar las propiedades de la Capa de la [Imagen PSD](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}


Y después de todo, necesitamos actualizar las capas de texto en la imagen PSD existente con C#. Aspose.PSD soporta la [actualización de TextLayer por Porciones](/psd/es/net/working-with-text-layers/). Cada [porción de texto](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) tiene una combinación única de Estilo y Propiedades de Párrafo.

Cómo copiar las propiedades de la Capa de la [Imagen PSD](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentación-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}


Como resultado, hemos cambiado la plantilla PSD mediante código con una nueva Capa de un archivo Jpeg, Png, J2k, Bmp, Gif o Tiff y [texto multilínea con diferentes estilos](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) en cada fila.

![todo:image_alt_text](usar-archivos-psd-como-plantillas-para-automatizacion-caso-de-tarjetas-de-presentacion_4.png)
