---
title: Aspose.PSD dla Javy 23.6 - Notatki dotyczące wydania
type: docs
weight: 40
url: /pl/java/aspose-psd-dla-java-23-6-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}} Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla Javy 23.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.6/) {{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                                                                                                | **Kategoria** |
|:------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-479 | Refaktoryzacja interfejsu API TimeLine                                                                                                         | Usprawnienie |
| PSDJAVA-480 | Usunięcie artefaktów podczas renderowania deformacji                                                                                             | Usprawnienie |
| PSDJAVA-481 | Optymalizacja renderowania deformacji                                                                                                          | Usprawnienie |
| PSDJAVA-482 | Obsługa warstwy dostosowania progów                                                                                                             | Funkcja      |
| PSDJAVA-483 | Obsługa warstwy dostosowania selektywnego koloru                                                                                                | Funkcja      |
| PSDJAVA-484 | Możliwość eksportu TimeLine PSD do pliku Animated Gif                                                                                        | Funkcja      |
| PSDJAVA-485 | Dodanie obsługi warstwy tekstowej bez prostokątnych ramek                                                                                    | Funkcja      |
| PSDJAVA-486 | Obsługa warstwy kształtu                                                                                                                      | Funkcja      |
| PSDJAVA-487 | Zastąpienie obrazu w inteligentnym obiekcie nie jest aktualizowane                                                                             | Błąd         |
| PSDJAVA-488 | Plik PSD nie może być zapisany jako PSD ze względu na następujący wyjątek: Przestrzenie Rgb i Lab nie mogą zawierać mniej niż 3 kanałów i więcej niż 4 kanałów   | Błąd         |
| PSDJAVA-489 | Centrowanie tekstu jest utracone podczas otwierania warstwy tekstowej w trybie edycji Photoshopa                                             | Błąd         |
| PSDJAVA-490 | Wyjątek z odwołaniem do null podczas zapisywania pliku PSD                                                                                    | Błąd         |
| PSDJAVA-491 | Wyjątek podczas ładowania warstwy kształtu: Punkty dla granic wektora nie są jeszcze obsługiwane                                              | Błąd         |
| PSDJAVA-492 | Wyjątek podczas ładowania zasobu VogkResource: Punkty są zapisywane jako DoubleStructures, odczytujemy jako UnitStructures                    | Błąd         |
| PSDJAVA-493 | LayerType warstwy kształtu jest puste                                                                                                         | Błąd         |

## **Zmiany w Publicznych API**
# **Dodane API:**
- M:com.aspose.psd.PixelDataFormat.getRgba64Bpp
- F:com.aspose.psd.fileformats.psd.PsdImage.horizontalResolution
- M:com.aspose.psd.fileformats.psd.PsdImage.addSelectiveColorAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addVibranceAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addThresholdAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.getTimeline
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.getColorMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.setColorMode(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.#ctor(com.aspose.psd.PixelDataFormat,short)
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.getColorMode
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.setColorMode(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.ShmdResource.getSubResources
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.getPointsUnitType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.setPointsUnitType(int)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Horizontal
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Vertical
- M:com.aspose.psd.imageoptions.PsdOptions.isColorModeSet
- T:com.aspose.psd.fileformats.psd.layers.animation.Frame
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.#ctor
- ...

# **Usunięte API:**

- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLayers
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLength
- ...

## **Przykłady użycia:**

**PSDJAVA-482. Obsługa warstwy dostosowania progów**

...

**PSDJAVA-483. Obsługa warstwy dostosowania selektywnego koloru**

...

**PSDJAVA-484. Możliwość eksportu TimeLine PSD do pliku Animated Gif**

...

**PSDJAVA-487. Zastąpienie obrazu w inteligentnym obiekcie nie jest aktualizowane**

...

**PSDJAVA-479. Refaktoryzacja interfejsu TimeLine**

...

**PSDJAVA-488. Plik PSD nie może być zapisany jako PSD ze względu na wyjątek: Przestrzenie Rgb i Lab nie mogą zawierać mniej niż 3 kanałów i więcej niż 4 kanałów**

...

**PSDJAVA-480. Usunięcie artefaktów podczas renderowania deformacji**

...

**PSDJAVA-481. Optymalizacja renderowania deformacji**

...

**PSDJAVA-489. Centrowanie tekstu jest utracone podczas otwierania warstwy tekstowej w trybie edycji Photoshopa**

...

**PSDJAVA-485. Dodanie obsługi warstwy tekstowej bez prostokątnych ramek**

...

**PSDJAVA-491. Wyjątek podczas ładowania warstwy kształtu: Punkty dla granic wektora nie są jeszcze obsługiwane**

...

**PSDJAVA-492. Wyjątek podczas ładowania zasobu: Punkty są zapisywane jako DoubleStructures, odczytujemy jako UnitStructures**

...

**PSDJAVA-493. LayerType warstwy kształtu jest puste**

...

**PSDJAVA-486. Obsługa warstwy kształtu**

...**PSDJAVA-486. Obsługa warstwy kształtu**

{{< highlight java >}}
    String srcFile = "ShapeLayerTest.psd";
    String outFile = "ShapeLayerTest-out.psd";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer)image.getLayers()[1];
        IPath layerPath = shapeLayer.getPath();

        IPathShape[] pathShapeSource = layerPath.getItems();
        List<IPathShape> pathShapesDest = new List<IPathShape>(pathShapeSource);

        // Source file contains 2 figures. Remove the seconds one.
        pathShapesDest.removeAt(1);

          layerPath.setItems(pathShapesDest.toArray(new IPathShape[0]));

        shapeLayer.update();

        image.save(outFile);
    } catch (Exception e) {
        e.printStackTrace();
    }
{{< /highlight >}}

**PSDJAVA-487. Zastąpienie obrazu w inteligentnym obiekcie nie jest aktualizowane**

{{< highlight java >}}
    String sourceFile = "neiyi.psd";
    String changeFile = "bg6.png";

    String exportFile = "export.psd";
    String exportImgBefore = "export_before.png";
    String exportImgAfter = "export_after.png";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        for (Layer layer : psdImage.getLayers()) {
            if (layer instanceof SmartObjectLayer && layer.getName().equals("sucai1")) {
                SmartObjectLayer smartObjectLayer = (SmartObjectLayer) layer;
                smartObjectLayer.replaceContents(changeFile);
                smartObjectLayer.embedLinked();

                break;
            }
        }

        psdImage.save(exportFile, new PsdOptions());
        psdImage.save(exportImgBefore, new PngOptions());
    }

    try (PsdImage psdImage = (PsdImage) Image.load(exportFile)) {
    {
        psdImage.save(exportImgAfter, new PngOptions());
    }
{{< /highlight >}}

**PSDJAVA-488. Plik PSD nie może być zapisany jako PSD ze względu na wyjątek: Przestrzenie Rgb i Lab nie mogą zawierać mniej niż 3 kanałów i więcej niż 4 kanałów**

{{< highlight java >}}
    String sourceFile = "Ex3_B1H1_Dave_Arthur.psd";
    String exportPath = "export.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        // It takes default saving options from header but header has wrong number of channels.
        try {
            image.save(exportPath);
        } catch (PsdImageException ex) {
            if (ex.getMessage() != "Rgb and Lab modes can not contain less than 3 channels and more than 4 channels") {
                throw new Exception("It is wrong PsdImageException");
            }
        }

        // Without error
        image.save(exportPath, new PsdOptions());
    }
{{< /highlight >}}

**PSDJAVA-489. Centrowanie tekstu jest utracone podczas otwierania warstwy tekstowej w trybie edycji Photoshopa**

{{< highlight java >}}
public static void main(String[] args) throws Exception {
    String sourceFile = "input-test.psd";
    String outputFile = "output.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        IText textData = ((TextLayer) psdImage.getLayers()[2]).getTextData();

        ITextStyle defaultStyle = textData.getItems()[0].getStyle();
        ITextParagraph defaultParagraph = textData.getItems()[0].getParagraph();
        defaultParagraph.setJustification(JustificationMode.Center);
        textData.removePortion(0);

        addTextPortion("Lorem Ipsum", textData, defaultStyle, defaultParagraph);
        addTextPortion("\r", textData, defaultStyle, defaultParagraph);
        addTextPortion(
                "Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.",
                textData,
                defaultStyle,
                defaultParagraph);

        textData.updateLayerData();

        psdImage.save(outputFile);
    } catch (Exception e) {
        e.printStackTrace();
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        // Get justification value from Txt2Resource
        Txt2Resource txt2Resource = (Txt2Resource) psdImage.getGlobalLayerResources()[1];

        String textData = Encoding.getEncoding("Windows-1251").getString(txt2Resource.getData());
        String search = ") /5 << /0 "; // specific character set to find justification value in this file.

        // Find last value of justification mode in text paragraph features
        int index = textData.lastIndexOf(search);
        String lastJustificationResult = textData.substring(index + search.length(), index + search.length() + 1);
        int justificationValue = Integer.parseInt(lastJustificationResult);

        // Check fix of Justification
        if (JustificationMode.Center != justificationValue) {
            throw new Exception("Incorrect Justification value.");
        }
    }
}

static void addTextPortion (String text, IText textData, ITextStyle style, ITextParagraph paragraph)
{
    ITextPortion newPortion = textData.producePortion();
    newPortion.getStyle().apply(style);
    newPortion.getParagraph().apply(paragraph);
    newPortion.setText(text);
    textData.addPortion(newPortion);
}
{{< /highlight >}}

**PSDJAVA-490. Wyjątek z odwołaniem do null podczas zapisywania pliku PSD**

{{< highlight java >}}
    String sourceFile = "test.psd";
    String outputFile = "output.psd";

     try (PsdImage pfile = (PsdImage) Image.load(sourceFile)) {
        TextLayer textLayer = (TextLayer)pfile.getLayers()[1];
        textLayer.updateText("save");

        pfile.save(outputFile);
    } catch (Exception e) {
        e.printStackTrace();
    }
{{< /highlight >}}

**PSDJAVA-485. Dodanie obsługi warstwy tekstowej bez prostokątnych ramek**

{{< highlight java >}}
    String sourceFile = "textNoBounds.psd";
    String outputFile = "output.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        TextLayer noBoundsTextLayer = (TextLayer) psdImage.getLayers()[1];
        TextLayer boundsTextLayer = (TextLayer) psdImage.getLayers()[2];

        boundsTextLayer.setTextBoundBox(RectangleF.getEmpty());
        noBoundsTextLayer.setTextBoundBox(new RectangleF(0, 0, 200, 100));

        TextLayer newTextLayerNoTextBox = psdImage.addTextLayer(
                "New text - no text box",
                new Rectangle(10, 300, 0, 0)
        );

        TextLayer newTextLayerWithTextBox = psdImage.addTextLayer(
                "New text - with text box",
                new Rectangle(10, 400, 400, 100)
        );

        boundsTextLayer.getTextData().updateLayerData();
        noBoundsTextLayer.getTextData().updateLayerData();

        psdImage.save(outputFile);
    } catch (Exception e) {
        e.printStackTrace();
    }
{{< /highlight >}}