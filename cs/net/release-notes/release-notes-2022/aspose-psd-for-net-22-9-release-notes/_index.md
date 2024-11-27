---
title: Aspose.PSD pro .NET 22.9 - Poznámky k vydání
type: docs
weight: 40
url: /cs/net/aspose-psd-for-net-22-9-release-notes/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Toto vydání má regresi v případě exportů 16bitů, proto doporučujeme opatrnost při používání této funkce v tomto vydání.
Prosím neaktualizujte Aspose.PSD na verzi 22.9, pokud je zpracování obrázků 16bitů vaší primární funkcí.
- Pro některé verze programu Photoshop se uživatelé mohou setkat s oknem s chybou čtení vrstvy, což neovlivní práci se souborem PSD.

Pracujeme na řešení těchto problémů.

{{% /alert %}}

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-1237|Vytvořit interní model vrstvy LayerStyleFX, který bude obsahovat efekty a související data pro použití jediného modelu v zdrojích efektů Lfx2, lmfx a mlst|Vylepšení|
|PSDNET-1227|Přidání čtení a zápisu struktur 'Lefx' s informacemi o efektech pro vrstvy v modelech časové osy|Funkce|
|PSDNET-1230|Aplikování stavu vrstvy časové osy na vrstvu v objektu typu PsdImage|Funkce|
|PSDNET-1072|Nesprávná průhlednost při ukládání souboru PSD (RGB/16bit) při exportu do 8bitů|Chyba|
|PSDNET-1140|Výjimka při načítání globálních zdrojů vrstevových kroků při otevírání dokumentu PSB|Chyba|
|PSDNET-1266|Únik paměti při zpracování konkrétních souborů|Chyba|


## **Změny ve veřejném API**
# **Přidaná API:**
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


# **Odebraná API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **Příklady použití:**

**PSDNET-1072. Nesprávná průhlednost při ukládání souboru PSD (RGB/16bit) při exportu do 8bitů**

{{< highlight csharp >}}
string inputPsdFile    = "8bitWithTransparency.psd";
string outputPsdFile   = "16bitWithTransparency.psd";
string outputImageFile = "OutputWithTransparency.png";

using (var img = Image.Load(inputPsdFile))
{
    // Nastavení 16 bitových možností uložení
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(outputPsdFile, p16);
}
using (var img = Image.Load(outputPsdFile))
{
    // Uloží obrázek s 16bitovými barvami
    img.Save(outputImageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. Výjimka při načítání globálních zdrojů vrstevových kroků při otevírání dokumentu PSB**

{{< highlight csharp >}}
string sourcePsdFile = "input.psb";
string outputImageFile = "output.png";

using (var image = (PsdImage)Image.Load(sourcePsdFile))
{
    // Zde by neměla být výjimka.
    image.Save(outputImageFile, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. Přidání čtení a zápisu struktur 'Lefx' s informacemi o efektech pro vrstvy v modelech časové osy**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputFile = "output.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    int[] layerIds = timeLine.LayerIds;

    var vrstvaStavuEfektů11 = timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects;

    vrstvaStavuEfektů11.AddDropShadow();
    vrstvaStavuEfektů11.AddGradientOverlay();

    var vrstvaStavuEfektů21 = timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects;
    vrstvaStavuEfektů21.AddStroke(FillType.Color);
    vrstvaStavuEfektů21.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1230. Aplikování stavu vrstvy časové osy na vrstvu v objektu typu PsdImage**

{{< highlight csharp >}}
string sourceFile = "3_animated.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    var vrstvaStavu11 = timeLine.Frames[1].LayerStates[layerIds[1]];

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddPatternOverlay();
    vrstvaStavu11.BlendMode = BlendMode.Multiply;

    // Změna aktivního kroku ze 0 na 1 pro aktivaci použití stavu vrstvy na vrstvu
    timeLine.ActiveFrame = 1;

    // Aplikování změn na PsdImage
    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. Únik paměti při zpracování konkrétních souborů**

{{< highlight csharp >}}
string[] filesToLoad = new string[] { "testPsd0.psd", "testPsd1.psd", "testPsd2.psd" };
int inputNumber = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(inputNumber, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Celkově použitá paměť před testem: {0:N2} MiB", memCount);

double max = memCount;

for (int i = 0; i < 50; i++)
{
    int fileIndex = i % inputNumber;
    string sourceFile = Path.Combine(baseFolder, filesToLoad[fileIndex]);

    // Kontrola otevření a uložení
    using (MemoryStream outputStream = new MemoryStream())
    {
        using (PsdImage psd = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
        {
            psd.Save(outputStream, new JpegOptions() { Quality = 100 });
        }
    }

#if NETCOREAPP
    GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
    GC.Collect(inputNumber, GCCollectionMode.Forced);
    GC.WaitForFullGCComplete();

    memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
    max = Math.Max(max, memCount);
}

memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Celkově použitá paměť po testu: {0:N2} MiB", memCount);
Assert.IsTrue(Math.Abs(memCount - max) < 20, "Nalezen únik paměti v základní funkčnosti!");
{{< /highlight >}}
