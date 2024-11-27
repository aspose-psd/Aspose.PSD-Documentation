---
title: Dibujando imágenes usando GraphicsPath
type: docs
weight: 30
url: /es/net/dibujando-imagenes-usando-graphicspath/
---

## **Dibujando imágenes usando GraphicsPath**
La clase [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) es responsable de crear y mantener una ruta gráfica. El GraphicsPath no tiene referencia a una imagen y no cambia la imagen en sí, en cambio, puede considerarse como un objeto que contiene metadatos que describen las rutas que la clase Graphics puede dibujar. La clase GraphicsPath utiliza figuras; cada figura está compuesta por una secuencia de líneas y curvas conectadas o una forma primitiva geométrica. Cada forma puede dividirse en segmentos de forma. Puedes añadir, quitar y cambiar diferentes figuras o formas en un objeto GraphicsPath. Una vez que el GraphicsPath ha sido totalmente descrito, utiliza los métodos correspondientes de la clase Graphics (Dibujar ruta y Rellenar rutas) para dibujar sobre o rellenar las rutas. La clase Graphics toma cada segmento de forma y lo dibuja para producir la imagen final.
### **Dibujando usando la clase GraphicsPath**
A continuación se muestra un ejemplo que demuestra el uso de la clase [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath). El código fuente del ejemplo se ha dividido en varias partes para mantenerlo sencillo y fácil de seguir. Paso a paso, los ejemplos te muestran cómo:

- Crear una imagen.
- Inicializar un objeto Graphics.
- Limpiar la superficie.
- Crear una instancia de [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath).
- Crear una figura.
- Añadir formas a la figura.
- Crear un array de Figuras.
- Dibujar rutas.
- Rellenar rutas.


### **Dibujando imágenes usando GraphicsPath: Ejemplos de programación**
#### **GraphicsPath: Crear una imagen**
Comienza creando una imagen usando cualquiera de los métodos descritos en Crear archivos.
#### **GraphicsPath: Inicializar un objeto Graphics**
Crea e inicializa un objeto Graphics pasando el objeto Image a su constructor.
#### **GraphicsPath: Limpiar la superficie**
Limpia la superficie de Graphics llamando al método Clear de la clase Graphics y pasando un Color como parámetro. Este método llena la superficie de Graphics con el color pasado como argumento.
#### **GraphicsPath: Crear una instancia de GraphicsPath**
Crea una instancia de GraphicsPath con GraphicsPath establecido en Alternate de forma predeterminada. Este modo determina cómo rellenar el interior de una figura cerrada. El otro valor posible de GraphicsPath es Winding.
#### **GraphicsPath: Crear una figura**
Crea una instancia de la clase Figure. Como se discutió anteriormente, Figure puede contener Shapes y las formas residen en el espacio de nombres Aspose.PSD.Shapes.
#### **GraphicsPath: Añadir formas a la figura**
El método Add Shapes expuesto por la clase Figure te permite añadir formas a la figura. En los ejemplos de código a continuación, se añaden varias formas a un objeto Figure.
#### **GraphicsPath: Añadir figuras a un array**
Múltiples figuras pueden agregarse a un objeto GraphicsPath usando el método AddFigures expuesto por la clase GraphicsPath. Este método acepta un array de figuras como parámetro.
#### **GraphicsPath: Dibujar las rutas**
Dibuja el GraphicsPath usando el método DrawPath expuesto por la clase Graphics. El método acepta dos parámetros. El primer parámetro es un objeto de la clase Pen, que determina el color, ancho y estilo de la ruta. El segundo parámetro es el objeto de la clase GraphicsPath, que representa la ruta en sí.
#### **GraphicsPath: Rellenar rutas**


Puedes rellenar una ruta pasando un objeto GraphicsPath al método Fill Paths expuesto por la clase Graphics. El método Fill Paths llena la ruta según el modo de relleno (alternativo o winding) actualmente establecido para la ruta. Si la ruta tiene alguna figura abierta, la ruta se rellena como si esas figuras estuvieran cerradas.

El método Fill Paths acepta dos parámetros. El primer parámetro es un objeto de cualquier clase de pincel del espacio de nombres Aspose.PSD.Brushes. El segundo parámetro es la propia ruta. Para este ejemplo, utiliza HatchBrush, que es un pincel rectangular con un estilo de hatch, un color frontal y un color de fondo. Antes de pasar el objeto HatchBrush al método Fill Paths, configura sus propiedades.
### **GraphicsPath: Fuente completa**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}



Todas las clases que implementan IDisposable se instancian en una declaración Using para asegurar que se eliminen correctamente.

