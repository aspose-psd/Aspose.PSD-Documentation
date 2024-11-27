---
title: Catatan Rilis Aspose.PSD untuk Java 24.7
type: docs
weight: 40
url: /id/java/aspose-psd-untuk-java-24-7-catatan-rilis/
---

{{% alert color="primary" %}} Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}}

| **Kunci**   | **Ringkasan**                                                                                  | **Kategori** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | Pengecualian "Image loading failed." saat membuka dokumen AI                                    | Bug          |
| PSDJAVA-636 | Teks dirender dengan tidak benar pada file PDF output                                          | Bug          |
| PSDJAVA-637 | Perbaiki ImageSaveException: Ekspor gambar gagal untuk file yang diberikan di Linux            | Bug          |
| PSDJAVA-638 | Perbaiki pemuatan font saat menggunakan Aspose.Drawing                                          | Bug          |
| PSDJAVA-639 | 'Operasi aritmatika menghasilkan overflow' saat membuat layer objek pintar menggunakan JPEG besar | Bug     |
| PSDJAVA-640 | File AI tidak dapat dikonversi menjadi file JPG                                                 | Bug          |

## **Perubahan API Publik**
# **API Ditambahkan:**

- Tidak ada

# **API Dihapus:**

- Tidak ada

## **Contoh Penggunaan:**

**PSDJAVA-635. Pengecualian "Image loading failed." saat membuka dokumen AI**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. Teks dirender dengan tidak benar pada file PDF output**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. Perbaiki ImageSaveException: Ekspor gambar gagal untuk file yang diberikan di Linux**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Bed_Roll-Sticker4_1.psd";
    String outputFile = "src/main/resources/output.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        JpegOptions saveOptions = new JpegOptions();
        saveOptions.setQuality(70);
        psdImage.save(outputFile, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-638. Perbaiki pemuatan font saat menggunakan Aspose.Drawing**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- Sebelum pembaruan. Jumlah font yang diinstal: " + installedFonts.getFamilies().length);
        System.out.println("- Platform: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- Perbarui cache font dengan mencoba mendapatkan nama font Adobe untuk 'Arial': "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- Setelah pembaruan. Jumlah font yang diinstal: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'Operasi aritmatika menghasilkan overflow' saat membuat layer objek pintar menggunakan JPEG besar**

{{< highlight java >}}

    String srcFile = "src/main/resources/source.psd";
    String imageJpg = "src/main/resources/test.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setDataRecoveryMode(DataRecoveryMode.MaximalRecover);
    try (var image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        final FileStream stream = new FileStream(imageJpg, FileMode.Open);
        try {
            var addedLayer = new SmartObjectLayer(stream);
            addedLayer.setName("Test Layer");
            image.addLayer(addedLayer);
        } finally {
            stream.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. File AI tidak dapat dikonversi menjadi file JPG**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}
