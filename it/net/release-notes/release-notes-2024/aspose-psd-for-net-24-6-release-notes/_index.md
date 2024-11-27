---
title: Aspose.PSD per .NET 24.6 - Note sulla versione
type: docs
weight: 70
url: /it/net/aspose-psd-per-net-24-6-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                         | **Categoria** |
|:------------|:------------------------------------------------------------------------------------|:-------------|
| PSDNET-1450 | Implementa il supporto al livello di mappa di sfumatura                                  | Funzionalità |
| PSDNET-1670 | [Formato AI] Aggiungi supporto ai metadati XPacket al formato AI                  | Funzionalità |
| PSDNET-1831 | Implementa i tipi di deformazione Inflate, Squeeze e Twist                           | Funzionalità |
| PSDNET-1653 | I modi Rgb e Lab non possono contenere meno di 3 canali e più di 4 canali nel file con Livelli ArtBoard          | Bug      |
| PSDNET-1775 | L'area di elaborazione superiore deve essere positiva. (Parametro 'areaToProcess') nell'elaborazione di un file specifico  | Bug      |
| PSDNET-2052 | L'immagine espansa sopra il canvas viene tagliata dopo il salvataggio. I dati vengono persi ma l'anteprima sembra corretta | Bug      |

## **Cambiamenti nella API pubblica**
# **API Aggiunte:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **API Rimosse:**
- Nessuna

## **Esempi di Utilizzo:**

**PSDNET-1450. Implementa il supporto al livello di mappa di sfumatura**

{{< highlight csharp >}}
string fileSorgente = Path.Combine(cartellaBase, "gradient_map_src.psd");
string fileOutput = Path.Combine(cartellaOutput, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(fileSorgente))
{
    // Aggiungi il livello di aggiustamento mappa di sfumatura.
    GradientMapLayer layer = im.AddGradientMapAdjustmentLayer();
    layer.GradientSettings.Reverse = true;

    im.Save(fileOutput);
}

// Controlla i cambiamenti salvati
using (PsdImage im = (PsdImage)Image.Load(fileOutput))
{
    GradientMapLayer gradientMapLayer = im.Layers[1] as GradientMapLayer;
    GradientFillSettings gradientSettings = (GradientFillSettings)gradientMapLayer.GradientSettings;

    AssertAreEqual(0.0, gradientSettings.Angle);
    AssertAreEqual((short)4096, gradientSettings.Interpolation);
    AssertAreEqual(true, gradientSettings.Reverse);
    AssertAreEqual(false, gradientSettings.AlignWithLayer);
    AssertAreEqual(false, gradientSettings.Dither);
    AssertAreEqual(GradientType.Linear, gradientSettings.GradientType);
    AssertAreEqual(100, gradientSettings.Scale);
    AssertAreEqual(0.0, gradientSettings.HorizontalOffset);
    AssertAreEqual(0.0, gradientSettings.VerticalOffset);
    AssertAreEqual("Custom", gradientSettings.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Gli oggetti non sono uguali.");
    }
}
{{< /highlight >}}

**PSDNET-1670. [Formato AI] Aggiungi supporto ai metadati XPacket al formato AI**

{{< highlight csharp >}}
string fileSorgente = Path.Combine(cartellaBase, "ai_one.ai");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Gli oggetti non sono uguali.");
    }
}

void AssertIsNotNull(object testObject)
{
    if (testObject == null)
    {
        throw new Exception("Gli oggetti di test sono nulli.");
    }
}

string creatorToolKey = ":CreatorTool";
string nPagesKey = "xmpTPg:NPages";
string unitKey = "stDim:unit";
string heightKey = "stDim:h";
string widthKey = "stDim:w";

string expectedCreatorTool = "Adobe Illustrator CC 22.1 (Windows)";
string expectedNPages = "1";
string expectedUnit = "Pixels";
double expectedHeight = 768;
double expectedWidth = 1366;

using (AiImage image = (AiImage)Image.Load(fileSorgente))
{
    // I metadati Xmp sono stati aggiunti.
    var xmpMetaData = image.XmpData;

    AssertIsNotNull(xmpMetaData);

    // Ora possiamo accedere ai pacchetti Xmp dei file AI.
    var basicPackage = xmpMetaData.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var package = xmpMetaData.Packages[4];

    // E abbiamo accesso al contenuto di questi pacchetti.
    var creatorTool = basicPackage[creatorToolKey].ToString();
    var nPages = package[nPagesKey];
    var unit = package[unitKey];
    var height = double.Parse(package[heightKey].ToString(), CultureInfo.InvariantCulture);
    var width = double.Parse(package[widthKey].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(creatorTool, expectedCreatorTool);
    AssertAreEqual(nPages, expectedNPages);
    AssertAreEqual(unit, expectedUnit);
    AssertAreEqual(height, expectedHeight);
    AssertAreEqual(width, expectedWidth);
}
{{< /highlight >}}

**PSDNET-1831. Implementa i tipi di deformazione Inflate, Squeeze e Twist**

{{< highlight csharp >}}
string[] files = { "Twist", "Squeeze", "Squeeze_vert", "Inflate" };

foreach (string prefix in files)
{
    string fileSorgente = Path.Combine(cartellaBase, prefix + ".psd");
    string fileOutput = Path.Combine(cartellaOutput, prefix + "_export.png");

    using (var psdImage = (PsdImage)Image.Load(fileSorgente, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        psdImage.Save(fileOutput, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. I modi Rgb e Lab non possono contenere meno di 3 canali e più di 4 canali nel file con Livelli ArtBoard**

{{< highlight csharp >}}
string fileSorgente = Path.Combine(cartellaBase, "Rgb5Channels.psb");
string fileOutput = Path.Combine(cartellaOutput, "Rgb5Channels_output.psd");

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(fileSorgente))
{
    // Qui non dovrebbe esserci eccezione
    image.Save(fileOutput);
}
{{< /highlight >}}

**PSDNET-1775. L'area di elaborazione superiore deve essere positiva. (Parametro 'areaToProcess') nell'elaborazione di un file specifico**

{{< highlight csharp >}}
string fileSorgente = @"BANNERS_2_Intel-Gamer_psak.psd";
string fileOutput = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
using (PsdImage image = (PsdImage)PsdImage.Load(fileSorgente, psdLoadOptions))
{
    image.Save(fileOutput);
    // Non dovrebbe esserci eccezione
}
{{< /highlight >}}

**PSDNET-2052. L'immagine espansa sopra il canvas viene tagliata dopo il salvataggio. I dati vengono persi ma l'anteprima sembra corretta**

{{< highlight csharp >}}
string fileSorgente = Path.Combine(cartellaBase, "bigfile.psd");

string fileOutput = Path.Combine(cartellaOutput, "bigfile_output.psd");
string immagineOutput = Path.Combine(cartellaOutput, "bigfile.png");

PsdLoadOptions loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(fileSorgente, loadOptions))
{
    // Non dovrebbero esserci errori qui
    psdImage.Save(fileOutput, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var psdImage = (PsdImage)Image.Load(fileOutput, loadOptions))
{
    psdImage.Resize(psdImage.Width / 10, psdImage.Height / 10);

    // Non dovrebbero esserci errori qui
    psdImage.Save(immagineOutput, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
