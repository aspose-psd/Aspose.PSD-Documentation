---
title: Agregar una Firma a una Imagen
type: docs
weight: 70
url: /es/net/adding-a-signature-to-an-image/
---

## **Agregar una Firma**


Agregar una firma a una imagen a veces es necesario para firmar digitalmente las imágenes y evitar la falsificación. Otra idea podría ser tratar la imagen más como si se estuviera mostrando en una galería. Sea cual sea la razón, las API de Aspose.PSD proporcionan la característica de agregar una firma a una imagen utilizando el mecanismo más simple como se explica a continuación. Tenga en cuenta que este ejemplo utiliza la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para dibujar otra imagen con una firma en la superficie de la imagen original. Para demostrar la operación, cargaremos una imagen PSD desde el disco y dibujaremos otra imagen como firma en la superficie de la imagen original utilizando el método [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage) de la clase Graphics. Guardaremos la imagen resultante en formato PNG utilizando la clase [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions). A continuación se muestra un ejemplo de código que demuestra cómo agregar una firma a una imagen. El código de ejemplo se ha dividido en partes para facilitar su comprensión. Paso a paso, el ejemplo muestra cómo:

- Cargar las imágenes primarias y secundarias (firma).
- Crear e inicializar un objeto Graphics.
- Dibujar la imagen utilizando el método DrawImage de la clase Graphics.
- Guardar el resultado en formato PNG.
### **Ejemplos del Programa**
#### **Cargando las Imágenes**
En primer lugar, crear instancias de la clase Image para cargar las imágenes de muestra desde el disco.
#### **Creando e Inicializando un Objeto Gráfico**
Después de cargar las imágenes, crear e inicializar un objeto de la clase Graphics utilizando el objeto de la imagen primaria.
#### **Dibujando la Imagen Secundaria sobre la Imagen Primaria**
Luego, utilizando el método DrawImage de la clase Graphics, agregar la imagen secundaria a la imagen primaria. Hay varias sobrecargas del método DrawImage que aceptan un objeto de Image como primer parámetro, mientras que todos los demás parámetros corresponden a la ubicación donde se debe dibujar la imagen. Para efectos de demostración, el siguiente código utiliza la versión de sobrecarga de DrawImage que acepta un objeto de Point como segundo parámetro e intenta dibujar la firma en la esquina inferior derecha de la imagen primaria.
#### **Guardando la Imagen**
Finalmente, guardar la imagen de nuevo en el disco local como un archivo PNG utilizando la clase PngOptions.
#### **Código Fuente Completo**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddSignatureToImage-AddSignatureToImage.cs" >}}
