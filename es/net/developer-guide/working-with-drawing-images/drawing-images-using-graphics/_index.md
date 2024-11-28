---
title: Dibujar imágenes usando Graphics
type: docs
weight: 20
url: /es/net/dibujo-de-imagenes-usando-graphics/
---

## **Dibujar imágenes usando Graphics**
Con la librería Aspose.PSD puedes dibujar formas simples como líneas, rectángulos y círculos, así como formas complejas como polígonos, curvas, arcos y formas de Bézier. La librería Aspose.PSD crea tales formas utilizando la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) que reside en el espacio de nombres Aspose.PSD. Los objetos Graphics son responsables de realizar diferentes operaciones de dibujo en una imagen, cambiando así la superficie de la imagen. La clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) utiliza una variedad de objetos auxiliares para mejorar las formas:

·         Plumas, para dibujar líneas, contornos de formas o representaciones geométricas.

·         Pinceles, para definir cómo se rellenan las áreas.

·         Fuentes, para definir la forma de los caracteres de texto.
### **Dibujar con la clase Graphics**
A continuación se muestra un ejemplo de código que demuestra el uso de la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). El código de ejemplo se ha dividido en varias partes para mantenerlo simple y fácil de seguir. Paso a paso, los ejemplos muestran cómo:

1. Crear una imagen.
1. Crear e inicializar un objeto Graphics.
1. Borrar la superficie.
1. Dibujar una elipse.
1. Dibujar un polígono relleno y guardar la imagen.
### **Muestras de programación**
#### **Creación de una imagen**
Comience creando una imagen utilizando cualquiera de los métodos descritos en Crear archivos.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Crear e inicializar un objeto Graphics**
Luego cree e inicialice un objeto Graphics pasando el objeto de imagen a su constructor.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **Borrar la superficie**
Borre la superficie Graphics llamando al método Clear de la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) y pase el color como parámetro. Este método rellena la superficie de Graphics con el color pasado como argumento.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **Dibujar una elipse**
Puede notar que la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) ha expuesto muchas funciones para dibujar y rellenar formas. Encontrará la lista completa de métodos en la Referencia de API de Aspose.PSD para .NET. Hay varias versiones sobrecargadas del método DrawEllipse expuesto por la clase Graphics. Todos estos métodos aceptan un objeto Pen como su primer argumento. Los parámetros posteriores se utilizan para definir el rectángulo delimitador alrededor de la elipse. Para este ejemplo, use la versión que acepta un objeto Rectangle como segundo parámetro para dibujar una elipse utilizando el objeto Pen en el color deseado.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Dibujar un polígono relleno**
A continuación, dibuje un polígono utilizando LinearGradientBrush y una matriz de puntos. La clase Graphics ha expuesto varias versiones sobrecargadas del método FillPolygon(). Todas estas aceptan un objeto Brush como su primer argumento, definiendo las características del relleno. El segundo parámetro es una matriz de puntos. Tenga en cuenta que cada dos puntos consecutivos en la matriz especifican un lado del polígono.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **Dibujar imágenes usando Graphics: Código fuente completo**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

Todas las clases que implementan IDisposable y acceden a recursos no administrados se instancian en una declaración Using para asegurarse de que se desechen correctamente.  
