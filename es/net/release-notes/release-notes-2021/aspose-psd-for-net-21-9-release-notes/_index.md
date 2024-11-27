---
title: Notas de la versión de Aspose.PSD para .NET 21.9
type: docs
weight: 40
url: /es/net/aspose-psd-for-net-21-9-release-notes/
---

{{% alert color="primary" %}} 

Esta página contiene notas de la versión para [Aspose.PSD para .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-574|Hacer la Compresión RLE Predeterminada para Guardar PSD y evitar una producción enorme de PSD|Característica|
|PSDNET-747|Soportar los Efectos de Capa de Patrón de Superposición con el modo de color multicanal en el archivo PSD|Característica|
|PSDNET-951|Después de la creación de una nueva capa, su propiedad Recursos es nula lo que impide manipulaciones (Redimensionamiento, por ejemplo)|Error|
|PSDNET-955|No soportado de los métodos de Compresión ZipWithPrediction para 8 bits|Error|

## **Cambios públicos en la API**
# **APIs agregadas:**
- Ninguna

# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**

**PSDNET-574. Hacer la Compresión RLE Predeterminada para Guardar PSD y evitar una producción enorme de PSD**

{{< highlight csharp >}}
            string rutaArchivoEntrada = "file.psd";
            string salida1 = "output_original.psd";
            string salida2 = "output_psdOptions.psd";

            using (Image imagen = Image.Load(rutaArchivoEntrada))
            {
                imagen.Save(salida1);
                imagen.Save(salida2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. Soportar los Efectos de Capa de Patrón de Superposición con el modo de color multicanal en el archivo PSD**

{{< highlight csharp >}}
            var nombreArchivo = "AllEffects.psd";
            var archivoSalida = "AllEffects_out.psd";
            var opcionesCarga = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // No debería lanzar excepción
            using (var im = Image.Load(nombreArchivo, opcionesCarga))
            {
                // No debería lanzar excepción
                im.Save(archivoSalida);
            }
{{< /highlight >}}

**PSDNET-951. Después de la creación de una nueva capa, su propiedad Recursos es nula lo que impide manipulaciones (Redimensionamiento, por ejemplo)**

{{< highlight csharp >}}
            string ArchivoPSD = "Layer1.psd";
            string ArchivoCapa1 = "Layer2.png";
            string ArchivoCapa2 = "Layer3.png";
            string nombreArchivoSalida = "finaloutput.psd";

            void ReemplazarColor(RasterImage imagen, Color colorAntiguo, int dif, Color colorNuevo)
            {
                var pixeles = imagen.LoadArgb32Pixels(imagen.Bounds);
                var longitud = pixeles.Length;

                var rojoAntiguo = colorAntiguo.R;
                var verdeAntiguo = colorAntiguo.G;
                var azulAntiguo = colorAntiguo.B;
                var valorColorNuevo = colorNuevo.ToArgb();

                for (int i = 0; i < longitud; i++)
                {
                    // Rojo
                    var r = (byte)((pixeles[i] >> 16) & 0xff);
                    // Verde
                    var g = (byte)((pixeles[i] >> 8) & 0xff);
                    // Azul
                    var b = (byte)(pixeles[i] & 0xff);

                    int difActual = Math.Abs(r - rojoAntiguo) + Math.Abs(g - verdeAntiguo) + Math.Abs(b - azulAntiguo);

                    if (difActual <= dif)
                    {
                        pixeles[i] = valorColorNuevo;
                    }
                }

                imagen.SaveArgb32Pixels(imagen.Bounds, pixeles);
            }

            Layer Capa2 = null;
            Layer Capa3 = null;
            using (PsdImage imagen = (PsdImage)Image.Load(ArchivoPSD))
            {
                #region Añadiendo Capa 1

                using (var flujo = new FileStream(ArchivoCapa1, FileMode.Open))
                {
                    Capa2 = new Layer(flujo);

                    Capa2.Resize(imagen.Width, imagen.Height);
                    var ancho = Capa2.Width;
                    var altura = Capa2.Height;

                    Capa2.Left = 675;
                    Capa2.Top = 0;

                    Capa2.Right = Capa2.Left + ancho;
                    Capa2.Bottom = Capa2.Top + altura;

                    imagen.AddLayer(Capa2);
                }

                #endregion

                using (var flujo = new FileStream(ArchivoCapa2, FileMode.Open))
                {
                    Capa3 = new Layer(flujo);
                    // Reemplazar el color blanco por Transparente
                    ReemplazarColor(Capa3, Color.White, 256, Color.Transparent);
                    Capa2.DrawImage(new Point(0, 0), Capa3);
                }

                imagen.Save(nombreArchivoSalida, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. No soportado de los métodos de Compresión ZipWithPrediction para 8 bits**

{{< highlight csharp >}}
            string rutaArchivoEntrada = "zipTest698.psd";
            string salidaZip8 = "out_Zip8bit.psd";
            string salidaZip16 = "out_Zip16bit.psd";

            using (PsdImage imagen = (PsdImage)Image.Load(rutaArchivoEntrada))
            {
                imagen.Save(salidaZip8, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 8 });
                imagen.Save(salidaZip16, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 16 });
            }
{{< /highlight >}}
