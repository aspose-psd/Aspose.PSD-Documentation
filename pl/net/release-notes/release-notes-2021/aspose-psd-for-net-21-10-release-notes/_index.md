---
title: Notatki wydania Aspose.PSD dla .NET 21.10
type: docs
weight: 30
url: /pl/net/notatki-wydania-aspose-psd-dla-net-21-10/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 21.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-128|Wsparcie dla mechanizmu inteligentnych filtrów|Funkcja|
|PSDNET-414|Wsparcie dla Fxid/FEidResource|Funkcja|
|PSDNET-556|Błąd podczas ładowania AliasStructure|Błąd|
|PSDNET-948|Zmiana czcionki i koloru dla warstwy tekstowej PSD|Błąd|
|PSDNET-971|Dodanie możliwości własnego tworzenia warstwy z maską wektorową|Udoskonalenie|

## **Zmiany w publicznym API**
# **Dodane API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.SmartFilters
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.Distribution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.AmountNoise
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.IsMonochromatic
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.Radius
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution.Uniform
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution.Gaussian
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.IsEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.BlendMode
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Apply(Aspose.PSD.RasterImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.ApplyToMask(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.OnLoad
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Clone
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.sourceDescriptor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter.FilterId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsValidAtPosition
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskExtendWithWhite
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.Filters
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.UpdateResourceValues
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.#ctor(System.Int32,System.Int32,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.FilterEffectMasks
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Length
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.FEidTypeToolKey
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.FXidTypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.#ctor(System.String,Aspose.PSD.Rectangle,System.Int32,System.Int32,Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation[],Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation,Aspose.PSD.Rectangle,Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.GUID
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Rectangle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.PixelsDepth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.MaxChannels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Channels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.UserMask
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.MaskRectangle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.SheetMask
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.SaveData(Aspose.PSD.StreamContainer)

# **Usunięte API:**
- Brak

## **Przykłady użycia:**

**PSDNET-128. Wsparcie dla mechanizmu inteligentnych filtrów**

{{< highlight csharp >}}
            string sourceFilte = "r2_SmartFilters.psd";
            string outputPsd = "out_r2_SmartFilters.psd";

            void AssertAreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Obiekty nie są równe.");
                }
            }

            using (var image = (PsdImage)Image.Load(sourceFilte))
            {
                SmartObjectLayer smartObj = (SmartObjectLayer)image.Layers[1];

                // edytuj inteligentne filtry
                GaussianBlurSmartFilter gaussianBlur = (GaussianBlurSmartFilter)smartObj.SmartFilters.Filters[0];

                // sprawdź wartości filtra
                AssertAreEqual(3.1, gaussianBlur.Radius);
                AssertAreEqual(BlendMode.Dissolve, gaussianBlur.BlendMode);
                AssertAreEqual(90d, gaussianBlur.Opacity);
                AssertAreEqual(true, gaussianBlur.IsEnabled);

                // zaktualizuj wartości filtra
                gaussianBlur.Radius = 1;
                gaussianBlur.BlendMode = BlendMode.Divide;
                gaussianBlur.Opacity = 75;
                gaussianBlur.IsEnabled = false;
                AddNoiseSmartFilter addNoise = (AddNoiseSmartFilter)smartObj.SmartFilters.Filters[1];
                addNoise.Distribution = NoiseDistribution.Uniform;

                // dodaj nowe filtry
                var filtry = new List<SmartFilter>(smartObj.SmartFilters.Filters);
                filtry.Add(new GaussianBlurSmartFilter());
                filtry.Add(new AddNoiseSmartFilter());
                smartObj.SmartFilters.Filters = filtry.ToArray();

                // zastosuj zmiany
                smartObj.SmartFilters.UpdateResourceValues();

                // Zastosuj filtry
                smartObj.SmartFilters.Filters[0].Apply(image.Layers[2]);
                smartObj.SmartFilters.Filters[4].ApplyToMask(image.Layers[2]);

                image.Save(outputPsd);
            }

            using (var image = (PsdImage)Image.Load(outputPsd))
            {
                SmartObjectLayer smartObj = (SmartObjectLayer)image.Layers[1];

                GaussianBlurSmartFilter gaussianBlur = (GaussianBlurSmartFilter)smartObj.SmartFilters.Filters[0];

                // sprawdź wartości filtra
                AssertAreEqual(1d, gaussianBlur.Radius);
                AssertAreEqual(BlendMode.Divide, gaussianBlur.BlendMode);
                AssertAreEqual(75d, gaussianBlur.Opacity);
                AssertAreEqual(false, gaussianBlur.IsEnabled);

                AssertAreEqual(true, smartObj.SmartFilters.Filters[5] is GaussianBlurSmartFilter);
                AssertAreEqual(true, smartObj.SmartFilters.Filters[6] is AddNoiseSmartFilter);
            }
{{< /highlight >}}

**PSDNET-414. Wsparcie dla Fxid/FEidResource**

{{< highlight csharp >}}
            string inputFilePath = "psdnet414_3.psd";
            string output = "out_psdnet414_3.psd";

            int resLength = 1144;
            int maskLength = 369;

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Obiekty nie są równe.");
                }
            }

            using (var psdImage = (PsdImage)Image.Load(inputFilePath))
            {
                FXidResource fXidResource = (FXidResource)psdImage.GlobalLayerResources[3];

                AssertAreEqual(resLength, fXidResource.Length);
                foreach (var maskData in fXidResource.FilterEffectMasks)
                {
                    AssertAreEqual(maskLength, maskData.Length);
                }

                psdImage.Save(output);
            }

            // sprawdź po zapisaniu
            using (var psdImage = (PsdImage)Image.Load(output))
            {
                FXidResource fXidResource = (FXidResource)psdImage.GlobalLayerResources[3];

                AssertAreEqual(resLength, fXidResource.Length);
                foreach (var maskData in fXidResource.FilterEffectMasks)
                {
                    AssertAreEqual(maskLength, maskData.Length);
                }
            }
{{< /highlight >}}

**PSDNET-556. Błąd podczas ładowania AliasStructure**

{{< highlight csharp >}}
            string srcFile = "Aspose.psd";
            string outputPsd = "out_Aspose.psd";
            string outputPng = "out_Aspose.png";

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Obiekty nie są równe.");
                }
            }

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                LnkeResource lnkeResource = (LnkeResource)image.GlobalLayerResources[3];
                LiFeDataSource dataSource = (LiFeDataSource)lnkeResource[0];
                AssertAreEqual(2484L, dataSource.Length);

                foreach (var warstwa in image.Layers)
                {
                    if (warstwa is TextLayer)
                    {
                        TextLayer textLayer = warstwa as TextLayer;
                        textLayer.UpdateText("Test", Aspose.PSD.Color.Black);
                    }
                }

                image.Save(outputPsd);
                image.Save(outputPng, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
            }
{{< /highlight >}}

**PSDNET-948. Zmień czcionkę i kolor dla warstwy tekstowej PSD**

{{< highlight csharp >}}
            string sourceFileName = "fontExamples948.psd";
            string testFontsFolder = "Fonts";
            string outputPng = "output.png";

            FontSettings.SetFontsFolder(testFontsFolder);

            using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFileName))
            {
                foreach (var warstwa in image.Layers)
                {
                    var warstwaTekstu = warstwa as TextLayer;
                    if (warstwaTekstu != null)
                    {
                        ITextPortion kawalekTekstu = warstwaTekstu.TextData.Items[0];
                        kawalekTekstu.Style.FillColor = Color.BlueViolet;

                        warstwaTekstu.TextData.UpdateLayerData();
                    }
                }

                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-971. Dodanie możliwości tworzenia warstwy z maską wektorową**

{{< highlight csharp >}}
        public void CreatingVectorPathExample()
        {
            string fileName = "PathExample2.psd";

            string outputPsd = "out_CreatingVectorPathExampleTest.psd";
            string outputPng = "out_CreatingVectorPathExampleTest.png";

            using (var psdImage = (PsdImage)Image.Load(fileName))
            {
                VectorDataProvider.RemoveVectorPathDataFromLayer(psdImage.Layers[2]);

                // tworzenie obiektu VectorPath dla istniejącej warstwy bez danych ścieżki wektorowej.
                VectorPath vectorPath = VectorDataProvider.CreateVectorPathForLayer(psdImage.Layers[1]);

                // Ustaw kolor wypełnienia ścieżki wektorowej
                vectorPath.FillColor = Color.MediumPurple;

                // dodaj nowy kształt
                PathShape newShape = new PathShape();
                newShape.Points.Add(new BezierKnot(new PointF(65, 175), true));
                newShape.Points.Add(new BezierKnot(new PointF(65, 210), true));
                newShape.Points.Add(new BezierKnot(new PointF(190, 210), true));
                newShape.Points.Add(new BezierKnot(new PointF(190, 175), true));
                vectorPath.Shapes.Add(newShape);

                // zaktualizuj dane ścieżki w warstwie
                VectorDataProvider.UpdateLayerFromVectorPath(psdImage.Layers[1], vectorPath, true);


                // tworzenie obiektu VectorPath dla nowej warstwy.
                FillLayer layer2 = FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color);
                layer2.DisplayName = "Layer 2";
                psdImage.AddLayer(layer2);
                VectorPath vectorPath2 = VectorDataProvider.CreateVectorPathForLayer(layer2);

                // Ustaw kolor wypełnienia ścieżki wektorowej
                vectorPath2.FillColor = Color.IndianRed;

                // dodaj nowy kształt
                PathShape newShape2 = new PathShape();
                newShape2.Points.Add(new BezierKnot(new PointF(50, 150), true));
                newShape2.Points.Add(new BezierKnot(new PointF(100, 200), true));
                newShape2.Points.Add(new BezierKnot(new PointF(0, 200```)
                vectorPath2.Shapes.Add(newShape2);

                // zaktualizuj dane ścieżki w warstwie
                VectorDataProvider.UpdateLayerFromVectorPath(layer2, vectorPath2, true);

                psdImage.Save(outputPsd);
                psdImage.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
            }
        }


    #region Edytor ścieżki wektorowej (Tutaj umieszczone są klasy do edycji ścieżek wektorowych).

    /// <summary>
    /// Klasa zapewniająca pracę między <see cref="Warstwa"/> a <see cref="VectorPath"/>.
    /// </summary>
    public static class VectorDataProvider
    {
        /// <summary>
        /// Tworzy instancję <see cref="VectorPath"/> na podstawie zasobów z warstwy wejściowej.
        /// </summary>
        /// <param name="psdLayer">Warstwa psd.</param>
        /// <returns>instancję <see cref="VectorPath"/> na podstawie zasobów z warstwy wejściowej.</returns>
        public static VectorPath CreateVectorPathForLayer(Warstwa psdLayer)
        {
            VectorPathDataResource pathResource = FindVectorPathDataResource(psdLayer, true);
            SoCoResource socoResource = FindSoCoResource(psdLayer, true);
            VectorPath vectorPath = new VectorPath(pathResource);
            if (socoResource != null)
            {
                vectorPath.FillColor = socoResource.Color;
            }

            return vectorPath;
        }

        /// <summary>
        /// Aktualizuje zasoby warstwy wejściowej z instancji <see cref="VectorPath"/>, lub zamienia je na nowy zasób ścieżki i aktualizuje.
        /// </summary>
        /// <param name="psdLayer">Warstwa psd.</param>
        /// <param name="vectorPath">Ścieżka wektorowa.</param>
        /// <param name="createIfNotExist">Jeśli zasoby nie istnieją, dla <see cref="true"/> tworzy nowy zasób, w przeciwnym razie zwraca <see cref="null"/>.</param>
        public static void UpdateLayerFromVectorPath(Warstwa psdLayer, VectorPath vectorPath, bool createIfNotExist = false)
        {
            VectorPathDataResource pathResource = FindVectorPathDataResource(psdLayer, createIfNotExist);
            VogkResource vogkResource = FindVogkResource(psdLayer, createIfNotExist);
            SoCoResource socoResource = FindSoCoResource(psdLayer, createIfNotExist);

            UpdateResources(pathResource, vogkResource, socoResource, vectorPath);

            ReplaceVectorPathDataResourceInLayer(psdLayer, pathResource, vogkResource, socoResource);
        }

        /// <summary>
        /// Usuwa dane ścieżki wektorowej z warstwy wejściowej.
        /// </summary>
        /// <param name="psdLayer">Warstwa psd.</param>
        public static void RemoveVectorPathDataFromLayer(Warstwa psdLayer)
        {
            List<LayerResource> oldResources = new List<LayerResource>(psdLayer.Resources);
            List<LayerResource> newResources = new List<LayerResource>();
            for (int i = 0; i < oldResources.Count; i++)
            {
                LayerResource resource = oldResources[i];

                if (resource is VectorPathDataResource || resource is VogkResource || resource is SoCoResource)
                {
                    continue;
                }
                else
                {
                    newResources.Add(resource);
                }
            }

            psdLayer.Resources = newResources.ToArray();
        }

        /// <summary>
        /// Aktualizuje dane zasobów z instancji <see cref="VectorPath"/>.
        /// </summary>
        /// <param name="pathResource">Zasób ścieżki.</param>
        /// <param name="vogkResource">Zasób danych oryginalnych ścieżki wektorowej.</param>
        /// <param name="socoResource">Zasób koloru jednolitego.</param>
        /// <param name="vectorPath">Ścieżka wektorowa.</param>
        private static void UpdateResources(VectorPathDataResource pathResource, VogkResource vogkResource, SoCoResource socoResource, VectorPath vectorPath)
        {
            pathResource.Version = vectorPath.Version;
            pathResource.IsNotLinked = vectorPath.IsNotLinked;
            pathResource.IsDisabled = vectorPath.IsDisabled;
            pathResource.IsInverted = vectorPath.IsInverted;

            List<VectorShapeOriginSettings> originSettings = new List<VectorShapeOriginSettings>();
            List<VectorPathRecord> path = new List<VectorPathRecord>();
            path.Add(new PathFillRuleRecord(null));
            path.Add(new InitialFillRuleRecord(vectorPath.IsFillStartsWithAllPixels));
            for (ushort i = 0; i < vectorPath.Shapes.Count; i++)
            {
                PathShape shape = vectorPath.Shapes[i];
                shape.ShapeIndex = i;
                path.AddRange(shape.ToVectorPathRecords());
                originSettings.Add(new VectorShapeOriginSettings() { IsShapeInvalidated = true, OriginIndex = i });
            }

            pathResource.Paths = path.ToArray();
            vogkResource.ShapeOriginSettings = originSettings.ToArray();

            socoResource.Color = vectorPath.FillColor;
        }

        /// <summary>
        /// Zamienia zasoby w warstwie na zaktualizowane lub nowe.
        /// </summary>
        /// <param name="psdLayer">Warstwa psd.</param>
        /// <param name="pathResource">Zasób ścieżki.</param>
        /// <param name="vogkResource">Zasób danych oryginalnych ścieżki wektorowej.</param>
        /// <param name="socoResource">Zasób koloru jednolitego.</param>
        private static void ReplaceVectorPathDataResourceInLayer(Warstwa psdLayer, VectorPathDataResource pathResource, VogkResource vogkResource, SoCoResource socoResource)
        {
            bool pathResourceExist = false;
            bool vogkResourceExist = false;
            bool socoResourceExist = false;

            List<LayerResource> resources = new List<LayerResource>(psdLayer.Resources);
            for (int i = 0; i < resources.Count; i++)
            {
                LayerResource resource = resources[i];
                if (resource is VectorPathDataResource)
                {
                    resources[i] = pathResource;
                    pathResourceExist = true;
                }
                else if (resource is VogkResource)
                {
                    resources[i] = vogkResource;
                    vogkResourceExist = true;
                }
                else if (resource is SoCoResource)
                {
                    resources[i] = socoResource;
                    socoResourceExist = true;
                }
            }

            if (!pathResourceExist)
            {
                resources.Add(pathResource);
            }

            if (!vogkResourceExist)
            {
                resources.Add(vogkResource);
            }

            if (!socoResourceExist)
            {
                resources.Add(socoResource);
            }

            psdLayer.Resources = resources.ToArray();
        }

        /// <summary>
        /// Znajduje zasób <see cref="VectorPathDataResource"/> w zasobach warstwy wejściowej.
        /// </summary>
        /// <param name="psdLayer">Warstwa psd.</param>
        /// <param name="createIfNotExist">Jeśli zasób nie istnieje, dla <see cref="true"/> tworzy nowy zasób, w przeciwnym razie zwraca <see cref="null"/>.</param>
        /// <returns>Zasób <see cref="VectorPathDataResource"/>.</returns>
        private static VectorPathDataResource FindVectorPathDataResource(Warstwa psdLayer, bool createIfNotExist)
        {
            VectorPathDataResource pathResource = null;
            foreach (var resource in psdLayer.Resources)
            {
                if (resource is VectorPathDataResource)
                {
                    pathResource = (VectorPathDataResource)resource;
                    break;
                }
            }

            if (createIfNotExist && pathResource == null)
            {
                pathResource = new VmskResource();
            }

            return pathResource;
        }

        /// <summary>
        /// Znajduje zasób <see cref="VogkResource"/> w zasobach warstwy wejściowej.
        /// </summary>
        /// <param name="psdLayer">Warstwa psd.</param>
        /// <param name="createIfNotExist">Jeśli zasób nie istnieje, dla <see cref="true"/> tworzy nowy zasób, w przeciwnym razie zwraca <see cref="null"/>.</param>
        /// <returns>Zasób <see cref="VogkResource"/>.</returns>
        private static VogkResource FindVogkResource(Warstwa psdLayer, bool createIfNotExist)
        {
            VogkResource vogkResource = null;
            foreach (var resource in psdLayer.Resources)
            {
                if (resource is VogkResource)
                {
                    vogkResource = (VogkResource)resource;
                    break;
                }
            }

            if (createIfNotExist && vogkResource == null)
            {
                vogkResource = new VogkResource();
            }

            return vogkResource;
        }

        /// <summary>
        /// Znajduje zasób <see cref="SoCoResource"/> w zasobach warstwy wejściowej.
        /// </summary>
        /// <param name="psdLayer">Warstwa psd.</param>
        /// <param name="createIfNotExist">Jeśli zasób nie istnieje, dla <see cref="true"/> tworzy nowy zasób, w przeciwnym razie zwraca <see cref="null"/>.</param>
        /// <returns>Zasób <see cref="SoCoResource"/>.</returns>
        private static SoCoResource FindSoCoResource(Warstwa psdLayer, bool createIfNotExist)
        {
            SoCoResource socoResource = null;
            foreach (var resource in psdLayer.Resources)
            {
                if (resource is SoCoResource)
                {
                    socoResource = (SoCoResource)resource;
                    break;
                }
            }

            if (createIfNotExist && socoResource == null)
            {
                socoResource = new SoCoResource();
            }

            return socoResource;
        }
    }

    /// <summary>
    /// Węzeł krzywej Beziera, zawiera jeden punkt kotwicy i dwa punkty kontrolne.
    /// </summary>
    public class BezierKnot
    {
        /// <summary>
        /// Inicjalizuje nową instancję klasy <see cref="BezierKnot" />.
        /// </summary>
        /// <param name="anchorPoint">Punkt kotwicy.</param>
        /// <param name="controlPoint1">Pierwszy punkt kontrolny.</param>
        /// <param name="controlPoint2">Drugi punkt kontrolny.</param>
        /// <param name="isLinked">Wartość wskazująca, czy ten węzeł jest połączony.</param>
        public BezierKnot(PointF anchorPoint, PointF controlPoint1, PointF controlPoint2, bool isLinked)
        {
            this.AnchorPoint = anchorPoint;
            this.ControlPoint1 = controlPoint1;
            this.ControlPoint2 = controlPoint2;
            this.IsLinked = isLinked;
        }

        /// <summary>
        /// Inicjalizuje nową instancję klasy <see cref="BezierKnot" /> na podstawie <see cref="BezierKnotRecord"/>.
        /// </summary>
        /// <param name="bezierKnotRecord">Rekord <see cref="BezierKnotRecord"/>.</param>
        public BezierKnot(BezierKnotRecord bezierKnotRecord)
        {
```