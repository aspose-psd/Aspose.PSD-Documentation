---
title: Aspose.PSD voor Python via .NET 24.2 - Release-opmerkingen
type: docs
weight: 10
url: /nl/net/aspose-psd-voor-python-via-net-24-2-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Python via .NET 24.2](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Sleutel**   | **Samenvatting**                                                             | **Categorie** |
|:--------------|:------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-28  | Handel Angle-eigenschap af voor PatternFillSettings                           | Functie      |
| PSDPYTHON-29  | Ondersteuning voor verticale en horizontale schaal voor TextLayer            | Functie      |
| PSDPYTHON-33  | [AI-indeling] Implementeer correcte weergave van achtergrond in op PDF gebaseerde AI-indeling.| Functie      |
| PSDPYTHON-34  | Verander vervormingsmechanisme in warp                                        | Verbetering  |
| PSDPYTHON-35  | Warp versnellen                                                             | Verbetering  |
| PSDPYTHON-36  | "Afbeelding laden mislukt." uitzondering bij openen document                    | Fout         |
| PSDPYTHON-37  | Herstel opslaan psd-bestanden met Stroke-patroon                              | Fout         |
| PSDPYTHON-38  | De tekststijl is onjuist in een slim object wanneer we ReplaceContents gebruiken| Fout         |
| PSDPYTHON-39  | [AI-indeling] Los het renderen van Cubic Bezier op in AI-bestand              | Fout         |



## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**

**Gebruik voorbeelden:**

**PSDPYTHON-28. Angle-eigenschap afhandelen voor PatternFillSettings**

{{< highlight python >}}

	    bestandsnaam = "PatternFillLayerWide_0"
        sourceBestand = bestandsnaam + ".psd"
        outputBestand = bestandsnaam + "_output.psd"

        laadOpties = PsdLaadOpties()
        laadOpties.laad_effecten_resource = True
        with PsdAfbeelding.laden(sourceBestand, laadOpties) als img:
            afbeelding = cast(PsdAfbeelding, img)
            vulLaag = cast(VulLaag, afbeelding.lagen[1])
            vulInstellingen = vulLaag.vul_instellingen
            vulInstellingen.hoek = 70
            vulLaag.bijwerken()
            afbeelding.opslaan(outputBestand, PsdOpties())

        with PsdAfbeelding.laden(outputBestand, laadOpties) als img:
            afbeelding = cast(PsdAfbeelding, img)
            vulLaag = cast(VulLaag, afbeelding.lagen[1])
            vulInstellingen = vulLaag.vul_instellingen

            assert vulInstellingen.hoek == 70

{{< /highlight >}}

**PSDPYTHON-29. Ondersteuning van verticale en horizontale schaal voor TextLayer**

{{< highlight python >}}

           sourceBestand = "1719_src.psd"
           outputBestand = "output.png"

           # Voeg enkele lettertypen toe
           lettertypeMap = "1719_Fonts"
           lettertypeMappen = lijst(FontInstellingen.get_fonts_folders())
           lettertypeMappen.append(lettertypeMap)
           FontInstellingen.set_fonts_folders(lettertypeMappen, True)

           with PsdAfbeelding.laden(sourceBestand) als afbeelding:
               afbeelding.opslaan(outputBestand, PngOpties())

{{< /highlight >}}

**PSDPYTHON-33. [AI-indeling] Implementeer correcte weergave van achtergrond in op PDF gebaseerde AI-indeling**

{{< highlight python >}}

           sourceBestand = "ananas.ai"
           outputBestand = "ananas.png"

           with AiAfbeelding.laden(sourceBestand) als afbeelding:
               afbeelding.opslaan(outputBestand, PngOpties())

{{< /highlight >}}

**PSDPYTHON-34. Verander vervormingsmechanisme in warp**

{{< highlight python >}}

        sourceBestand = "crow_grid.psd"       
        outputBestand = self.GetFileInOutputFolder("export.png")

        opties = PsdLaadOpties()
        opties.laad_effecten_resource = True
        opties.sta_warp_opnieuw_schilderen_toe = True

        pngOpties = PngOpties()
        pngOpties.compressie_niveau = 9
        pngOpties.kleurtype = PngKleurtype.TRUECOLOR_MET_ALPHA
        with PsdAfbeelding.laden(sourceBestand, opties) als img:
            img.opslaan(outputBestand, pngOpties)

{{< /highlight >}}

**PSDPYTHON-35. Warp versnellen**

{{< highlight python >}}

        sourceBestand = "output.psd"
        outputBestand = "export.png"

        opties = PsdLaadOpties()
        opties.laad_effecten_resource = True
        opties.sta_warp_opnieuw_schilderen_toe = True

        start_tijd = time.time()

        pngOpties = PngOpties()
        pngOpties.compressie_niveau = 9
        pngOpties.kleurtype = PngKleurtype.TRUECOLOR_MET_ALPHA

        with PsdAfbeelding.laden(sourceBestand, opties) als img:
            img.opslaan(outputBestand, pngOpties)

        verstreken_tijd = time.time() - start_tijd

        # oude waarde = 193300
        # nieuwe waarde =   55500
        tijd_in_sec = int(verstreken_tijd * 1000)
        if tijd_in_sec > 100000:
            raise Exception("Procestijd is te lang")        
			
{{< /highlight >}}

**PSDPYTHON-36. "Afbeelding laden mislukt." uitzondering bij openen document**

{{< highlight python >}}
        bronBestand1 = "PRODUCT.ai"
        outputBestand1 = "PRODUCT.png"

        with AiAfbeelding.laden(bronBestand1) als afbeelding:
            afbeelding.opslaan(outputBestand1, PngOpties())

        bronBestand2 = "Dolota.ai"
        outputBestand2 = "Dolota.png"

        with AiAfbeelding.laden(bronBestand2) als afbeelding:
            afbeelding.opslaan(outputBestand2, PngOpties())       

        bronBestand3 = "ARS_novelty_2108_out_01(1).ai"
        outputBestand3 = "ARS_novelty_2108_out_01(1).png"

        with AiAfbeelding.laden(bronBestand3) als afbeelding:
            afbeelding.opslaan(outputBestand3, PngOpties())

        bronBestand4 = "bit_gear.ai"      
        outputBestand4 = "bit_gear.png"

        with AiAfbeelding.laden(bronBestand4) als afbeelding:
            afbeelding.opslaan(outputBestand4, PngOpties())

        bronBestand5 = "test.ai"
        outputBestand5 = "test.png"

        with AiAfbeelding.laden(bronBestand5) als afbeelding:
            afbeelding.opslaan(outputBestand5, PngOpties())
{{< /highlight >}}

**PSDPYTHON-37. Herstel opslaan psd-bestanden met Stroke-patroon**

{{< highlight python >}}
	    bronBestand = "StrokeShapePattern.psd"
        outputBestand = "StrokeShapePattern_output.psd"

        nieuwePatroonGrenzen = Rechthoek(0, 0, 4, 4)
        guid = str(uuid.uuid4())
        nieuwePatroonnaam = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0"
        nieuwPatroon = [
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
        ]

        with PsdAfbeelding.laden(bronBestand) als img:
            afbeelding = cast(PsdAfbeelding, img)
            vormLaag = cast(VormLaag, afbeelding.lagen[1])
            slagInterneVulInstellingen = vormLaag.vul

            pattResource = None
            for globaleLaagResource in afbeelding.globale_layer_resources:


                pattResource = as_of(globaleLaagResource, PattResource)
                if pattResource is not None:
                    patroonItem = pattResource.patterns[0]  # Interne slag patroon gegevens

                    patroonItem.pattern_id = guid
                    patroonItem.naam = nieuwePatroonnaam
                    patroonItem.set_patroon(nieuwPatroon, nieuwePatroonGrenzen)
                    breken


            slagInterneVulInstellingen.pattern_name = nieuwePatroonnaam
            slagInterneVulInstellingen.pattern_id = guid + "\0"

            vormLaag.bijwerken()

            afbeelding.opslaan(outputBestand)

        # Controleer gewijzigde gegevens.
        with PsdAfbeelding.laden(outputBestand) als img:
            afbeelding = cast(PsdAfbeelding, img)
            vormLaag = cast(VormLaag, afbeelding.lagen[1])
            slagInterneVulInstellingen = vormLaag.vul

            assert guid.upper() == slagInterneVulInstellingen.pattern_id
            assert nieuwePatroonnaam == slagInterneVulInstellingen.pattern_name + "\0"
			
{{< /highlight >}}

**PSDPYTHON-38. De tekststijl is onjuist in een slim object wanneer we ReplaceContents gebruiken**

{{< highlight python >}}
        invoerBestand = "bron.psd"
        output2 = "output.png"

        psdLaadOpties = PsdLaadOpties()
        psdLaadOpties.laad_effecten_resource = True

        with PsdAfbeelding.laden(invoerBestand, psdLaadOpties) als afbeelding:
            psdAfbeelding = cast(PsdAfbeelding, afbeelding)
            slimObject = cast(SlimObjectLaag, psdAfbeelding.lagen[1])

            slimObjectAfbeelding = cast(PsdAfbeelding, slimObject.inhoud_laden(psdLaadOpties))

            with slimObjectAfbeelding:
                slimObject.vervang_inhoud(slimObjectAfbeelding)

            pngOpties = PngOpties()
            pngOpties.kleurtype = PngKleurtype.TRUECOLOR_MET_ALPHA
            psdAfbeelding.opslaan(output2, pngOpties)

{{< /highlight >}}

**PSDPYTHON-39. [AI-indeling] Los het renderen van Cubic Bezier op in AI-bestand**

{{< highlight python >}}

        bronBestand = "Typografie.ai"
        uitvoerBestandsPad = "Typografie.png"

        with AiAfbeelding.laden(bronBestand) als afbeelding:
            afbeelding.opslaan(uitvoerBestandsPad, PngOpties())

{{< /highlight >}}
