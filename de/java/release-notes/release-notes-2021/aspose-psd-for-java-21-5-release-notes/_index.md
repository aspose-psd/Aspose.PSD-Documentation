---
title: Aspose.PSD für Java 21.5 - Versionshinweise
type: docs
weight: 40
url: /de/java/aspose-psd-fur-java-21-5-versionshinweise/
---

{{% alert color="primary" %}} Diese Seite enthält Versionshinweise für [Aspose.PSD für Java 21.5](https://downloads.aspose.com/psd/java/neue-versionen/aspose.psd-fur-java-21.5/) {{% /alert %}}

{{% alert color="info" %}}
Dies ist eine Zwischenversion von Aspose.PSD für Java. Es gibt einige bekannte Probleme. Wenn Sie also eine stabile Version benötigen, sollten Sie [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/neue-versionen/aspose.psd-fur-java-20.9/) verwenden, bis Aspose.PSD 21.6 veröffentlicht wird. Diese Version enthält alle Aspose.PSD .Net Funktionen (einschließlich Smart Object) seit 20.9 sowie die unten aufgeführten Features.
{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-340|Unterstützung beim Ändern der Formebenen mit Vektorpfaden, wenn nur eine Ebene geändert wird|Funktion|
|PSDJAVA-341|Unterstützung beim Ändern der Formebenen mit Vektorpfaden|Funktion|
|PSDJAVA-342|Abgeschnittener Textstring|Fehler|

# **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- M:com.aspose.psd.CmykColor.isEquals(com.aspose.psd.CmykColor,com.aspose.psd.CmykColor)
- M:com.aspose.psd.Color.isEquals(com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.ColorPaletteHelper.getCloseImagePalette(com.aspose.psd.RasterImage,com.aspose.psd.Rectangle,int,boolean)
- M:com.aspose.psd.ColorPaletteHelper.hasTransparentColors(com.aspose.psd.IColorPalette)
- T:com.aspose.psd.CompositeException
- T:com.aspose.psd.CurrentThreadSettings
- M:com.aspose.psd.CurrentThreadSettings.getLocale
- M:com.aspose.psd.CurrentThreadSettings.setLocale(java.lang.String)
- M:com.aspose.psd.CurrentThreadSettings.setLocale(java.util.Locale)
- M:com.aspose.psd.DataStreamSupporter.save(java.io.RandomAccessFile)
- M:com.aspose.psd.DataStreamSupporter.saveData(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.DisposableObject.close
- M:com.aspose.psd.Font.makeFontWithGraphUnit(java.lang.String,float,int)
- M:com.aspose.psd.FontSettings.addFontsFolder(java.lang.String)
- M:com.aspose.psd.FontSettings.removeFontsFolder(java.lang.String)
- M:com.aspose.psd.FontSettings.setFontsFolders(java.lang.String[])
- M:com.aspose.psd.Image.create(com.aspose.psd.Image[])
- M:com.aspose.psd.Image.create(com.aspose.psd.Image[],boolean)
- M:com.aspose.psd.Image.getImage2Export(com.aspose.psd.ImageOptionsBase,com.aspose.psd.Rectangle)
- M:com.aspose.psd.Image.isAutoAdjustPalette
- M:com.aspose.psd.Image.isUsePalette
- M:com.aspose.psd.Image.load(java.io.RandomAccessFile)
- M:com.aspose.psd.Image.load(java.io.RandomAccessFile,com.aspose.psd.LoadOptions)
- M:com.aspose.psd.Image.save(java.io.RandomAccessFile,com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.Image.save(java.io.RandomAccessFile,com.aspose.psd.ImageOptionsBase,com.aspose.psd.Rectangle)
- M:com.aspose.psd.ImageOptionsBase.deepClone
- M:com.aspose.psd.ImageOptionsBase.getFullFrame
- M:com.aspose.psd.ImageOptionsBase.memberwiseClone
- M:com.aspose.psd.ImageOptionsBase.setFullFrame(boolean)
- F:com.aspose.psd.Matrix.TYPE_FLIP
- F:com.aspose.psd.Matrix.TYPE_GENERAL_ROTATION
- F:com.aspose.psd.Matrix.TYPE_GENERAL_SCALE
- F:com.aspose.psd.Matrix.TYPE_GENERAL_TRANSFORM
- F:com.aspose.psd.Matrix.TYPE_IDENTITY
- F:com.aspose.psd.Matrix.TYPE_MASK_ROTATION
- F:com.aspose.psd.Matrix.TYPE_MASK_SCALE
- F:com.aspose.psd.Matrix.TYPE_QUADRANT_ROTATION
- F:com.aspose.psd.Matrix.TYPE_TRANSLATION
- F:com.aspose.psd.Matrix.TYPE_UNIFORM_SCALE
- M:com.aspose.psd.Matrix.isEquals(com.aspose.psd.Matrix,com.aspose.psd.Matrix)
- M:com.aspose.psd.Matrix.isIdentity
- M:com.aspose.psd.NonGenericDictionary.#ctor
- M:com.aspose.psd.NonGenericDictionary.getKeysTyped
- M:com.aspose.psd.NonGenericDictionary.getValuesTyped
- M:com.aspose.psd.NonGenericList.add(int,java.lang.Object)
- M:com.aspose.psd.NonGenericList.addAll(java.util.Collection)
- M:com.aspose.psd.NonGenericList.addAll(int,java.util.Collection)
- M:com.aspose.psd.NonGenericList.containsAll(java.util.Collection)
- M:com.aspose.psd.NonGenericList.get(int)
- M:com.aspose.psd.NonGenericList.getList
- M:com.aspose.psd.NonGenericList.isEmpty
- M:com.aspose.psd.NonGenericList.lastIndexOf(java.lang.Object)
- M:com.aspose.psd.NonGenericList.listIterator
- M:com.aspose.psd.NonGenericList.listIterator(int)
- M:com.aspose.psd.NonGenericList.remove(int)
- M:com.aspose.psd.NonGenericList.removeAll(java.util.Collection)
- M:com.aspose.psd.NonGenericList.retainAll(java.util.Collection)
- M:com.aspose.psd.NonGenericList.set(int,java.lang.Object)
- M:com.aspose.psd.NonGenericList.subList(int,int)
- M:com.aspose.psd.NonGenericList.toArray
- M:com.aspose.psd.NonGenericList.toArray(java.lang.Object[])
- T:com.aspose.psd.PdfComplianceVersion
- F:com.aspose.psd.PdfComplianceVersion.Pdf15
- F:com.aspose.psd.PdfComplianceVersion.PdfA1a
- F:com.aspose.psd.PdfComplianceVersion.PdfA1b
-...
-...

# **Entfernte APIs:**
- M:com.aspose.psd.coreexceptions.imageformats.BmpImageException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.compressors.RleCompressorException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.compressors.LzwCompressorException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.compressors.DeflateCompressorException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.XmpException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.StreamReadException.setActualReadCount(int)
- M:com.aspose.psd.coreexceptions.StreamReadException.setExpectedReadCount(int)
- M:com.aspose.psd.coreexceptions.LimitMemoryException.#ctor(java.lang.String,java.lang.RuntimeException,int)
- M:com.aspose.psd.coreexceptions.LimitMemoryException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.IndexOutOFRangeException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.ImageSaveException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.ImageLoadException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.ImageException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.ImageCreateException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.FrameworkException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.CompressorException.#ctor(java.lang.String,java.lang.RuntimeException)
- F:com.aspose.psd.StreamContainer.ReadWriteBytesCount
- F:com.aspose.psd.StreamContainer.StartPosition
-...
-...

# **Beispiele für die Verwendung:**

**PSDJAVA-340. Unterstützung beim Ändern der Formebenen mit Vektorpfaden, wenn nur eine Ebene geändert wird**

{{< highlight java >}}
    // This example shows how to resize layers with a Vogk and vector path resource in the PSD image
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

**PSDJAVA-341. Unterstützung beim Ändern der Formebenen mit Vektorpfaden**

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
        PngOptionsOptions options = new PngOptions();
        options.setColorType(PngColorType.TruecolorWithAlpha);
        psdImage.save(outputPath, options);
    } finally {
        psdImage.dispose();
    }
{{< /highlight >}}

**PSDJAVA-342. Abgeschnittener Textstring**

{{< highlight java >}}
    String dataDir = "PSDNET948";
    String fileName = "text_in_psd.psd";
    String outputPath = Paths.get(dataDir, "output.psd").toString();
    String outputPngPath = Paths.get(dataDir, "output.png").toString();
    PsdImage psdImage = (PsdImage) Image.load(fileName);
    try {
        psdImage.save(outputPath);
        PngOptions options = new PngOptions();
        options.setColorType(PngColorType.TruecolorWithAlpha);
        psdImage.save(outputPngPath, options);
    } finally {
        psdImage.dispose();
    }
{{< /highlight >}}