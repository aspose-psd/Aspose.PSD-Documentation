---
title: Notas de la versión de Aspose.PSD para .NET 22.10
type: docs
weight: 30
url: /es/net/aspose-psd-para-net-22-10-notas-de-version/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión de [Aspose.PSD para .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Esta versión tiene una regresión en el caso de las exportaciones de 16 bits, por lo que recomendamos precaución al utilizar esta función en esta versión.
Por favor, no actualice Aspose.PSD a 22.9-22.10 si el procesamiento de imágenes de 16 bits es su funcionalidad principal.

Estamos trabajando en soluciones para estos problemas.

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-1287|Eliminar propiedades obsoletas en Lfx2Resource|Mejora|
|PSDNET-1071|Aspose.PSD no puede abrir PSD (RGB/16 bits) con compresión ZipWithoutPrediction|Error|
|PSDNET-1257|Los efectos de la línea de tiempo desaparecen y se muestran de manera extraña. (en Photoshop)|Error|
|PSDNET-1278|La transparencia no funciona para el efecto Stroke con la posición Interior|Error|
|PSDNET-1279|Regresión: Error en la apertura del archivo PSD|Error|
|PSDNET-1284|La actualización de texto falla con algunos símbolos asiáticos. Error al analizar un símbolo específico|Error|
|PSDNET-1291|La actualización de texto falla con algunos símbolos asiáticos. Error al renderizar un símbolo específico|Error|
|PSDNET-1292|Error al abrir el archivo exportado por Photoshop después de guardar símbolos asiáticos específicos|Error|


## **Cambios en la API pública**
# **APIs añadidas:**
- Ninguna


# **APIs eliminadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Ejemplos de uso:**

**PSDNET-1071. Aspose.PSD no puede abrir PSD (RGB/16 bits) con compresión ZipWithoutPrediction**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Los efectos de la línea de tiempo desaparecen y se muestran de manera extraña. (en Photoshop)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Crear línea de tiempo con algunos cuadros.
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    List<Frame> frames = new List<Frame>(timeLine.Frames);
    for (int i = 0; i < 3; i++)
    {
        frames.Add(new Frame(timeLine));
    }
    timeLine.Frames = frames.ToArray();

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddColorOverlay();

    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.AddGradientOverlay();
    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1278. La transparencia no funciona para el efecto Stroke con la posición Interior**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Regresión: Error en la apertura del archivo PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. La actualización de texto falla con algunos símbolos asiáticos. Error al analizar un símbolo específico**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // seleccionar el símbolo problemático

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Eliminar propiedades obsoletas en Lfx2Resource**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // Actualizar opción BlendMode del efecto
    effect.BlendMode = BlendMode.Darken;

    // Actualizar opción de Opacity del efecto
    effect.Opacity = 128; // 50%

    // Actualizar opción de color de relleno del efecto de trazo
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. La actualización de texto falla con algunos símbolos asiáticos. Error al renderizar un símbolo específico**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // seleccionar los símbolos problemáticos

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. Error al abrir el archivo exportado por Photoshop después de guardar símbolos asiáticos específicos**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

string srcFile = "TestFileForAsianCharsBig 2.psd";
string outFile = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);

    image.Save(outFile);
}
{{< /highlight >}}
