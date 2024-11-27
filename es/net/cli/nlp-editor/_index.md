---
title: Aplicación de edición de Aspose.PSD CLI NLP para .NET
type: docs
weight: 10
url: /es/net/cli/nlp-editor/
is_root: false
keywords: CLI Herramienta de Photoshop NLP Procesamiento de lenguaje natural Archivo PSD Consola Biblioteca C# API PSD
description: Aplicación Aspose.PSD basada en CLI NLP para la edición de archivos PSD, PSB y AI. Automatización CI/CD sin código. Admite el procesamiento de lenguaje natural para la edición de archivos PSD. Simplemente escriba su solicitud en lenguaje natural para realizar varias operaciones como conversión, ajuste, cambio de tamaño y más. No requiere la instalación de Adobe Photoshop o Adobe Illustrator y se puede ejecutar desde la consola sin código adicional.
---

**![Logo del producto Aspose.PSD para .NET](home_1.png)**

**Bienvenido a la aplicación de edición de Aspose.PSD NLP CLI para .NET**

La aplicación de edición de Aspose.PSD CLI NLP es una utilidad de consola ligera para editar archivos PSD utilizando comandos de lenguaje natural. Fácil integración en canalizaciones CI/CD.

**Descargo de responsabilidad**

Esta es una aplicación experimental. Por favor, pruébela y deje sus comentarios. Cualquier comentario es muy apreciado. Queremos llevar la aplicación sin código al siguiente nivel. Nuestra meta es lograr una integración fácil en cualquier canalización de compilación o proceso empresarial.

**Funcionalidades principales de la aplicación de edición de Aspose.PSD NLP CLI para .NET**

1. Realizar operaciones en archivos PSD, PSB, AI utilizando comandos de lenguaje natural.
2. Admite diversas operaciones como conversión, ajuste, cambio de tamaño y más.
3. Automatización CI/CD sin código.
4. Admite escribir solicitudes en lenguaje natural para la edición de archivos PSD.

## **Uso desde la línea de comandos:**

{{% alert color="primary" %}}
Primero instale esta herramienta dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Recomendamos antes del primer uso ejecutar el siguiente comando:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Después de este comando, podrá ejecutar esta aplicación con el nombre corto nlp.cli en lugar de Aspose.PSD.CLI.NLP.Editor. Puede especificar su propio nombre corto.
{{% /alert %}}

**Parámetros disponibles para la aplicación Aspose.PSD.CLI.Crop**

| **Argumento** | **Descripción**                         |
|:-------------|:----------------------------------------|
| cualquier texto    | Requerido. Su comando en lenguaje natural para actualizar un archivo PSD o PSB      |
| licencia      | Ruta de la licencia.                    |
| detallado      | Muestra más información sobre un comando específico. |
| configuración        | Crea un archivo bat en la carpeta de herramientas para una llamada rápida desde la consola. Ejemplo: --setup psd.nlp. Luego puede llamar a la herramienta con el comando psd.nlp |

**Ejemplos de uso**

1. Este comando convertirá el primer archivo encontrado (que se puede abrir con Aspose.PSD) de la carpeta actual y lo guardará en formato png con transparencia. Además, se configurará la licencia. Solo necesita especificar la licencia una vez. En las ejecuciones posteriores, la licencia se usará desde la ruta especificada. Este comando mostrará el registro detallado del procesamiento NLP si está disponible.
{{< highlight bash >}}
  nlp.cli Convertir archivo de esta carpeta a formato png con alfa --licencia "C:\Aspose\ArchivoDeLicencia.lic --detallado "
{{< /highlight >}}

2. Este comando encontrará el archivo con el nombre más similar a "smth.psd". Luego ajustará el contraste y lo guardará en jpeg con la mejor calidad. Se imprimirá el nombre del archivo de salida. Será smth.jpg
{{< highlight bash >}}
Ajustar contraste en 10 de la capa con nombre elipse en el archivo smth.psd y guardarlo como output.jpg con la mejor calidad
{{< /highlight >}}

3. Este comando girará el archivo en la ruta especificada y reducirá su tamaño al 25%. Se imprimirá el archivo de salida. Se guardará en la carpeta actual de la consola.
{{< highlight bash >}}
Cambio de tamaño del archivo C:\Usuarios\algunusuario\Escritorio\entrada.psd al 25%
{{< /highlight >}}

4. Este comando encontrará el archivo input.psd en  C:\Usuarios\algunusuario\Escritorio\. Luego encontrará la capa con índice 3 y la cambiará de tamaño a un ancho de 50px y una altura de 100px. Luego esta capa se guardará como PDF en C:\Usuarios\algunusuario\Escritorio\salida.pdf
{{< highlight bash >}}
 Cambiar tamaño de la capa con índice 3 de C:\Usuarios\algunusuario\Escritorio\entrada.psd a un ancho de 50 y una altura de 100 y guardarlo en C:\Usuarios\algunusuario\Escritorio\salida.pdf
 {{< /highlight >}}

 5. Este comando abrirá smth.psd en la carpeta actual, pero todos los efectos estarán desactivados. Luego este archivo se convertirá a formato BMP y se guardará como output.bmp en la carpeta actual.
 {{< highlight bash >}}
 Abrir smth.psd sin efectos y guardarlo como output.bmp
  {{< /highlight >}}

**Por favor, consulte otras [Aplicaciones CLI de Aspose.PSD](https://docs.aspose.com/psd/net/cli) para .NET si necesita agregar soporte para los formatos PSD, PSB y AI a su flujo de trabajo**

1. [Aspose.PSD CLI Convertir](/psd/es/net/cli/convert)
2. [Aspose.PSD CLI Recortar](/psd/es/net/cli/crop)
3. [Aspose.PSD CLI Cambiar tamaño](/psd/es/net/cli/resize)
4. [Aspose.PSD CLI Exportar](/psd/es/net/cli/export)
5. [Aspose.PSD CLI Editor NLP](/psd/es/net/cli/nlp-editor)

**Por favor, consulte Aspose.PSD para .NET u [otras plataformas]**

Las Aplicaciones CLI de Aspose.PSD son una solución lista para usar para operaciones populares. Si necesita una solución flexible, consulte la versión completa de Aspose.PSD

1. [Aspose.PSD para .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD para Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD para Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Recursos de Aspose.PSD para .NET**

A continuación se presentan los enlaces a algunos recursos útiles que pueda necesitar para completar sus tareas.

- [Documentación en línea de las Aplicaciones CLI de Aspose.PSD para .NET](/psd/es/net/cli/conversion)
- [Notas de la versión de las Aplicaciones CLI de Aspose.PSD para .NET](/psd/es/net/cli/conversion/release-notes/)
- [Página del producto de las Aplicaciones CLI de Aspose.PSD para .NET](https://products.aspose.com/psd/net/cli)
- [Guía de referencia de la API de Aspose.PSD para .NET](https://reference.aspose.com/net/psd)
- [Descargar ejemplos en el repositorio de GitHub](https://github.com/aspose-psd/CLI-Applications)
- [Foro de soporte gratuito de Aspose.PSD para .NET](https://forum.aspose.com/c/psd)
- [Centro de ayuda de soporte pagado de Aspose.PSD para .NET](https://helpdesk.aspose.com/)

