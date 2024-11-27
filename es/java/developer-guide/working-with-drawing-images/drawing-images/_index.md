---
title: Dibujando Imágenes
type: docs
weight: 10
url: /es/java/dibujando-imagenes/
---

## **Dibujando Líneas**
Este ejemplo utiliza la clase Graphics para dibujar formas de línea en la superficie de la imagen. Para demostrar la operación, el ejemplo crea una nueva imagen y dibuja líneas en la superficie de la imagen utilizando el método DrawLine expuesto por la clase Graphics. Primero, crearemos una PsdImage especificando su altura y anchura.

Una vez que se ha creado la imagen, utilizaremos el método Clear expuesto por la clase Graphics para establecer el color de fondo. El método DrawLine de la clase Graphics se utiliza para dibujar una línea en una imagen que conecta dos estructuras de puntos. Este método tiene varios sobrecargas que aceptan la instancia de la clase Pen y pares de coordenadas de puntos o estructuras Point/PointF como argumentos. La clase Pen define un objeto utilizado para dibujar líneas, curvas y figuras. La clase Pen tiene varios constructores sobrecargados para dibujar líneas con un color, grosor y pincel especificados. La clase SolidBrush se utiliza para dibujar de manera continua con un color específico. Finalmente, la imagen se exporta al formato de archivo BMP. El siguiente fragmento de código te muestra cómo dibujar formas de línea en la superficie de la imagen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingLines-DrawingLines.java" >}}

## **Dibujando Elipse**
El ejemplo de dibujo de elipse es el segundo artículo de la serie de formas de dibujo. Utilizaremos la clase Graphics para dibujar la forma de elipse en la superficie de la imagen. Para demostrar la operación, el ejemplo crea una nueva imagen y dibuja la forma de elipse en la superficie de la imagen utilizando el método DrawEllipse expuesto por la clase Graphics. Primero, crearemos una PsdImage especificando su altura y anchura.

Después de crear la imagen, crearemos e inicializaremos un objeto de la clase Graphics y estableceremos el color de fondo de la imagen utilizando el método Clear de la clase Graphics. El método DrawEllipse de la clase Graphics se utiliza para dibujar la forma de elipse en una superficie de imagen especificada por la estructura del rectángulo límite. Este método tiene varias sobrecargas que aceptan las instancias de las clases Pen y Rectangle/RectangleF o un par de coordenadas, una altura y una anchura como argumentos. La clase Pen define un objeto utilizado para dibujar líneas, curvas y figuras. La clase Pen tiene varios constructores sobrecargados para dibujar líneas con un color, grosor y pincel especificados. La clase Rectangle almacena un conjunto de cuatro enteros que representan la ubicación y el tamaño de un rectángulo. La clase Rectangle tiene varios constructores sobrecargados para dibujar la estructura del rectángulo con el tamaño y la ubicación especificados. La clase SolidBrush se utiliza para dibujar de manera continua con un color específico. Finalmente, la imagen se exporta al formato de archivo BMP. El siguiente fragmento de código te muestra cómo dibujar la forma de elipse en la superficie de la imagen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}

## **Dibujando Rectángulo**
En este ejemplo, dibujaremos la forma de rectángulo en la superficie de la imagen. Para demostrar la operación, el ejemplo crea una nueva imagen y dibuja la forma de rectángulo en la superficie de la imagen utilizando el método DrawRectangle expuesto por la clase Graphics. Primero, crearemos una PsdImage especificando su altura y anchura. Luego, estableceremos el color de fondo de la imagen utilizando el método Clear de la clase Graphics.

El método DrawRectangle de la clase Graphics se utiliza para dibujar la forma de rectángulo en una superficie de imagen especificada por la estructura del rectángulo. Este método tiene varias sobrecargas que aceptan las instancias de las clases Pen y Rectangle/RectangleF o un par de coordenadas, un ancho y una altura como argumentos. La clase Rectangle almacena un conjunto de cuatro enteros que representan la ubicación y el tamaño de un rectángulo. La clase Rectangle tiene varios constructores sobrecargados para dibujar la estructura de rectángulo con el tamaño y ubicación especificados. Finalmente, la imagen se exporta al formato de archivo BMP. El siguiente fragmento de código te muestra cómo dibujar la forma de rectángulo en la superficie de la imagen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingRectangle-DrawingRectangle.java" >}}

## **Dibujando Arco**
En esta sesión de la serie de formas de dibujo, dibujaremos la forma del arco en la superficie de la imagen. Utilizaremos el método DrawArc de Graphics para demostrar la operación en una imagen BMP. Primero, crearemos una PsdImage especificando su altura y anchura. Una vez que se haya creado la imagen, utilizaremos el método Clear expuesto por la clase Graphics para establecer el color de fondo.

El método DrawArc de la clase Graphics se utiliza para dibujar la forma del arco en una superficie de imagen. DrawArc representa una parte de una elipse especificada por la estructura del rectángulo o par de coordenadas. Este método tiene varias sobrecargas que aceptan las instancias de las clases Pen y Rectangle/RectangleF o un par de coordenadas, un ancho y una altura como argumentos. Finalmente, la imagen se exporta al formato de archivo BMP. El siguiente fragmento de código te muestra cómo dibujar la forma del arco en la superficie de la imagen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}

## **Dibujando Bezier**
Este ejemplo utiliza la clase Graphics para dibujar la forma de Bezier en la superficie de la imagen. Para demostrar la operación, el ejemplo crea una nueva imagen y dibuja la forma de Bezier en la superficie de la imagen utilizando el método DrawBezier expuesto por la clase Graphics. Primero, crearemos una PsdImage especificando su altura y anchura. Una vez que se haya creado la imagen, utilizaremos el método Clear expuesto por la clase Graphics para establecer el color de fondo.

El método DrawBezier de la clase Graphics se utiliza para dibujar la forma de segmento de Bezier en una superficie de imagen definida por cuatro estructuras de puntos. Este método tiene varias sobrecargas que aceptan las instancias de la clase Pen y cuatro pares ordenados de coordenadas o cuatro estructuras de Point/PointF o matriz de estructuras de Point/PointF. La clase Pen define un objeto utilizado para dibujar líneas, curvas y figuras. La clase Pen tiene varios constructores sobrecargados para dibujar líneas con un color, grosor y pincel especificados. Finalmente, la imagen se exporta al formato de archivo BMP. El siguiente fragmento de código te muestra cómo dibujar la forma de Bezier en la superficie de la imagen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}

## **Dibujando Imágenes utilizando la Funcionalidad Principal**
Aspose.PSD es una biblioteca que ofrece muchas características valiosas, incluida la creación de imágenes desde cero. Dibuja utilizando la funcionalidad principal como manipular la información de bits de una imagen, o utiliza las características avanzadas como Graphics y GraphicsPath para dibujar formas en la superficie de la imagen con la ayuda de diferentes pinceles y plumas. Usando la clase RasterImage de Aspose.PSD, puedes obtener la información de píxeles de una imagen y manipularla. La clase RasterImage contiene toda la funcionalidad principal de dibujo, como obtener y establecer píxeles y otros métodos para la manipulación de imágenes. Crea una nueva imagen utilizando cualquiera de los métodos descritos en la creación de archivos y asígnala a una instancia de la clase RasterImage. Utiliza el método LoadPixels de la clase RasterImage para obtener la información de píxeles de una porción de una imagen. Una vez que tengas un arreglo de píxeles, puedes manipularlo cambiando, por ejemplo, el color de cada píxel. Después de manipular la información de píxeles, agrégala nuevamente al área deseada en la imagen utilizando el método SavePixels de la clase RasterImage. El siguiente fragmento de código te muestra cómo dibujar imágenes utilizando la funcionalidad principal.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.java" >}}
