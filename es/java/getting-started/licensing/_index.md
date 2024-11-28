---
title: Licencia
type: docs
weight: 60
url: /es/java/licencia/
---

## **Limitaciones de la Versión de Evaluación**
Puede descargar una versión de evaluación de Aspose.PSD para Java desde la [página de descargas](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). La versión de evaluación proporciona las mismas funciones que la versión con licencia completa del componente con algunas restricciones. Cuando compre Aspose.PSD, simplemente aplicar la licencia eliminará cualquier restricción de la versión de evaluación instalada.

La versión de evaluación de Aspose.PSD para Java proporciona la funcionalidad completa del producto, con solo dos limitaciones:

- **Una marca de agua en cada imagen**: Cualquier imagen que guarde, modifique o exporte tiene una marca de agua que dice "Solo Evaluación. Creado con Aspose.PSD. Copyright 2018-2019 Aspose Pty Ltd.". En imágenes pequeñas, donde la marca de agua completa no cabe, aparecen dos líneas diagonales a través de la imagen en su lugar.
- **No hay soporte para la funcionalidad principal de dibujo**: En modo de evaluación, los píxeles de imagen no pueden cargarse ni guardarse en la imagen. Para dibujar imágenes, utilice en su lugar la funcionalidad de dibujo avanzada. Esta limitación afecta a la funcionalidad que depende de la funcionalidad principal de dibujo. Aspose.PSD para Java le permite registrar su propio formato de archivo. Sin embargo, esta característica depende de la funcionalidad principal de dibujo, por lo que no tiene sentido usarla en modo de evaluación porque no puede cambiar el contenido de esos archivos.

{{% alert color="primary" %}}

Si desea probar Aspose.PSD para Java sin las limitaciones de la versión de prueba, solicite una licencia temporal de 30 días. Consulte [Cómo obtener una Licencia Temporal?](https://purchase.aspose.com/temporary-license) para obtener más información.

{{% /alert %}} 
## **Acerca del Archivo de Licencia**
Una vez que esté satisfecho con su evaluación de Aspose.PSD, puede adquirir una licencia en el [sitio web de Aspose](https://purchase.aspose.com/default.aspx). Familiarícese con los distintos tipos de suscripciones ofrecidos. Si tiene alguna pregunta, no dude en ponerse en contacto con el [equipo de ventas de Aspose](https://company.aspose.com/contact).

Cada licencia de Aspose incluye una suscripción de un año para actualizaciones de software. Después del primer año, renueve sus suscripciones para continuar obteniendo las últimas funciones y correcciones. El soporte técnico es gratuito e ilimitado y se proporciona tanto a usuarios con licencia como de evaluación a través de nuestros [Foros de Soporte](https://forum.aspose.com/).

La licencia es un archivo XML que contiene detalles como el nombre del producto, la cantidad de desarrolladores con licencia, la fecha de vencimiento de la suscripción, entre otros. El archivo está firmado digitalmente, así que no lo modifique: incluso agregar inadvertidamente un salto de línea adicional invalida el archivo.

Después de comprar Aspose.PSD, es necesario aplicar la licencia antes de crear, editar o manipular imágenes. Si olvida aplicar la licencia, las imágenes resultantes tendrán una marca de agua de evaluación. Solo necesita establecer la licencia una vez por aplicación o proceso que desarrolle.
## **Aplicación de la Licencia**
Puede descargar una versión de evaluación de **Aspose.PSD** para Java desde [su página de descargas](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). La versión de evaluación proporciona exactamente las mismas capacidades que la versión con licencia del producto. Además, la versión de evaluación se convierte en una licencia cuando compra una licencia y agrega un par de líneas de código para aplicarla.

Una vez que esté satisfecho con su evaluación de **Aspose.PSD**, puede [comprar una licencia](http://www.aspose.com/Purchase/Components/Default.aspx) en el sitio web de Aspose. Familiarícese con los distintos tipos de suscripciones ofrecidos. Si tiene alguna pregunta, no dude en ponerse en contacto con el equipo de ventas de Aspose.

Cada licencia de Aspose incluye una suscripción de un año para actualizaciones gratuitas a nuevas versiones o correcciones que salgan durante este tiempo. El soporte técnico es gratuito e ilimitado y se proporciona tanto a usuarios con licencia como de evaluación.

{{% alert color="primary" %}}

Si desea probar **Aspose.PSD** sin las limitaciones de la versión de evaluación, solicite una licencia temporal de 30 días. Consulte [Cómo obtener una Licencia Temporal?](http://www.aspose.com/corporate/how-to-get-temporary-license.aspx) para obtener más información.

{{% /alert %}} 
### **Estableciendo una Licencia**
La licencia es un archivo XML de texto plano que contiene detalles como el nombre del producto, la cantidad de developers a quienes se les otorga licencia, la fecha de vencimiento de la suscripción, entre otros. El archivo está firmado digitalmente, así que no modifiques el archivo; incluso la adición involuntaria de un salto de línea adicional en el archivo lo invalidará.

Debe establecer una licencia antes de utilizar **Aspose.PSD** si desea evitar sus limitaciones de evaluación. Solo se requiere establecer una licencia una vez por aplicación o proceso.

La licencia se puede cargar desde un flujo de datos o un archivo en las siguientes ubicaciones:

1. Ruta explícita.
1. La carpeta que contiene Aspose.PSD.jar.

Utilice el método [License](http://www.aspose.com/api/java/psd/com.aspose.psd/classes/License).setLicense para otorgar licencia al componente. A menudo, la manera más sencilla de establecer una licencia es colocar el archivo de licencia en la misma carpeta que Aspose.PSD.jar y especificar solo el nombre del archivo sin la ruta como se muestra en el siguiente ejemplo:
#### **Ejemplo 1**
En este ejemplo, **Aspose.PSD** intentará encontrar el archivo de licencia en la carpeta que contiene los JARs de su aplicación.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense("Aspose.PSD.Java.lic");

{{< /highlight >}}
#### **Ejemplo 2**
Inicializa una licencia desde un flujo de datos.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense(new java.io.FileInputStream("Aspose.PSD.Java.lic"));

{{< /highlight >}}
### **Validar la Licencia**
Es posible validar si la licencia se ha establecido correctamente o no. La clase License tiene el campo isLicensed que devolverá true si la licencia se ha establecido correctamente.

**Java**

{{< highlight csharp >}}

 License license = new License();

license.setLicense("Aspose.PSD.Java.lic");

if (License.isLicensed()) {

    System.out.println("Licencia Establecida!");

}

{{< /highlight >}}
## **Dónde Aplicar una Licencia en su Aplicación**
Dónde aplicar una licencia depende del tipo de aplicación que esté desarrollando. Siga estas reglas simples:

- La licencia solo necesita establecerse una vez por dominio de aplicación. Llamar a License.setLicense múltiples veces no es perjudicial pero consume tiempo del procesador.
- Aplique la licencia antes de llamar a cualquier clase de Aspose.PSD.
- **Aplicaciones Java**: llame a License.SetLicense en el código de inicio.
- **Biblioteca de Clases**: llame a License.setLicense desde un constructor estático de la clase que utiliza Aspose.PSD. El constructor estático se ejecuta antes de crear una instancia de su clase, asegurando que la licencia de Aspose.PSD esté establecida correctamente.
## **Uso de Múltiples Productos Aspose**
Si utiliza más de un producto Aspose en su aplicación, por ejemplo Aspose.PSD y Aspose.Cells, aquí hay algunos consejos útiles.

- **Aplique la licencia para cada producto Aspose por separado**. Incluso si tiene un solo archivo de licencia para todos los componentes, por ejemplo 'Aspose.Total.lic', aún necesita llamar a License.setLicense por separado para cada producto Aspose en su aplicación.
- **Utilice un nombre de clase de licencia completamente calificado**. Cada producto Aspose tiene una clase License en su espacio de nombres. Por ejemplo, Aspose.PSD tiene com.aspose.psd.license.License y Aspose.Cells tiene com.aspose.cells.License. Utilizar un nombre de clase completamente calificado evita cualquier confusión sobre qué licencia se aplica a qué producto.

