---
title: Notatki wydania Aspose.PSD dla Python via .NET 24.4
type: docs
weight: 10
url: /pl/python-net/aspose-psd-dla-pythona-za-posrednictwem-net-24-4-notatki-o-wydaniu/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD dla Python via .NET 24.4](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Klucz**      | **Podsumowanie**                                                          | **Kategoria**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-50 | [Format AI] Dodanie obsługi zasobów XObjectForm                        | Funkcja     |
| PSDPYTHON-51 | Dodanie konstruktora dla warstwy kształtu                               | Funkcja     |
| PSDPYTHON-52 | Naprawa konwersji pliku PSD z RGB na CMYK                               | Błąd         |
| PSDPYTHON-53 | Określony plik PSD nie może być eksportowany za pomocą Aspose.PSD       | Błąd         |



## **Zmiany w API publicznym**
# **Dodane API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **Usunięte API:**
- Brak


## **Przykłady użycia:**

**PSDPYTHON-50. [Format AI] Dodanie obsługi zasobów XObjectForm**

{{< highlight python >}}
        nazwaPlikuŹródłowego = "przykład.ai"
        ścieżkaWyjściowa = "przykład_wyjście.png"

        with AiImage.load(nazwaPlikuŹródłowego) as obraz:
            obraz.save(ścieżkaWyjściowa, PngOptions())
{{< /highlight >}}

**PSDPYTHON-51. Dodanie konstruktora dla warstwy kształtu**

{{< highlight python >}}
     def sprawdź KonstruktorWarstwyKształtu():
        plikWyjściowy = "DodajWarstwęKształtu_wyjście.psd"

        with PsdImage(600, 400) as nowyPsd:
            warstwaKształtu = nowyPsd.add_shape_layer()

            nowyKształt = generuj_nowy_kształt(nowyPsd.size)
            noweKształty = [nowyKształt]
            warstwaKształtu.path.set_items(noweKształty)

            warstwaKształtu.update()

            nowyPsd.save(plikWyjściowy)

        with PsdImage.load(plikWyjściowy) as obraz:
            obrazek = cast(PsdImage, obraz)
            assert len(obrazek.layers) == 2

            warstwaKształtu = cast(ShapeLayer, obrazek.layers[1])
            wewnętrzneWypełnienie = warstwaKształtu.fill
            ustawieniaKonturu = warstwaKształtu.stroke
            wypełnienieKonturu = warstwaKształtu.stroke.fill

            assert len(warstwaKształtu.path.get_items()) == 1
            assert len(warstwaKształtu.path.get_items()[0].get_items()) == 3

            assert wewnętrzneWypełnienie.color.to_argb() == -16127182

            assert ustawieniaKonturu.size == 7.41
            assert not ustawieniaKonturu.enabled
            assert ustawieniaKonturu.line_alignment == StrokePosition.CENTER
            assert ustawieniaKonturu.line_cap == LineCapType.BUTT_CAP
            assert ustawieniaKonturu.line_join == LineJoinType.MITER_JOIN
            assert wypełnienieKonturu.color.to_argb() == -16777216
			
    def generuj_nowy_kształt(rozmiarObrazu):
        nowyKształt = PathShape()

        punkt1 = PointF(20, 100)
        punkt2 = PointF(200, 100)
        punkt3 = PointF(300, 10)

        węzeł1 = BezierKnotRecord()
        węzeł1.is_linked = True
        węzeł1.points = [
                    PointFNaPunktZasobu(punkt1, rozmiarObrazu),
                    PointFNaPunktZasobu(punkt1, rozmiarObrazu),
                    PointFNaPunktZasobu(punkt1, rozmiarObrazu)
                ]

        węzeł2 = BezierKnotRecord()
        węzeł2.is_linked = True
        węzeł2.points = [
                    PointFNaPunktZasobu(punkt2, rozmiarObrazu),
                    PointFNaPunktZasobu(punkt2, rozmiarObrazu),
                    PointFNaPunktZasobu(punkt2, rozmiarObrazu)
                ]

        węzeł3 = BezierKnotRecord()
        węzeł3.is_linked = True
        węzeł3.points = [
                    PointFNaPunktZasobu(punkt3, rozmiarObrazu),
                    PointFNaPunktZasobu(punkt3, rozmiarObrazu),
                    PointFNaPunktZasobu(punkt3, rozmiarObrazu)
                ]

        węzłyBeziere = [
            węzeł1,
            węzeł2,
            węzeł3
        ]

        nowyKształt.set_items(węzłyBeziere)

        return nowyKształt
		
    def PointFNaPunktZasobu(punkt, rozmiarObrazu):
        StosunekImgDoPsd = 256 * 65535
        return Point(
            int(round(punkt.y * (StosunekImgDoPsd / rozmiarObrazu.height))),
            int(round(punkt.x * (StosunekImgDoPsd / rozmiarObrazu.width)))
        )

    def sprawdź_czy_równe(oczekiwany, rzeczywisty, komunikat=None):
        if oczekiwany != rzeczywisty:
            raise Exception(komunikat or "Obiekty nie są równe.")
			
{{< /highlight >}}

**PSDPYTHON-52. Naprawa konwersji pliku PSD z RGB na CMYK**

{{< highlight python >}}
     def sprawdźKonwersjęZRgbNaCmyk():
        plikŹródłowy = "frog_nosymb.psd"
        plikWyjściowy = "frog_nosymb_wyjście.psd"

        with PsdImage.load(plikŹródłowy) as obraz:
            psdObraz = cast(PsdImage, obraz)
            psdObraz.has_transparency_data = False

            opcjePsd = PsdOptions(psdObraz)
            opcjePsd.color_mode = ColorModes.CMYK
            opcjePsd.compression_method = CompressionMethod.RLE
            opcjePsd.channels_count = 4

            psdObraz.save(plikWyjściowy, opcjePsd)

        with PsdImage.load(plikWyjściowy) as obraz:
            psdObraz = cast(PsdImage, obraz)
            assert not psdObraz.has_transparency_data
            assert psdObraz.layers[0].channels_count == 4

        def sprawdź_czy_równe(oczekiwany, rzeczywisty, komunikat=None):
            if oczekiwany != rzeczywisty:
                raise Exception(komunikat or "Obiekty nie są równe.")	

    def sprawdź_czy_równe(oczekiwany, rzeczywisty, komunikat=None):
        if oczekiwany != rzeczywisty:
            raise Exception(komunikat or "Obiekty nie są równe.")
				
{{< /highlight >}}

**PSDPYTHON-53. Określony plik PSD nie może być eksportowany za pomocą Aspose.PSD**

{{< highlight python >}}
        plikŹródłowy = "1966źródło.psd"
        wyjściePng = "wyjście.png"

        opcjeŁadowania = PsdLoadOptions()
        opcjeŁadowania.load_effects_resource = True

        with PsdImage.load(plikŹródłowy, opcjeŁadowania) as psdObraz:
            psdObraz.save(wyjściePng, PngOptions())
			
{{< /highlight >}}
