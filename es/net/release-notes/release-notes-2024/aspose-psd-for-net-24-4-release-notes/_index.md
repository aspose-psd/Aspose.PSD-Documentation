---
title: Notas de la versión de Aspose.PSD para .NET 24.4
type: docs
weight: 90
url: /es/net/aspose-psd-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión para [Aspose.PSD para .NET 24.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clave**    | **Resumen**                                            | **Categoría** |
|:------------|:-------------------------------------------------------|:-------------|
| PSDNET-1871 | [AI Formato] Agregar manejo de recurso XObjectForm     | Característica      |
| PSDNET-1961 | Agregar Constructor para ShapeLayer                    | Característica      |
| PSDNET-1879 | Corregir la conversión de archivo Psd de RGB a CMYK    | Error          |
| PSDNET-1966 | Un archivo PSD específico no se puede exportar usando Aspose.PSD | Error          |

## **Cambios en la API pública**
# **APIs añadidas:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**

**PSDNET-1871. [AI Formato] Agregar manejo de recurso XObjectForm**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "ejemplo.ai");
string rutaArchivoSalida = Path.Combine(outputFolder, "ejemplo.png");

using (AiImage imagen = (AiImage)Image.Load(archivoFuente))
{
    imagen.Save(rutaArchivoSalida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1879. Corregir conversión de archivo Psd de RGB a CMYK**

{{< highlight csharp >}}
// Verificar que el archivo psd convertido a CMYK + RLE 4 canales desde el archivo psd en RGB + RLE 4 canales, realmente tiene 4 canales
// y HasTransparencyData == false.

string archivoFuente = Path.Combine(baseFolder, "rana_nosimb.psd");
string archivoSalida = Path.Combine(outputFolder, "rana_nosimb_salida.psd");

using (PsdImage imagenPsd = (PsdImage)Image.Load(archivoFuente))
{
    imagenPsd.HasTransparencyData = false;

    PsdOptions opcionesPsd = new PsdOptions(imagenPsd)
    {
        ColorMode = ColorModes.Cmyk,
        CompressionMethod = CompressionMethod.RLE,
        ChannelsCount = 4,
    };

    imagenPsd.Save(archivoSalida, opcionesPsd);
}

using (PsdImage imagenPsd = (PsdImage)Image.Load(archivoSalida))
{
    AssertAreEqual(false, imagenPsd.HasTransparencyData);
    AssertAreEqual((ushort)4, imagenPsd.Layers[0].ChannelsCount);
}

void AssertAreEqual(object esperado, object actual, string mensaje = null)
{
    if (!object.Equals(esperado, actual))
    {
        throw new Exception(mensaje ?? "Los objetos no son iguales.");
    }
}
{{< /highlight >}}

**PSDNET-1961. Agregar Constructor para ShapeLayer**

{{< highlight csharp >}}
string archivoSalida = Path.Combine(outputFolder, "AgregarShapeLayer_salida.psd");

const int RelacionImgAPsd = 256 * 65535;

using (PsdImage nuevoPsd = new PsdImage(600, 400))
{
    ShapeLayer capa = nuevoPsd.AddShapeLayer();

    var nuevaForma = GenerarNuevaForma(nuevoPsd.Size);
    List<IPathShape> nuevasFormas = new List<IPathShape>();
    nuevasFormas.Add(nuevaForma);
    capa.Path.SetItems(nuevasFormas.ToArray());

    capa.Update();

    nuevoPsd.Save(archivoSalida);
}

using (PsdImage imagen = (PsdImage)Image.Load(archivoSalida))
{
    AssertAreEqual(2, imagen.Layers.Length);

    ShapeLayer capaForma = imagen.Layers[1] as ShapeLayer;
    ColorFillSettings rellenoInterno = capaForma.Fill as ColorFillSettings;
    IStrokeSettings configuraciónTrazo = capaForma.Stroke;
    ColorFillSettings rellenoTrazo = capaForma.Stroke.Fill as ColorFillSettings;

    AssertAreEqual(1, capaForma.Path.GetItems().Length); // 1 forma
    AssertAreEqual(3, capaForma.Path.GetItems()[0].GetItems().Length); // 3 puntos en una forma

    AssertAreEqual(-16127182, rellenoInterno.Color.ToArgb()); // ff09eb32

    AssertAreEqual(7.41, configuraciónTrazo.Size);
    AssertAreEqual(false, configuraciónTrazo.Enabled);
    AssertAreEqual(StrokePosition.Center, configuraciónTrazo.LineAlignment);
    AssertAreEqual(LineCapType.ButtCap, configuraciónTrazo.LineCap);
    AssertAreEqual(LineJoinType.MiterJoin, configuraciónTrazo.LineJoin);
    AssertAreEqual(-16777216, rellenoTrazo.Color.ToArgb()); // ff000000
}

PathShape GenerarNuevaForma(Size tamañoImagen)
{
    var nuevaForma = new PathShape();

    PointF punto1 = new PointF(20, 100);
    PointF punto2 = new PointF(200, 100);
    PointF punto3 = new PointF(300, 10);

    BezierKnotRecord[] puntosBezier = new BezierKnotRecord[]
    {
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFAPuntoRecurso(punto1, tamañoImagen),
                          PointFAPuntoRecurso(punto1, tamañoImagen),
                          PointFAPuntoRecurso(punto1, tamañoImagen),
                      }
         },
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFAPuntoRecurso(punto2, tamañoImagen),
                          PointFAPuntoRecurso(punto2, tamañoImagen),
                          PointFAPuntoRecurso(punto2, tamañoImagen),
                      }
         },
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFAPuntoRecurso(punto3, tamañoImagen),
                          PointFAPuntoRecurso(punto3, tamañoImagen),
                          PointFAPuntoRecurso(punto3, tamañoImagen),
                      }
         },
    };

    nuevaForma.SetItems(puntosBezier);

    return nuevaForma;
}

Point PointFAPuntoRecurso(PointF punto, Size tamañoImagen)
{
    return new Point(
        (int)Math.Round(punto.Y * (RelacionImgAPsd / tamañoImagen.Height)),
        (int)Math.Round(punto.X * (RelacionImgAPsd / tamañoImagen.Width)));
}

void AssertAreEqual(object esperado, object actual, string mensaje = null)
{
    if (!object.Equals(esperado, actual))
    {
        throw new Exception(mensaje ?? "Los objetos no son iguales.");
    }
}
{{< /highlight >}}

**PSDNET-1966. Un archivo PSD específico no se puede exportar usando Aspose.PSD**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "fuente1966.psd");
string salidaPng = Path.Combine(outputFolder, "salida.png");

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    imagenPsd.Save(salidaPng, new PngOptions());
}
{{< /highlight >}}
