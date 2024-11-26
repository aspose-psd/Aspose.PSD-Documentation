---
title: Notas da Versão Aspose.PSD para .NET 22.10
type: docs
weight: 30
url: /pt/net/aspose-psd-para-net-22-10-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém as notas de lançamento do [Aspose.PSD para .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Esta versão tem uma regressão no caso de exportações de 16 bits, portanto, recomendamos cautela ao usar esse recurso nesta versão.
Por favor, não atualize o Aspose.PSD para 22.9-22.10 se o processamento de imagem de 16 bits for sua funcionalidade principal.

Estamos trabalhando em soluções para esses problemas.

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-1287|Remover propriedades obsoletas em Lfx2Resource|Melhoria|
|PSDNET-1071|Aspose.PSD não consegue abrir PSD (RGB/16 bits) com compressão ZipWithoutPrediction|Bug|
|PSDNET-1257|Efeitos da linha do tempo desaparecem e aparecem de forma estranha (no Photoshop)|Bug|
|PSDNET-1278|A transparência não está funcionando para o efeito de traço com Posição Interna|Bug|
|PSDNET-1279|Regressão: Erro na abertura do Arquivo PSD|Bug|
|PSDNET-1284|Falha na atualização de texto com alguns símbolos asiáticos. Erro ao analisar símbolo específico|Bug|
|PSDNET-1291|Falha na atualização de texto com alguns símbolos asiáticos. Erro na renderização do símbolo específico|Bug|
|PSDNET-1292|Erro ao abrir o arquivo exportado pelo Photoshop após salvar símbolos asiáticos específicos|Bug|


## **Mudanças na API Pública**
# **APIs Adicionadas:**
- Nenhuma


# **APIs Removidas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Exemplos de Uso:**

**PSDNET-1071. Aspose.PSD não consegue abrir PSD (RGB/16 bits) com compressão ZipWithoutPrediction**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Efeitos da linha do tempo desaparecem e aparecem de forma estranha (no Photoshop)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Criar linha do tempo com alguns quadros.
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

**PSDNET-1278. Transparência não está funcionando para o efeito de traço com Posição Interna**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Regressão: Erro na abertura do Arquivo PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. A atualização de texto falha com alguns símbolos asiáticos. Erro ao analisar símbolo específico**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // selecionar o símbolo problemático

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Remover propriedades obsoletas em Lfx2Resource**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // Atualizar opção BlendMode do efeito
    effect.BlendMode = BlendMode.Darken;

    // Atualizar opção de Opacity do efeito
    effect.Opacity = 128; // 50%

    // Atualizar cor de preenchimento do efeito de traço
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. A atualização de texto falha com alguns símbolos asiáticos. Erro na renderização do símbolo específico**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // selecionar os símbolos problemáticos

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. Erro na abertura do arquivo exportado pelo Photoshop após salvar símbolos asiáticos específicos**

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
