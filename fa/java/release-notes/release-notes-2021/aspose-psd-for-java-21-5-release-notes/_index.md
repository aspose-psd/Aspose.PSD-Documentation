```
---
title: یادداشتهای انتشار Aspose.PSD برای Java 21.5
type: docs
weight: 40
url: /fa/java/aspose-psd-for-java-21-5-release-notes/
---

{{% alert color="primary" %}} این صفحه شامل یادداشتهای انتشار برای [Aspose.PSD for Java 21.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.5/) است. {{% /alert %}}

{{% alert color="info" %}}
این یک انتشار میانی از Aspose.PSD برای Java می‌باشد.
این دارای برخی مشکلات شناخته شده است. بنابراین، اگر نیاز به یک نسخه پایدار دارید، باید از [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.9/) استفاده کنید تا نسخه 21.6 منتشر شود.
این انتشار شامل تمام ویژگی‌های Aspose.PSD .Net (شامل Smart Object) از نسخه 20.9 به بعد و ویژگی‌های زیر است.
{{% /alert %}} 

| **کلید** | **خلاصه** | **دسته‌بندی** |
| :- | :- | :- |
| PSDJAVA-340 | پشتیبانی از تغییر اندازه لایه‌ها با مسیرهای برداری زمانی که تنها یک لایه اندازه تغییر یافته است | ویژگی |
| PSDJAVA-341 | پشتیبانی از تغییر اندازه لایه‌ها با مسیرهای برداری | ویژگی |
| PSDJAVA-342 | رشته متن قطع شده | اشکال |

# **تغییرات عمومی API:**
# **API‌های اضافه:**
- M:com.aspose.psd.CmykColor.isEquals(com.aspose.psd.CmykColor,com.aspose.psd.CmykColor)
- ...
- ...

# **API‌های حذف شده:**
- M:com.aspose.psd.coreexceptions.imageformats.BmpImageException.#ctor(java.lang.String,java.lang.RuntimeException)
- ...
- ...

# **مثال‌های استفاده:**

**PSDJAVA-340. پشتیبانی از تغییر اندازه لایه‌ها با مسیرهای برداری زمانی که تنها یک لایه اندازه تغییر یافته است**

{{< highlight java >}}
    // این مثال نشان می‌دهد چگونه لایه‌ها با Vogk و منبع مسیر برداری در تصویر PSD تغییر اندازه داده می‌شوند
    float scaleX = 0.45f;
    float scaleY = 1.60f;
    String dataDir = "PSDNET862_1";
    String sourceFileName = Paths.get(dataDir,"vectorShapes.psd").toString();
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

**PSDJAVA-341. پشتیبانی از تغییر اندازه لایه‌ها با مسیرهای برداری**

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

**PSDJAVA-342. رشته متن قطع شده**

{{< highlight java >}}
    String srcFile = "grinched-regular-font.psd";
    String output = "output_grinched-regular-font.psd.png";

    // تنظیم مسیر فونت‌ها
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