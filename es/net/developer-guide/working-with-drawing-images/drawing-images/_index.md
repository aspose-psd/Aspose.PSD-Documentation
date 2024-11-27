---
title: Dibujar Imágenes
type: docs
weight: 10
url: /es/net/drawing-images/
---

## **Dibujar Líneas**
Este ejemplo utiliza la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para dibujar formas de líneas en la superficie de la imagen. Para demostrar la operación, el ejemplo crea una nueva imagen y dibuja líneas en la superficie de la imagen utilizando el método [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) expuesto por la clase Graphics. Primero, crearemos una PsdImage especificando su altura y ancho.

Una vez que la imagen ha sido creada, utilizaremos el método Clear expuesto por la clase Graphics para establecer su color de fondo. El método [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) de la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) se utiliza para dibujar una línea en una imagen conectando dos estructuras de puntos. Este método tiene varias sobrecargas que aceptan la instancia de la clase Pen y pares de coordenadas de puntos o estructuras Point/PointF como argumentos. La clase Pen define un objeto utilizado para dibujar líneas, curvas y figuras. La clase Pen tiene varios constructores sobrecargados para dibujar líneas con color, ancho y pincel especificados. La clase SolidBrush se utiliza para dibujar continuamente con un color específico. Finalmente, la imagen se exporta al formato de archivo bmp. El siguiente fragmento de código muestra cómo dibujar las formas de líneas en la superficie de la imagen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingLines-DrawingLines.cs" >}}
## **Dibujar Elipse**
El ejemplo de dibujar una elipse es el segundo artículo de la serie de formas de dibujo. Utilizaremos la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para dibujar la forma de elipse en la superficie de la imagen. Para demostrar la operación, el ejemplo crea una nueva imagen y dibuja la forma de elipse en la superficie de la imagen utilizando el método DrawEllipse expuesto por la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Primero, crearemos una PsdImage especificando su altura y ancho.

Después de crear la imagen, crearemos e inicializaremos un objeto de la clase Graphics y configuraremos el color de fondo de la imagen utilizando el método Clear de la clase Graphics. El método DrawEllipse de la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) se utiliza para dibujar la forma de elipse en una superficie de imagen especificada por la estructura de rectángulo delimitante. Este método tiene varias sobrecargas que aceptan las instancias de las clases Pen y Rectangle/RectangleF o un par de coordenadas, un alto y un ancho como argumentos. La clase Pen define un objeto utilizado para dibujar líneas, curvas y figuras. La clase Pen tiene varios constructores sobrecargados para dibujar líneas con color, ancho y pincel especificados. La clase Rectangle almacena un conjunto de cuatro enteros que representan la ubicación y el tamaño de un rectángulo. La clase Rectangle tiene varios constructores sobrecargados para dibujar la estructura del rectángulo con tamaño y ubicación especificados. La clase SolidBrush se utiliza para dibujar continuamente con un color específico. Finalmente, la imagen se exporta al formato de archivo bmp. El siguiente fragmento de código muestra cómo dibujar la forma de elipse en la superficie de la imagen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingEllipse-DrawingEllipse.cs" >}}
## **Dibujar Rectángulo**
En este ejemplo, dibujaremos la forma de rectángulo en la superficie de la imagen. Para demostrar la operación, el ejemplo crea una nueva imagen y dibuja la forma de rectángulo en la superficie de la imagen utilizando el método DrawRectangle expuesto por la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Primero, crearemos una PsdImage especificando su altura y ancho. Luego, configuraremos el color de fondo de la imagen utilizando el método Clear de la [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).

El método DrawRectangle de la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) se utiliza para dibujar la forma de rectángulo en una superficie de imagen especificada por la estructura de rectángulo. Este método tiene varias sobrecargas que aceptan las instancias de las clases Pen y Rectangle/RectangleF o par de coordenadas, ancho y alto como argumentos. La clase Rectangle almacena un conjunto de cuatro enteros que representan la ubicación y el tamaño de un rectángulo. La clase Rectangle tiene varios constructores sobrecargados para dibujar la estructura del rectángulo con tamaño y ubicación especificados. Finalmente, la imagen se exporta al formato de archivo bmp. El siguiente fragmento de código muestra cómo dibujar la forma de rectángulo en la superficie de la imagen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingRectangle-DrawingRectangle.cs" >}}
## **Dibujar Arco**
En esta sesión de la serie de formas de dibujo, dibujaremos la forma de arco en la superficie de la imagen. Utilizaremos el método DrawArc de [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para demostrar la operación en una imagen BMP. Primero, crearemos una PsdImage especificando su altura y ancho. Una vez que la imagen ha sido creada, utilizaremos el método Clear expuesto por la [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para establecer su color de fondo.

El método DrawArc de la [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) se utiliza para dibujar la forma de arco en una superficie de imagen. DrawArc representa una porción de una elipse especificada por la estructura de rectángulo o un par de coordenadas. Este método tiene varias sobrecargas que aceptan las instancias de las clases Pen y estructura Rectangle/RectangleF o un par de coordenadas, un ancho y un alto como argumentos. Finalmente, la imagen se exporta al formato de archivo bmp. El siguiente fragmento de código muestra cómo dibujar la forma de arco en la superficie de la imagen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
## **Dibujar Bezier**
Este ejemplo utiliza la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para dibujar la forma de bezier en la superficie de la imagen. Para demostrar la operación, el ejemplo crea una nueva imagen y dibuja la forma de bezier en la superficie de la imagen utilizando el método DrawBezier expuesto por la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Primero, crearemos una PsdImage especificando su altura y ancho. Una vez que la imagen ha sido creada, utilizaremos el método Clear expuesto por la [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para establecer su color de fondo.

El método DrawBezier de la [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) se utiliza para dibujar la forma de spline bezier en una superficie de imagen definida por cuatro estructuras de Point. Este método tiene varias sobrecargas que aceptan las instancias de la clase Pen y cuatro pares ordenados de coordenadas o cuatro estructuras Point/PointF o una matriz de estructuras Point/PointF. La clase Pen define un objeto utilizado para dibujar líneas, curvas y figuras. La clase Pen tiene varios constructores sobrecargados para dibujar líneas con color, ancho y pincel especificados. Finalmente, la imagen se exporta al formato de archivo bmp. El siguiente fragmento de código muestra cómo dibujar la forma de bezier en la superficie de la imagen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingBezier-DrawingBezier.cs" >}}
## **Dibujar Imágenes usando Funcionalidad Principal**
Aspose.PSD es una biblioteca que ofrece muchas características valiosas, incluida la creación de imágenes desde cero. Dibuja utilizando la funcionalidad principal como la manipulación de la información de mapa de bits de una imagen, o utiliza las características avanzadas como [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) y [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) para dibujar formas en la superficie de la imagen con la ayuda de diferentes pinceles y lápices. Utilizando la clase RasterImage de Aspose.PSD, puedes recuperar la información de píxeles de un área de imagen y manipularla. La clase RasterImage contiene toda la funcionalidad principal de dibujo, como obtener y establecer píxeles y otros métodos para la manipulación de imágenes. Crea una nueva imagen utilizando cualquiera de los métodos descritos en la creación de archivos y asígnala a una instancia de la clase RasterImage. Utiliza el método LoadPixels de la clase RasterImage para recuperar la información de píxeles de una porción de una imagen. Una vez que tienes una matriz de píxeles, puedes manipularla, por ejemplo, cambiando el color de cada píxel. Después de manipular la información de los píxeles, establece de nuevo en el área deseada de la imagen utilizando el método SavePixels de la clase RasterImage. El siguiente fragmento de código muestra cómo dibujar imágenes usando la funcionalidad principal. 



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}

