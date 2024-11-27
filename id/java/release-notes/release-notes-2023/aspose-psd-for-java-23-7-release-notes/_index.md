---
title: Catatan Rilis Aspose.PSD untuk Java 23.7
type: docs
weight: 40
url: /id/java/aspose-psd-for-java-23-7-release-notes/
---

{{% alert color="primary" %}} Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **Kunci**   | **Ringkasan**                                                                                             | **Kategori** |
|:------------|:----------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | Menambahkan kemampuan untuk mengekspor setiap lapisan Berkas PSD ke Berkas Gif Animasi                      | Fitur  |
| PSDJAVA-503 | Menetapkan properti Isian dari lapisan Bentuk dari sumber vscg                                             | Fitur  |
| PSDJAVA-504 | Menambahkan tipe warp baru (busur & lengkung)                                                              | Fitur  |
| PSDJAVA-505 | Mengubah aplikasi yang menyimpan Berkas PSD menjadi Aspose.PSD jika properti UpdateMetadata diatur ke benar | Fitur  |
| PSDJAVA-510 | Meningkatkan area perhitungan dari gambar warp                                                             | Fitur  |
| PSDJAVA-511 | Proses Lapisan Penyesuaian Hitam dan Putih semi-transparan salah                                           | Bug    |
| PSDJAVA-512 | SmartObject ReplaceContents (saat opsi AllowWarpRepaint aktif) gagal setelah 2 menit menghitung             | Bug    |
| PSDJAVA-513 | Menambahkan kemampuan untuk mendapatkan posisi Kiri dan Atas LayerGroup yang sebenarnya                     | Bug    |
| PSDJAVA-514 | Pengubah ukuran lapisan bekerja salah ketika berkas psd memiliki VogkResource dengan struktur dalam titik  | Bug    |
| PSDJAVA-515 | TextBound tidak berfungsi seperti yang diharapkan                                                         | Bug    |
| PSDJAVA-516 | Menambahkan lapisan yang dibuat dengan konstruktor default ke gambar PSD tidak menambahkan sumber daya default kepadanya | Bug    |
| PSDJAVA-517 | Timeline.LoopesCount diabaikan saat mengekspor ke GIF animasi                                             | Bug    |

## **Perubahan API Publik**
# **API Ditambahkan:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **API Dihapus:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **Contoh Penggunaan:**

**PSDJAVA-502. Menambahkan kemampuan untuk Mengekspor Setiap Layer Berkas PSD ke Berkas Gif Animasi**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // Buat bingkai untuk setiap lapisan.
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

        // Perbarui keadaan saat ini
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}} 

**PSDJAVA-503. Menetapkan Properti Isian dari Lapisan Bentuk dari Sumber Vscg**

{{< highlight java >}}
        // Contoh pengisian solid
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

            // Periksa perubahan yang disimpan
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
            assertAreEqual(expected, actual, "Objects are not equal.");
        }
		
		//Gradient fill example:

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

    // Check saved changes
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
        GradientFillSettings fillSettings = (GradientFillSettings) shapeLayer.getFill();

        assertAreEqual(true, fillSettings.getDither());
        assertAreEqual(true, fillSettings.getReverse());
        assertAreEqual(false, fillSettings.getAlignWithLayer());
        assertAreEqual((double) 20, fillSettings.getAngle());
        assertAreEqual(50, fillSettings.getScale());
        assertAreEqual(100, fillSettings.getColorPoints()[0].getLocation());
        assertAreEqual(4000, fillSettings.getColorPoints()[1].getLocation());
        assertAreEqual(200, fillSettings.getTransparencyPoints()[0].getLocation());
        assertAreEqual(3800, fillSettings.getTransparencyPoints()[1].getLocation());
        assertAreEqual((double) 90, fillSettings.getTransparencyPoints()[0].getOpacity());
        assertAreEqual((double) 10, fillSettings.getTransparencyPoints()[1].getOpacity());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Objects are not equal.");
}

{{< /highlight >}}

**PSDJAVA-504. Menambahkan tipe warp baru (busur & lengkung)**

{{< highlight java >}}
    String sourceArcFile = "src/main/resources/arc_warp.psd";
    String outputArcFile = "src/main/resources/arc_export.png";

    String sourceArchFile = "src/main/resources/arch_warp.psd";
    String outputArchFile = "src/main/resources/arch_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceArcFile, psdLoadOptions)) {
        psdImage.save(outputArcFile, pngOptions);
    }


    try (PsdImage psdImage = (PsdImage) Image.load(sourceArchFile, psdLoadOptions)) {
        psdImage.save(outputArchFile, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-505. Mengubah aplikasi yang menyimpan Berkas PSD menjadi Aspose.PSD jika properti UpdateMetadata diatur ke benar**

{{< highlight java >}}
    String path = "src/main/resources/output.psd";
    try (PsdImage image = new PsdImage(100, 100)) {
        // Jika Anda ingin mengubah alat pembuat, pastikan properti "UpdateMetadata" diatur ke benar. Properti ini secara default diatur ke benar.
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setUpdateMetadata(true