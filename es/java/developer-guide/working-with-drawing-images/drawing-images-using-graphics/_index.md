---
title: Dibujando imágenes usando Graphics
type: docs
weight: 20
url: /es/java/drawing-images-using-graphics/
---

## **Dibujando imágenes usando Graphics**

Con la biblioteca Aspose.PSD puedes dibujar formas simples como líneas, rectángulos y círculos, así como formas complejas como polígonos, curvas, arcos y formas de Bezier. La biblioteca Aspose.PSD crea tales formas utilizando la clase Graphics que reside en el espacio de nombres Aspose.PSD. Los objetos Graphics son responsables de realizar diferentes operaciones de dibujo en una imagen, cambiando así la superficie de la imagen. La clase Graphics utiliza una variedad de objetos auxiliares para mejorar las formas:

- Lápices, para dibujar líneas, contornos de formas u otras representaciones geométricas.
- Pinceles, para definir cómo se rellenan las áreas.
- Fuentes, para definir la forma de los caracteres de texto.

### **Dibujando con la Clase Graphics**

A continuación se muestra un ejemplo de código que demuestra el uso de la clase Graphics. El código de ejemplo se ha dividido en varias partes para mantenerlo simple y fácil de seguir. Paso a paso, los ejemplos muestran cómo:

1. Crear una imagen.
1. Crear e inicializar un objeto Graphics.
1. Borrar la superficie.
1. Dibujar una elipse.
1. Dibujar un polígono relleno y guardar la imagen.

### **Muestras de Programación**

#### **Creando una Imagen**

Comience creando una imagen utilizando cualquiera de los métodos descritos en la creación de archivos.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}

#### **Crear e Inicializar un Objeto Graphics**

Luego cree e inicialice un objeto Graphics pasando el objeto de imagen a su constructor.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}

#### **Borrar la Superficie**

Borre la superficie de Graphics llamando al método Clear de la clase Graphics y pasando un color como parámetro. Este método llena la superficie de Graphics con el color pasado como argumento.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

#### **Dibujar una Elipse**

Puede notar que la clase Graphics ha expuesto un montón de métodos para dibujar y rellenar formas. Encontrará la lista completa de métodos en Aspose.PSD para la Referencia de API de Java. Existen varias versiones sobrecargadas del método DrawEllipse expuesto por la clase Graphics. Todos estos métodos aceptan un objeto Pen como su primer argumento. Los parámetros posteriores se pasan para definir el rectángulo delimitador alrededor de la elipse. Para este ejemplo, use la versión que acepta un objeto Rectangle como segundo parámetro para dibujar una elipse utilizando el objeto Pen en el color deseado.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}

#### **Dibujar un Polígono Relleno**

A continuación, dibuje un polígono usando el LinearGradientBrush y una matriz de puntos. La clase Graphics ha expuesto varias versiones sobrecargadas del método FillPolygon. Todos estos aceptan un objeto Brush como primer argumento, definiendo las características del relleno. El segundo parámetro es una matriz de puntos. Tenga en cuenta que cada dos puntos consecutivos en el array especifican un lado del polígono.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

### **Dibujando Imágenes usando Graphics: Código Fuente Completo**

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}



Todas las clases que implementan IDisposable y acceden a recursos no administrados se instancian en una declaración Using para asegurar que se eliminen correctamente.

