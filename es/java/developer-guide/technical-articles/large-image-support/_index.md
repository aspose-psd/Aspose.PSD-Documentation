---
title: Soporte de Imágenes Grandes
type: docs
weight: 60
url: /es/java/soporte-de-imagenes-grandes/
---

## **Soporte de Imágenes Grandes**
Dado que la biblioteca estándar de Java tiene algunas limitaciones en cuanto al tamaño de imagen que puede procesar, hemos introducido un nuevo mecanismo para el soporte de imágenes grandes. El nuevo enfoque supera las limitaciones, pero debido a las limitaciones de tamaño de datos, las dimensiones máximas admitidas para la creación y carga son de 2,147,483,647 x 2,147,483,647 píxeles.
### **Trabajar con Imágenes Grandes**
Aspose.PSD ha mejorado el rendimiento y el soporte para imágenes grandes. Las imágenes que tienen cientos de megabytes de tamaño ya no son un problema, por lo que puedes crear, cargar y dibujar sobre esas imágenes. Sin embargo, debido al procesamiento parcial y al manejo de excepciones de OutOfMemoryException, el rendimiento puede ser muy bajo en imágenes muy grandes. Esto se debe al hecho de que Aspose.PSD intenta reasignar una cantidad menor de datos para el procesamiento y cada paso de reasignación es muy costoso. Los beneficios de la nueva arquitectura son obvios:

- No hay limitación en el tamaño de la imagen.
- No estás limitado por la memoria disponible en tu computadora.

Si experimentas un procesamiento lento, se recomienda aumentar la cantidad total de RAM para que quepan todos tus píxeles en memoria. Si no lo haces, el procesamiento sigue siendo posible pero más lento. El enfoque es el siguiente:

- Llama al método LoadPartialPixels con el rectángulo deseado y un delegado para recibir los píxeles cargados especificados.

Aspose.PSD intenta cargar todo el rectángulo.

- Si hay suficiente memoria para almacenar todos los píxeles, entonces todos los píxeles simplemente se devuelven al llamador.
- Si no hay suficiente memoria, el llamador recibe un subconjunto de píxeles del interior del rectángulo especificado. Cuando esos píxeles han sido procesados, el llamador recibe el siguiente rectángulo. El procesamiento finaliza cuando se ha procesado todo el rectángulo.

Aspose.PSD intenta extraer tantas líneas como sea posible. Si no hay suficiente memoria para almacenar una sola línea de píxeles, entonces una línea se divide en partes en conformidad con los rectángulos que tienen una altura de 1. También puedes dibujar en imágenes grandes. El proceso de dibujo intenta afectar todo el rectángulo deseado. Si no hay suficiente memoria, el dibujo se realiza en rectángulos parciales hasta que se dibuje toda el área. Además, Aspose.PSD admite guardar y exportar imágenes grandes. Guarda la imagen de origen en disco o expórtala a otro formato de archivo. El proceso de guardado o exportación se realiza utilizando rectángulos parciales si es necesario.
### **Formatos de Imagen Soportados**
Los siguientes formatos son soportados para el procesamiento de imágenes grandes:

- BMP
- GIF
- TIFF
- PSD
- JPG
- PNG

Los formatos anteriores pueden ser procesados de forma segura a través de la creación, modificación, aplicación de operaciones de dibujo, guardado en disco o exportación independientemente del tamaño de la imagen.

