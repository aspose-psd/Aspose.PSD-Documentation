---
title: Cómo crear un generador de miniaturas de YouTube programáticamente en Java
type: docs
weight: 10
url: /es/java/como-crear-un-generador-de-miniaturas-de-youtube-programaticamente-en-java/
---

## **Introducción**
El propósito de este documento es demostrar el uso de la API de algunas herramientas compuestas de [Aspose.PSD para Java](https://products.aspose.com/psd/java) en un ejemplo del mundo real. En este artículo, se escribirá y explicará **un programa Java simple que genera miniaturas de YouTube** para el canal [DW Documentary](https://www.youtube.com/channel/UCW39zufHfsuGgpLviKh297Q). Se ha elegido este canal del mundo real porque sus miniaturas son bastante estándar e ilustran el uso de algunas herramientas compuestas populares de Aspose.PSD para Java (por ejemplo, efecto de [sombra](/psd/es/java/manipulando-formatos-photoshop/#manipulandophotoshopformats-soporteefectosombra), relleno radial degradado, dibujo de texto y formas):

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_1.png)

## **Cómo funciona en pocas palabras**
Un programa Java simple toma como entrada dos argumentos: un título y una imagen. Se **genera un documento de Photoshop en memoria (PSD)** a partir de esa entrada utilizando Aspose.PSD para Java. Luego, el programa **convierte el documento de PSD a formato de archivo PNG** para obtener una miniatura de YouTube con un tamaño de 1280x720 píxeles. La imagen de salida se ve similar a la siguiente:

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_2.png)

## **Requisitos técnicos**
Se requieren las siguientes tecnologías para ejecutar el código de este artículo con éxito:

- Java 6+
- [Aspose.PSD para Java](/psd/es/java/installation/) (la última versión)

## **Comenzando**
Como se mencionó anteriormente, el programa utiliza PSD en memoria para generar una miniatura. Por lo tanto, comencemos **creando un documento PSD**:

```java
PsdImage psdImage = new PsdImage(1280, 720);
```

Si observas la miniatura de YouTube anterior, podrás notar que **consta de varios componentes**:

1. una imagen de fondo (máscara impresa)
2. un degradado radial PSD (destaca el área en la esquina superior derecha)
3. un logotipo con efecto de sombra
4. un título y un dibujo simple (rectángulo azul)

Profundicemos para ver cómo implementar cada uno de estos componentes utilizando Aspose.PSD para Java en las siguientes secciones.

## **1. Agregar una imagen de fondo**
El orden de las capas es importante. Por lo tanto, es necesario agregar primero una imagen de fondo para que no se superponga a otras capas. Presta atención que solo se admiten [formatos de archivo raster](/psd/es/java/formatos-de-archivo-soportados/) en este momento.

### **1.1. Agregar una imagen de fondo a una capa de Photoshop**
Para **agregar una imagen raster en PSD**, se debe pasar un flujo de entrada como argumento durante la construcción de la capa (ver más [ejemplos de carga de imágenes raster](https://docs.aspose.com/display/psdnet/Creaci%C3%B3n%2C+Apertura+y+Guardado+de+Im%C3%A1genes)):

```java
// Código de ejemplo para añadir una imagen de fondo
```

1.2. Ajustar la imagen de fondo al lienzo

Las siguientes 2 acciones (redimensionar, posicionar) son útiles para aquellos casos en los que **el tamaño de la imagen difiere del tamaño del lienzo**, aunque la imagen de este artículo tiene el mismo tamaño que el lienzo (supongamos que no siempre será así).

Asegúrate de que la imagen cargada **se ajuste** al **tamaño del lienzo** (ver más [ejemplos de redimensionamiento](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages)):

```java
// Código de ejemplo para redimensionar una imagen
```

Después de redimensionar, la posición de la imagen cambia. Por lo tanto, para **restablecer la posición de la imagen**, mueve la imagen redimensionada a la esquina superior izquierda:

```java
// Código de ejemplo para reajustar la posición de la imagen
```

## **2. Agregar un degradado radial**
Hay **dos formas de agregar un degradado radial**, utilizando:

- un [efecto de superposición de degradado](/psd/es/java/aspose-psd-for-java-20-4-release-notes/#-~-text=psdjava-163) en una capa existente (un efecto de degradado que se vincula a la capa actual y se aplica a su contenido)
- una nueva [capa de relleno degradado](/psd/es/java/support-of-fill-layers/#supportoffilllayers-supportoffilllayerswithgradientfill) (una capa independiente que mantiene la configuración independiente del degradado)

Es suficiente utilizar el efecto de superposición de degradado para este ejemplo. Sin embargo, para que este artículo sea más interesante y útil, **se utiliza la capa de relleno degradado** ya que todos los efectos de capa se aplican de manera similar y se utilizará otro efecto de capa en la próxima sección.

### **2.1. Agregar una capa de relleno degradado radial**
El proceso de agregar una nueva capa de relleno degradado consta de los siguientes 2 pasos:

1. Es necesario **declarar la configuración de relleno degradado** ya que no hay uno predefinido. La configuración mínima requerida se parece a lo siguiente (se supone que el tipo de degradado, la escala, el color y los puntos de transparencia son propiedades requeridas):

```java
// Código de ejemplo para configurar un degradado radial
```

La configuración anterior declara un degradado radial que es transparente en los bordes y azul oscuro en el centro. La posición del degradado está en el centro del lienzo de forma predeterminada.

Para invertir el relleno de degradado y desplazarlo ligeramente hacia la esquina superior derecha, utiliza las propiedades opcionales correspondientes:

```java
// Código de ejemplo para invertir y desplazar un degradado radial
```

2. Cuando se haya hecho la configuración, agrega una capa de relleno degradado junto con su configuración en el PSD:

```java
// Código de ejemplo para agregar una capa de relleno degradado radial
```

## **Agregar un logotipo con una sombra**
La **sombra paralela** es un efecto que permite agregar una sombra personalizada a lo largo del contorno del objeto (imagen, texto, etc.).
### **3.1. Agregar un logotipo a una capa de Photoshop**
Se puede utilizar el mismo enfoque que en la sección 1.1. para **agregar un logotipo en PSD**:

```java
// Código de ejemplo para añadir un logotipo
```

### **3.2. Posicionar el logotipo**
La imagen cargada está adherida a la esquina superior izquierda de forma predeterminada. Sin embargo, es necesario agregar algunos **márgenes** para que se parezca a la miniatura original de YouTube en el canal. Por lo tanto, la posición de la imagen debe alejarse de los bordes de la capa:

```java
// Código de ejemplo para posicionar el logotipo
```

### **3.3. Agregar un efecto de sombra paralela al logotipo**
El logotipo puede ser invisible si se usa una imagen de fondo clara. Por lo tanto, es deseable **agregar un efecto de sombra paralela** a un logotipo a través de la propiedad de opciones de fusión (ver más [ejemplos de sombreado](/psd/es/java/manipulando-formatos-photoshop/#manipulandophotoshopformats-soporteefectosombra)):

```java
// Código de ejemplo para agregar un efecto de sombra paralela al logotipo
```

El efecto de sombra paralela no tiene las propiedades requeridas debido a la configuración predeterminada (se ve como la de Photoshop). Sin embargo, la sombra anterior se modifica para que parezca un borde translúcido borroso en los bordes.

## **4. Agregar un dibujo de texto y una forma**
### **3.1. Crear una capa gráfica**
El dibujo no es compatible directamente con una capa regular. Por lo tanto, se utiliza el motor gráfico junto a la capa para **proporcionar una API para dibujar** (ver más [ejemplos de dibujo](/psd/es/java/dibujar-imagenes-usando-graficos/)):

```java
// Código de ejemplo para crear una capa gráfica
```

### **3.2. Dibujar texto multilineal**
Un lector experimentado puede preguntar: ¿por qué no usar una capa de texto para agregar texto? Bueno, hay un par de razones: no se necesita editar texto en este caso porque PSD se genera desde cero cada vez; la personalización de fuentes no es compatible con la [API de texto](https://docs.aspose.com/display/psdnet/Working+With+Text+Layers) aún (v20.6 en el momento de escribir esto).

Es fácil **dibujar algo de texto con una fuente personalizada** simplemente instanciando una fuente deseable e invocando el método correspondiente desde el motor gráfico. Sin embargo, hacer un rectángulo (ver detalles en la siguiente sección) que cambie su altura automáticamente en función del número de líneas de texto es un poco más difícil. Primero se deben calcular las alturas exactas de todas las líneas:

```java
// Código de ejemplo para dibujar texto multilineal
```

Donde 1.15 es la altura de la línea, 3 son los rellenos de texto.

### **3.3. Dibujar un rectángulo**
Incluso es fácil dibujar un rectángulo con un pincel degradado (solo establece un área para dibujar y un rango de colores). Cuando se conoce la altura del texto, se calcula el tamaño y la posición del rectángulo. Para **dibujar un rectángulo relleno en PSD** (no solo un marco) llama al método correspondiente del motor gráfico con todo eso:

```java
// Código de ejemplo para dibujar un rectángulo relleno
```

Donde 40, 15, 25 son sangrías.

## **Resultado**
Por lo tanto, la formación de la miniatura ha terminado. Por lo tanto, es hora de **exportar la miniatura a un formato de archivo raster** (por ejemplo, PNG) para su distribución posterior:

```java
// Código de ejemplo para exportar la miniatura a un formato de archivo raster
```

## **Conclusión**
En este artículo, hemos creado un generador de miniaturas de YouTube para el canal DW Documentary y explicado cómo usar algunas de las herramientas compuestas más populares como el efecto de sombra, el relleno degradado radial, el dibujo de texto y formas.

## **Ejemplo Completo**
Puedes [descargar Aspose.PSD SDK](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentación-Java-Aspose-YouTubeThumbnailGenerator.java" >}}
