---
title: Procesamiento de datos brutos
type: docs
weight: 70
url: /es/java/procesamiento-de-datos-brutos/
---

## **Procesamiento de datos brutos**
Para mejorar el rendimiento de la API Aspose.PSD, introdujimos un método para el procesamiento de datos brutos con la versión 2.4.0. El procesamiento de datos brutos se utiliza internamente y tiene una API externa para que pueda ser utilizado desde fuera de la biblioteca para mejorar el rendimiento general. A veces, el procesamiento se vuelve un poco complicado y necesita una explicación. Actualmente, el procesamiento de datos brutos está disponible solo para el formato BMP.

Para ayudar a los desarrolladores a obtener el mejor rendimiento, la API Aspose.PSD proporciona un sistema de procesamiento de datos brutos que tiene una API externa para personalización. Los desarrolladores llaman a la familia de métodos LoadRawData y SaveRawData para usar el procesamiento de datos brutos. Estos métodos también requieren que el formato de datos brutos deseado se establezca utilizando la clase RawDataSettings. La clase RawDataSettings permite a los desarrolladores especificar cualquier formato de datos brutos. Sin embargo, para lograr el mejor rendimiento, se necesita usar el formato de datos brutos en el que los datos están almacenados. Los RawDataSettings definidos en la clase RasterImage ayudan a determinar el formato de datos brutos de la imagen. Al pasar la instancia de RawDataSettings al método LoadRawData, los datos se devuelven tal como están, sin ninguna conversión aplicada, y pueden mejorar el rendimiento. Por otro lado, es necesario tener cuidado con todos los posibles formatos de disposición de datos brutos, que a veces pueden ser un poco complicados.

Para simplificar el proceso de manejo, a costa de una pequeña penalización de rendimiento, puede especificar los RawDataSettings deseados instanciando e inicializando la clase con la configuración de datos brutos deseada. Hay casos en los que no es posible devolver los datos brutos en el formato especificado (por ejemplo, la conversión del espacio de color CMYK a RGB no está disponible en la versión 2.4.0). Además, puede haber escenarios en los que el procesamiento de datos brutos no esté disponible en absoluto para un formato de imagen. Para determinar si puede utilizar las familias de métodos LoadRawData y SaveRawData, debe consultar la propiedad IsRawDataAvailable.
### **Visión general**
Para el formato de datos de píxeles RGB, existen formatos de datos brutos basados en índices (paleta) y basados en RGB. Los formatos de datos brutos basados en índices contienen índices de entrada de paleta en el rango 0..(2^bis cont - 1). Los formatos de datos brutos basados en índices son de 1, 2, 4 y 8 bits por píxel. El resto son formatos de datos brutos basados en RGB. Al cargar datos brutos, asegúrese de que haya suficientes bytes disponibles para cargar los datos; de lo contrario, se generará la excepción correspondiente. Puede estimar fácilmente el tamaño de la matriz de bytes multiplicando el tamaño de línea por las líneas requeridas. El tamaño de línea puede variar y depende del formato de almacenamiento de datos brutos.

Para lograr el mejor rendimiento, siempre use un tamaño de línea de datos brutos igual al valor de la propiedad RasterImage.RawLineSize. Sin embargo, a veces puede ser necesario agregar relleno adicional a las filas de datos brutos, o reducirlo, y en ese caso se puede utilizar un tamaño de línea diferente. Si se requiere un subconjunto de un rectángulo delimitador de una imagen, entonces tenga en cuenta los desplazamientos de bits que pueden ocurrir para los formatos de píxeles RGB indexados. Por ejemplo, consideremos una imagen con dimensiones de 100x100 píxeles y un formato de datos brutos de 1 bit por píxel. Desea cargar un rectángulo de datos brutos con la ubicación (7,0) y dimensiones (2,1), o en otras palabras, necesita 2 píxeles a partir de x=7 e y=0. En este caso, debe recibir el siguiente diseño de datos:



![todo:texto_alternativo_de_la_imagen](procesamiento-de-datos-brutos_1.png)

Esto significa que recibe 2 bytes donde el primer byte contiene 7 píxeles no deseados, luego 1 píxel deseado, y el segundo byte contiene 1 píxel deseado y luego 7 no deseados. Podría preguntarse por qué no hemos realizado un desplazamiento de datos y colocado esos 2 píxeles en un solo byte. La respuesta es simple: para mantener un alto rendimiento. Todo el procesamiento interno se realiza típicamente con todos los datos comenzando desde el primer píxel y terminando con el último píxel disponible. Hay situaciones poco comunes en las que se requiere un subconjunto de píxeles. Además, no tenemos idea de cómo se procesarán esos píxeles posteriormente, por lo que el desplazamiento reducirá el rendimiento y hará que el código sea innecesariamente complejo. Siempre estime el bit correcto (no es necesario determinar el byte correcto ya que los datos siempre vienen con el primer byte lleno) donde comenzarán los píxeles demandados. Para calcular el bit correcto, se puede usar una fórmula simple: (rect.Izquierda * bitsCount) % 8.
### **Conversión de color RGB indexado**
Para obtener el mayor rendimiento posible, siempre use la misma configuración de datos brutos de origen y destino, formatos de píxel y tamaños de línea. Sin embargo, a veces puede ser necesario realizar una conversión de datos. Por ejemplo, puede cargar una imagen RGB de 1 bit por píxel y guardarla con 2 bits por píxel, o cargar una imagen RGB de 4 bits y reducir su rango de color a 2 bits por píxel. En ambos casos, se debe aplicar una conversión de color. La conversión de imágenes RGB indexadas a veces puede ser complicada y no se puede realizar sin algunas configuraciones aplicadas. Necesitamos determinar cómo se asigna el rango de color de la fuente al espacio de color de destino. Para llevar a cabo esta tarea, tenemos diferentes modos:

- Mapeo de paletas (DitheringMethods.PaletteConversion)
- Mapeo de datos brutos (DitheringMethods.PaletteIgnore)
- Conversión personalizada (DitheringMethods.CustomConverter)

Cuando se utiliza la conversión de paleta, el espacio de color de origen intenta coincidir lo más posible con el espacio de color de destino. Por ejemplo, supongamos que tenemos una imagen de 4 bits con los siguientes colores:
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
[3] RGB=51, 51, 51
[4] RGB=68, 68, 68
[5] RGB=85, 85, 85
[6] RGB=102, 102, 102
[7] RGB=119, 119, 119
[8] RGB=136, 136, 136
[9] RGB=153, 153, 153
[10] RGB=170, 170, 170
[11] RGB=187, 187, 187
[12] RGB=204, 204, 204
[13] RGB=221, 221, 221
[14] RGB=238, 238, 238
[15] RGB=255, 255, 255

La imagen de origen se ve así:



![todo:texto_alternativo_de_la_imagen](procesamiento-de-datos-brutos_2.png)

Y convertimos la imagen de 4 bits a una imagen de 1 bit con los siguientes colores de paleta definidos:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

En el modo de conversión de paleta, el convertidor lee el color de origen y determina el índice de destino utilizando el método GetNearestColorIndex de la paleta de destino. El valor de la propiedad RasterImage.RawFallbackIndex se utiliza en caso de que el método GetNearestColorIndex de la paleta dé un índice fuera de rango. Esto convierte los colores de origen a los colores de destino más cercanos en términos de valores de intensidad. La imagen de destino coincide lo más posible con la imagen de origen. Puede ver el siguiente resultado:



![todo:texto_alternativo_de_la_imagen](procesamiento-de-datos-brutos_3.png)

En el modo de mapeo de datos brutos se utiliza un escenario diferente. Las paletas de colores de origen y destino simplemente se ignoran y los índices de origen se asignan a los índices de destino. Cuando se encuentra un valor que no se puede asignar al rango de destino (cuando se disminuyen los bits), entonces se utiliza el valor de la propiedad RasterImage.RawFallbackIndex. El valor es 0 de forma predeterminada y se asignará al primer color de la paleta de destino. Si este valor de propiedad está fuera del rango de destino, se generará la excepción apropiada. Esto conduce a resultados menos predecibles que se pueden mostrar en la siguiente imagen:



![todo:texto_alternativo_de_la_imagen](procesamiento-de-datos-brutos_4.png)

El modo de conversión de paleta es una solución más correcta para el problema de mapeo de colores, pero también requiere un poco más de tiempo para completarse, ya que se deben realizar cálculos para estimar el mapeo correcto de las paletas. (Por lo general, hay una diferencia de rendimiento muy pequeña entre los dos métodos). Por otro lado, el modo de mapeo de datos brutos se ejecuta un poco más rápido y puede usarse para una conversión de color más áspera cuando la asignación exacta de colores no es tan importante. Por ejemplo, hay casos en los que la paleta de colores de origen se recorta y se puede convertir de manera segura a un menor número de bits, ya que los bits adicionales no se han utilizado de todos modos.

Para utilizar cualquiera de estos enfoques, use la propiedad RawDitheringMethod de la clase RasterImage. De forma predeterminada, está configurada en el método de conversión de paleta para lograr los mejores resultados visuales. Puede cambiar esta propiedad antes de que se realice cualquier conversión (por ejemplo, al guardar una imagen en un flujo). Tenga en cuenta que los métodos de ignorar paleta y conversión de paleta no se ejecutarán si ha cargado una imagen y ha reescrito algunos de los datos de píxeles originales, ya que los nuevos datos van a caché y el caché almacena los datos en el formato máximo disponible 32ARGB (a partir de la versión 2.4.0, sujeto a cambios). Este formato se utiliza para superar problemas con posibles rangos de colores diferentes para las imágenes cargadas y guardadas. Además, los métodos de ignorar paleta y conversión de paleta serán ignorados cuando una imagen se carga en modo RGB y se convierte a modo indexado o viceversa.
### **Convertidores de color personalizados**
A veces no es suficiente utilizar el enfoque estándar para la conversión de colores. Es posible que desee utilizar un algoritmo personalizado para obtener completa libertad al usar rutinas de conversión de colores. Cuando los formatos de píxeles de las imágenes de origen y destino son ambos formatos RGB indexados, se puede usar una interfaz más simple, IIndexedColorConverter. Debe establecer la propiedad RawIndexedColorConverter de la clase RasterImage en una instancia de la interfaz IIndexedColorConverter y usar el valor de propiedad DitheringMethods.CustomConverter para RawDitheringMethod. Cuando se implica esta combinación, cualquier conversión de color indexada pasa a través de esa instancia específica de IIndexedColorConverter. El convertidor de color indexado personalizado tiene el siguiente método definido:



{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



El método FillIndexedtoIndexedMap se llama cuando se requiere la conversión desde una imagen RGB indexada a un formato de imagen RGB indexado (cuando cualquiera de los conteos de 1, 2, 4 o 8 bits se convierten entre sí). El arreglo de map tiene la longitud de todos los posibles conteos de entradas de formato de origen. Debe completar ese arreglo para mapear desde la entrada de la paleta de colores de origen a la entrada de la paleta de colores de destino. Asegúrese de que el valor del índice de destino esté en el rango de 0..(bits count - 1), o se generará la excepción correspondiente.

Si se requiere realizar un escenario de conversión de colores más personalizado, entonces la propiedad RawCustomColorConverter de la clase RasterImage debería establecerse en una instancia de la interfaz IColorConverter. La propiedad RawCustomColorConverter siempre anula la propiedad RawIndexedColorConverter si ambas están establecidas y un convertidor de color indexado no se usará en dicho caso. La interfaz IColorConverter tiene un solo método:



{{< highlight java >}}

 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 

{{< /highlight >}}



El método Convert se llama cada vez que se requiere una conversión de color. El método recibe los datos brutos de origen en el formato de origen y tiene un búfer de salida para recibir el formato de color convertido al destino. El búfer de destino debe ser suficiente para recibir los datos convertidos (si la llamada a la interfaz se realiza internamente por la biblioteca Aspose.PSD) y debe contener los datos brutos convertidos al finalizar el método. El método Convert puede ser llamado varias veces hasta que se cubran todos los datos de origen.