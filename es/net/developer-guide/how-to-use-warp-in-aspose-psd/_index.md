---
title: Cómo utilizar Warp en Aspose.PSD
type: docs
weight: 40
url: /es/net/como-utilizar-warp-en-aspose-psd/
---

## **Parte 1 – Renderizar un archivo PSD con el efecto Warp**

Photoshop guarda la imagen renderizada después de aplicar el efecto Warp. Nuestra biblioteca puede reproducir o volver a renderizar la imagen con el efecto Warp. Para habilitar esta función, simplemente configure el flag AllowWarpRepaint en la configuración al abrir el archivo PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-1.cs" >}}

Resultado:
![Aspose.PSD para .NET Resultado de Warp 1](warp1.png)

Además de renderizar el efecto Warp para SmartLayers, nuestra biblioteca también admite Warp para TextLayers. El código de implementación sigue siendo idéntico, con la única diferencia en el nombre de archivo.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-2.cs" >}}

Resultado:
![Aspose.PSD para .NET Resultado de Warp 2](warp2.png)

**! Nota:** Actualmente, nuestra biblioteca soporta renderizar tanto Warp personalizado (donde los usuarios manipulan puntos de malla) como todos los tipos estándar de Warp.

## **Parte 2 – Modificar el efecto Warp**

Nuestra biblioteca le permite no solo renderizar, sino también modificar (agregar) el efecto Warp. Estas modificaciones se facilitan a través de las características de la clase **WarpParams**.

| **Característica** | **Descripción**                                                         | 
|:-------------------|:------------------------------------------------------------------------|
| Límites            | Devuelve los límites de la imagen deformada.                           |
| MeshPoints         | Una matriz de puntos, donde cada punto representa un vértice de la malla de deformación. |
| Valor              | El valor del efecto warp para efectos de deformación no personalizados. |
| WarpRotates        | Una enumeración que define la dirección de efectos de deformación no personalizados. |
| WarpStyles         | Una enumeración que define el tipo de efecto Warp.                    |

El siguiente ejemplo de código demuestra cómo determinar el tipo de efecto Warp para una Smart Layer y ajustar el tipo e intensidad de distorsión para el efecto.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-3.cs" >}}

Resultado:
![Aspose.PSD para .NET Resultado de Warp 3](warp3.png)

## **Parte 3 – Agregar el efecto Warp**

El siguiente ejemplo de código muestra cómo agregar un efecto Warp estándar a una Smart Layer.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-4.cs" >}}

Resultado:
![Aspose.PSD para .NET Resultado de Warp 4](warp4.png)

El siguiente ejemplo de código muestra cómo agregar un efecto Warp personalizado a una Smart Layer.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-5.cs" >}}

Resultado:
![Aspose.PSD para .NET Resultado de Warp 5](warp5.png)

El siguiente ejemplo de código muestra cómo agregar un efecto Warp a una Text Layer. 
**! Nota:** Según los estándares de Photoshop, el efecto Warp para Text Layers suele estar limitado al tipo estándar. Sin embargo, nuestra biblioteca admite el uso de dos tipos de efectos Warp. Tenga en cuenta que dichos archivos pueden no ser completamente compatibles con Photoshop.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-5.cs" >}}

Resultado:
![Aspose.PSD para .NET Resultado de Warp 6](warp6.png)

Continuamos mejorando y expandiendo las capacidades de nuestro efecto Warp, centrándonos en mejorar su velocidad, calidad y funcionalidad soportada. Manténgase actualizado con nuestros lanzamientos mensuales para conocer las últimas novedades.
Su equipo de Aspose.PSD
