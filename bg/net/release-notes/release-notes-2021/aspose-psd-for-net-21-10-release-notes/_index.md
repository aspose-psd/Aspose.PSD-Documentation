---
title: Aspose.PSD за .NET 21.10 - Бележки за изданието
type: docs
weight: 30
url: /bg/net/aspose-psd-for-net-21-10-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 21.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-128|Поддръжка на механизма за интелигентни филтри|Функционалност|
|PSDNET-414|Поддръжка на Fxid/FEidResource|Функционалност|
|PSDNET-556|Грешка при зареждане на AliasStructure|Проблем|
|PSDNET-948|Промяна на шрифта и цвета на TextLayer PSD|Проблем|
|PSDNET-971|Добавяне на възможност за персонализирано създаване на слой с векторна маска|Подобрение|

## **Промени в публичния API**
# **Добавени API:**
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

# **Премахнати API:**
- Няма

## **Примери за използване:**

**PSDNET-128. Поддръжка на механизма за интелигентни филтри**

{{< highlight csharp >}}
           // код на C# - пример за използване   
{{< /highlight >}}

**PSDNET-414. Поддръжка на Fxid/FEidResource**

{{< highlight csharp >}}
           // код на C# - пример за използване   
{{< /highlight >}}

**PSDNET-556. Грешка при зареждане на AliasStructure**

{{< highlight csharp >}}
           // код на C# - пример за използване   
{{< /highlight >}}

**PSDNET-948. Промяна на шрифта и цвета на TextLayer PSD**

{{< highlight csharp >}}
           // код на C# - пример за използване   
{{< /highlight >}}

**PSDNET-971. Добавяне на възможност за персонализирано създаване на слой с векторна маска**

{{< highlight csharp >}}
           // код на C# - пример за използване   
{{< /highlight >}}
**PSDNET-128. Поддръжка на механизма за интелигентни филтри**

{{< highlight csharp >}}
            // код на C# - пример за използване  
{{< /highlight >}}

**PSDNET-414. Поддръжка на Fxid/FEidResource**

{{< highlight csharp >}}
            // код на C# - пример за използване    
{{< /highlight >}}

**PSDNET-556. Грешка при зареждане на AliasStructure**

{{< highlight csharp >}}
            // код на C# - пример за използване    
{{< /highlight >}}

**PSDNET-948. Промяна на шрифта и цвета на TextLayer PSD**

{{< highlight csharp >}}
            // код на C# - пример за използване    
{{< /highlight >}}

**PSDNET-971. Добавяне на възможност за персонализирано създаване на слой с векторна маска**

{{< highlight csharp >}}
            // код на C# - пример за използване    
{{< /highlight >}}**PSDNET-128. Поддръжка на механизма за интелигентни филтри**

{{< highlight csharp >}}
            string sourceFilte = "r2_SmartFilters.psd";
            string outputPsd = "out_r2_SmartFilters.psd";

            void AssertAreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Обектите не са еднакви.");
                }
            }

            using (var image = (PsdImage)Image.Load(sourceFilte))
            {
                SmartObjectLayer smartObj = (SmartObjectLayer)image.Layers[1];

                // редакция на интелигентни филтри
                GaussianBlurSmartFilter gaussianBlur = (GaussianBlurSmartFilter)smartObj.SmartFilters.Filters[0];

                // проверка на стойности на филтъра
                AssertAreEqual(3.1, gaussianBlur.Radius);
                AssertAreEqual(BlendMode.Dissolve, gaussianBlur.BlendMode);
                AssertAreEqual(90d, gaussianBlur.Opacity);
                AssertAreEqual(true, gaussianBlur.IsEnabled);

                // актуализиране на стойностите на филтъра
                gaussianBlur.Radius = 1;
                gaussianBlur.BlendMode = BlendMode.Divide;
                gaussianBlur.Opacity = 75;
                gaussianBlur.IsEnabled = false;
                AddNoiseSmartFilter addNoise = (AddNoiseSmartFilter)smartObj.SmartFilters.Filters[1];
                addNoise.Distribution = NoiseDistribution.Uniform;

                // добавяне на нови елементи на филтърите
                var filters = new List<SmartFilter>(smartObj.SmartFilters.Filters);
                filters.Add(new GaussianBlurSmartFilter());
                filters.Add(new AddNoiseSmartFilter());
                smartObj.SmartFilters.Filters = filters.ToArray();

                // приложение на промените
                smartObj.SmartFilters.UpdateResourceValues();

                // Приложи филтрите
                smartObj.SmartFilters.Filters[0].Apply(image.Layers[2]);
                smartObj.SmartFilters.Filters[4].ApplyToMask(image.Layers[2]);

                image.Save(outputPsd);
            }

            using (var image = (PsdImage)Image.Load(outputPsd))
            {
                SmartObjectLayer smartObj = (SmartObjectLayer)image.Layers[1];

                GaussianBlurSmartFilter gaussianBlur = (GaussianBlurSmartFilter)smartObj.SmartFilters.Filters[0];

                // проверка на стойности на филтъра
                AssertAreEqual(1d, gaussianBlur.Radius);
                AssertAreEqual(BlendMode.Divide, gaussianBlur.BlendMode);
                AssertAreEqual(75d, gaussianBlur.Opacity);
                AssertAreEqual(false, gaussianBlur.IsEnabled);

                AssertAreEqual(true, smartObj.SmartFilters.Filters[5] is GaussianBlurSmartFilter);
                AssertAreEqual(true, smartObj.SmartFilters.Filters[6] is AddNoiseSmartFilter);
            }
{{< /highlight >}}

**PSDNET-414. Поддръжка на Fxid/FEidResource**

{{< highlight csharp >}}
            string inputFilePath = "psdnet414_3.psd";
            string output = "out_psdnet414_3.psd";

            int resLength = 1144;
            int maskLength = 369;

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Обектите не са еднакви.");
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

            // проверка след запазване
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

**PSDNET-556. Грешка при зареждане на AliasStructure**

{{< highlight csharp >}}
            string srcFile = "Aspose.psd";
            string outputPsd = "out_Aspose.psd";
            string outputPng = "out_Aspose.png";

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Обектите не са еднакви.");
                }
            }

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                LnkeResource lnkeResource = (LnkeResource)image.GlobalLayerResources[3];
                LiFeDataSource dataSource = (LiFeDataSource)lnkeResource[0];
                AssertAreEqual(2484L, dataSource.Length);

                foreach (var layer in image.Layers)
                {
                    if (layer is TextLayer)
                    {
                        TextLayer textLayer = layer as TextLayer;
                        textLayer.UpdateText("Тест", Aspose.PSD.Color.Black);
                    }
                }

                image.Save(outputPsd);
                image.Save(outputPng, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
            }
{{< /highlight >}}

**PSDNET-948. Промяна на шрифта и цвета на TextLayer PSD**

{{< highlight csharp >}}
            string sourceFileName = "fontExamples948.psd";
            string testFontsFoler = "Fonts";
            string outputPng = "output.png";

            FontSettings.SetFontsFolder(testFontsFoler);

            using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFileName))
            {
                foreach (var layer in image.Layers)
                {
                    var textLayer = layer as TextLayer;
                    if (textLayer != null)
                    {
                        ITextPortion textPortion = textLayer.TextData.Items[0];
                        textPortion.Style.FillColor = Color.BlueViolet;

                        textLayer.TextData.UpdateLayerData();
                    }
                }

                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}} 

**PSDNET-971. Добавяне на възможност за персонализирано създаване на слой с векторна маска**

{{< highlight csharp >}}
        public void CreatingVectorPathExample()
        {
            string fileName = "PathExample2.psd";

            string outputPsd = "out_CreatingVectorPathExampleTest.psd";
            string outputPng = "out_CreatingVectorPathExampleTest.png";

            using (var psdImage = (PsdImage)Image.Load(fileName))
            {
                VectorDataProvider.RemoveVectorPathDataFromLayer(psdImage.Layers[2]);

                // създаване на обект VectorPath за съществуващ слой без данни за векторен път.
                VectorPath vectorPath = VectorDataProvider.CreateVectorPathForLayer(psdImage.Layers[1]);

                // Задайте цвета за попълване на векторния път
                vectorPath.FillColor = Color.MediumPurple;

                // добавяне на нова форма
                PathShape newShape = new PathShape();
                newShape.Points.Add(new BezierKnot(new PointF(65, 175), true));
                newShape.Points.Add(new BezierKnot(new PointF(65, 210), true));
                newShape.Points.Add(new BezierKnot(new PointF(190, 210), true));
                newShape.Points.Add(new BezierKnot(new PointF(190, 175), true));
                vectorPath.Shapes.Add(newShape);

                // актуализиране на пътните данни в слоя
                VectorDataProvider.UpdateLayerFromVectorPath(psdImage.Layers[1], vectorPath, true);


                // създаване на обект VectorPath за нов слой.
                FillLayer layer2 = FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color);
                layer2.DisplayName = "Layer 2";
                psdImage.AddLayer(layer2);
                VectorPath vectorPath2 = VectorDataProvider.CreateVectorPathForLayer(layer2);

                // Задайте цвета за попълване на векторния път
                vectorPath2.FillColor = Color.IndianRed;

                // добавяне на нова форма
                PathShape newShape2 = new PathShape();
                newShape2.Points.Add(new BezierKnot(new PointF(50, 150), true));
                newShape2.Points.Add(new BezierKnot(new PointF(100, 200), true));
                newShape2.Points.Add(new BezierKnot(new PointF(0, 200), true));
                vectorPath2.Shapes.Add(newShape2);

                // актуализиране на пътните данни в слоя
                VectorDataProvider.UpdateLayerFromVectorPath(layer2, vectorPath2, true);

                psdImage.Save(outputPsd);
                psdImage.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
            }
        }
{{< /highlight >}}**PSDNET-128. Поддръжка на механизма за интелигентни филтри**

{{< highlight csharp >}}
        public void CreatingVectorPathExample()
        {
            string fileName = "PathExample2.psd";

            string outputPsd = "out_CreatingVectorPathExampleTest.psd";
            string outputPng = "out_CreatingVectorPathExampleTest.png";

            using (var psdImage = (PsdImage)Image.Load(fileName))
            {
                VectorDataProvider.RemoveVectorPathDataFromLayer(psdImage.Layers[2]);

                // създаване на обект VectorPath за съществуващ слой без данни за векторен път.
                VectorPath vectorPath = VectorDataProvider.CreateVectorPathForLayer(psdImage.Layers[1]);

                // Задайте цвета за попълване на векторния път
                vectorPath.FillColor = Color.MediumPurple;

                // добавяне на нова форма
                PathShape newShape = new PathShape();
                newShape.Points.Add(new BezierKnot(new PointF(65, 175), true));
                newShape.Points.Add(new BezierKnot(new PointF(65, 210), true));
                newShape.Points.Add(new BezierKnot(new PointF(190, 210), true));
                newShape.Points.Add(new BezierKnot(new PointF(190, 175), true));
                vectorPath.Shapes.Add(newShape);

                // актуализиране на пътните данни в слоя
                VectorDataProvider.UpdateLayerFromVectorPath(psdImage.Layers[1], vectorPath, true);


                // създаване на обект VectorPath за нов слой.
                FillLayer layer2 = FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color);
                layer2.DisplayName = "Layer 2";
                psdImage.AddLayer(layer2);
                VectorPath vectorPath2 = VectorDataProvider.CreateVectorPathForLayer(layer2);

                // Задайте цвета за попълване на векторния път
                vectorPath2.FillColor = Color.IndianRed;

                // добавяне на нова форма
                PathShape newShape2 = new PathShape();
                newShape2.Points.Add(new BezierKnot(new PointF(50, 150), true));
                newShape2.Points.Add(new BezierKnot(new PointF(100, 200), true));
                newShape2.Points.Add(new BezierKnot(new PointF(0, 200), true));
                vectorPath2.Shapes.Add(newShape2);

                // актуализиране на пътните данни в слоя
                VectorDataProvider.UpdateLayerFromVectorPath(layer2, vectorPath2, true);

                psdImage.Save(outputPsd);
                psdImage.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
            }
        }
{{< /highlight >}}