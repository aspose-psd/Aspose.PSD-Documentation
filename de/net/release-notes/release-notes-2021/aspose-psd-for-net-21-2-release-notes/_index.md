---
title: Aspose.PSD für .NET 21.2 - Versionshinweise
type: dok
weight: 110
url: /de/net/aspose-psd-fur-net-21-2-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält die Versionshinweise für [Aspose.PSD für .NET 21.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-404|Unterstützung von vogkResource|Funktion|
|PSDNET-809|Falsche Begrenzungen von Smart Object-Layern, wenn wir Smart Object-Inhalte durch die Datei ersetzen, die unterschiedliche Dimensionen und Auflösungen hat|Funktion|
|PSDNET-752|Fehler beim Konvertieren von FillLayer in SmartObjectLayer|Fehler|
|PSDNET-778|LayerGroup fügt neue Ebenen in umgekehrter Reihenfolge hinzu|Fehler|
|PSDNET-790|Importieren eines Bildes in SmartObject-Layer führt zu einer PSD-Korruption|Fehler|
|PSDNET-810|Ausnahme beim Laden der Dateien|Fehler|
|PSDNET-824|Inkorrekte vogk-Ressource nach Laden und Speichern des PSD-Bildes mit Formebenen und Vektorpfaden|Fehler|
|PSDNET-827|Ausnahme beim Laden von Referenzstrukturen und EnumeratedReferenceStructure-Strukturen|Fehler|

## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginType
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginResolution
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginShapeBox
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginRadiiRectangle
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidatedPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginIndexPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginTypePresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginResolutionPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginRadiiRectanglePresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginShapeBBoxPresent
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Left
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Top
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Right
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Bottom
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.QuadVersion
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Bounds
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.TopLeft
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.TopRight
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.BottomRight
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.BottomLeft
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.QuadVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID.#ctor(System.String,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ReplaceContents(Aspose.PSD.Image,Aspose.PSD.ResolutionSetting)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ReplaceContents(System.String,Aspose.PSD.ResolutionSetting)

# **Entfernte APIs:** 
- Keine

## **Beispiele:**

**PSDNET-404. Unterstützung von vogkResource**

{{< highlight csharp >}}
            // Dieses Beispiel zeigt, dass das Laden und Speichern des PSD-Bildes mit Formebenen und Vektorpfaden korrekt funktioniert.
            string datenVerz = "PSDNET404_1";
            string quellePfad = Path.Combine(datenVerz, "vectorShapes.psd");
            string ausgabeDateiPfad = Path.Combine(datenVerz, "output_vectorShapes.psd");
            using (PsdImage bild = (PsdImage)Image.Load(quellePfad))
            {
                var ressource = GetVogkResource(bild);
                AssertAreEqual(1, ressource.ShapeOriginSettings.Length);
                var einstellung = ressource.ShapeOriginSettings[0];
                AssertAreEqual(true, einstellung.IsOriginIndexPresent);
                AssertAreEqual(false, einstellung.IsShapeInvalidatedPresent);
                AssertAreEqual(true, einstellung.IsOriginResolutionPresent);
                AssertAreEqual(true, einstellung.IsOriginTypePresent);
                AssertAreEqual(true, einstellung.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, einstellung.IsOriginRadiiRectanglePresent);
                AssertAreEqual(0, einstellung.OriginIndex);
                var ursprünglicheEinstellung = ressource.ShapeOriginSettings[0];
                ursprünglicheEinstellung.IsShapeInvalidated = true;
                ressource.ShapeOriginSettings = new[]
                {
                    ursprünglicheEinstellung,
                    new VectorShapeOriginSettings()
                    {
                        OriginIndex = 1,
                        OriginResolution = 144,
                        OriginType = 4,
                        OriginShapeBox = new VectorShapeBoundingBox()
                        {
                            Bounds = Rectangle.FromLeftTopRightBottom(10, 15, 40, 70)
                        }
                    },
                    new VectorShapeOriginSettings()
                    {
                        OriginIndex = 2,
                        OriginResolution = 301,
                        OriginType = 5,
                        OriginRadiiRectangle = new VectorShapeRadiiRectangle()
                        {
                            TopLeft = 2,
                            TopRight = 6,
                            BottomLeft = 23,
                            BottomRight = 42,
                            QuadVersion = 1
                        }
                    }
                };

                bild.Save(ausgabeDateiPfad, new PsdOptions());
            }

            using (PsdImage bild = (PsdImage)Image.Load(ausgabeDateiPfad))
            {
                var ressource = GetVogkResource(bild);
                AssertAreEqual(3, ressource.ShapeOriginSettings.Length);

                var einstellung = ressource.ShapeOriginSettings[0];
                AssertAreEqual(true, einstellung.IsOriginIndexPresent);
                AssertAreEqual(true, einstellung.IsShapeInvalidatedPresent);
                AssertAreEqual(true, einstellung.IsOriginResolutionPresent);
                AssertAreEqual(true, einstellung.IsOriginTypePresent);
                AssertAreEqual(true, einstellung.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, einstellung.IsOriginRadiiRectanglePresent);
                AssertAreEqual(0, einstellung.OriginIndex);
                AssertAreEqual(true, einstellung.IsShapeInvalidated);

                einstellung = ressource.ShapeOriginSettings[1];
                AssertAreEqual(true, einstellung.IsOriginIndexPresent);
                AssertAreEqual(false, einstellung.IsShapeInvalidatedPresent);
                AssertAreEqual(true, einstellung.IsOriginResolutionPresent);
                AssertAreEqual(true, einstellung.IsOriginTypePresent);
                AssertAreEqual(true, einstellung.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, einstellung.IsOriginRadiiRectanglePresent);
                AssertAreEqual(1, einstellung.OriginIndex);
                AssertAreEqual(144.0, einstellung.OriginResolution);
                AssertAreEqual(4, einstellung.OriginType);
                AssertAreEqual(Rectangle.FromLeftTopRightBottom(10, 15, 40, 70), einstellung.OriginShapeBox.Bounds);

                einstellung = ressource.ShapeOriginSettings[2];
                AssertAreEqual(true, einstellung.IsOriginIndexPresent);
                AssertAreEqual(false, einstellung.IsShapeInvalidatedPresent);
                AssertAreEqual(true, einstellung.IsOriginResolutionPresent);
                AssertAreEqual(true, einstellung.IsOriginTypePresent);
                AssertAreEqual(false, einstellung.IsOriginShapeBBoxPresent);
                AssertAreEqual(true, einstellung.IsOriginRadiiRectanglePresent);
                AssertAreEqual(2, einstellung.OriginIndex);
                AssertAreEqual(301.0, einstellung.OriginResolution);
                AssertAreEqual(5, einstellung.OriginType);
                AssertAreEqual(2.0, einstellung.OriginRadiiRectangle.TopLeft);
                AssertAreEqual(6.0, einstellung.OriginRadiiRectangle.TopRight);
                AssertAreEqual(23.0, einstellung.OriginRadiiRectangle.BottomLeft);
                AssertAreEqual(42.0, einstellung.OriginRadiiRectangle.BottomRight);
                AssertAreEqual(1, einstellung.OriginRadiiRectangle.QuadVersion);
            }

            VogkResource GetVogkResource(PsdImage bild)
            {
                var ebene = bild.Layers[1];

                VogkResource ressource = null;
                var ressourcen = ebene.Resources;
                for (int i = 0; i < ressourcen.Length; i++)
                {
                    if (ressourcen[i] is VogkResource)
                    {
                        ressource = (VogkResource)ressourcen[i];
                        break;
                    }
                }

                if (ressource == null)
                {
                    throw new Exception("VogkResource nicht gefunden.");
                }

                return ressource;
            }

            void AssertAreEqual(object erwartet, object tatsächlich, string nachricht = null)
            {
                if (!object.Equals(erwartet, tatsächlich))
                {
                    throw new FormatException(nachricht ?? "Die Objekte sind nicht gleich.");
                }
            }
{{< /highlight >}}

**PSDNET-752. Fehler beim Konvertieren von FillLayer in SmartObjectLayer**

{{< highlight csharp >}}
            string quelleDateiPfad = "effectlost.psd";
            string ausgabeDateiPfad = "output.psd";

            using (PsdImage psdBild = (PsdImage)Aspose.PSD.Image.Load(quelleDateiPfad))
            {
                SmartObjectLayer smartObject = psdBild.SmartObjectProvider.ConvertToSmartObject(0);

                psdBild.Save(ausgabeDateiPfad);
            }
{{< /highlight >}}

**PSDNET-778. LayerGroup fügt neue Ebenen in umgekehrter Reihenfolge hinzu**

{{< highlight csharp >}}
            void SindGleich(string erwartet, string tatsächlich)
            {
                if (!object.Equals(erwartet, tatsächlich))
                {
                    throw new Exception("Werte sind nicht gleich.");
                }
            }

            string ausgabeDatei = "output.psd";

            PsdOptions psdOptionen = new PsdOptions();
            psdOptionen.Source = new StreamSource(new MemoryStream());
            using (PsdImage psdBild = (PsdImage)Image.Create(psdOptionen, 100, 100))
            {
                LayerGroup ebenenGruppe = psdBild.AddLayerGroup("Ordner", 0, true);
                ebenenGruppe.AddLayer(new Layer() { DisplayName = "Ebene 1" });
                ebenenGruppe.AddLayer(new Layer() { DisplayName = "Ebene 2" });

                SindGleich("Ebene 1", ebenenGruppe.Layers[0].DisplayName);
                SindGleich("Ebene 2", ebenenGruppe.Layers[1].DisplayName);

                psdBild.Save(ausgabeDatei);
            }
{{< /highlight >}}

**PSDNET-790. Importieren eines Bildes in SmartObject-Layer führt zu einer PSD-Korruption**

{{< highlight csharp >}}
            const string basisOrdner = "PSDNET790_1\\";
            const string outputOrdner = basisOrdner + "output\\";

            // Testet, ob die Ebene, die aus einem Bild importiert wurde, in ein Smart Object-Layer konvertiert wird und die gespeicherte PSD-Datei korrekt ist.
            using (PsdImage bild = (PsdImage)Image.Load(basisOrdner + @"layerTest1.psd"))
            {

                string ebenenDateiPfad = basisOrdner + @"picture.jpg";
                string ausgabeDateiPfad = outputOrdner + "layerTest2.psd";
                string ausgabePngDateiPfad = Path.ChangeExtension(ausgabeDateiPfad, ".png");
                using (var stream = new FileStream(ebenenDateiPfad, FileMode.Open))
                {
                    Layer ebene = null;
                    try
                    {
                        ebene = new Layer(stream);
                        bild.AddLayer(ebene);
                    }
                    catch (Exception)
                    {
                        if (ebene != null)
                        {
                            ebene.Dispose();
                        }

                        throw;
                    }

                    var ebene2 = bild.Layers[2];
                    var ebene3 = bild.SmartObjectProvider.ConvertToSmartObject(bild.Layers.Length - 1);
                    var grenzen = ebene3.Bounds;
                    ebene3.Left = (bild.Width - ebene3.Width) / 2;
                    ebene3.Top = ebene2.Top;
                    ebene3.Right = ebene3.Left + grenzen.Width;
                    ebene3.Bottom = ebene3.Top + grenzen.Height;

                    bild.Save(ausgabeDateiPfad);
                    bild.Save(ausgabePngDateiPfad, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}

**PSDNET-809. Falsche Begrenzungen von Smart Object-Layern, wenn wir Smart Object-Inhalte durch die Datei ersetzen, die unterschiedliche Dimensionen und Auflösungen hat**

{{< highlight csharp >}}
            // Dieses Beispiel zeigt, dass die ReplaceContents-Methode korrekt funktioniert, wenn die neue Inhaltsdatei eine unterschiedliche Auflösung hat.
            const string basisOrdner = "PSDNET809_1\\";
            const string outputOrdner = basisOrdner + "output\\";
            const string dateiName = "CommonPsb.psd";
            const string dateiPfad = basisOrdner + dateiName; // Original PSD-Bild
            const string neueInhaltsPfad = basisOrdner + "image.jpg"; // Neue Inhaltsdatei für das Smart Object
            const string ausgabeDateiPfad = outputOrdner + "ChangedPsd";
            const string pngAusgabePfad = ausgabeDateiPfad + ".png"; // Die Ausgabe-PNG-Datei
            const string psdAusgabePfad = ausgabeDateiPfad + ".psd"; // Die Ausgabe-PSD-Datei
            using (PsdImage psdBild = (PsdImage)Image.Load(dateiPfad))
            {
                for (int i = 0; i < psdBild.Layers.Length; i++)
                {
                    var ebene = psdBild.Layers[i];
                    SmartObjectLayer smartObjectEbene = ebene as SmartObjectLayer;
                    if (smartObjectEbene != null)
                    {
                        smartObjectEbene.ReplaceContents(neueInhaltsPfad);

                        psdBild.Save(psdAusgabePfad);
                        psdBild.Save(pngAusgabePfad, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
                    }
                }
            }
{{< /highlight >}}

**PSDNET-810. Ausnahme beim Laden der Dateien**

{{< highlight csharp >}}
            string testDatei1 = "face.psd";
            string testDatei2 = "BigFile2.psd";

            using (var psdBild = (PsdImage)Image.Load(testDatei1))
            {
                // Datei erfolgreich geladen
            }

            using (var psdBild = (PsdImage)Image.Load(testDatei2))
            {
                // Datei erfolgreich geladen
            }
{{< /highlight >}}

**PSDNET-824. Falsche vogk-Ressource nach Laden und Speichern des PSD-Bildes mit Formebenen und Vektorpfaden**

{{< highlight csharp >}}
            // Dieses Beispiel zeigt, dass das Laden und Speichern des PSD-Bildes mit Formebenen und Vektorpfaden korrekt funktioniert und die Live Shape-Eigenschaften erhalten bleiben.
            string datenVerz = "PSDNET824_1\\";
            string quelleDatei = datenVerz + "vectorShapes.psd";
            string ausgabeDateiPfad = datenVerz + @"\output\vectorShapes.psd";
            using (PsdImage psd = (PsdImage)Image.Load(quelleDatei))
            {
                psd.Save(ausgabeDateiPfad);
            }

            // Überprüfen, ob die Live Shape-Eigenschaften in der Ausgabe-PSD-Datei in Adobe® Photoshop® vorhanden sind.
{{< /highlight >}}

**PSDNET-827. Ausnahme beim Laden von Referenzstrukturen und EnumeratedReferenceStructure-Strukturen**

{{< highlight csharp >}}
            string quelleDatei = "sourceFile.psd";
            string ausgabe = "output.psd";

            using (var psdBild = (PsdImage)Image.Load(quelleDatei))
            {
                // Datei erfolgreich geladen

                SmartObjectLayer ebene = (SmartObjectLayer)psdBild.Layers[1];
                SoLdResource ressource = (SoLdResource)ebene.Resources[9];

                DescriptorStructure struktur1 = (DescriptorStructure)ressource.Items[15];
                ListStructure struktur2 = (ListStructure)struktur1.Structures[5];
                DescriptorStructure str