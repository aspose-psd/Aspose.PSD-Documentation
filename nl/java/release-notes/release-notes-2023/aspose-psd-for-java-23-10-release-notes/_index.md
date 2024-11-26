---
title: Aspose.PSD for Java 23.10 - Release Notities
type: docs
weight: 40
url: /nl/java/aspose-psd-voor-java-23-10-release-notities/
---

{{% alert color="primary" %}} Deze pagina bevat release notities voor [Aspose.PSD voor Java 23.10](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-voor-java-23.10/) {{% /alert %}}

| **Sleutel**     | **Samenvatting**                                                                     | **Categorie** |
|:---------------|:----------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-538    | Ondersteuning van verticale tekst richting                                              |    Feature   |
| PSDJAVA-542    | Gebruik van Slag instellingen van vstk bron in Vorm Slag weergave                      |    Feature   |
| PSDJAVA-540    | Implementeer weergave van intern gebied van Slag vormen                                |    Feature   |
| PSDJAVA-541    | Shape laag niet herschilderen als deze niet is gewijzigd                               |    Feature   |
| PSDJAVA-545    | [AI Formaat] Toevoegen ondersteuning voor lezen van Header uit PDF-gebaseerde AI Bestanden |    Feature   |
| PSDJAVA-546    | Verschillende manieren om Psd Bestandsresolutie in te stellen werken niet              |      Bug     |
| PSDJAVA-547    | FontSettings.SetFontsFolders werkt niet of Aspose.PSD gebruikt onjuist lettertype      |      Bug     |
| PSDJAVA-548    | Herstel. Null referentie uitzondering veroorzaken op PsdImage.Save bij het hebben van Shape laag |      Bug     |

## **Veranderingen in Openbare API**
# **Toegevoegde API's:**

- M:com.aspose.psd.FontSettings.getGetSystemAlternativeFont
- M:com.aspose.psd.FontSettings.setGetSystemAlternativeFont(boolean)
- M:com.aspose.psd.Graphics.getPaintableImageOptions
- M:com.aspose.psd.Graphics.setPaintableImageOptions(com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.Image.getAutoAdjustPalette
- M:com.aspose.psd.Image.getFileFormat(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.extensions.RegionExtensions.#ctor
- M:com.aspose.psd.fileformats.psd.PsdImage.setResolution(double,double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.getStroke
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.setStroke(com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.getFillSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.JustificationMode.Center
- T:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getEnabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getFill
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineAlignment
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineCap
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineDashSet
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineJoin
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setFill(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineAlignment(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineCap(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineDashSet(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineJoin(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setSize(double)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getEnabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getFill
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineAlignment
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setFill(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineDashSet(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineCap
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineDashSet
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineJoin
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineAlignment(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineCap(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineJoin(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setSize(double)
- T:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String)
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)

# **Verwijderde API's:**

- M:com.aspose.psd.Image.isAutoAdjustPalette
- M:com.aspose.psd.ImageOptionsBase.memberwiseClone
- M:com.aspose.psd.imageoptions.BmpOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.CmxRasterizationOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.GifOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.Jpeg2000Options.memberwiseClone
- M:com.aspose.psd.imageoptions.JpegOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PdfOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PngOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PsdOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.TiffOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.VectorRasterizationOptions.memberwiseClone
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.JustificationMode.Center

## **Voorbeelden van gebruik:**

** PSDJAVA-538. Ondersteuning van verticale tekst richting**

{{< highlight java >}}
    
    String bronBestand = "src/main/resources/692_lt1.psd";
    String uitvoerBestand = "src/main/resources/692_output.png";
    String lettertypeMap = "src/main/resources/692_Fonts";

        Lijst<String> lettertypeMappen = new Lijst<>(FontSettings.getFontsFolders());
        lettertypeMappen.add(lettertypeMap);
        FontSettings.setFontsFolders(lettertypeMappen.toArray(new String[0]), true);

        probeer(PsdImage psdAfbeelding = (PsdImage)Image.load(bronBestand)) {
            PngOptions pngOpties = new PngOptions();
            pngOpties.setColorType(PngColorType.TruecolorWithAlpha);

            psdAfbeelding.save(uitvoerBestand, pngOpties);
        }

{{< /highlight >}}

** PSDJAVA-542. Gebruik van Slag instellingen van vstk bron in Vorm Slag weergave**

{{< highlight java >}}

    public static void main(String[] args) {
        String bronBestand = "src/main/resources/StrokeShapeTest.psd";
        String uitvoerBestandPsd = "src/main/resources/StrokeShapeTest.out.psd";
        String uitvoerBestandPng = "src/main/resources/StrokeShapeTest.out.png";

        probeer (PsdImage afbeelding = (PsdImage) Image.load(bronBestand)) {
            Laag laag = afbeelding.getLayers()[1];
            ShapeLayer vormLaag = (ShapeLayer) afbeelding.getLayers()[1];
            ColorFillSettings vulInstellingen = (ColorFillSettings) vormLaag.getFill();
            vulInstellingen.setColor(Color.getGreenYellow());
            vormLaag.update();

            ShapeLayer vormLaag2 = (ShapeLayer) afbeelding.getLayers()[3];
            GradientFillSettings gradiëntInstellingen = (GradientFillSettings) vormLaag2.getFill();
            gradiëntInstellingen.setDither(true);
            gradiëntInstellingen.setReverse(true);
            gradiëntInstellingen.setAlignWithLayer(false);
            gradiëntInstellingen.setAngle(20);
            gradiëntInstellingen.setScale(50);
            gradiëntInstellingen.getColorPoints()[0].setLocation(100);
            gradiëntInstellingen.getColorPoints()[1].setLocation(4000);
            gradiëntInstellingen.getTransparencyPoints()[0].setLocation(200);
            gradiëntInstellingen.getTransparencyPoints()[1].setLocation(3800);
            gradiëntInstellingen.getTransparencyPoints()[0].setOpacity(90);
            gradiëntInstellingen.getTransparencyPoints()[1].setOpacity(10);
            vormLaag2.update();

            ShapeLayer vormLaag3 = (ShapeLayer) afbeelding.getLayers()[5];
            StrokeSettings slagInstellingen = (StrokeSettings) vormLaag3.getStroke();
            slagInstellingen.setSize(15);
            ColorFillSettings slagVulInstellingen = (ColorFillSettings) slagInstellingen.getFill();
            slagVulInstellingen.setColor(Color.getGreenYellow());
            vormLaag3.update();

            afbeelding.save(uitvoerBestandPsd);
            afbeelding.save(uitvoerBestandPng, new PngOptions());
        }

        // Controleren van gewijzigde gegevens.
        probeer (PsdImage afbeelding = (PsdImage) Image.load(uitvoerBestandPsd)) {
            ShapeLayer vormLaag = (ShapeLayer) afbeelding.getLayers()[1];
            ColorFillSettings vulInstellingen = (ColorFillSettings) vormLaag.getFill();
            assertAreEqual(Color.getGreenYellow(), vulInstellingen.getColor());

            ShapeLayer vormLaag2 = (ShapeLayer) afbeelding.getLayers()[3];
            GradientFillSettings gradiëntInstellingen = (GradientFillSettings) vormLaag2.getFill();
            assertAreEqual(true, gradiëntInstellingen.getDither());
            assertAreEqual(true, gradiëntInstellingen.getReverse());
            assertAreEqual(false, gradiëntInstellingen.getAlignWithLayer());
            assertAreEqual(20.0, gradiëntInstellingen.getAngle());
            assertAreEqual(50, gradiëntInstellingen.getScale());
            assertAreEqual(100, gradiëntInstellingen.getColorPoints()[0].getLocation());
            assertAreEqual(4000, gradiëntInstellingen.getColorPoints()[1].getLocation());
            assertAreEqual(200, gradiëntInstellingen.getTransparencyPoints()[0].getLocation());
            assertAreEqual(3800, gradiëntInstellingen.getTransparencyPoints()[1].getLocation());
            assertAreEqual(90.0, gradiëntInstellingen.getTransparencyPoints()[0].getOpacity());
            assertAreEqual(10.0, gradiëntInstellingen.getTransparencyPoints()[1].getOpacity());

            ShapeLayer vormLaag3 = (ShapeLayer) afbeelding.getLayers()[5];
            StrokeSettings slagInstellingen = (StrokeSettings) vormLaag3.getStroke();
            ColorFillSettings slagVulInstellingen = (ColorFillSettings) slagInstellingen.getFill();
            assertAreEqual(15.0, slagInstellingen.getSize());
            assertAreEqual(Color.getGreenYellow(), slagVulInstellingen.getColor());
        }
    }

    static void assertAreEqual(Object verwacht, Object daadwerkelijk) {
        assertAreEqual(verwacht, daadwerkelijk, "Objecten zijn niet gelijk.");
    }

    static void assertAreEqual(Object verwacht, Object daadwerkelijk, String bericht) {
        if (!verwacht.equals(daadwerkelijk)) {
            throw new IllegalArgumentException(bericht);
        }
    }

{{< /highlight >}}


** PSDJAVA-540. Implementeer weergave van intern gebied van Slag vormen**

{{< highlight java >}}

    public static void main(String[] args) {
        String bronBestand = "src/main/resources/StrokeShapeTest.psd";
        String uitvoerBestandPsd = "src/main/resources/StrokeShapeTest.out.psd";
        String uitvoerBestandPng = "src/main/resources/StrokeShapeTest.out.png";

        probeer (PsdImage afbeelding = (PsdImage) Image.load(bronBestand)) {
            Laag laag = afbeelding.getLayers()[1];
            ShapeLayer vormLaag = (ShapeLayer) afbeelding.getLayers()[1];
            ColorFillSettings vulInstellingen = (ColorFillSettings) vormLaag.getFill();
            vulInstellingen.setColor(Color.getGreenYellow());
            vormLaag.update();

            ShapeLayer vormLaag2 = (ShapeLayer) afbeelding.getLayers()[3];
            GradientFillSettings gradiëntInstellingen = (GradientFillSettings) vormLaag2.getFill();
            gradiëntInstellingen.setDither(true);
            gradiëntInstellingen.setReverse(true);
            gradiëntInstellingen.setAlignWithLayer(false);
            gradiëntInstellingen.setAngle(20);
            gradiëntInstellingen.setScale(50);
            gradiëntInstellingen.getColorPoints()[0].setLocation(100);
            gradiëntInstellingen.getColorPoints()[1].setLocation(4000);
            gradiëntInstellingen.getTransparencyPoints()[0].setLocation(200);
            gradiëntInstellingen.getTransparencyPoints()[1].setLocation(3800);
            gradiëntInstellingen.getTransparencyPoints()[0].setOpacity(90);
            gradiëntInstellingen.getTransparencyPoints()[1].setOpacity(10);
            vormLaag2.update();

            ShapeLayer vormLaag3 = (ShapeLayer) afbeelding.getLayers()[5];
            StrokeSettings slagInstellingen = (StrokeSettings) vormLaag3.getStroke();
            slagInstellingen.setSize(15);
            ColorFillSettings slagVulInstellingen = (ColorFillSettings) slagInstellingen.getFill();
            slagVulInstellingen.setColor(Color.getGreenYellow());
            vormLaag3.update();

            afbeelding.save(uitvoerBestandPsd);
            afbeelding.save(uitvoerBestandPng, new PngOptions());
        }

        // Controleren van gewijzigde gegevens.
        probeer (PsdImage afbeelding = (PsdImage) Image.load(uitvoerBestandPsd)) {
            ShapeLayer vormLaag = (ShapeLayer) afbeelding.getLayers()[1];
            ColorFillSettings vulInstellingen = (ColorFillSettings) vormLaag.getFill();
            assertAreEqual(Color.getGreenYellow(), vulInstellingen.getColor());

            ShapeLayer vormLaag2 = (ShapeLayer) afbeelding.getLayers()[3];
            GradientFillSettings gradiëntInstellingen = (GradientFillSettings) vormLaag2.getFill();
            assertAreEqual(true, gradiëntInstellingen.getDither());
            assertAreEqual(true, gradiëntInstellingen.getReverse());
            assertAreEqual(false, gradiëntInstellingen.getAlignWithLayer());
            assertAreEqual(20.0, gradiëntInstellingen.getAngle());
            assertAreEqual(50, gradiëntInstellingen.getScale());
            assertAreEqual(100, gradiëntInstellingen.getColorPoints()[0].getLocation());
            assertAreEqual(4000, gradiëntInstellingen.getColorPoints()[1].getLocation());
            assertAreEqual(200, gradiëntInstellingen.getTransparencyPoints()[0].getLocation());
            assertAreEqual(3800, gradiëntInstellingen.getTransparencyPoints()[1].getLocation());
            assertAreEqual(90.0, gradiënt