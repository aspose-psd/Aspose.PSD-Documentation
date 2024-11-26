---
title: Aspose.PSD dla .NET 20.4 - Informacje o wersji
type: docs
weight: 90
url: /pl/net/aspose-psd-for-net-20-4-release-notes/
---

{{% alert color="primary" %}} 

Ta strona zawiera informacje o wersji [Aspose.PSD dla .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-567|Wsparcie dla zasobu 'Vector Origination Data'|Nowa funkcja|
|PSDNET-373|Wsparcie dla lclrResource (Ustawienia koloru arkusza)|Nowa funkcja|
|PSDNET-563|Wsparcie dla właściwości z danych LengthRecord. (Operacje ścieżkowe (operacje logiczne), indeks kształtu w warstwie, liczba rekordów węzłów krzywych)|Nowa funkcja|
|PSDNET-425|Wsparcie dla koloru tła sekcji obrazu zasobu #1010|Nowa funkcja|
|PSDNET-530|Dodawanie warstw wypełnienia w trakcie działania programu|Nowa funkcja|
|PSDNET-424|Wsparcie dla informacji o obramowaniu obrazu zasobu #1009|Nowa funkcja|
|PSDNET-592|Wsparcie dla warstw w plikach formatu AI|Nowa funkcja|
|PSDNET-256|Wsparcie dla odczytu i edycji efektu warstwy nakładki gradientu|Nowa funkcja|
|PSDNET-257|Renderowanie efektu warstwy nakładki gradientu|Nowa funkcja|
|PSDNET-585|Zmiany właściwości GradientOverlayEffect.BlendMode nie są wyświetlane w programie Photoshop|Błąd|
|PSDNET-561|Naprawa zapisywania obrazu PSD z kolorowym trybem Grayscale i 16 bitów na kanał do formatu PSD w skali szarości|Błąd|
|PSDNET-560|Naprawa zapisywania obrazu PSD z kolorowym trybem Grayscale i 16 bitów na kanał do formatu PNG|Błąd|

## **Zmiany w interfejsie publicznym**
# **Dodane interfejsy API:**
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Name
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsTemplate
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsLocked
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsShown
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPrinted
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPreview
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsImagesDimmed
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.DimValue
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorNumber
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Red
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Green
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Blue
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- T:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.Color
- T:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Width
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Unit
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.#ctor(System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.BezierKnotRecordsCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.ShapeIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.ShapeOriginSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.#ctor(System.Boolean,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidated
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.OriginIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.ExcludeOverlappingShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.CombineShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.SubtractFrontShape
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.IntersectShapeAreas
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.#ctor(Aspose.PSD.Color,System.Int32,System.Int32)
# **Usunięte interfejsy API:**
- Brak

## **Przykłady użycia:**

**PSDNET-567. Wsparcie dla zasobu 'Vector Origination Data'**

{{< highlight java >}}

         // Wsparcie dla zasobu VogkResource

        static void PrzykladWsparciaDlaVogkResource()

        {

            string nazwaPliku = "VectorOriginationDataResource.psd";

            string nazwaPlikuWyjsciowego = "out_VectorOriginationDataResource_.psd";

            using (var obrazPsd = (PsdImage)Image.Load(nazwaPliku))

            {

                var zasob = PobierzZasobVogk(obrazPsd);

                // Odczyt

                if (zasob.ShapeOriginSettings.Length != 1 ||

                    !zasob.ShapeOriginSettings[0].IsShapeInvalidated ||

                    zasob.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    throw new Exception("VogkResource został odczytany niepoprawnie.");

                }

                // Edycja

                zasob.ShapeOriginSettings = new[]

                {

                    zasob.ShapeOriginSettings[0],

                    new VectorShapeOriginSettings(true, 1)

                };

                obrazPsd.Save(nazwaPlikuWyjsciowego);

            }

        }

        static VogkResource PobierzZasobVogk(PsdImage obraz)

        {

            var warstwa = obraz.Layers[1];

            VogkResource zasob = null;

            var zasoby = warstwa.Resources;

            for (int i = 0; i < zasoby.Length; i++)

            {

                if (zasoby[i] is VogkResource)

                {

                    zasob = (VogkResource)zasoby[i];

                    break;

                }

            }

            if (zasob == null)

            {

                throw new Exception("Nie znaleziono zasobuVogk.");

            }

            return zasob;

        }   

{{< /highlight >}}

**PSDNET-373. Wsparcie dla lclrResource (Ustawienia koloru arkusza)**

{{< highlight java >}}

         static void SprawdzKoloryArkuszaIWsteczne(SheetColorHighlightEnum[] koloryArkusza, PsdImage obraz)

        {

            int liczbaWarstw = obraz.Layers.Length;

            for (int indeksWarstwy = 0; indeksWarstwy < liczbaWarstw; indeksWarstwy++)

            {

                Layer warstwa = obraz.Layers[indeksWarstwy];

                LayerResource[] zasoby = warstwa.Resources;

                foreach (LayerResource zasobWarstwy in zasoby)

                {

                    // Zasób lclrResource zawsze znajduje się na liście zasobów pliku psd.

                    LclrResource zasob = zasobWarstwy as LclrResource;

                    if (zasob != null)

                    {

                        if (zasob.Color != koloryArkusza[indeksWarstwy])

                        {

                            throw new Exception("Kolor arkusza został odczytany niepoprawnie");

                        }

                        // Odwrócenie kolorów arkusza. Ustawienie podświetlenia koloru warstwy.

                        zasob.Color = koloryArkusza[liczbaWarstw - indeksWarstwy - 1];

                        break;

                    }

                }

            }

        }

            string sciezkaPlikuZrodlowego = "AllLclrResourceColors.psd";

            string sciezkaPlikuWyjsciowego = "AllLclrResourceColorsReversed.psd";

            // W pliku kolory podświetlania warstw są w tej kolejności

            SheetColorHighlightEnum[] koloryArkusza = new SheetColorHighlightEnum[] {

                SheetColorHighlightEnum.Red,

                SheetColorHighlightEnum.Orange,

                SheetColorHighlightEnum.Yellow,

                SheetColorHighlightEnum.Green,

                SheetColorHighlightEnum.Blue,

                SheetColorHighlightEnum.Violet,

                SheetColorHighlightEnum.Gray,

                SheetColorHighlightEnum.NoColor

            };            

            // Kolor arkiusz jest używany do wizualnego wyróżnienia warstw. 

            // Na przykład można zaktualizować niektóre warstwy w pliku PSD, a następnie wyróżnić kolorem warstwę, na którą chcesz zwrócić uwagę.

            using (PsdImage obraz = (PsdImage)Image.Load(sciezkaPlikuZrodlowego))

            {

                SprawdzKoloryArkuszaIWsteczne(koloryArkusza, obraz);

                obraz.Save(sciezkaPlikuWyjsciowego, new PsdOptions());

            }

            using (PsdImage obraz = (PsdImage)Image.Load(sciezkaPlikuWyjsciowego))

            {

                // Kolory powinny być odwrócone

                Array.Reverse(koloryArkusza);

                SprawdzKoloryArkuszaIWsteczne(koloryArkusza, obraz);

            }

{{< /highlight >}}

**PSDNET-563. Wsparcie dla właściwości z danych LengthRecord. (Operacje ścieżkowe (operacje logiczne), indeks kształtu w warstwie, liczba rekordów węzłów krzywych)**

{{< highlight java >}}

            string nazwaPliku = "PathOperationsShape.psd";

            using (var obraz = (PsdImage)Image.Load(nazwaPliku))

            {

                VsmsResource zasob = null;

                foreach (var zasobWarstwy in obraz.Layers[1].Resources)

                {

                    if (zasobWarstwy is VsmsResource)

                    {

                        zasob = (VsmsResource)zasobWarstwy;

                        break;

                    }

                }

                LengthRecord lengthRecord0 = (LengthRecord)zasob.Paths[2];

                LengthRecord lengthRecord1 = (LengthRecord)zasob.Paths[7];

                LengthRecord lengthRecord2 = (LengthRecord)zasob.Paths[11];

                // Tu zmieniamy sposób łączenia kształtów.

                lengthRecord0.PathOperations = PathOperations.ExcludeOverlappingShapes;

                lengthRecord1.PathOperations = PathOperations.IntersectShapeAreas;

                lengthRecord2.PathOperations = PathOperations.SubtractFrontShape;

                obraz.Save("out_" + nazwaPliku);

            }

{{< /highlight >}}

**PSDNET-425. Wsparcie dla koloru tła sekcji obrazu zasobu #1010**

{{< highlight java >}}

             string plikZrodlowy = "input.psd";

            string plikWyjsciowy = "output.psd";

            using (var obraz = (PsdImage)Image.Load(plikZrodlowy))

            {

                ResourceBlock[] zasobyObrazu = obraz.ImageResources;

                BackgroundColorResource zasobKoloruTla = null;

                foreach (var zasobObrazu in zasobyObrazu)

                {

                    if (zasobObrazu is BackgroundColorResource)

                    {

                        zasobKoloruTla = (BackgroundColorResource)zasobObrazu;

                        break;

                    }

                }

                // aktualizacja BackgroundColorResource

                zasobKoloruTla.Color = Color.DarkRed;

                obraz.Save(plikWyjsciowy);

            }

{{< /highlight >}}

**PSDNET-530. Dodawanie warstw wypełnienia w trakcie działania programu**

{{< highlight java >}}

             string plikWyjsciowyPsd = "output.psd";

            using (var obraz = new PsdImage(100, 100))

            {

                FillLayer warstwaWypelnieniaKolorem = FillLayer.CreateInstance(FillType.Color);

                warstwaWypelnieniaKolorem.DisplayName = "Warstwa wypełnienia kolorem";

                obraz.AddLayer(warstwaWypelnieniaKolorem);

                FillLayer warstwaWypelnieniaGradientem = FillLayer.CreateInstance(FillType.Gradient);

                warstwaWypelnieniaGradientem.DisplayName = "Warstwa wypełnienia gradientem";

                obraz.AddLayer(warstwaWypelnieniaGradientem);

                FillLayer warstwaWypelnieniaWzorem = FillLayer.CreateInstance(FillType.Pattern);

                warstwaWypelnieniaWzorem.DisplayName = "Warstwa wypełnienia wzorem";

                warstwaWypelnieniaWzorem.Opacity = 50;

                obraz.AddLayer(warstwaWypelnieniaWzorem);

                obraz.Save(plikWyjsciowyPsd);

            }

{{< /highlight >}}

**PSDNET-424. Wsparcie dla informacji o obramowaniu obrazu zasobu #1009**

{{< highlight java >}}

             string plikZrodlowy = "input.psd";

            string plikWyjsciowy = "output.psd";

            using (var obraz = (PsdImage)Image.Load(plikZrodlowy))

            {

                ResourceBlock[] zasobyObrazu = obraz.ImageResources;

                BorderInformationResource zasobInformacjiObramowania = null;

                foreach (var zasobObrazu in zasobyObrazu)

                {

                    if (zasobObrazu is BorderInformationResource)

                    {

                        zasobInformacjiObramowania = (BorderInformationResource)zasobObrazu;

                        break;

                    }

                }

                // aktualizacja BorderInformationResource

                zasobInformacjiObramowania.Width = 0.1;

                zasobInformacjiObramowania.Unit = PhysicalUnit.Inches;

                obraz.Save(plikWyjsciowy);

            }

{{< /highlight >}}

**PSDNET-592. Wsparcie dla warstw w plikach formatu AI**

{{< highlight java >}}

         void SprawdzCzyPrawda(bool warunek, string komunikat)

        {

            if (!warunek)

            {

                throw new FormatException(komunikat