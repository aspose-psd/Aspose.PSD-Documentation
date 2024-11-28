---
title: Aspose.PSD pro Java 21.5 - Poznámky k verzi
type: docs
weight: 40
url: /cs/java/aspose-psd-pro-java-21-5-poznamky-k-verzi/
---

{{% alert color="primary" %}} Tato stránka obsahuje poznámky k verzi [Aspose.PSD pro Java 21.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.5/) {{% /alert %}}

{{% alert color="info" %}}
Jedná se o mezipředstavení Aspose.PSD pro Java.
Obsahuje některé známé problémy. Proto pokud potřebujete stabilní verzi, měli byste používat [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.9/) do vydání Aspose.PSD 21.6.
Tato verze zahrnuje všechny funkce Aspose.PSD .Net (včetně inteligentního objektu) od verze 20.9 a níže uvedené funkce.
{{% /alert %}} 

| **Klíč** | **Souhrn** | **Kategorie** |
| :- | :- | :- |
| PSDJAVA-340 | Podpora změny velikosti vrstev tvarů s vektorovými cestami, když je změněna pouze vrstva | Funkce |
| PSDJAVA-341 | Podpora změny velikosti vrstev tvarů s vektorovými cestami | Funkce |
| PSDJAVA-342 | Oříznutý textový řetězec | Chyba |

# **Změny ve veřejném rozhraní API**
# **Přidaná API:**
- M:com.aspose.psd.CmykColor.isEquals(com.aspose.psd.CmykColor,com.aspose.psd.CmykColor)
- M:com.aspose.psd.Color.isEquals(com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.ColorPaletteHelper.getCloseImagePalette(com.aspose.psd.RasterImage,com.aspose.psd.Rectangle,int,boolean)
- M:com.aspose.psd.ColorPaletteHelper.hasTransparentColors(com.aspose.psd.IColorPalette)
- ...

# **Odebrané API:**
- M:com.aspose.psd.coreexceptions.imageformats.BmpImageException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.compressors.RleCompressorException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.compressors.LzwCompressorException.#ctor(java.lang.String,java.lang.RuntimeException)
- ...

# **Příklady použití:**

**PSDJAVA-340. Podpora změny velikosti vrstev tvarů s vektorovými cestami, když je změněna pouze vrstva**

{{< highlight java >}}
    // Tento příklad ukazuje, jak změnit velikost vrstev s vrstvami Vogk a vektorovými cestami v obraze PSD
    float scaleX = 0.45f;
    float scaleY = 1.60f;
    String dataDir = "PSDNET862_1";
    String sourceFileName = Paths.get(dataDir, "vectorShapes.psd").toString();
    PsdImage image = (PsdImage) Image.load(sourceFileName);
    try {
        for (int layerIndex = 1; layerIndex < image.getLayers().length; layerIndex++, scaleX += 0.25f, scaleY -= 0.25f) {
            Layer layer = image.getLayers()[layerIndex];
            int newWidth = (int) Math.round(layer.getWidth() * scaleX);
            int newHeight = (int) Math.round(layer.getHeight() * scaleY);
            layer.resize(newWidth, newHeight);

            String outputName = String.format("resized_%1$s_%2$s_%2$s", layerIndex, scaleX, scaleY);
            String outputPath = Paths.get(dataDir, outputName + ".psd").toString();
            String outputPngPath = Paths.get(dataDir, outputName + ".png").toString();
            image.save(outputPath, new PsdOptions(image));
            PngOptions options = new PngOptions();
            options.setColorType(PngColorType.TruecolorWithAlpha);
            image.save(outputPngPath, options);
        }
    } finally {
        image.dispose();
    }
{{< /highlight >}}

**PSDJAVA-341. Podpora změny velikosti vrstev tvarů s vektorovými cestami**

{{< highlight java >}}
    String sourceFileName = "vectorShapes.psd";
    String outputFileName = "out_vectorShapes.psd";
    String dataDir = "PSDNET758_1";
    String sourcePath = Paths.get(dataDir, sourceFileName).toString();
    String outputPath = Paths.get(dataDir, outputFileName).toString();
    PsdImage psdImage = (PsdImage) Image.load(sourcePath);
    try {
        for (Layer layer : psdImage.getLayers())
        {
            layer.resize(layer.getWidth() * 5 / 4, layer.getHeight() / 2);
        }

        psdImage.save(outputPath);
        PngOptions options = new PngOptions();
        options.setColorType(PngColorType.TruecolorWithAlpha);
        psdImage.save(outputPath + ".png", options);
    } finally {
        psdImage.dispose();
    }
{{< /highlight >}}

**PSDJAVA-342. Oříznutý textový řetězec**

{{< highlight java >}}
    String srcFile = "grinched-regular-font.psd";
    String output = "output_grinched-regular-font.psd.png";

    // Nastavit cestu k písmům
    List<String> fonts = new ArrayList<>();
    fonts.addAll(Arrays.asList(FontSettings.getDefaultFontsFolders()));
    fonts.add("Fonts\\");
    FontSettings.setFontsFolders(fonts.toArray(new String[0]), true);

    PsdImage image = (PsdImage) Image.load(srcFile);
    try {
        image.save(output, new PngOptions());
    } finally {
        image.dispose();
    }
{{< /highlight >}}# **Příklady použití:**

**PSDJAVA-340. Podpora změny velikosti vrstev tvarů s vektorovými cestami, když je změněna pouze vrstva**

{{< highlight java >}}
    // Tento příklad ukazuje, jak změnit velikost vrstev s vrstvami Vogk a vektorovými cestami v obraze PSD
    float scaleX = 0.45f;
    float scaleY = 1.60f;
    String dataDir = "PSDNET862_1";
    String sourceFileName = Paths.get(dataDir, "vectorShapes.psd").toString();
    PsdImage image = (PsdImage) Image.load(sourceFileName);
    try {
        for (int layerIndex = 1; layerIndex < image.getLayers().length; layerIndex++, scaleX += 0.25f, scaleY -= 0.25f) {
            Layer layer = image.getLayers()[layerIndex];
            int newWidth = (int) Math.round(layer.getWidth() * scaleX);
            int newHeight = (int) Math.round(layer.getHeight() * scaleY);
            layer.resize(newWidth, newHeight);

            String outputName = String.format("resized_%1$s_%2$s_%2$s", layerIndex, scaleX, scaleY);
            String outputPath = Paths.get(dataDir, outputName + ".psd").toString();
            String outputPngPath = Paths.get(dataDir, outputName + ".png").toString();
            image.save(outputPath, new PsdOptions(image));
            PngOptions options = new PngOptions();
            options.setColorType(PngColorType.TruecolorWithAlpha);
            image.save(outputPngPath, options);
        }
    } finally {
        image.dispose();
    }
{{< /highlight >}}

**PSDJAVA-341. Podpora změny velikosti vrstev tvarů s vektorovými cestami**

{{< highlight java >}}
    String sourceFileName = "vectorShapes.psd";
    String outputFileName = "out_vectorShapes.psd";
    String dataDir = "PSDNET758_1";
    String sourcePath = Paths.get(dataDir, sourceFileName).toString();
    String outputPath = Paths.get(dataDir, outputFileName).toString();
    PsdImage psdImage = (PsdImage) Image.load(sourcePath);
    try {
        for (Layer layer : psdImage.getLayers())
        {
            layer.resize(layer.getWidth() * 5 / 4, layer.getHeight() / 2);
        }

        psdImage.save(outputPath);
        PngOptions options = new PngOptions();
        options.setColorType(PngColorType.TruecolorWithAlpha);
        psdImage.save(outputPath + ".png", options);
    } finally {
        psdImage.dispose();
    }
{{< /highlight >}}

**PSDJAVA-342. Oříznutý textový řetězec**

{{< highlight java >}}
    String srcFile = "grinched-regular-font.psd";
    String output = "output_grinched-regular-font.psd.png";

    // Nastavit cestu k písmům
    List<String> fonts = new ArrayList<>();
    fonts.addAll(Arrays.asList(FontSettings.getDefaultFontsFolders()));
    fonts.add("Fonts\\");
    FontSettings.setFontsFolders(fonts.toArray(new String[0]), true);

    PsdImage image = (PsdImage) Image.load(srcFile);
    try {
        image.save(output, new PngOptions());
    } finally {
        image.dispose();
    }
{{< /highlight >}}

**PSDJAVA-342. Oříznutý textový řetězec**