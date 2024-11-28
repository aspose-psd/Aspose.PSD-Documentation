---
title: Capa de ajuste de filtro fotográfico
type: docs
weight: 30
url: /es/java/layer-types/adjustment-layer/photo-filter/
---

# Trabajando con la capa de ajuste de filtro fotográfico de Photoshop en Java

Hoy veremos cómo aplicar una capa de ajuste de filtro fotográfico a un documento existente de Photoshop usando Aspose.PSD for Java, que es la biblioteca para manipular el formato de archivo PSD.

**El API de la capa de ajuste de filtro fotográfico** cambia el equilibrio de color de la imagen utilizando tonalidades. La imagen resultante se verá igual que si se hubiera usado un filtro de cámara real. Es importante tener en cuenta que el API de la capa de ajuste de filtro fotográfico de la biblioteca difiere ligeramente del de Photoshop porque aún no hay filtros predefinidos. Sin embargo, es igual en todos los demás aspectos. Esto significa que puedes establecer un color de tono y cambiar su intensidad (densidad), así como utilizar la opción de Preservar luminosidad.

## Resumen del API

El API de la capa de ajuste de filtro fotográfico es bastante simple de usar. Existe la clase principal [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer) que sirve como punto de entrada a esta capa de ajuste y contiene solo tres propiedades públicas, a saber, color, densidad y preservar luminosidad, a través de las cuales se produce el ajuste.

## Ajustar el equilibrio de color

Dado que no hay mucho que explicar, vamos a considerar **un ejemplo de ajuste de equilibrio de color** utilizando el filtro fotográfico de inmediato. Vamos a agregar un filtro cálido (a) manualmente a la imagen de la escultura de ciervo (b) para obtener la imagen en tonos cálidos (c) que es más agradable de ver.

![Ejemplo de capa de ajuste de filtro fotográfico](photo-filter-adjustment-layer-figure-1.png)

Primero que nada, cabe destacar que [el método de fábrica](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-) difiere de los [otros tipos de capas de ajuste](https://docs.aspose.com/display/psdjava/PSD+Adjustment+Layers) porque no hay un método predeterminado (sin argumentos). Por lo tanto, para agregar una capa de ajuste de filtro fotográfico a un documento de Photoshop cargado, se requiere un solo argumento, que es [color](https://reference.aspose.com/psd/java/com.aspose.psd/Color). Entonces, para recrear el efecto de filtro cálido, simplemente pasa el color naranja como argumento al método de fábrica, luego establece la densidad usando los métodos correspondientes:

    PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
    photoFilterLayer.setDensity(25);

Cabe destacar que la propiedad Density tiene un valor predeterminado que es 100, al igual que la opción Preserve Luminosity tiene el valor predeterminado de verdadero (razón por la cual no habilitamos explícitamente esta opción).

## Conclusión

En este artículo, consideramos el uso del API de la capa de ajuste de filtro fotográfico de Aspose.PSD para Java. Esta herramienta es fácil de usar y permite agregar un tono a una imagen con una densidad variable. Es una forma rápida de ajustar el equilibrio de color de toda la imagen.
