---
title: Notas de la versión de Aspose.PSD para .NET 22.7
type: docs
weight: 60
url: /es/net/aspose-psd-for-net-22-7-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 22.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-482|Soporte del recurso de sección de imagen #4000-4999 recurso(s) de complemento|Característica|
|PSDNET-875|Se produce una excepción no controlada del tipo "System.OutOfMemoryException" en Aspose.PSD.dll|Error|
|PSDNET-1050|Después de exportar el archivo PSD, el resultado es mucho más grande que el archivo fuente|Error|
|PSDNET-1083|Análisis incorrecto de datos para XmpResource|Error|
|PSDNET-1205|Después de exportar, el tamaño de los archivos PSD con subcarpetas ha aumentado|Error|


## **Cambios en la API pública**
# **APIs añadidas:**

- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Items
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.SaveData(Aspose.PSD.StreamContainer)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.KeyName
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.AnimatedDataSection
- M:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.SaveData(Aspose.PSD.StreamContainer)


# **APIs eliminadas:**

- Ninguna


## **Ejemplos de uso:**

**PSDNET-482. Soporte del recurso de sección de imagen #4000-4999 recurso(s) de complemento**

{{< highlight csharp >}}
// El siguiente código demuestra cómo establecer/actualizar el tiempo de retardo en el fotograma de la línea de tiempo de datos animados.
string archivoFuente = "3_animated.psd";
string psdSalida = "salida_3_animated.psd";

T EncontrarEstructura<T>(IEnumerable<EstructuraTipoOS> estructuras, string nombreClave) where T : EstructuraTipoOS
{
    foreach (var estructura in estructuras)
    {
        if (estructura.NombreClave.NombreClase == nombreClave)
        {
            return estructura como T;
        }
    }

    return null;
}

EstructuraTipoOS[] AgregarOReemplazarEstructura(IEnumerable<EstructuraTipoOS> estructuras, EstructuraTipoOS nuevaEstructura)
{
    List<EstructuraTipoOS> listaDeEstructuras = new List<EstructuraTipoOS>(estructuras);

    for (int i = 0; i < listaDeEstructuras.Count; i++)
    {
        EstructuraTipoOS estructura = listaDeEstructuras[i];
        if (estructura.NombreClave.NombreClase == nuevaEstructura.NombreClave.NombreClase)
        {
            listaDeEstructuras.RemoveAt(i);
            break;
        }
    }

    listaDeEstructuras.Add(nuevaEstructura);

    return listaDeEstructuras.ToArray();
}

using (ImagenPsd imagen = (ImagenPsd)Image.Load(archivoFuente))
{
    foreach (var recursoImagen in imagen.RecursosImagen)
    {
        if (recursoImagen is RecursoSeccionDatosAnimados)
        {
            var datosAnimados =
            (EstructuraSeccionDatosAnimados) (recursoImagen as RecursoSeccionDatosAnimados).SeccionDatosAnimados;
            var listaFrames = EncontrarEstructura<ListaEstructura>(datosAnimados.Items, "FrIn");

            var frame1 = (EstructuraDescriptor)listaFrames.Tipos[1];

            // Crea el registro de retardo del fotograma con un valor de 100 centésimas de segundo que es igual a 1 segundo.
            var retardoFrame = new EstructuraEntero(new ClaseID("FrDl"));
            retardoFrame.Valor = 100; // establecer el tiempo en centésimas de segundo.

            frame1.Estructuras = AgregarOReemplazarEstructura(frame1.Estructuras, retardoFrame);

            break;
        }
    }

    imagen.Save(psdSalida);
}
{{< /highlight >}}

**PSDNET-875. Se produce una excepción no controlada del tipo "System.OutOfMemoryException" en Aspose.PSD.dll**

{{< highlight csharp >}}
string archivoFuente = "001-.psd";
string rutaJpg = "T_0003.jpg";
string rutaArchivoSalida = "nuevoPsd.psd";

using (var im = (ImagenPsd)Image.Load(archivoFuente))
{
    using (FileStream fs = new FileStream(rutaJpg, FileMode.Open))
    {
        var nuevaCapa = new Aspose.PSD.FileFormats.Psd.Layers.Capal(fs);
        nuevaCapa.NombreVisual = "NuevaCapa";

        im.AgregarCapa(nuevaCapa);

        im.Save(rutaArchivoSalida, true);   
    }
}
{{< /highlight >}}

**PSDNET-1050. Después de exportar el archivo PSD, el resultado es mucho más grande que el archivo fuente**

{{< highlight csharp >}}
string fuente = "ShimadzuLetterhead100.psd";
string salida = "salida.psd";
using (var img = (ImagenPsd)Image.Load(fuente))
{
    img.Save(salida);
}

double tamañoSalidaMb = new FileInfo(salida).Length / 1024d / 1024d;
if (tamañoSalidaMb > 6)
{
    throw new Exception("El archivo de salida es más grande de lo que debería ser.");
}
{{< /highlight >}}

**PSDNET-1083. Análisis incorrecto de datos para XmpResource**

{{< highlight csharp >}}
string rutaImagenPsdEntrada = @"entrada.psd";
string rutaImagenPsdGuardada = @"guardado.psd";

bool esOriginalContiene = false;
bool esGuardadoContiene = false;

// Encuentra la subclave XMP en el archivo de entrada
using (ImagenPsd img = (ImagenPsd)Image.Load(rutaImagenPsdEntrada))
{
    foreach (var paquete in img.DatosXmp.Paquetes)
    {
        foreach (var paq in paquete)
        {
            if (paq.Valor is MatrizXmp)
            {
                MatrizXmp matrizXmp = (MatrizXmp)paq.Valor;

                string valorXml = matrizXmp.ObtenerValorXml();

                if (valorXml.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    esOriginalContiene = true;
                    break;
                }
            }
        }

        if (esOriginalContiene)
        {
            break;
        }
    }
    img.Save(rutaImagenPsdGuardada);
}

// Encuentra la subclave XMP en el archivo guardado
using (ImagenPsd img = (ImagenPsd)Image.Load(rutaImagenPsdGuardada))
{
    foreach (var paquete in img.DatosXmp.Paquetes)
    {
        foreach (var paq in paquete)
        {
            if (paq.Valor is MatrizXmp)
            {
                MatrizXmp matrizXmp = (MatrizXmp)paq.Valor;

                string valorXml = matrizXmp.ObtenerValorXml();

                if (valorXml.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    esGuardadoContiene = true;
                    break;
                }
            }
        }

        if (esGuardadoContiene)
        {
            break;
        }
    }
    img.Save(rutaImagenPsdGuardada);
}

if (esOriginalContiene && esGuardadoContiene)
{
    // ¡Todo está bien!
}
else
{
    throw new Exception("No funciona");
}
{{< /highlight >}}

**PSDNET-1205. Después de exportar, el tamaño de los archivos PSD con subcarpetas ha aumentado**

{{< highlight csharp >}}
string[] archivosFuente = new string[] { "1lvlFoldersTest.psd", "5lvlFoldersTest.psd"};

foreach (var nombreArchivo in archivosFuente)
{
    string rutaArchivoFuente = nombreArchivo;
    string rutaArchivoSalida = "salida_" + nombreArchivo;

    using (ImagenPsd imagen = (ImagenPsd)Image.Load(rutaArchivoFuente))
    {
        imagen.Save(rutaArchivoSalida);
    }

    double tamañoSalidaMb = new FileInfo(rutaArchivoSalida).Length / 1024d / 1024d;
    if (tamañoSalidaMb > 1.9)
    {
        throw new Exception("El archivo de salida es más grande de lo que debería ser.");
    }
}
{{< /highlight >}}
