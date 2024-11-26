---
title: Notas da Versão Aspose.PSD para .NET 22,9
type: docs
weight: 40
url: /pt/net/aspose-psd-para-net-22-9-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/).

{{% /alert %}}

{{% alert color="warning" %}}

- Esta versão possui uma regressão no caso de exportações de 16 bits, portanto, recomendamos cautela ao usar esse recurso nesta versão.
Por favor, não atualize o Aspose.PSD para 22.9 se o processamento de imagem de 16 bits for sua funcionalidade principal.
- Para várias versões do Photoshop, os usuários podem encontrar uma janela com um erro lendo a camada, isso não afetará o trabalho com o arquivo PSD.

Estamos trabalhando em soluções para esses problemas.

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-1237|Criar o modelo interno LayerStyleFX que conterá efeitos e dados relacionados para usar o modelo único em recursos de efeitos Lfx2, lmfx e mlst|Melhoria|
|PSDNET-1227|Adicionar leitura e escrita das estruturas 'Lefx' com informações de efeitos para estados de camada em modelos de linha do tempo|Recurso|
|PSDNET-1230|Aplicar estado de camada de TimeLine à camada em PsdImage|Recurso|
|PSDNET-1072|Transparência incorreta ao salvar o arquivo PSD (RGB/16 bits) na exportação para 8 bits|Erro|
|PSDNET-1140|Exceção ao carregar etapa de recursos globais de camada ao abrir documento PSB|Erro|
|PSDNET-1266|Vazamento de memória no processamento de arquivos específicos|Erro|


## **Mudanças na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.PositionOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.StateEffects
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.Effects
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddDropShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddInnerShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddOuterGlow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddColorOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddGradientOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddPatternOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.ClearLayerStyle
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.RemoveEffectAt(System.Int32)


# **APIs Removidas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **Exemplos de Uso:**

**PSDNET-1072. Transparência incorreta ao salvar o arquivo PSD (RGB/16 bits) na exportação para 8 bits**

{{< highlight csharp >}}
string arquivoPsdEntrada    = "8bitComTransparencia.psd";
string arquivoPsdSaida   = "16bitComTransparencia.psd";
string arquivoImagemSaida = "SaidaComTransparencia.png";

using (var img = Image.Load(arquivoPsdEntrada))
{
    // Opções de salvamento de 16 bits
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(arquivoPsdSaida, p16);
}
using (var img = Image.Load(arquivoPsdSaida))
{
    // Salvar imagem com cores de 16 bits
    img.Save(arquivoImagemSaida, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. Exceção ao carregar etapa de recursos globais de camada ao abrir documento PSB**

{{< highlight csharp >}}
string arquivoPsdFonte = "entrada.psb";
string arquivoImagemSaida = "saida.png";

using (var imagem = (PsdImage)Image.Load(arquivoPsdFonte))
{
    // Aqui não deve haver exceção.
    imagem.Save(arquivoImagemSaida, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. Adicionar leitura e escrita das estruturas 'Lefx' com informações de efeitos para estados de camadas em modelos de linha do tempo**

{{< highlight csharp >}}
string arquivoFonte = "4_animado.psd";
string arquivoSaida = "saida.psd";

using (var psdImagem = (PsdImage)Image.Load(arquivoFonte))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImagem);
    int[] idsCamadas = timeLine.LayerIds;

    var efeitosEstadoCamada11 = timeLine.Frames[1].LayerStates[idsCamadas[1]].StateEffects;

    efeitosEstadoCamada11.AddDropShadow();
    efeitosEstadoCamada11.AddGradientOverlay();

    var efeitosEstadoCamada21 = timeLine.Frames[2].LayerStates[idsCamadas[1]].StateEffects;
    efeitosEstadoCamada21.AddStroke(FillType.Color);
    efeitosEstadoCamada21.IsVisible = false;

    timeLine.ApplyTo(psdImagem);

    psdImagem.Save(arquivoSaida);
}
{{< /highlight >}}

**PSDNET-1230. Aplicar estado de camada de TimeLine à camada em PsdImage**

{{< highlight csharp >}}
string arquivoFonte = "3_animado.psd";
string arquivoPsdSaida = "saida.psd";
string arquivoPngSaida = "saida.png";

using (var psdImagem = (PsdImage)Image.Load(arquivoFonte, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImagem);
    var idsCamadas = timeLine.LayerIds;

    var estadoCamada11 = timeLine.Frames[1].LayerStates[idsCamadas[1]];

    timeLine.Frames[1].LayerStates[idsCamadas[1]].StateEffects.AddPatternOverlay();
    estadoCamada11.BlendMode = BlendMode.Multiply;

    // Mudar o quadro ativo de 0 para 1 para ativar a aplicação do LayerState na camada
    timeLine.ActiveFrame = 1;

    // Aplicar alterações à PsdImage
    timeLine.ApplyTo(psdImagem);

    psdImagem.Save(arquivoPsdSaida);
    psdImagem.Save(arquivoPngSaida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. Vazamento de memória no processamento de arquivos específicos**

{{< highlight csharp >}}
string[] arquivosParaCarregar = new string[] { "testePsd0.psd", "testePsd1.psd", "testePsd2.psd" };
int numeroEntrada = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(numeroEntrada, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double contagemMem = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Total de bytes usados antes do teste: {0:N2} MiB", contagemMem);

double maximo = contagemMem;

for (int i = 0; i < 50; i++)
{
    int indiceArquivo = i % numeroEntrada;
    string arquivoFonte = Path.Combine(pastaBase, arquivosParaCarregar[indiceArquivo]);

    // Verificação de Abertura e Salvamento
    using (MemoryStream streamSaida = new MemoryStream())
    {
        using (PsdImage psd = (PsdImage)Image.Load(arquivoFonte, new PsdLoadOptions { LoadEffectsResource = true }))
        {
            psd.Save(streamSaida, new JpegOptions() { Quality = 100 });
        }
    }

#if NETCOREAPP
    GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
    GC.Collect(numeroEntrada, GCCollectionMode.Forced);
    GC.WaitForFullGCComplete();

    contagemMem = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
    maximo = Math.Max(maximo, contagemMem);
}

contagemMem = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Total de bytes usados após o teste: {0:N2} MiB", contagemMem);
Assert.IsTrue(Math.Abs(contagemMem - maximo) < 20, "Vazamento de memória na funcionalidade base encontrado!");
{{< /highlight >}}
