---
title: Aspose.PSD dla Python via .NET 24.6 - Notatki dotyczące wydania
type: docs
weight: 10
url: /pl/python-net/aspose-psd-dla-python-za-posrednictwem-net-24-6-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla Python via .NET 24.6](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Klucz**     | **Podsumowanie**                                                                                                  | **Kategoria** |
|:--------------|:-------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDPYTHON-69  | Wdrożenie obsługi warstwy mapy gradientu                                                                           | Funkcja       |
| PSDPYTHON-70  | [Format AI] Dodaj obsługę metadanych XPacket do formatu AI (W tym momencie niedostępne dla wersji Python)         | Funkcja       |
| PSDPYTHON-71  | Wdrożenie typów deformacji Inflate, Squeeze i Twist                                                                | Funkcja       |
| PSDPYTHON-72  | Tryby Rgb i Lab nie mogą zawierać mniej niż 3 kanały i więcej niż 4 kanały w pliku z warstwami ArtBoard            | Błąd          |
| PSDPYTHON-79  | Górna część obszaru przetwarzania musi być dodatnia (Parametr 'areaToProcess') podczas przetwarzania określonego pliku| Błąd          |
| PSDPYTHON-74  | Rozszerzone poza obraz płótna jest przycinane po zapisaniu. Dane są tracone, ale podgląd wygląda poprawnie         | Błąd          |

## **Zmiany w interfejsie API publicznego**
# **Dodane interfejsy API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Usunięte interfejsy API:**
- Brak

## **Przykłady użycia:**

**PSDPYTHON-69. Wdrożenie obsługi warstwy mapy gradientu**

{{< highlight python >}}
        sourceFile = "gradient_map_src.psd"
        outputFile = "gradient_map_src_output.psd"
      
        def SprawdzCzyRowne(oczekiwane, rzeczywiste, wiadomosc=None):
            if oczekiwane != rzeczywiste:
                raise Exception(wiadomosc or "Obiekty nie są równe.")

        with PsdImage.load(sourceFile) as obraz:
            im = cast(PsdImage, obraz)
            warstwa = im.add_gradient_map_adjustment_layer()
            warstwa.gradient_settings.reverse = True

            im.save(outputFile)

        with PsdImage.load(outputFile) as obraz:
            im = cast(PsdImage, obraz)
            warstwa_mapy_gradientu = cast(GradientMapLayer, im.layers[1])
            ustawienia_gradientu = cast(GradientFillSettings, warstwa_mapy_gradientu.gradient_settings)

            SprawdzCzyRowne(0.0, ustawienia_gradientu.angle)
            SprawdzCzyRowne(4096, ustawienia_gradientu.interpolation)
            SprawdzCzyRowne(True, ustawienia_gradientu.reverse)
            SprawdzCzyRowne(False, ustawienia_gradientu.align_with_layer)
            SprawdzCzyRowne(False, ustawienia_gradientu.dither)
            SprawdzCzyRowne(GradientType.LINEAR, ustawienia_gradientu.gradient_type)
            SprawdzCzyRowne(100, ustawienia_gradientu.scale)
            SprawdzCzyRowne(0.0, ustawienia_gradientu.horizontal_offset)
            SprawdzCzyRowne(0.0, ustawienia_gradientu.vertical_offset)
            SprawdzCzyRowne("Custom", ustawienia_gradientu.gradient_name)
{{< /highlight >}}

**PSDPYTHON-70. [Format AI] Dodaj obsługę metadanych XPacket do AI Formatu (W tym momencie niedostępne dla wersji Python)**

{{< highlight python >}}
    #     W tym momencie to API nie jest dostępne dla Aspose.PSD dla Python
    #     sourceFile = "ai_one.ai"
    #
    #     def SprawdzCzyRowne(oczekiwane, rzeczywiste):
    #         if oczekiwane != rzeczywiste:
    #             raise Exception("Obiekty nie są równe.")
    #
    #     def SprawdzCzyNieNull(testowy_obiekt):
    #         if testowy_obiekt is None:
    #             raise Exception("Obiekt testowy jest pusty.")
    #
    #     klucz_narzedzia_tworzenia = ":CreatorTool"
    #     klucz_n_stron = "xmpTPg:NPages"
    #     klucz_jednostki = "stDim:unit"
    #     klucz_wysokosci = "stDim:h"
    #     klucz_szerokosci = "stDim:w"
    #
    #     oczekiwane_narzedzie_tworzenia = "Adobe Illustrator CC 22.1 (Windows)"
    #     oczekiwane_n_strony = "1"
    #     oczekiwana_jednostka = "Piksele"
    #     oczekiwana_wysokosc = 768
    #     oczekiwana_szerokosc = 1366
    #
    #     with AiImage.load(sourceFile) as img:
    #         obraz = cast(AiImage, img)
    #
    #         metadane_xmp = obraz.xmp_data
    #        # XmpPacketWrapper a
    #         SprawdzCzyNieNull(metadane_xmp)
    #
    #         podstawowy_pakiet = cast(XmpBasicPackage, metadane_xmp.get_package(Namespaces.XMP_BASIC))
    #         pakiet = metadane_xmp.packages[4]
    #
    #         narzedzie_tworzenia = podstawowy_pakiet.g[klucz_narzedzia_tworzenia].to_string()
    #         n_strony = pakiet[klucz_n_stron]
    #         jednostka = pakiet[klucz_jednostki]
    #         wysokosc = np.double.parse(pakiet[klucz_wysokosci].to_string())
    #         szerokosc = np.double.parse(pakiet[klucz_szerokosci].to_string())
    #
    #         SprawdzCzyRowne(narzedzie_tworzenia, oczekiwane_narzedzie_tworzenia)
    #         SprawdzCzyRowne(n_strony, oczekiwane_n_strony)
    #         SprawdzCzyRowne(jednostka, oczekiwana_jednostka)
    #         SprawdzCzyRowne(wysokosc, oczekiwana_wysokosc)
    #         SprawdzCzyRowne(szerokosc, oczekiwana_szerokosc)

{{< /highlight >}}

**PSDPYTHON-71. Wdrożenie typów deformacji Inflate, Squeeze i Twist**

{{< highlight python >}}
        pliki = ["Twist", "Squeeze", "Squeeze_vert", "Inflate"]

        for prefiks in pliki:
            sourceFile = prefiks + ".psd"
            outputFile = prefiks + "_export.png"

            loadOpt = PsdLoadOptions()
            loadOpt.allow_warp_repaint = True
            loadOpt.load_effects_resource = True

            pngOpt = PngOptions()
            pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
            with PsdImage.load(sourceFile, loadOpt) as obrazPSD:
                obrazPSD.save(outputFile, pngOpt)
{{< /highlight >}}

**PSDPYTHON-72. Tryby Rgb i Lab nie mogą zawierać mniej niż 3 kanały i więcej niż 4 kanały w pliku z warstwami ArtBoard**

{{< highlight python >}}
        sourceFile = "Rgb5Channels.psb"
        outputFile = "Rgb5Channels_output.psd"

        with PsdImage.load(sourceFile) as obraz:
            obraz.save(outputFile)

{{< /highlight >}}

**PSDPYTHON-79. Górna część obszaru przetwarzania musi być dodatnia (Parametr 'areaToProcess') podczas przetwarzania określonego pliku**

{{< highlight python >}}
        sourceFile = "BANNERS_2_Intel-Gamer_psak.psd"
        outputFile = "BANNERS_2_Intel-Gamer_psak_out.psd"
        psdLoadOptions = PsdLoadOptions()
        psdLoadOptions.load_effects_resource = True
        psdLoadOptions.allow_warp_repaint = True

        with PsdImage.load(sourceFile, psdLoadOptions) as obraz:
            obraz.save(outputFile)
{{< /highlight >}}

**PSDPYTHON-74. Rozszerzone poza obrazem płótna jest przycinane po zapisaniu. Dane są tracone, ale podgląd wygląda poprawnie**

{{< highlight python >}}
        sourceFile = "bigfile.psd"
        outputFile = "bigfile_output.psd"
        outputPicture = "bigfile.png"

        loadOptions = PsdLoadOptions()
        loadOptions.load_effects_resource = True
        loadOptions.use_disk_for_load_effects_resource = True

        with PsdImage.load(sourceFile, loadOptions) as obraz:
            obrazPSD = cast(PsdImage, obraz)
            psdOpt = PsdOptions()
            psdOpt.compression_method = CompressionMethod.RLE
            obrazPSD.save(outputFile, psdOpt)


{{< /highlight >}}
