---
title: עטי Aspose.PSD עבור Java 23.4 - הופק תיאורי גרסה
type: מסמכים
weight: 40
url: /he/java/aspose-psd-for-java-23-4-release-notes/
---

{{% alert color="primary" %}} דף זה מכיל תיאורי גרסה עבור [Aspose.PSD עבור Java 23.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.4/) {{% /alert %}}

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDJAVA-446|העברת פונקציונליות שנאבדה מ- Aspose.PSD עבור .Net אל Aspose.PSD עבור Java|שיפור|
|PSDJAVA-441|עיצוב מחלקת RawColor עבור ה- API הציבורי לשימוש ב- PSD API במקום מבנה Color מיושן|שיפור|
|PSDJAVA-418|אינטגרציה של רישיון Modern Aspose ל- Aspose.PSD|שיפור|
|PSDJAVA-445|היעבור עובי בעריכה ב- Photoshop|באג|
|PSDJAVA-443|עריכת טקסט באמצעות חלקי טקסט לא שומרת את התוצאה הנכונה|באג|
|PSDJAVA-444|התחלה וסיום הסגנונות או הפסקות מוצגים במקום לא נכון בעריכת שכבת טקסט על ידי ITextPortion|באג|

# **שינויים ב- API הציבורי**
# **APIs שנוספו:**
- M:com.aspose.psd.FontSettings.getFontReplacements(java.lang.String)
- M:com.aspose.psd.FontSettings.getReplacementFont(java.lang.String)
- M:com.aspose.psd.FontSettings.setAllowedFonts(java.lang.String[])
- M:com.aspose.psd.FontSettings.setFontReplacements(java.lang.String,java.lang.String[])
- M:com.aspose.psd.FontSettings.isFontAllowed(java.lang.String)
- M:com.aspose.psd.License.setLicense(java.io.File)
- M:com.aspose.psd.License.getRenewSubscriptionStartMessage
- M:com.aspose.psd.License.getErrorCodeMessages
- M:com.aspose.psd.License.removeLicense
- T:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.#ctor(int,int,com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getFilterEffectMasks
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.save(com.aspose.psd.StreamContainer,int)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.FEidTypeToolKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.FXidTypeToolKey
- T:com.aspose.psd.fileformats.psd.resources.AnimatedDataSectionResource
- M:com.aspose.psd.fileformats.psd.resources.AnimatedDataSectionResource.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.AnimatedDataSectionResource.getMinimalVersion
- M:com.aspose.psd.fileformats.psd.resources.AnimatedDataSectionResource.getKeyName
- M:com.aspose.psd.fileformats.psd.resources.AnimatedDataSectionResource.getAnimatedDataSection

...

**PSDJAVA-445|העברת עיצוב בעת עריכה בפוטושופ**
{{< highlight java >}}
public class Main {
    public static void main(String[] args) throws Exception {
        String strings1 = Directory.getCurrentDirectory() + "/input-lsaks-strings1-forTicket.txt";
        String psdInput = Directory.getCurrentDirectory() + "/input_for_ticket.psd";

        PsdImage image = (PsdImage) Image.load(psdInput);
        List<String> linesLsaks = Files.readAllLines(Paths.get(strings1));
        Map<String, String> lsaksDictionary = linesLsaks.stream()
                .filter(line -> line != null && !line.trim().isEmpty())
                .map(line -> line.split("="))
                .collect(Collectors.toMap(
                        items -> items[0].trim(),
                        items -> items[1].trim(),
                        (oldValue, newValue) -> newValue));

        // Step: Replace text
        for (Layer layerItem : image.getLayers()) {
            if (!(layerItem instanceof TextLayer)) {
                continue;
            }
            TextLayer layerToExtractText = (TextLayer) layerItem;
            Pattern p = Pattern.compile("#lsak[^#]+#", Pattern.CASE_INSENSITIVE);
            Matcher m = p.matcher(layerToExtractText.getText());

            if (!m.find()) {
                continue;
            }

            String resultLsakValue = m.group().trim();
            if (resultLsakValue.isEmpty()) {
                continue;
            }

            replaceLsakText(layerToExtractText.getTextData(), lsaksDictionary); // replaceLsakText needs to be defined
        }
        // Step: Format and Center
        for (Layer layerItem : image.getLayers()) {
            if (!(layerItem instanceof TextLayer)) {
                continue;
            }
            TextLayer layerToExtractText = (TextLayer) layerItem;

            formatStyleText(layerToExtractText.getTextData(), lsaksDictionary); // formatStyleText needs to be defined
        }

        image.save("c:\\output.psd");
        image.dispose();
    }

    public static String replaceText(String lsak, Map<String, String> lsaksToReplace) {
        StringBuilder sb = new StringBuilder(lsak.trim());
        for (Map.Entry<String, String> kvp : lsaksToReplace.entrySet()) {
            int index;
            while ((index = sb.indexOf(kvp.getKey())) != -1) {
                sb.replace(index, index + kvp.getKey().length(), kvp.getValue());
            }
        }
        int index;
        while ((index = sb.indexOf("\r")) != -1) {
            sb.deleteCharAt(index);
        }
        while ((index = sb.indexOf("#")) != -1) {
            sb.deleteCharAt(index);
        }
        return sb.toString();
    }

    private static void replaceLsakText(IText textData, Map<String, String> lsaksDictionary) {
        int countPortions = textData.getItems().length;
        ITextStyle defaultStyle = textData.getItems()[0].getStyle();
        ITextParagraph defaultParagraph = textData.getItems()[0].getParagraph();
        String textToReplace = textData.getText();

        // remove old portions
        for (int i = 0; i < countPortions; i++) {
            textData.removePortion(0);
        }

        ITextPortion newPortion = textData.producePortion();
        newPortion.getParagraph().apply(defaultParagraph);
        newPortion.getStyle().apply(defaultStyle);
        newPortion.setText(replaceText(textToReplace, lsaksDictionary));
        textData.addPortion(newPortion);
        textData.updateLayerData();
    }

    static void formatStyleText(IText textData, Map<String, String> lsaksToReplace) {
        // validate if there are tags
        Pattern tagPattern = Pattern.compile("<[^>]+>");
        Matcher tagMatcher = tagPattern.matcher(textData.getText());
        boolean hasTags = tagMatcher.find();

        int countPortions = textData.getItems().length;
        ITextStyle defaultStyle = textData.getItems()[0].getStyle();
        ITextParagraph defaultParagraph = textData.getItems()[0].getParagraph();

        if (hasTags) {
            String tagRegex1 = "[^<>]+|<\\s*([^ >]+)[^>]*>.*?<\\s*/\\s*\\1\\s*>";
            Matcher matchesImgSrc = Pattern.compile(tagRegex1, Pattern.CASE_INSENSITIVE | Pattern.DOTALL).matcher(textData.getText());

            List<String> listlsaks = new ArrayList<>();
            while (matchesImgSrc.find()) {
                listlsaks.add(matchesImgSrc.group());
            }

            String[] textSplit = listlsaks.toArray(new String[0]);

            for (int i = 0; i < countPortions; i++) {
                textData.removePortion(0);
            }

            for (String s : textSplit) {
                ITextPortion newPortion = textData.producePortion();
                newPortion.getParagraph().apply(defaultParagraph);
                newPortion.getStyle().apply(defaultStyle);

                if (s.contains("font:")) {
                    newPortion.getStyle().setFontName(s);
                }
                if (s.contains("pt")) {
                    newPortion.getStyle().setFontSize(Double.parseDouble(s));
                }
                if (s.contains("color:")) {
                    newPortion.getStyle().setFillColor(Color.fromName(s));
                }
                if (s.contains("br/")) {
                    s = "\r";
                }

                newPortion.setText(s.replaceAll("<.*?>", ""));
                textData.addPortion(newPortion);
            }

            textData.updateLayerData();
        }
    }
}
{{< /highlight >}}**PSDJAVA-443|עריכת טקסט באמצעות חלקי טקסט לא שומרת את התוצאה הנכונה**

{{< highlight java >}}
  public static void main(String[] args) {
    String sourceFilePSDEmail = Directory.getCurrentDirectory() + "/files-input/inputv5.psd";
    PsdImage imageTestEmail = (PsdImage) Image.load(sourceFilePSDEmail);
    var layers = imageTestEmail.getLayers();

    List<Layer> layersOnlyTextLayers = Arrays.stream(imageTestEmail.getLayers())
            .filter(layer -> layer instanceof TextLayer)
            .toList();

    for (Layer layerItem : layers) {
        boolean isTextLayer = layerItem instanceof TextLayer;

        if (isTextLayer) {
            var layerTLToUpdateText = (TextLayer) layerItem;

            //Search for lsak text
            if (layerTLToUpdateText.getText().contains("lsak")) {
                var textDataTL = layerTLToUpdateText.getTextData();

                if (textDataTL.getText().contains("lsak") && textDataTL.getText().contains("\r")) {
                    //Replace text
                    replaceLsakText(textDataTL);
                    //Format text
                    formatStyleText(textDataTL);
                }
            }
        }
    }

    String outputFile = Directory.getCurrentDirectory() + "TestEmailFifthMethod" + ".psd";
    imageTestEmail.save(outputFile);
}
{{< /highlight >}}

**PSDJAVA-444|התחלה וסיום הסגנונות או הפסקות מוצגים במקום לא נכון בעריכת שכבת טקסט על ידי ITextPortion**

{{< highlight java >}}
    public static void main(String[] args) throws Exception {
        String sourceFilePSDEmail = Directory.getCurrentDirectory() + "/inputv2.psd";
        String outputFile = Directory.getCurrentDirectory() + "/export.psd";

        PsdImage imageTestEmail = (PsdImage) Image.load(sourceFilePSDEmail);

        Layer[] layers = imageTestEmail.getLayers();

        for (Layer layerItem : layers) {
            boolean isTextLayer = layerItem instanceof TextLayer;

            if (isTextLayer) {
                var layerTLToUpdateText = (TextLayer) layerItem;

                //Search for lsak text
                if (layerTLToUpdateText.getText().contains("lsak")) {

                    var textDataTL = layerTLToUpdateText.getTextData();

                    if (textDataTL.getText().contains("lsak")) {

                        //Step: Replace text
                        replaceLsakFourthMethod(textDataTL);

                        System.out.println("Replaced text " + textDataTL.getText());

                        //Step: Format text
                        formatLsakFourthMethod(textDataTL);

                        System.out.println("Formatted text " + textDataTL.getText());

                        //Step: Center textlayer
                        if (layerTLToUpdateText.getDisplayName().equals("cc")
                                || layerTLToUpdateText.getDisplayName().equals("tl")
                                || layerTLToUpdateText.getDisplayName().equals("cl")) {

                            //old Values
                            var boundBoxOld = layerTLToUpdateText.getTextBoundBox();

                            var wordSizeOld = layerTLToUpdateText.getSize();

                            var OldY = layerTLToUpdateText.getTop();

                            textDataTL.updateLayerData();

                            // new values
                            var wordSize = layerTLToUpdateText.getSize();

                            var boundBox = layerTLToUpdateText.getTextBoundBox();

                            var newSize = new Size((int) Math.ceil(boundBoxOld.getWidth()), wordSize.getHeight());

                            var beforePoint = centerInRectangle(wordSize, new RectangleF(layerTLToUpdateText.getLeft(),
                                    layerTLToUpdateText.getTop(), layerTLToUpdateText.getWidth(), boundBoxOld.getHeight()));

                            layerTLToUpdateText.setTextBoundBox(
                                    new RectangleF(new PointF(0, beforePoint.getY() - OldY), Size.to_SizeF(newSize)));

...

                            textDataTL.updateLayerData();

                            System.out.println("Center text");
                        }
                    }
                }
            }
        }

        imageTestEmail.save(outputFile);
    }

    static PointF centerInRectangle(Size inner, RectangleF outer) {
        PointF pointF = new PointF();
        pointF.setX(outer.getX() + (outer.getWidth() - inner.getWidth()) / 2);
        pointF.setY(outer.getY() + (outer.getHeight() - inner.getHeight()) / 2);

        return pointF;
    }
{{< /highlight >}}