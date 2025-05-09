---
title: Aspose.PSD for Python via .NET 23.12 - Notities bij vrijgave
type: docs
weight: 10
url: /nl/net/aspose-psd-voor-python-via-net-23-12-release-notities/
---

{{% alert color="primary" %}}

Deze pagina bevat de vrijgavenotities voor [Aspose.PSD for Python via .NET 23.12](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                                                           | **Categorie** |
|:--------------|:------------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-7  | [AI-indeling] Ondersteuning toegevoegd voor renderen van rasterafbeelding in nieuwe versie van AI           |   Feature   |
|  PSDPYTHON-8  | Verwerken van gradiënttype Noise in GdflResrource                                                           |   Feature   |
|  PSDPYTHON-9  | Fout "Objectreference niet ingesteld op een exemplaar van een object." bij opslaan van tekstlaag na bijwerken |     Bug     |
|  PSDPYTHON-10 | Repareer het handmatig laden van lettertypen op MacOS met behulp van System.Drawing.Common en Aspose.Drawing. |     Bug     |
|  PSDPYTHON-11 | AllowWarpRepaint in de PsdLoadOptions leidt tot de uitzondering                                             |     Bug     |
|  PSDPYTHON-12 | [AI-indeling] Implementatie van verwerking van kruisverwijzingsstreams                                       | Verbetering  |
|  PSDPYTHON-13 | Licentiebeheer voor VectorPathDataResource werkt onjuist                                                  | Verbetering  |


## **Openbare API-wijzigingen**
# **Toegevoegde API's:**
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.#ctor(System.IO.Stream)
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.RGB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.HSB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.LAB
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.GradientMode
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.#ctor
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.Metered.GetProductName
- M:Aspose.PSD.Metered.IsMeteredLicensed
- T:Aspose.PSD.PluginLicenseException
- M:Aspose.PSD.PluginLicenseException.#ctor
- M:Aspose.PSD.Metered.Equals(System.Object)

# **Verwijderde API's:**
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- M:Aspose.PSD.Metered.Equals(System.Object)


## **Gebruik voorbeelden:**

**PSDPYTHON-7. [AI-indeling] Ondersteuning toegevoegd voor het renderen van rasterafbeeldingen in nieuwe versie van AI**

{{< highlight python >}}
        bronBestand = "raster.ai"
        uitvoerBestand = "raster_output.png"

        with Image.load(bronBestand) as afbeelding:
            afbeelding.save(uitvoerBestand, PngOptions())
{{< /highlight >}}

**PSDPYTHON-8. Handelen met Gradiënttype Noise in GdflResrource**

{{< highlight python >}}
        # Voorbeeld om deze GdFlResource te gebruiken met basis-API   
        bronBestand = "Gradient-Fill.psd"
        doelBestand = "Gradient-Fill-out.psd"

        with Image.load(bronBestand, PsdLoadOptions()) as afbeelding:
            psdAfbeelding = cast(PsdImage, afbeelding)
            laag = psdAfbeelding.layers[1]

            for res in laag.resources:
                resource = as_of(res, GdFlResource)
                if (resource != None):
                    resource.scale = 90
                    resource.angle = 30
                    resource.dither = False
                    resource.align_with_layer = True
                    resource.reverse = False

                    break

            psdAfbeelding.save(doelBestand, PsdOptions())
		
		# Voorbeeld van het handelen van een solide Gradiënt
		sourceFile = "ComplexGradientFillLayer.psd"
        uitvoerBestand =  "ComplexGradientFillLayer_output.psd"

        with Image.load(bronBestand) as afbeelding:
            im = cast(PsdImage, afbeelding)
            for laag in im.layers:
                if is_assignable(laag, FillLayer):
                    fillLaag = as_of(laag, FillLayer)
                    gradientFillSettings = fillLaag.fill_settings

                    # Lezen
                    assert gradientFillSettings.align_with_layer == False
                    assert abs(gradientFillSettings.angle - 45.0) < 0.001

                    assert gradientFillSettings.dither == True
                    assert gradientFillSettings.reverse == False
                    assert gradientFillSettings.color == Color.empty
                    assert gradientFillSettings.horizontal_offset == -39
                    assert gradientFillSettings.vertical_offset == -5

                    assert len(gradientFillSettings.transparency_points) == 3
                    assert len(gradientFillSettings.color_points) == 2

                    point = gradientFillSettings.transparency_points[0]
                    assert abs(100.0 - point.opacity) < 0.25
                    assert point.location == 0
                    assert point.median_point_location == 50

                    point = gradientFillSettings.transparency_points[1]
                    assert abs(50.0 - point.opacity) < 0.25
                    assert point.location == 2048
                    assert point.median_point_location == 50

                    point = gradientFillSettings.transparency_points[2]
                    assert abs(100.0 - point.opacity) < 0.25
                    assert point.location == 4096
                    assert point.median_point_location == 50

                    color_point = gradientFillSettings.color_points[0]
                    assert color_point.color == Color.from_argb(203, 64, 140)
                    assert color_point.location == 0
                    assert color_point.median_point_location == 50

                    color_point = gradientFillSettings.color_points[1]
                    assert color_point.color == Color.from_argb(203, 0, 0)
                    assert color_point.location == 4096
                    assert color_point.median_point_location == 50

                    # Bewerken
                    gradientFillSettings.angle = 30.0
                    gradientFillSettings.dither = False
                    gradientFillSettings.align_with_layer = True
                    gradientFillSettings.reverse = True
                    gradientFillSettings.horizontal_offset = 25
                    gradientFillSettings.vertical_offset = -15

                    color_points = list(gradientFillSettings.color_points)
                    transparency_points = list(gradientFillSettings.transparency_points)

                    gradPoint1 = GradientColorPoint()
                    gradPoint1.color = Color.violet
                    gradPoint1.location = 4096
                    gradPoint1.median_point_location = 75
                    color_points.append(gradPoint1)

                    color_points[1].location = 3000

                    gradPoint2 = GradientTransparencyPoint()
                    gradPoint2.opacity = 80.0
                    gradPoint2.location = 4096
                    gradPoint2.median_point_location = 25
                    transparency_points.append(gradPoint2)

                    transparency_points[2].location = 3000

                    gradientFillSettings.color_points = color_points
                    gradientFillSettings.transparency_points = transparency_points

                    im.save(uitvoerBestand)

        with Image.load(uitvoerBestand) as afbeelding:
            im = cast(PsdImage, afbeelding)
            for laag in im.layers:
                if isinstance(laag, FillLayer):
                    fillLaag = laag
                    gradientFillSettings = fillLaag.fill_settings

                    assert abs(gradientFillSettings.angle - 30) < 0.001
                    assert gradientFillSettings.align_with_layer == True
                    assert gradientFillSettings.dither == False
                    assert gradientFillSettings.reverse == True
                    assert gradientFillSettings.horizontal_offset == 25
                    assert gradientFillSettings.vertical_offset == -15

                    assert len(gradientFillSettings.transparency_points) == 4
                    assert len(gradientFillSettings.color_points) == 3

                    point = gradientFillSettings.transparency_points[0]
                    assert abs(100.0 - point.opacity) < 0.25
                    assert point.location == 0
                    assert point.median_point_location == 50

                    point = gradientFillSettings.transparency_points[1]
                    assert abs(50.196 - point.opacity) < 0.25
                    assert point.location == 2048
                    assert point.median_point_location == 50

                    point = gradientFillSettings.transparency_points[2]
                    assert abs(100.0 - point.opacity) < 0.25
                    assert point.location == 3000
                    assert point.median_point_location == 50

                    point = gradientFillSettings.transparency_points[3]
                    assert abs(80 - point.opacity) < 0.25
                    assert point.location == 4096
                    assert point.median_point_location == 25

                    color_point = gradientFillSettings.color_points[0]
                    assert color_point.color == Color.FromArgb(203, 64, 140)
                    assert color_point.location == 0
                    assert color_point.median_point_location == 50

                    color_point = gradientFillSettings.color_points[1]
                    assert color_point.color == Color.FromArgb(203, 0, 0)
                    assert color_point.location == 3000
                    assert color_point.median_point_location == 50

                    color_point = gradientFillSettings.color_points[2]
                    assert color_point.color == Color.FromArgb(238, 130, 238)
                    assert color_point.location == 4096
                    assert color_point.median_point_location == 75
					
		# Voorbeeld om noise Gradient te behandelen
        bronBestand = "FillLayerGradientNoise.psd"
        uitvoerBestand = "FillLayerGradientNoise_output.psd"

        with Image.load(bronBestand) as afbeelding:
            im = cast(PsdImage, afbeelding)
            for laag in im.layers:
                if is_assignable(laag, FillLayer):
                    fillLaag = as_of(laag, FillLayer)
                    if fillLaag is not None:
                        gradientFillSettings = fillLaag.fill_settings

                        assert gradientFillSettings.align_with_layer == False
                        assert abs(gradientFillSettings.angle - 41.0) < 0.001
                        assert gradientFillSettings.dither == True
                        assert gradientFillSettings.reverse == True
                        assert gradientFillSettings.scale == 133
                        assert gradientFillSettings.gradient_mode == GradientKind.NOISE

                        assert gradientFillSettings.show_transparency == True
                        assert gradientFillSettings.use_vector_color == True
                        assert gradientFillSettings.color_model == NoiseColorModel.RGB
                        assert gradientFillSettings.rnd_number_seed == 2015172547
                        assert gradientFillSettings.roughness == 3727

                        assert gradientFillSettings.minimum_color.components[1].value == 15
                        assert gradientFillSettings.minimum_color.components[2].value == 33
                        assert gradientFillSettings.minimum_color.components[3].value == 56
                        assert gradientFillSettings.minimum_color.components[0].value == 0

                        assert gradientFillSettings.maximum_color.components[1].value == 234
                        assert gradientFillSettings.maximum_color.components[2].value == 209
                        assert gradientFillSettings.maximum_color.components[3].value == 186
                        assert gradientFillSettings.maximum_color.components[0].value == 255

                        # Bewerken
                        gradientFillSettings.angle = 30.0
                        gradientFillSettings.dither = False
                        gradientFillSettings.align_with_layer = True
                        gradientFillSettings.reverse = False
                        gradientFillSettings.scale = 60
                        gradientFillSettings.show_transparency = False
                        gradientFillSettings.use_vector_color = False
                        gradientFillSettings.color_model = NoiseColorModel.HSB
                        gradientFillSettings.roughness = 4096
                        gradientFillSettings.rnd_number_seed = 12345678

                        gradientFillSettings.minimum_color.components[1].value = 0
                        gradientFillSettings.minimum_color.components[2].value = 0
                        gradientFillSettings.minimum_color.components[3].value = 0
                        gradientFillSettings.minimum_color.components[0].value = 0

                        gradientFillSettings.maximum_color.components[1].value = 255
                        gradientFillSettings.maximum_color.components[2].value = 255
                        gradientFillSettings.maximum_color.components[3].value = 255
                        gradientFillSettings.maximum_color.components[0].value = 255

                        im.save(uitvoerBestand)

        with Image.load(uitvoerBestand) as afbeelding:
            im = cast(PsdImage, afbeelding)
            for laag in im.layers:
                if is_assignable(laag, FillLayer):
                    fillLaag = as_of(laag, FillLayer)
                    gradientFillSettингs = fillLaag.fill_settings

                    assert gradientFillSettингs.align_with_layer == True
                    assert abs(gradientFillSettингs.angle - 30.0) < 0.001
                    assert gradientFillSettингs.dither == False
                    assert gradientFillSettингs.reverse == False
                    assert gradientFillSettингs.scale == 60

                    assert gradientFillSettингs.show_transparency == False
                    assert gradientFillSettингs.use_vector_color == False
                    assert gradientFillSettингs.color_model == NoiseColorModel.HSB
                    assert gradientFillSettингs.rnd_number_seed == 12345678
                    assert gradientFillSettингs.roughness == 4096

                    assert gradientFillSettингs.minimum_color.components[1].value == 0
                    assert gradientFillSettингs.minimum_color.components[2].value == 0
                    assert gradientFillSettингs.minimum_color.components[3].value == 0
                    assert gradientFillSettингs.minimum_color.components[0].value == 0

                    assert gradientFillSettингs.maximum_color.components[1].value == 255
                    assert gradientFillSettингs.maximum_color.components[2].value == 255
                    assert gradientFillSettингs.maximum_color.components[3].value == 255
                    assert gradientFillSettингs.maximum_color.components[0].value == 255
		
{{< /highlight >}}

**PSDPYTHON-9. Fout "Objectreference niet ingesteld op een exemplaar van een object." bij opslaan van tekstlaag na bijwerken**

{{< highlight python >}}
        bronBestand = "input_1827.psd"
