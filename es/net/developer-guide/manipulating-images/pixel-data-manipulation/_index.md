---
title: Manipulación de datos de píxeles utilizando Aspose.PSD para C#
weight: 100
type: docs
description: Ejemplo de cómo actualizar rápidamente y de forma directa datos de píxeles crudos utilizando la API de C# de PSD
keywords: [editar píxeles, editar psd, editar capa, manipulación de datos crudos, editar datos psd, api psd, C#, csharp, muestra de código]
url: es/net/manipulacion-datos-pixel/
---

## Introducción

Aspose.PSD es una biblioteca poderosa que te permite trabajar con archivos de Adobe Photoshop (PSD) en C#. En este artículo, exploraremos cómo manipular datos de píxeles en un archivo PSD utilizando Aspose.PSD para C#.

## Visión general

El código proporcionado demuestra cómo crear un archivo PSD, agregar una nueva capa, manipular directamente los datos de píxeles y guardar la imagen modificada.

### Pasos para manipular datos de píxeles

1. **Importar los módulos requeridos**:
   Importar los módulos necesarios. Debes importar las clases `PsdImage` y `Layer` de la biblioteca Aspose.PSD.

2. **Definir las rutas de archivo de entrada y salida**:
   Especificar las rutas de archivo de entrada y salida.

3. **Abrir el archivo de entrada como un flujo**:
   Abrir el archivo de entrada como un flujo utilizando la clase `FileStream` en modo de lectura. Crear un objeto `PsdImage` cargando el flujo.

4. **Crear una nueva imagen PSD**:
   Crear una nueva imagen PSD utilizando el constructor `PsdImage` y proporcionar el ancho y alto de la capa como argumentos.

5. **Asignar la capa a la imagen PSD**:
   Asignar la capa a la propiedad `Layers` de la imagen PSD.

6. **Manipular los datos de píxeles**:
   Cargar los píxeles ARGB32 de la capa utilizando el método `LoadArgb32Pixels`. Definir un rango de índices basado en la longitud del arreglo de píxeles y modificar los valores de los píxeles según sea necesario.

7. **Guardar los datos de píxeles modificados**:
   Guardar los datos de píxeles modificados de vuelta a la capa utilizando el método `SaveArgb32Pixels`.

8. **Guardar la imagen PSD**:
   Guardar la imagen PSD en el archivo de salida utilizando el método `Save`.

### Ejemplo

Aquí tienes un ejemplo de código que muestra cómo manipular datos de píxeles utilizando Aspose.PSD para C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "PixelDataManipulation-PixelDataManipulation.cs" >}}

### Resumen

Aspose.PSD para C# ofrece un conjunto poderoso de funciones para manipular datos de píxeles en archivos PSD. Ya sea que necesites modificar píxeles basándote en condiciones específicas o crear patrones complejos, Aspose.PSD hace que estas tareas sean sencillas y eficientes.

Para obtener más información detallada y ejemplos, visita la [documentación de Aspose.PSD para C#](https://docs.aspose.com/psd/net/).
