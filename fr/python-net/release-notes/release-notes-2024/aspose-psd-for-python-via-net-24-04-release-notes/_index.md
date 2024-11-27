---
title: Aspose.PSD pour Python via .NET 24.4 - Notes de version
type: docs
weight: 10
url: /fr/python-net/aspose-psd-pour-python-via-net-24-4-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour Python via .NET 24.4](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clé**      | **Résumé**                                                          | **Catégorie**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-50 | [Format AI] Ajout de la gestion des ressources XObjectForm          | Fonctionnalité     |
| PSDPYTHON-51 | Ajout du constructeur pour ShapeLayer                              | Fonctionnalité     |
| PSDPYTHON-52 | Correction de la conversion du fichier Psd de RGB à CMJN           | Problème         |
| PSDPYTHON-53 | Impossible d'exporter un fichier PSD spécifique avec Aspose.PSD    | Problème         |



## **Changements dans l'API publique**
# **APIs ajoutées:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **APIs supprimées:**
- Aucune


## **Exemples d'utilisation:**

**PSDPYTHON-50. [Format AI] Ajout de la gestion des ressources XObjectForm**

{{< highlight python >}}
        nomFichierSource = "exemple.ai"
        cheminSortie = "exemple_sortie.png"

        with AiImage.load(nomFichierSource) as image:
            image.save(cheminSortie, PngOptions())
{{< /highlight >}}

**PSDPYTHON-51. Ajout du constructeur pour ShapeLayer**

{{< highlight python >}}
     def vérifier ShapeLayerConstructor():
        fichierSortie = "SortieAjoutShapeLayer.psd"

        with PsdImage(600, 400) as newPsd:
            shapeLayer = newPsd.add_shape_layer()

            newShape = generate_new_shape(newPsd.size)
            newShapes = [newShape]
            shapeLayer.path.set_items(newShapes)

            shapeLayer.update()

            newPsd.save(fichierSortie)

        with PsdImage.load(fichierSortie) as img:
            image = cast(PsdImage, img)
            assert len(image.layers) == 2

            shapeLayer = cast(ShapeLayer, image.layers[1])
            internalFill = shapeLayer.fill
            strokeSettings = shapeLayer.stroke
            strokeFill = shapeLayer.stroke.fill

            assert len(shapeLayer.path.get_items()) == 1
            assert len(shapeLayer.path.get_items()[0].get_items()) == 3

            assert internalFill.color.to_argb() == -16127182

            assert strokeSettings.size == 7.41
            assert not strokeSettings.enabled
            assert strokeSettings.line_alignment == StrokePosition.CENTER
            assert strokeSettings.line_cap == LineCapType.BUTT_CAP
            assert strokeSettings.line_join == LineJoinType.MITER_JOIN
            assert strokeFill.color.to_argb() == -16777216
			
    def generate_new_shape(imageSize):
        newShape = PathShape()

        point1 = PointF(20, 100)
        point2 = PointF(200, 100)
        point3 = PointF(300, 10)

        knot1 = BezierKnotRecord()
        knot1.is_linked = True
        knot1.points = [
                    Release_24_04_Tests.PointFToResourcePoint(point1, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(point1, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(point1, imageSize)
                ]

        knot2 = BezierKnotRecord()
        knot2.is_linked = True
        knot2.points = [
                    Release_24_04_Tests.PointFToResourcePoint(point2, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(point2, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(point2, imageSize)
                ]

        knot3 = BezierKnotRecord()
        knot3.is_linked = True
        knot3.points = [
                    Release_24_04_Tests.PointFToResourcePoint(point3, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(point3, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(point3, imageSize)
                ]

        bezierKnots = [
            knot1,
            knot2,
            knot3
        ]

        newShape.set_items(bezierKnots)

        return newShape
		
    def PointFToResourcePoint(point, imageSize):
        ImgToPsdRatio = 256 * 65535
        return Point(
            int(round(point.y * (ImgToPsdRatio / imageSize.height))),
            int(round(point.x * (ImgToPsdRatio / imageSize.width)))
        )

    def assert_are_equal(expected, actual, message=None):
        if expected != actual:
            raise Exception(message or "Les objets ne sont pas égaux.")
			
{{< /highlight >}}

**PSDPYTHON-52. Correction de la conversion du fichier PSD de RGB à CMJN**

{{< highlight python >}}
     def vérifierConversionDeRgbÀCmjn():
        fichierSource = "grenouille_nosymb.psd"
        fichierSortie = "grenouille_nosymb_sortie.psd"

        with PsdImage.load(fichierSource) as image:
            psdImage = cast(PsdImage, image)
            psdImage.has_transparency_data = False

            psdOptions = PsdOptions(psdImage)
            psdOptions.color_mode = ColorModes.CMYK
            psdOptions.compression_method = CompressionMethod.RLE
            psdOptions.channels_count = 4

            psdImage.save(fichierSortie, psdOptions)

        with PsdImage.load(fichierSortie) as image:
            psdImage = cast(PsdImage, image)
            assert not psdImage.has_transparency_data
            assert psdImage.layers[0].channels_count == 4

        def assert_are_equal(expected, actual, message=None):
            if expected != actual:
                raise Exception(message or "Les objets ne sont pas égaux.")			

    def assert_are_equal(expected, actual, message=None):
        if expected != actual:
            raise Exception(message or "Les objets ne sont pas égaux.")
				
{{< /highlight >}}

**PSDPYTHON-53. Impossible d'exporter un fichier PSD spécifique avec Aspose .PSD**

{{< highlight python >}}
        fichierSource = "1966source.psd"
        sortiePng = "sortie.png"

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True

        with PsdImage.load(fichierSource, loadOpt) as psdImage:
            psdImage.save(sortiePng, PngOptions())
			
{{< /highlight >}}
