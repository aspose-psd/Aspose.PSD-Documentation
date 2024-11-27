---
title: Licencias
type: docs
weight: 70
url: /es/net/licensing/
description: Evaluar la biblioteca de C# de Photoshop PSD de NuGet y aplicar la licencia utilizando un archivo o flujo para eliminar cualquier restricción de la evaluación instalada.
---

## **Limitaciones de la Versión de Evaluación**
Puede descargar una versión de evaluación de Aspose.PSD para .NET desde [NuGet](https://www.nuget.org/packages/Aspose.psd/). La versión de evaluación proporciona las mismas características que la versión con licencia completa del componente con un par de restricciones. Cuando compre Aspose.PSD, simplemente aplicar la licencia elimina cualquier restricción de la evaluación instalada. La versión de evaluación de Aspose.PSD para .NET proporciona funcionalidad completa del producto, con solo dos limitaciones:

- **Una marca de agua en cada imagen**: Cualquier imagen que guarde, modifique o exporte tiene una marca de agua que lee "Solo Evaluación. Creado con Aspose.PSD. Copyright 2010-2018 Aspose Pty Ltd.". En imágenes pequeñas, donde la marca de agua completa no cabe, hay dos líneas diagonales a través de la imagen en su lugar.
- **No hay soporte para funcionalidades de dibujo core**: En modo de evaluación, los píxeles de la imagen no pueden cargarse o guardarse en la imagen. Para dibujar imágenes, use en su lugar la funcionalidad de dibujo avanzada. Esta limitación afecta a la funcionalidad que depende de la funcionalidad de dibujo principal. Aspose.PSD para .NET le permite registrar su propio formato de archivo. Sin embargo, esta característica depende de la funcionalidad de dibujo principal, por lo que no tiene sentido usarla en modo de evaluación porque no se puede cambiar el contenido de esos archivos.

Si desea probar Aspose.PSD para .NET sin las limitaciones de la evaluación, solicite una licencia temporal de 30 días. Consulte [Cómo obtener una Licencia Temporal?](https://purchase.aspose.com/temporary-license) para obtener más información.
## **Acerca del Archivo de Licencia**
Una vez que esté satisfecho con su evaluación de Aspose.PSD, puede comprar una licencia en el [sitio web de Aspose](https://purchase.aspose.com/default.aspx). Familiarícese con los diferentes tipos de suscripciones ofrecidas. Si tiene alguna pregunta, no dude en contactar al [equipo de ventas de Aspose](https://company.aspose.com/contact). Cada licencia de Aspose viene con una suscripción de un año para actualizaciones de software. Después del primer año, renueve sus suscripciones para seguir obteniendo las últimas características y correcciones. El soporte técnico es gratuito e ilimitado y se proporciona tanto a usuarios con licencia como a evaluación a través de nuestros [Foros de Soporte](https://forum.aspose.com/). La licencia es un archivo XML que contiene detalles como el nombre del producto, el número de desarrolladores con licencia, la fecha de vencimiento de la suscripción, entre otros. El archivo está firmado digitalmente, así que no lo modifique: incluso agregar involuntariamente un salto de línea adicional invalidará el archivo. Después de comprar Aspose.PSD, necesita aplicar la licencia antes de crear, editar o manipular imágenes. Si olvida aplicar la licencia, cualquier imagen de salida tendrá una marca de agua de evaluación. Solo necesita establecer la licencia una vez por aplicación o proceso que desarrolle.
## **Dónde Aplicar una Licencia en su Aplicación**
Dónde aplicar una licencia depende del tipo de aplicación que esté desarrollando. Siga estas reglas simples:

- Aplique la licencia solo una vez por dominio de aplicación. Llamar a License.SetLicense varias veces no es perjudicial pero desperdicia tiempo de procesador.
- Aplique la licencia antes de llamar a cualquier clase de Aspose.PSD para .NET.
- **Aplicaciones de Windows Forms o de consola**: llame a License.SetLicense en el código de inicio, antes de usar cualquier clase de Aspose.PSD para .NET.
- **Aplicaciones ASP.NET**: llama a License.SetLicense desde el archivo Global.asax.cs (Global.asax.vb), en el método protegido Application_Start. De esta manera, se llama una vez cuando la aplicación se inicia. No llame a License.SetLicense desde los métodos Page_Load o la licencia se cargará cada vez que se cargue una página web.
- **Aplicaciones Silverlight**: llame a License.SetLicense desde el evento Application_Startup en el archivo App.xaml.cs (App.xaml.vb).
- **Biblioteca de clases**: llame a License.SetLicense desde un constructor estático de la clase que utiliza Aspose.PSD. El constructor estático se ejecuta antes de que se cree una instancia de su clase, asegurando que la licencia de Aspose.PSD esté correctamente configurada.
## **Aplicando una Licencia**
Puede descargar fácilmente una versión de evaluación de Aspose.PSD desde la página de descargas de NuGet [download page](https://www.nuget.org/packages/Aspose.psd/). La versión de evaluación proporciona absolutamente las mismas capacidades que la versión con licencia de Aspose.PSD. Además, la versión de evaluación simplemente se convierte en licenciada cuando compra una licencia y agrega un par de líneas de código para aplicar la licencia.
### **Usando un Archivo o un Flujo**
Si desea evitar trabajar con las limitaciones de la evaluación, necesita establecer una licencia antes de usar Aspose.PSD. Solo necesita establecer una licencia una vez por aplicación (o proceso).
### **Aplicando una licencia desde un archivo**
La forma más fácil de aplicar una licencia es poner el archivo de licencia en la misma carpeta que el Aspose.PSD.dll. Luego puede especificar el nombre del archivo en el código en lugar de una ruta completa.



{{< highlight java >}}

 // Instancie una instancia de licencia y aplique la licencia usando una ruta completa

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense("Aspose.PSD.lic");



{{< /highlight >}}



Cuando llame al método SetLicense, el nombre de la licencia debe ser el mismo que el nombre de su archivo de licencia. Por ejemplo, si cambia el nombre del archivo de licencia a "Aspose.PSD.lic.xml", debe usar este nombre de licencia para el método SetLicense.
### **Aplicando una licencia usando un flujo**
También es posible cargar una licencia desde un flujo como se muestra a continuación.



{{< highlight java >}}



// Instancie una instancia de licencia y aplique la licencia usando un flujo

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense(myStream);



{{< /highlight >}}
### **Comprobando el estado de la licencia**
La clase Aspose.PSD.License tiene la propiedad IsLicensed que devolverá true si la licencia se ha configurado correctamente.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("¡Licencia configurada!");

}

{{< /highlight >}}
### **Usando un Recurso Integrado**
Una forma práctica de empaquetar la licencia con su aplicación y asegurarse de que no se pierda, es incluirla como un recurso integrado en una de las bibliotecas que llama a Aspose.PSD. Para incluir el archivo de licencia como un recurso integrado:

1. En Visual Studio .NET, haga clic en el menú **Archivo** y seleccione **Agregar elemento existente**.
1. Incluya el archivo de licencia (extensión .lic) en el proyecto.
1. Seleccione el archivo en el Explorador de soluciones.
1. En la ventana de propiedades, establezca **Acción de compilación** en **Recurso integrado**.

No es necesario llamar a los métodos GetExecutingAssembly o GetManifestResourceStream de System.Reflection.Assembly en el Marco de Trabajo de .NET de Microsoft para acceder a una licencia integrada. En su lugar, incluya el archivo como un recurso en el proyecto y luego pase el nombre del archivo de licencia al método SetLicense. La clase License encuentra automáticamente el archivo de licencia en los recursos integrados. El siguiente ejemplo muestra cómo incluir la licencia como un recurso integrado y aplicarla a su aplicación.



{{< highlight java >}}

 // Instancie la clase License

Aspose.PSD.License license = new Aspose.PSD.License();



// Pase el nombre del archivo de licencia integrado

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}


### **Comprobando el estado de la licencia**
La clase Aspose.PSD.License tiene la propiedad IsLicensed que devolverá true si la licencia se ha configurado correctamente.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("¡Licencia configurada!");

}

{{< /highlight >}}
