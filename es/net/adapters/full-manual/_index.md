---
title: Manual completo de los Adaptadores de Aspose.PSD para .NET
type: docs
weight: 10
url: /es/net/adapters/manual-completo
keywords: Adaptadores Manual Completo PSD PSB AI WebP SVG PNG JPEG TIFF GIF BMP guía de inicio rápido
description: Manual completo de los Adaptadores de Aspose.PSD.
---

## Resumen

Este es un manual completo de cómo trabajar con los adaptadores de Aspose.PSD para ampliar las capacidades de Aspose.PSD. Los adaptadores son paquetes especiales de Nuget que permiten la integración sin problemas de Aspose.PSD con otros productos de Aspose, lo que te permite exportar tus archivos a varios formatos no admitidos sin esfuerzo, sin necesidad de escribir código adicional de integración.

## Aplicación de licencias

Por favor, consulta el [artículo completo sobre cómo aplicar licencias](/psd/es/net/adapters/license) para los adaptadores.

{{% alert color="primary" %}} 
Ten en cuenta que para utilizar los Adaptadores necesitas tanto la licencia de Aspose.PSD como la de los adaptadores.
{{% /alert %}} 

La licencia puede aplicarse utilizando este ejemplo:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adaptadores-CSharp-License.cs" >}}

Es mejor aplicar la licencia una vez en el módulo de inicialización de tu proyecto

## Referencia de los Adaptadores de Aspose.PSD

Primero necesitas hacer referencia a Aspose.PSD.Adaptadores.Imaging desde [Nuget](https://www.nuget.org/aspose.psd.adapters.imaging) o descargarlos desde [la Página de lanzamientos de Aspose](https://releases.aspose.com/psd/net/)(los Adaptadores están incluidos en el artefacto de lanzamiento principal en este momento como un binario separado) a tu proyecto.

![Referencias necesarias](references.png)

Es posible que también necesites hacer referencia a otros paquetes adicionales.


## Habilitar Cargadores y Exportadores de los adaptadores

### Habilitar los adaptadores
Cuando necesitas usar adaptadores, simplemente usa el siguiente código:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adaptadores-CSharp-Habilitar-Adaptadores.cs" >}}
 
 
### Deshabilitar los adaptadores
En el proceso de desarrollo, puedes encontrarte con situaciones en las que los Adaptadores deben ser deshabilitados. Este es un caso común si necesitas en una parte del código utilizar los cargadores de Aspose.PSD y en otra los cargadores de los Adaptadores. En este caso, simplemente usa el siguiente código:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adaptadores-CSharp-Deshabilitar-Adaptadores.cs " >}}

## Carga de imágenes usando Adaptadores

Usando adaptadores, puedes [cargar formatos populares no admitidos por Aspose.PSD]((/es/net/adapters/load-unsupported-formats)) como SVG o WebP.

### Uso simple
Simplemente utiliza el siguiente código para la carga:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adaptadores-CSharp-Agregar-Carga-Adaptadores-De-Imagenes-Formatos-No-Admitidos.cs" >}}

### Uso intermedio para el Procesamiento de Imágenes Complejo
Si necesitas especificar opciones adicionales proporcionadas por el Adaptador, consulta el siguiente ejemplo:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adaptadores-CSharp-Manual-Completo-Carga-Compleja.cs" >}}

Puedes trabajar con imágenes SVG utilizando todas las funciones de Imágenes, y luego exportarlas con una llamada de método.

## Exportación de imágenes usando Adaptadores

Existen muchas situaciones en las que no necesitas [abrir un formato no admitido](/es/net/adapters/load-unsupported-formats), sino [exportar a él](/es/net/adapters/export-to-unsupported-formats). En estos casos, debes habilitar los exportadores y utilizar el siguiente código:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adaptadores-CSharp-Agregar-Exportadores-De-Imagenes-Formatos-No-Admitidos.cs" >}}

## Conclusión

El uso de los Adaptadores de Aspose.PSD para la carga y exportación de archivos es un cambio de juego para los desarrolladores. Estos potentes paquetes de Nuget permiten una integración sin problemas de Aspose.PSD con otros productos de Aspose, facilitando más que nunca la apertura y trabajo con formatos de archivo no admitidos sin necesidad de escribir código adicional de integración. Con los Adaptadores de Aspose.PSD, puedes ahorrar tiempo y esfuerzo al eliminar la necesidad de código adicional y procesos de conversión manuales. Ya sea cargando o exportando archivos, los Adaptadores de Aspose.PSD proporcionan una solución conveniente y eficiente que abre nuevas posibilidades para tus proyectos. Experimenta el poder de los Adaptadores de Aspose.PSD y lleva tu proceso de desarrollo al siguiente nivel.
