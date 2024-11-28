---
title: Wersja 19.5 Aspose.PSD dla .NET - Notatki dotyczące wydania
type: docs
weight: 80
url: /pl/net/aspose-psd-for-net-19-5-release-notes/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla Aspose.PSD dla .NET 19.5.

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-133|Dodano obsługę warstw wypełnienia: Wzór|Funkcja|
|PSDNET-138|Obsługa PtFlResource|Funkcja|
|PSDNET-129|Wprowadzenie poprawnej metody Kadrowania dla plików PSD|Funkcja|
|PSDNET-140|Obsługa VsmsResource|Funkcja|
|PSDNET-121|Widoczne warstwy w widocznym podfolderze w niewidocznym folderze są renderowane, ale nie powinny|Błąd|
|PSDNET-119|PSD (tryb RGB 16 bitów na kanał) nie jest właściwie konwertowany do JPG|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Linked
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PointType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternId
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternHeight
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternHeight
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.#ctor(System.String,System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Offset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.IsLinkedWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PatternId
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.TypeToolKey
- M:Aspose.PSD.Image.DoAfterCreate(System.Int64@,System.Int64)
- P:Aspose.PSD.ImageOptionsBase.BufferSizeHint
- M:Aspose.PSD.Metered.GetConsumptionCredit
# **Usunięte API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)

## **Przykłady użycia:**
**PSDNET-133. Dodaj obsługę warstw wypełnienia: Wzór**

{{< highlight java >}}

 // Dodaj obsługę warstw wypełnienia: Wzór

    string nazwaPlikuWejsciowego = "WarstwaWypelnieniaWzorem.psd";

    string sciezkaExportu = "WarstwaWypelnieniaWzorem_Edited.psd";

    double tolerancja = 0.0001;

    var obraz = (PsdImage)Image.Load(nazwaPlikuWejsciowego);

    using (obraz)

    {

         foreach (var warstwa in obraz.Layers)

         {

             if (warstwa is FillLayer)

             {

                  FillLayer warstwaWypelnienia = (FillLayer)warstwa;

                  PatternFillSettings ustawieniaWypelnienia = (PatternFillSettings)warstwaWypelnienia.FillSettings;

                  if (ustawieniaWypelnienia.HorizontalOffset != -46 || 

                      ustawieniaWypelnienia.VerticalOffset != -45 || 

                      ustawieniaWypelnienia.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5"||

                      ustawieniaWypelnienia.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares" ||

                      ustawieniaWypelnienia.AlignWithLayer != true ||

                      ustawieniaWypelnienia.Linked != true ||

                      ustawieniaWypelnienia.PatternHeight != 64 ||

                      ustawieniaWypelnienia.PatternWidth != 64 ||

                      ustawieniaWypelnienia.PatternData.Length != 4096 ||

                      Math.Abs(ustawieniaWypelnienia.Scale - 50) > tolerancja) 

                      {

                          throw new Exception("Obraz PSD został źle odczytany");

                      }

                  // Edycja 

                  ustawieniaWypelnienia.Scale = 300;

                  ustawieniaWypelnienia.HorizontalOffset = 2;

                  ustawieniaWypelnienia.VerticalOffset = -20;

                  ustawieniaWypelnienia.PatternData = new int[]

                  {

                       Color.Red.ToArgb(), Color.Blue.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Red.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Blue.ToArgb(),  Color.Red.ToArgb()

                  };

                  ustawieniaWypelnienia.PatternHeight = 3;

                  ustawieniaWypelnienia.PatternWidth = 3;

                  ustawieniaWypelnienia.AlignWithLayer = false;

                  ustawieniaWypelnienia.Linked = false;

                  ustawieniaWypelnienia.PatternId = Guid.NewGuid().ToString();

                  warstwaWypelnienia.Update();

                  break;

             }

         }

         obraz.Save(sciezkaExportu);

    }

{{< /highlight >}}

**PSDNET-138. Obsługa PtFlResource**

{{< highlight java >}}

  // Obsługa PtFlResource

    string nazwaPlikuWejsciowego = "WarstwaWypelnieniaWzorem.psd";

    string sciezkaExportu = "PtFlResource_Edited.psd";

    double tolerancja = 0.0001;

    var obraz = (PsdImage)Image.Load(nazwaPlikuWejsciowego);

    using (obraz)

    {

         foreach (var warstwa in obraz.Layers)

         {

             if (warstwa is FillLayer)

             {

                var warstwaWypelnienia = (FillLayer)warstwa;

                var zasoby = warstwaWypelnienia.Resources;

                foreach (var res in zasoby)

                {

                    if (res is PtFlResource)

                    {

                        // Odczyt

                        PtFlResource zasob = (PtFlResource)res;

                        if (

                            zasob.Offset.X != -46 || 

                            zasob.Offset.Y != -45 || 

                            zasob.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5\0" ||

                            zasob.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares\0" ||

                            zasob.AlignWithLayer != true ||

                            zasob.IsLinkedWithLayer != true ||

                            !(Math.Abs(zasob.Scale - 50) < tolerancja)) {

                                throw new Exception("Zasób PtFl został źle odczytany");

                            }

                        // Edycja

                        zasob.Offset = new Point(-11, 13);

                        zasob.Scale = 200;

                        zasob.AlignWithLayer = false;

                        zasob.IsLinkedWithLayer = false;

                        warstwaWypelnienia.Resources = warstwaWypelnienia.Resources;

                        // Nie mamy danych wzoru w PattResource, więc możemy je dodać.

                        var ustawieniaWypelnienia = (PatternFillSettings)warstwaWypelnienia.FillSettings;

                        ustawieniaWypelnienia.PatternData = new int[]

                        {

                            Color.Black.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                        };

                        ustawieniaWypelnienia.PatternHeight = 1;

                        ustawieniaWypelnienia.PatternWidth = 4;

                        ustawieniaWypelnienia.PatternName = "$$$/Presets/Patterns/VerticalLine=Vertical Line New\0";

                        ustawieniaWypelnienia.PatternId = Guid.NewGuid().ToString() + "\0";

                        warstwaWypelnienia.Update();

                    }

                    break;

                }

                break;

            }

         }

         obraz.Save(sciezkaExportu);

    } 

{{< /highlight >}}

**PSDNET-129. Wprowadzenie poprawnej metody Kadrowania dla plików PSD**

{{< highlight java >}}

             // Wprowadzenie poprawnej metody Kadrowania dla plików PSD.

            string nazwaPlikuWejsciowego = "1.psd";

            string sciezkaExportuPsd = "TestKadrowania.psd";

            string sciezkaExportuPng = "TestKadrowania.png";

            using (RasterImage obraz = Image.Load(nazwaPlikuWejsciowego) as RasterImage)

            {

                obraz.Crop(new Rectangle(10, 30, 100, 100));

                obraz.Save(sciezkaExportuPsd, new PsdOptions());

                obraz.Save(sciezkaExportuPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-140. Obsługa VsmsResource**

{{< highlight java >}}

 // Wsparcie dla VsmsResource

        static void PrzykladObslugiVsmsResource()

        {

            string nazwaPlikuWejsciowego = "PustyProstokat.psd";

            string sciezkaExportu = "PustyProstokat_zmieniony.psd";

            var obraz = (PsdImage)Image.Load(nazwaPlikuWejsciowego);

            using (obraz)

            {

                var zasob = GetVsmsResource(obraz);

                // Odczyt

                if (zasob.IsDisabled != false ||

                    zasob.IsInverted != false ||

                    zasob.IsNotLinked != false ||

                    zasob.Paths.Length != 7 ||

                    zasob.Paths[0].Type != VectorPathType.PathFillRuleRecord ||

                    zasob.Paths[1].Type != VectorPathType.InitialFillRuleRecord ||

                    zasob.Paths[2].Type != VectorPathType.ClosedSubpathLengthRecord ||

                    zasob.Paths[3].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    zasob.Paths[4].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    zasob.Paths[5].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked||

                    zasob.Paths[6].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked)

                {

                        throw new Exception("Zasób VsmsResource został źle odczytany");

                }

                var pathFillRule = (PathFillRuleRecord)zasob.Paths[0];

                var initialFillRule = (InitialFillRuleRecord)zasob.Paths[1];

                var subpathLength = (LengthRecord)zasob.Paths[2];

                // Reguła wypełnienia ścieżki nie zawiera dodatkowych informacji

                if (pathFillRule.Type != VectorPathType.PathFillRuleRecord || 

                initialFillRule.Type != VectorPathType.InitialFillRuleRecord ||

                initialFillRule.IsFillStartsWithAllPixels != false ||

                subpathLength.Type != VectorPathType.ClosedSubpathLengthRecord ||

                subpathLength.IsClosed != true ||

                subpathLength.IsOpen != false) 

                {

                    throw new Exception("Ścieżki VsmsResource zostały źle odczytane");

                }

                // Edycja

                zasob.IsDisabled = true;

                zasob.IsInverted = true;

                zasob.IsNotLinked = true;

                var bezierKnot = (BezierKnotRecord)zasob.Paths[3];

                bezierKnot.Points[0] = new Point(0, 0);

                bezierKnot = (BezierKnotRecord)zasob.Paths[4];

                bezierKnot.Points[0] = new Point(8039798, 10905191);

                initialFillRule.IsFillStartsWithAllPixels = true;

                subpathLength.IsClosed = false;

                obraz.Save(sciezkaExportu);

            }         

        }

        static VsmsResource GetVsmsResource(PsdImage obraz)

        {

            var warstwa = obraz.Layers[1];

            VsmsResource zasob = null;

            var zasoby = warstwa.Resources;

            for (int i = 0; i < zasoby.Length; i++)

            {

                if (zasoby[i] is VsmsResource)

                {

                    zasob = (VsmsResource)zasoby[i];

                    break;

                }

            }

            if (zasob == null)

            {

                throw new Exception("Zasób VsmsResource nie został znaleziony");

            }

            return zasob;

        }   

{{< /highlight >}}

**PSDNET-121: Widoczne warstwy w widocznym podfolderze w niewidocznym folderze są renderowane, ale nie powinny**

{{< highlight java >}}

 // Widoczne warstwy w widocznym podfolderze w niewidocznym folderze są renderowane, ale nie powinny

            string nazwaPlikuWejsciowego = "WieleFolderow.psd.psd";

            string sciezkaWyjsciaJpg = "outWieleFolderow.jpg";

            string sciezkaWyjsc