---
title: Soporte de Imágenes Grandes
type: docs
weight: 40
url: /es/net/soporte-de-imagenes-grandes/
---

## **Soporte de Imágenes Grandes**
Dado que la librería estándar de .NET tiene algunas limitaciones en cuanto al tamaño de imagen que puede procesar, introdujimos un mecanismo nuevo para el soporte de imágenes grandes. El nuevo enfoque supera las limitaciones, pero debido a las limitaciones de tamaño de datos, las dimensiones máximas admitidas para la creación y carga son de 2,147,483,647 x 2,147,483,647 píxeles.
### **Trabajando con Imágenes Grandes**
Aspose.PSD ha mejorado su rendimiento y compatibilidad con imágenes grandes. Las imágenes que tienen cientos de megabytes de tamaño ya no son un problema, por lo que puedes crear, cargar y dibujar sobre esas imágenes. Sin embargo, debido al procesamiento parcial y al manejo de excepciones OutOfMemoryException, el rendimiento puede ser muy bajo en imágenes muy grandes. Esto se debe a que Aspose.PSD intenta reasignar una cantidad menor de datos para su procesamiento y cada paso de reasignación es muy costoso. Los beneficios de la nueva arquitectura son evidentes:

- No hay limitación en el tamaño de la imagen.
- No estás limitado por la memoria disponible en tu PC.

Si experimentas un procesamiento lento, se recomienda aumentar la cantidad total de RAM para que quepan todos tus píxeles en la memoria. Si no lo haces, el procesamiento sigue siendo posible pero es más lento. El enfoque es el siguiente:

- Llama al método [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) con el rectángulo deseado y un delegado para recibir los píxeles cargados especificados.

Aspose.PSD intenta cargar todo el rectángulo.

- Si hay suficiente memoria para quepan todos los píxeles, entonces todos los píxeles se devuelven simplemente al llamante.
- Si no hay suficiente memoria, el llamante recibe un subconjunto de píxeles desde dentro del rectángulo especificado. Una vez que se hayan procesado esos píxeles, el llamante recibe el siguiente rectángulo. El procesamiento finaliza cuando se ha procesado todo el rectángulo.

Aspose.PSD intenta extraer tantas líneas como sea posible. Si no hay suficiente memoria para quepa una sola línea de píxeles, entonces una sola línea se divide en partes que se ajustan a los rectángulos que tienen 1 de altura. También puedes dibujar en imágenes grandes. El proceso de dibujo intenta afectar a todo el rectángulo deseado. Si no hay suficiente memoria, el dibujo se realiza en rectángulos parciales hasta que se haya dibujado toda el área. Además, Aspose.PSD admite el guardado y exportación de imágenes grandes. Guarda la imagen fuente en disco o expórtala a otro formato de archivo. El proceso de guardado o exportación se realiza mediante rectángulos parciales si es necesario.
### **Formatos de Imagen Soportados**
Los siguientes formatos son compatibles para el procesamiento de imágenes grandes:

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Los formatos anteriores pueden procesarse de forma segura a través de la creación, modificación, aplicación de operaciones de dibujo, guardado en disco o exportación, independientemente del tamaño de la imagen.
