---
title: Notas de lanzamiento de Aspose.PSD CLI NLP Editor para .NET 24.6
type: docs
weight: 90
url: /es/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

Esta página contiene las notas de lanzamiento para [Aspose.PSD CLI NLP Editor para .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Clave**   | **Resumen**                                                                                 | **Categoría** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Lanzamiento inicial de las aplicaciones Aspose.PSD CLI: Aspose.PSD.CLI.Export y Aspose.PSD.CLI.NLP.Editor |  Mejora |


## **Ejemplos de uso:**

**PSDNET-2110. Lanzamiento inicial de la aplicación Aspose.PSD CLI NLP Editor**


## **Uso desde la línea de comandos:**

{{% alert color="primary" %}}
Primero instale esta herramienta dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Recomendamos que antes del primer uso ejecute el siguiente comando:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Después de este comando, podrá ejecutar esta aplicación con el nombre corto nlp.cli en lugar de Aspose.PSD.CLI.NLP.Editor. Puede especificar su propio nombre corto.
{{% /alert %}}

**Ejemplos de uso**

1. Este comando convertirá el primer archivo encontrado (que pueda ser abierto con aspose.psd) de la carpeta actual y lo guardará en formato png con transparencia. Además, se configurará la licencia. Solo es necesario especificarla una vez. En las ejecuciones siguientes, se utilizará la licencia del path especificado. Este comando mostrará el registro detallado del procesamiento NLP si está disponible. 
{{< highlight bash >}}nlp.cli Convertir archivo de esta carpeta a formato png con alfa --licencia "C:\Aspose\ArchivoDeLicencia.lic --detallado "{{< /highlight >}}

2. Este comando buscará el archivo con el nombre más similar a "smth.psd". Luego ajustará el contraste y lo guardará en jpeg con la mejor calidad. Se imprimirá el nombre del archivo de salida. Será smth.jpg
{{< highlight bash >}}Ajustar contraste en 10 de la capa con el nombre de elipse en el archivo smth.psd y guardarlo como output.jpg con la mejor calidad{{< /highlight >}}

3. Este comando girará el archivo en la ruta especificada y reducirá su tamaño al 25%. Se imprimirá el archivo de salida. Se guardará en la carpeta actual de la consola.
{{< highlight bash >}}Redimensionar archivo C:\Usuarios\algúnusuario\Escritorio\entrada.psd al 25%{{< /highlight >}}

4. Este comando buscará el archivo entrada.psd en  C:\Usuarios\algúnusuario\Escritorio\. Luego buscará la capa con índice 3 y la redimensionará a un ancho de 50px y un alto de 100px. Luego esta capa se guardará como PDF en C:\Usuarios\algúnusuario\Escritorio\salida.pdf
{{< highlight bash >}}Redimensionar capa con índice 3 de C:\Usuarios\algúnusuario\Escritorio\entrada.psd a un ancho de 50 y un alto de 100 y guardarlo en C:\Usuarios\algúnusuario\Escritorio\salida.pdf{{< /highlight >}}

 5. Este comando abrirá smth.psd en la carpeta actual, pero todos los efectos estarán desactivados. Luego este archivo se convertirá al formato BMP y se guardará como output.bmp en la carpeta actual.
 {{< highlight bash >}}Abrir smth.psd sin efectos y guardarlo como output.bmp{{< /highlight >}}

**Descargo de responsabilidad**

Esta es una aplicación experimental. Por favor, pruébela y deje comentarios. Cualquier comentario es muy apreciado. Nuestro objetivo es llevar la aplicación sin código al siguiente nivel. La integración sencilla en cualquier canal de construcción o proceso comercial es nuestra meta.
