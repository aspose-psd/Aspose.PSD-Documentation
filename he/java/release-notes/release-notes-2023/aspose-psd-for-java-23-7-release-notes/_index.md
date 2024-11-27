---
title: גרסאות שחרור של Aspose.PSD ל-Java 23.7
type: docs
weight: 40
url: /he/java/aspose-psd-for-java-23-7-release-notes/
---

{{% alert color="primary" %}} דף זה מכיל את גרסאות השחרור של [Aspose.PSD ל-Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **מפתח**   | **סיכום**                                                                                                                                      | **קטגוריה** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | הוספת אפשרות לייצוא כל שכבת קובץ PSD לקובץ Animated Gif                                        | יכולת |
| PSDJAVA-503 | הקצאת מאפיין מילוי שכבת צורה ממשאב vscg                                                        | יכולת |
| PSDJAVA-504 | הוספת סוגי קשירה חדשים (קשירה עגולה וקשירה שולייתית)                                         | יכולת |
| PSDJAVA-505 | שינוי היישום השמור את קובץ ה-PSD ל-Aspose.PSD אם נקבע מאפיין UpdateMetadata ל-true              | יכולת |
| PSDJAVA-510 | הגדלת אזור החישוב של תמונת הכוונת האזור                                                        | יכולת |
| PSDJAVA-511 | תהליך הכיוון שחור ולבן לתיקון שקיפות חצאית מעביר טוב לא נכון                                     | באג |
| PSDJAVA-512 | החלפת התוכן של SmartObject (כאשר האפשרויות AllowWarpRepaint פעילות) נכשלות לאחר 2 דקות של חישוב | באג |
| PSDJAVA-513 | הוספת אפשרות לקבל את המיקום האמיתי של שכבת למעלה ושמאל                                        | באג |
| PSDJAVA-514 | שינוי גודל השכבה עובר תהליך לא נכון כאשר הקובץ PSD מכיל VogkResource עם מבנים בנקודות         | באג |
| PSDJAVA-515 | TextBound לא עובד כמצופה                                                                     | באג |
| PSDJAVA-516 | הוספת שכבה שנוצרה עם בנאי ברירת מחדל לתמונת PSD לא מוסיפה משאבים ברירת מחדל אליה         | באג |
| PSDJAVA-517 | Timeline.LoopesCount מתעלם בעת ייצוא ל-GIF מופעת                                             | באג |

## **שינויים ב-API הציבורי**
# **APIs שנוספו:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **APIs שהוסרו:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **דוגמאות לשימוש:**

**PSDJAVA-502. הוספת אפשרות לייצוא כל שכבת קובץ PSD לקובץ Animated Gif**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // יצירת מסגרות עבור כל שכבה.
        int framesCount = psdImage.getLayers().length;
        Timeline timeline = psdImage.getTimeline();

        Frame[] frames = new Frame[framesCount];
        for (int i = 0; i < framesCount; i++) {
            frames[i] = new Frame();
            LayerState[] layerStates = new LayerState[framesCount];

            for (int j = 0; j < framesCount; j++) {
                layerStates[j] = new LayerState();
                layerStates[j].setEnabled(i == j);
            }

            frames[i].setLayerStates(layerStates);
        }

        timeline.setFrames(frames);

        // עדכון מצבים נוכחיים
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

**PSDJAVA-503. הקצאת מאפיין מילוי שכבת צורה ממשאב vscg**

{{< highlight java >}}
        // התמלאות אחידה דוגמה
        public static void main(String[] args) {
            String srcFile = "src/main/resources/ShapeInternalSolid.psd";
            String outFile = "src/main/resources/ShapeInternalSolid.psd.out.psd";

            PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
            psdLoadOptions.setLoadEffectsResource(true);

            try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
                 ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
                  ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();
                 fillSettings.setColor(Color.getRed());

                 shapeLayer.update();

                 image.save(outFile);
            }

            // בדיקת שינויים שנשמרו
            try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();

            assertAreEqual(Color.getRed(), fillSettings.getColor());

            image.save(outFile);
        }

        static void assertAreEqual(Object expected, Object actual, String message) {
            if (!expected.equals(actual)) {
                throw new IllegalArgumentException(message);
            }
        }

        static void assertAreEqual(Object expected, Object actual) {
            assertAreEqual(expected, actual, "האוביקטים אינם שקולים.");
        }
		
		// דוגמה למילוי גרידיאנט

	public static void main(String[] args) {
    String srcFile = "src/main/resources/ShapeInternalGradient.psd";
    String outFile = "src/main/resources/ShapeInternalGradient.psd.out.psd";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
        GradientFillSettings fillSettings = (GradientFillSettings) shapeLayer.getFill();
        fillSettings.setDither(true);
        fillSettings.setReverse(true);
        fillSettings.setAlignWithLayer(false);
        fillSettings.setAngle(20);
        fillSettings.setScale(50);
        fillSettings.getColorPoints()[0].setLocation(100);
        fillSettings.getColorPoints()[1].setLocation(4000);
        fillSettings.getTransparencyPoints()[0].setLocation(200);
        fillSettings.getTransparencyPoints()[1].setLocation(3800);
        fillSettings.getTransparencyPoints()[0].setOpacity(90);
        fillSettings.getTransparencyPoints()[1].setOpacity(10);

        shapeLayer.update();

        image.save(outFile);
    }

    // בדיקת שינויים שנשמרו
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
        GradientFillSettings fillSettings = (GradientFillSettings) shapeLayer.get