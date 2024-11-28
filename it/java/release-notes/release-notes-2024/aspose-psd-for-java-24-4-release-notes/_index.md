---
title: Note sulla versione di Aspose.PSD per Java 24.4
type: docs
weight: 40
url: /it/java/aspose-psd-per-java-24-4-note-sulla-versione/
---

{{% alert color="primary" %}} Questa pagina contiene le note sulla versione di [Aspose.PSD per Java 24.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.4/) {{% /alert %}}

| **Chiave**  | **Sommario**                                                                                           | **Categoria** |
|:------------|:------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-610 | Impostare la licenza per Aspose.PSD per Java porta a un'eccezione se fatta più di una volta            | Bug          |
| PSDJAVA-611 | [Formato AI] Aggiunta gestione risorsa XObjectForm                                                     | Funzionalità |
| PSDJAVA-612 | Aggiungi costruttore per ShapeLayer                                                                    | Funzionalità |
| PSDJAVA-613 | Risolvere la conversione del file Psd da RGB a CMYK                                                    | Bug          |
| PSDJAVA-614 | Specifico file PSD non può essere esportato utilizzando Aspose.PSD                                     | Bug          |

## **Modifiche all'API pubblica**
# **API Aggiunte:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addShapeLayer

# **API Rimosse:**

- Nessuna

## **Esempi d'uso:**

**PSDJAVA-610. Impostare la licenza per Aspose.PSD per Java porta a un'eccezione se fatta più di una volta**

{{< highlight java >}}

        License license = new License();
        String liccorrectJava = "Aspose.PSD.Java.lic";

        license.setLicense(liccorrectJava);
        license.setLicense(liccorrectJava);

{{< /highlight >}}

**PSDJAVA-611. [Formato AI] Aggiunta gestione risorsa XObjectForm**

{{< highlight java >}}

        String fileSorgente = "src/main/resources/esempio.ai";
        String percorsoOutput = "src/main/resources/esempio.png";

        try (AiImage immagine = (AiImage) Image.load(fileSorgente)) {
            immagine.save(percorsoOutput, new PngOptions());
        }

{{< /highlight >}}

**PSDJAVA-612. Aggiungi costruttore per ShapeLayer**

{{< highlight java >}}

    private static final int RAPPORTO_IMMAGINE_PSD = 256 * 65535;

    public static void main(String[] args) {
        String fileDiOutput = "src/main/resources/OutputAggiungiShapeLayer.psd";

        try (PsdImage nuovoPsd = new PsdImage(600, 400)) {
            ShapeLayer layer = nuovoPsd.addShapeLayer();

            PathShape nuovaForma = generaNuovaForma(nuovoPsd.getSize());
            List<IPathShape> nuoveForme = new List<>();
            nuoveForme.add(nuovaForma);
            layer.getPath().setItems(nuoveForme.toArray(new IPathShape[0]));

            layer.update();

            nuovoPsd.save(fileDiOutput);
        }

        try (PsdImage immagine = (PsdImage) Image.load(fileDiOutput)) {
            assertAreEqual(2, immagine.getLayers().length);

            ShapeLayer shapeLayer = (ShapeLayer) immagine.getLayers()[1];
            ColorFillSettings riempimentoInterno = (ColorFillSettings) shapeLayer.getFill();
            IStrokeSettings impostazioniStroke = shapeLayer.getStroke();
            ColorFillSettings riempimentoStroke = (ColorFillSettings) strokeSettings.getFill();

            assertAreEqual(1, shapeLayer.getPath().getItems().length); // 1 Forma
            assertAreEqual(3, shapeLayer.getPath().getItems()[0].getItems().length); // 3 nodi in una forma

            assertAreEqual(-16127182, riempimentoInterno.getColor().toArgb()); // ff09eb32

            assertAreEqual(7.41, impostazioniStroke.getSize());
            assertAreEqual(false, impostazioniStroke.getEnabled());
            assertAreEqual(StrokePosition.Center, impostazioniStroke.getLineAlignment());
            assertAreEqual(LineCapType.ButtCap, impostazioniStroke.getLineCap());
            assertAreEqual(LineJoinType.MiterJoin, impostazioniStroke.getLineJoin());
            assertAreEqual(-16777216, riempimentoStroke.getColor().toArgb()); // ff000000
        }
    }

    static PathShape generaNuovaForma(Size dimensioneImmagine) {
        PathShape nuovaForma = new PathShape();

        PointF punto1 = new PointF(20, 100);
        PointF punto2 = new PointF(200, 100);
        PointF punto3 = new PointF(300, 10);

        BezierKnotRecord primoBezierKnotRecord = new BezierKnotRecord();
        primoBezierKnotRecord.setLinked(true);
        primoBezierKnotRecord.setPoints(new Point[]{
                puntoFToResourcePoint(punto1, dimensioneImmagine),
                puntoFToResourcePoint(punto1, dimensioneImmagine),
                puntoFToResourcePoint(punto1, dimensioneImmagine)
        });

        BezierKnotRecord secondoBezierKnotRecord = new BezierKnotRecord();
        secondoBezierKnotRecord.setLinked(true);
        secondoBezierKnotRecord.setPoints(new Point[]{
                puntoFToResourcePoint(punto2, dimensioneImmagine),
                puntoFToResourcePoint(punto2, dimensioneImmagine),
                puntoFToResourcePoint(punto2, dimensioneImmagine)
        });

        BezierKnotRecord terzoBezierKnotRecord = new BezierKnotRecord();
        terzoBezierKnotRecord.setLinked(true);
        terzoBezierKnotRecord.setPoints(new Point[]{
                puntoFToResourcePoint(punto3, dimensioneImmagine),
                puntoFToResourcePoint(punto3, dimensioneImmagine),
                puntoFToResourcePoint(punto3, dimensioneImmagine)
        });

        BezierKnotRecord[] nodiBezier = new BezierKnotRecord[]{
                primoBezierKnotRecord,
                secondoBezierKnotRecord,
                terzoBezierKnotRecord
        };

        nuovaForma.setItems(nodiBezier);

        return nuovaForma;
    }

    static Point puntoFToResourcePoint(PointF punto, Size dimensioneImmagine) {
        return new Point(
                Math.round(punto.getY() * (RAPPORTO_IMMAGINE_PSD / dimensioneImmagine.getHeight())),
                Math.round(punto.getX() * (RAPPORTO_IMMAGINE_PSD / dimensioneImmagine.getWidth())));
    }

    static void assertAreEqual(Object atteso, Object effettivo) {
        assertAreEqual(atteso, effettivo, "Gli oggetti non sono uguali.");
    }

    static void assertAreEqual(Object atteso, Object effettivo, String messaggio) {
        if (!atteso.equals(effettivo)) {
            throw new IllegalArgumentException(messaggio);
        }
    }

{{< /highlight >}}

**PSDJAVA-613. Risolvere la conversione del file Psd da RGB a CMYK**

{{< highlight java >}}

    public static void main(String[] args) {
        // Verifica che il file psd convertito in CMYK + RLE con 4 canali dal file psd in RGB + RLE con 4 canali, abbia realmente 4 canali
        // e HasTransparencyData == false.
        String fileSorgente = "src/main/resources/rana_nosimb.psd";
        String fileDiOutput = "src/main/resources/rana_nosimb_output.psd";

        try (PsdImage psdImage = (PsdImage) Image.load(fileSorgente)) {
            psdImage.setTransparencyData(false);

            PsdOptions psdOptions = new PsdOptions(psdImage);
            psdOptions.setColorMode(ColorModes.Cmyk);
            psdOptions.setCompressionMethod(CompressionMethod.RLE);
            psdOptions.setChannelsCount((short) 4);

            psdImage.save(fileDiOutput, psdOptions);
        }

        try (PsdImage psdImage = (PsdImage) Image.load(fileDiOutput)) {
            assertAreEqual(false, psdImage.hasTransparencyData());
            assertAreEqual(4, psdImage.getLayers()[0].getChannelsCount());
        }
    }

    static void assertAreEqual(Object atteso, Object effettivo) {
        assertAreEqual(atteso, effettivo, "Gli oggetti non sono uguali.");
    }

    static void assertAreEqual(Object atteso, Object effettivo, String messaggio) {
        if (!atteso.equals(effettivo)) {
            throw new IllegalArgumentException(messaggio);
        }
    }

{{< /highlight >}}

**PSDJAVA-614. Un file PSD specifico non può essere esportato utilizzando Aspose.PSD**

{{< highlight java >}}

        String fileSorgente = "src/main/resources/1966origine.psd";
        String outputPng = "src/main/resources/output.png";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setLoadEffectsResource(true);

        try (PsdImage psdImage = (PsdImage) Image.load(fileSorgente, psdLoadOptions)) {
            psdImage.save(outputPng, new PngOptions());
        }

{{< /highlight >}}
