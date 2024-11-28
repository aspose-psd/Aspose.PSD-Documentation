---
title: Aspose.PSD für Python via .NET 24.2 - Versionshinweise
type: docs
weight: 10
url: /de/net/aspose-psd-for-python-via-net-24-2-release-notes/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für Python via .NET 24.2](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                           | **Kategorie** |
|:-------------|:-----------------------------------------------------------------------------|:------------|
| PSDPYTHON-28 | Behandle Angle-Eigenschaft für PatternFillSettings                            |   Feature   |
| PSDPYTHON-29 | Unterstützung von vertikalem und horizontalem Maßstab für TextLayer          |   Feature   |
| PSDPYTHON-33 | [AI-Format] Implementierung der korrekten Rendering des Hintergrunds im PDF-basierten AI-Format.|   Feature   |
| PSDPYTHON-34 | Ändern des Verzerrungsmechanismus in Warp                                      | Leistungsverbesserung |
| PSDPYTHON-35 | Warp beschleunigen                                                            | Leistungsverbesserung |
| PSDPYTHON-36 | Ausnahme "Bildladen fehlgeschlagen" beim Öffnen des Dokuments                  |     Fehler     |
| PSDPYTHON-37 | Beheben des Speicherns von PSD-Dateien mit Strichmuster                        |     Fehler     |
| PSDPYTHON-38 | Der Textstil ist falsch in einem Smartobjekt, wenn wir ReplaceContents verwenden |    Fehler    |
| PSDPYTHON-39 | [AI-Format] Beheben des Cubic-Bezier-Renderings in der AI-Datei               |     Fehler    



## **Änderungen in der öffentlichen API**
# **Hinzugefügte APIs:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **Entfernte APIs:**
- Keine


## **Anwendungsbeispiele:**

## **Anwendungsbeispiele:**

**PSDPYTHON-28. Behandle Angle-Eigenschaft für PatternFillSettings**

{{< highlight python >}}

	    Dateiname = "PatternFillLayerWide_0"
        Quelldatei = Dateiname + ".psd"
        Ausgabedatei = Dateiname + "_output.psd"

        Ladeoptionen = PsdLoadOptions()
        Ladeoptionen.load_effects_resource = True
        with PsdImage.load(Quelldatei, Ladeoptionen) as img:
            Bild = cast(PsdImage, img)
            Füllschicht = cast(FillLayer, Bild.layers[1])
            FüllEinstellungen = Füllschicht.fill_settings
            FüllEinstellungen.angle = 70
            Füllschicht.update()
            Bild.save(Ausgabedatei, PsdOptions())

        with PsdImage.load(Ausgabedatei, Ladeoptionen) as img:
            Bild = cast(PsdImage, img)
            Füllschicht = cast(FillLayer, Bild.layers[1])
            FüllEinstellungen = Füllschicht.fill_settings

            assert FüllEinstellungen.angle == 70

{{< /highlight >}}

**PSDPYTHON-29. Unterstützung von vertikalem und horizontalem Maßstab für TextLayer**

{{< highlight python >}}

           Quelldatei = "1719_src.psd"
           Ausgabedatei = "output.png"

           # Einige Schriftarten hinzufügen
           SchriftartenOrdner = "1719_Fonts"
           SchriftOrdner = list(FontSettings.get_fonts_folders())
           SchriftOrdner.append(SchriftartenOrdner)
           FontSettings.set_fonts_folders(SchriftOrdner, True)

           with PsdImage.load(Quelldatei) as Bild:
               Bild.save(Ausgabedatei, PngOptions())

{{< /highlight >}}

**PSDPYTHON-33. [AI-Format] Implementierung der korrekten Rendering des Hintergrunds im PDF-basierten AI-Format**

{{< highlight python >}}

           Quelldatei = "pineapples.ai"
           Ausgabedatei  = "pineapples.png"

           with AiImage.load(Quelldatei) as Bild:
               Bild.save(Ausgabedatei, PngOptions())

{{< /highlight >}}

**PSDPYTHON-34. Ändern des Verzerrungsmechanismus in Warp**

{{< highlight python >}}

        Quelldatei = "crow_grid.psd"       
        Ausgabedatei = self.GetFileInOutputFolder("export.png")

        Opt = PsdLoadOptions()
        Opt.load_effects_resource = True
        Opt.allow_warp_repaint = True

        PngOpt = PngOptions()
        PngOpt.compression_level = 9
        PngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
        with PsdImage.load(Quelldatei, Opt) as img:
            img.save(Ausgabedatei, PngOpt)

{{< /highlight >}}

**PSDPYTHON-35. Warp beschleunigen**

{{< highlight python >}}

        Quelldatei = "output.psd"
        Ausgabedatei = "export.png"

        Opt = PsdLoadOptions()
        Opt.load_effects_resource = True
        Opt.allow_warp_repaint = True

        Startzeit = time.time()

        PngOpt = PngOptions()
        PngOpt.compression_level = 9
        PngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(Quelldatei, Opt) as img:
            img.save(Ausgabedatei, PngOpt)

        VergangeneZeit = time.time() - Startzeit

        # Alter Wert = 193300
        # Neuer Wert =  55500
        Zeit_in_Sek = int(VergangeneZeit * 1000)
        if Zeit_in_Sek > 100000:
            raise Exception("Prozesszeit ist zu langsam")        
			
{{< /highlight >}}

**PSDPYTHON-36. Ausnahme "Bildladen fehlgeschlagen." beim Öffnen des Dokuments**

{{< highlight python >}}
        Quelldatei1 = "PRODUCT.ai"
        Ausgabedatei1 = "PRODUCT.png"

        with AiImage.load(Quelldatei1) as Bild:
            Bild.save(Ausgabedatei1, PngOptions())

        Quelldatei2 = "Dolota.ai"
        Ausgabedatei2 = "Dolota.png"

        with AiImage.load(Quelldatei2) as Bild:
            Bild.save(Ausgabedatei2, PngOptions())       

        Quelldatei3 = "ARS_novelty_2108_out_01(1).ai"
        Ausgabedatei3 = "ARS_novelty_2108_out_01(1).png"

        with AiImage.load(Quelldatei3) as Bild:
            Bild.save(Ausgabedatei3, PngOptions())

        Quelldatei4 = "bit_gear.ai"      
        Ausgabedatei4 = "bit_gear.png"

        with AiImage.load(Quelldatei4) as Bild:
            Bild.save(Ausgabedatei4, PngOptions())

        Quelldatei5 = "test.ai"
        Ausgabedatei5 = "test.png"

        with AiImage.load(Quelldatei5) as Bild:
            Bild.save(Ausgabedatei5, PngOptions())
{{< /highlight >}}

**PSDPYTHON-37. Beheben des Speicherns von PSD-Dateien mit Strichmuster**

{{< highlight python >}}
	    Quelldatei = "StrokeShapePattern.psd"
        Ausgabedatei = "StrokeShapePattern_output.psd"

        neueMustergröße = Rectangle(0, 0, 4, 4)
        guid = str(uuid.uuid4())
        neuerMusternamen = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0"
        neuesMuster = [
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
        ]

        with PsdImage.load(Quelldatei) as img:
            Bild = cast(PsdImage, img)
            Shapelayer = cast(ShapeLayer, Bild.layers[1])
            StrichFülleinstellungen = Shapelayer.fill

            PattRessource = None
            for GlobaleEbenenressource in Bild.global_layer_resources:

                PattRessource = as_of(GlobaleEbenenressource, PattResource)
                if PattRessource is not None:
                    MusterElement = PattRessource.patterns[0]  # Muster für den internen Strich

                    MusterElement.pattern_id = guid
                    MusterElement.name = neuerMusternamen
                    MusterElement.set_pattern(neuesMuster, neueMustergröße)
                    break


            StrichFülleinstellungen.pattern_name = neuerMusternamen
            StrichFülleinstellungen.pattern_id = guid + "\0"

            Shapelayer.update()

            Bild.save(Ausgabedatei)

        # Überprüfen der geänderten Daten.
        with PsdImage.load(Ausgabedatei) as img:
            Bild = cast(PsdImage, img)
            Shapelayer = cast(ShapeLayer, Bild.layers[1])
            StrichFülleinstellungen = Shapelayer.fill

            assert guid.upper() == StrichFülleinstellungen.pattern_id
            assert neuerMusternamen == StrichFülleinstellungen.pattern_name + "\0"
			
{{< /highlight >}}

**PSDPYTHON-38. Der Textstil ist falsch in einem Smartobjekt, wenn wir ReplaceContents verwenden**

{{< highlight python >}}
        Eingabedatei = "source.psd"
        Ausgabe2 = "output.png"

        PsdLadeoptionen = PsdLoadOptions()
        PsdLadeoptionen.load_effects_resource = True

        with PsdImage.load(Eingabedatei, PsdLadeoptionen) as Bild:
            PsdImage = cast(PsdImage, Bild)
            Smartobjekt = cast(SmartObjectLayer, PsdImage.layers[1])

            SmartobjektBild = cast(PsdImage, Smartobjekt.load_contents(PsdLadeoptionen))

            with SmartobjektBild:
                Smartobjekt.replace_contents(SmartobjektBild)

            PngOpt = PngOptions()
            PngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
            PsdImage.save(Ausgabe2, PngOpt)

{{< /highlight >}}

**PSDPYTHON-39. [AI-Format] Beheben des Cubic-Bezier-Renderings in der AI-Datei**

{{< highlight python >}}

        Quelldatei = "Typography.ai"
        Ausgabedateipfad = "Typography.png"

        with AiImage.load(Quelldatei) as Bild:
            Bild.save(Ausgabedateipfad, PngOptions())

{{< /highlight >}}
