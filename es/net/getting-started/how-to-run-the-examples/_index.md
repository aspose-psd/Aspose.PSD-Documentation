---
title: Cómo Ejecutar los Ejemplos
type: docs
weight: 90
url: /es/net/como-ejecutar-los-ejemplos/
description: Aprenda cómo ejecutar los ejemplos relacionados con la biblioteca de formato de archivo PSD que se encuentran alojados en GitHub.
---

## **Requisitos del Software**
Asegúrese de cumplir con los siguientes requisitos antes de descargar y ejecutar los ejemplos.

1. Visual Studio 2010 o superior
1. Administrador de paquetes NuGet instalado en Visual Studio. Asegúrese de que la última versión de la API de NuGet esté instalada en Visual Studio. Para obtener detalles sobre cómo instalar el administrador de paquetes NuGet, por favor consulte [http://docs.nuget.org/ndocs/guides/install-nuget](http://docs.nuget.org/ndocs/guides/install-nuget)
1. Vaya a Herramientas->Opciones->Administrador de paquetes NuGet->Fuentes de paquete y asegúrese de que la opción **nuget.org** esté marcada
1. El proyecto de ejemplo utiliza la función de Restauración Automática de Paquetes NuGet, por lo tanto, debe tener una conexión a internet activa. Si no tiene una conexión a internet activa en la máquina donde se ejecutarán los ejemplos, por favor consulte [Instalación](/psd/es/net/installation/) para agregar referencia a Aspose.Imaging.dll en el proyecto de ejemplo.
## **Descargar desde GitHub**
Todos los ejemplos de Aspose.PSD para .NET se encuentran alojados en [GitHub](https://github.com/aspose-psd/Aspose.PSD-for-.NET).

- Puede clonar el repositorio usando su cliente GitHub favorito o descargar el archivo ZIP desde [aquí](https://github.com/aspose-psd/Aspose.PSD-for-.NET/archive/master.zip).
- Extraiga el contenido del archivo ZIP en cualquier carpeta de su computadora. Todos los ejemplos están ubicados en la carpeta **Ejemplos**.
- Hay un archivo de solución de Visual Studio para C#.
- Los proyectos están creados en Visual Studio 2013, pero los archivos de solución son compatibles con Visual Studio 2010 SP1 o superior.
- Abra el archivo de solución en Visual Studio y compile el proyecto.
- En la primera ejecución, las dependencias se descargarán automáticamente a través de NuGet.
- La carpeta **Data** en la carpeta raíz de **Ejemplos** contiene archivos de entrada que los ejemplos de C# utilizan. Es obligatorio que descargue la carpeta **Data** junto con el proyecto de ejemplos.
- Abra el archivo RunExamples.cs, todos los ejemplos se llaman desde aquí.
- Descomente los ejemplos que desee ejecutar desde dentro del proyecto.

No dude en comunicarse con nosotros a través de nuestros foros si tiene algún problema configurando o ejecutando los ejemplos.
## **Contribuir**
Si desea agregar o mejorar un ejemplo, lo alentamos a contribuir al proyecto. Todos los ejemplos y proyectos en esta repositorio son de código abierto y pueden ser utilizados libremente en sus propias aplicaciones.

Para contribuir, puede bifurcar el repositorio, editar el código fuente y crear una solicitud de extracción. Revisaremos los cambios e incluiremos en el repositorio si se consideran útiles.
