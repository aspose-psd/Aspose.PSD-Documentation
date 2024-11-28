---
title: Aspose.PSD voor Java 19.4 - Release-opmerkingen
type: docs
weight: 20
url: /nl/java/aspose-psd-voor-java-19-4-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat de release-opmerkingen voor Aspose.PSD voor Java 19.4.

{{% /alert %}} 

|**Belangrijk**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDJAVA-1|Functie toevoegen om JPEG/PNG/etc. afbeeldingsbestanden naar PsdImage te laden zonder direct laden (wat niet wordt ondersteund in Aspose.PSD)|Functie|
|PSDJAVA-2|Ondersteuning van RGB-kleurmodus met 16bits/kanaal (64 bits per kleur)|Functie|
|PSDJAVA-3|Ondersteuning van Layer Vector Masks en Text Layer Custom FlipRotate|Functie|
|PSDJAVA-4|Alle Aziatische tekens worden niet correct weergegeven|Fout|
|PSDJAVA-5|\r\n-symbolen worden geïnterpreteerd als dubbele regelovergangen, wat fout is|Fout|
|PSDJAVA-6|Als TextLayer wordt bijgewerkt met een string die LineBreaks bevat, wordt het PSD-bestand onleesbaar|Fout|
|PSDJAVA-7|Als TextLayer wordt bijgewerkt met een string die tab-symbolen bevat, mislukt de verwerking met een uitzondering|Fout|
# **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
## **Verwijderde API's:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- ...
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceNonTransparentColors(System.Int32)
- T:Aspose.PSD.FileFormats.Tiff.TiffImage
- ...
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceFrame(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
# **Voorbeelden van gebruik:**

**PSDJAVA-1. Functie toevoegen om JPEG/PNG/etc. afbeeldingsbestanden naar PsdImage te laden zonder direct laden (Wat niet wordt ondersteund in Aspose.PSD)**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-2. Ondersteuning van RGB-kleurmodus met 16bits/kanaal (64 bits per kleur)**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-3. Ondersteuning van Layer Vector Masks en Text Layer Custom FlipRotate**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJava-4. Alle Aziatische tekens worden niet correct weergegeven**

[**Controleer het bijgevoegde voorbeeldbestand**](attachments/92602686/92766213.java)

**PSDJAVA-5. \r\n-symbolen worden geïnterpreteerd als dubbele regelovergangen, wat fout is**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-6. Als TextLayer wordt bijgewerkt met een string die LineBreaks bevat, wordt het PSD-bestand onleesbaar**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-7. Als TextLayer wordt bijgewerkt met een string die tab-symbolen bevat, mislukt de verwerking met een uitzondering**

{{< highlight java >}}
...
{{< /highlight >}}