---
title: Dibujar imágenes usando GraphicsPath
type: docs
weight: 30
url: /es/java/dibujar-imagenes-usando-graphicspath/
---

## **Dibujar imágenes usando GraphicsPath**
La clase GraphicsPath es responsable de crear y mantener una ruta gráfica. El GraphicsPath no tiene referencia a una imagen y no cambia la imagen en sí, en cambio, puede considerarse como un objeto que contiene metadatos que describen las rutas que la clase Graphics puede dibujar. La clase GraphicsPath utiliza figuras; cada figura está compuesta ya sea por una secuencia de líneas y curvas conectadas o por una forma geométrica primitiva. Cada forma puede dividirse en segmentos de forma. Puedes añadir, eliminar y cambiar diferentes figuras o formas en un objeto GraphicsPath. Cuando el GraphicsPath ha sido totalmente descrito, utiliza los métodos correspondientes de la clase Graphics (DrawPath y Fill Paths) para dibujar sobre o rellenar las rutas. La clase Graphics toma cada segmento de forma y lo dibuja para producir la imagen final.

### **Dibujar usando la clase GraphicsPath**
A continuación se muestra un ejemplo que demuestra el uso de la clase GraphicsPath. El código fuente del ejemplo ha sido dividido en varias partes para mantenerlo simple y fácil de seguir. Paso a paso, los ejemplos te muestran cómo:

- Crear una imagen.
- Inicializar un objeto Graphics.
- Limpiar la superficie.
- Crear una instancia de GraphicsPath.
- Crear una figura.
- Añadir formas a la figura.
- Crear un array de figuras.
- Dibujar rutas.
- Rellenar rutas.

### **Dibujar imágenes usando GraphicsPath: Ejemplos de programación**
#### **GraphicsPath: Crear una imagen**
Comienza creando una imagen utilizando cualquiera de los métodos descritos en la creación de archivos.
#### **GraphicsPath: Inicializar un objeto Graphics**
Crea e inicializa un objeto Graphics pasando el objeto Image a su constructor.
#### **GraphicsPath: Limpiar la superficie**
Limpia la superficie gráfica llamando al método Clear de la clase Graphics y pasa un Color como parámetro. Este método llena la superficie gráfica con el color pasado como argumento.
#### **GraphicsPath: Crear una instancia de GraphicsPath**
Crea una instancia de GraphicsPath con GraphicsPath establecido en Alternar de forma predeterminada. Este modo determina cómo rellenar el interior de una figura cerrada. El otro valor posible de GraphicsPath es Winding.
#### **GraphicsPath: Crear una figura**
Crea una instancia de la clase Figure. Como se discutió anteriormente, Figure puede contener Shapes y las formas residen en el espacio de nombres Aspose.PSD.Shapes.
#### **GraphicsPath: Añadir formas a la figura**
El método Add Shapes expuesto por la clase Figure te permite añadir formas a la figura. En los ejemplos de código a continuación, varias formas se añaden a un objeto Figure.
#### **GraphicsPath: Añadir figuras a un array**
Se pueden añadir múltiples figuras a un objeto GraphicsPath utilizando el método AddFigures expuesto por la clase GraphicsPath. Este método acepta un array de figuras como parámetro.
#### **GraphicsPath: Dibujar las rutas**
Dibuja el GraphicsPath utilizando el método DrawPath expuesto por la clase Graphics. El método acepta dos parámetros. El primer parámetro es un objeto de la clase Pen, que determina el color, ancho y estilo de la ruta. El segundo parámetro es un objeto de la clase GraphicsPath, representando la ruta en sí.
#### **GraphicsPath: Rellenar rutas**

Puedes rellenar una ruta pasando un objeto GraphicsPath al método Fill Paths expuesto por la clase Graphics. El método Fill Paths rellena la ruta de acuerdo al modo de relleno (alternar o winding) establecido actualmente para la ruta. Si la ruta tiene alguna figura abierta, la ruta se rellena como si esas figuras estuvieran cerradas.

El método Fill Paths acepta dos parámetros. El primer parámetro es un objeto de cualquier clase de pincel del espacio de nombres Aspose.PSD.Brushes. El segundo parámetro es la ruta en sí. Para este ejemplo, utiliza HatchBrush que es un pincel rectangular con un estilo de trama, un color de primer plano y un color de fondo. Antes de pasar el objeto HatchBrush al método Fill Paths, establece sus propiedades.
### **GraphicsPath: Código fuente completo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}

Todas las clases que implementan IDisposable se instancian en una instrucción Using para garantizar que se eliminen correctamente.
