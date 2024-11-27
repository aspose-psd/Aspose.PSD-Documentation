---
title: Aspose.PSD para .NET 21.10 - Notas de la versión
type: docs
weight: 30
url: /es/net/aspose-psd-for-net-21-10-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 21.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-128|Soporte del mecanismo de Filtros Inteligentes|Característica|
|PSDNET-414|Soporte de Fxid/FEidResource|Característica|
|PSDNET-556|Error al cargar AliasStructure|Error|
|PSDNET-948|Cambio de Fuente y Color para TextLayer PSD|Error|
|PSDNET-971|Agregar habilidad para crear personalmente una capa con una máscara de vector|Mejora|

## **Cambios en la API pública**
# **APIs Añadidas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.SmartFilters
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.Nombre
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.Distribución
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.CantidadRuido
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.EsMonocromático
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.TipoFiltro
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.Nombre
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.Radio
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.TipoFiltro
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution.Uniforme
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution.Gaussiano
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.FiltroInteligente
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.FiltroInteligente.Nombre
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.FiltroInteligente.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.FiltroInteligente.EsHabilitado
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.FiltroInteligente.Opacidad
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.FiltroInteligente.ModoMezcla
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.FiltroInteligente.Aplicar(Aspose.PSD.RasterImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.FiltroInteligente.AplicarAMáscara(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.FiltroInteligente.AlCargar
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.FiltroInteligente.Clonar
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.FiltroInteligente.DescriptorFuente
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter.Nombre
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter.FilterId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.EsHabilitado
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.EsVálidoEnPosición
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.EsMáscaraHabilitada
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.EsMáscaraVinculada
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.EsExtensiónMáscaraBlanca
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.Filtros
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.ActualizarValoresRecurso
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.#ctor(System.Int32,System.Int32,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Firma
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Clave
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.VersionPSD
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Versión
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.MáscarasEfectoFiltro
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Longitud
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Guardar(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.TipoFEidClaveHerramienta
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.TipoFxidClaveHerramienta
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.#ctor(System.String,Aspose.PSD.Rectangle,System.Int32,System.Int32,Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation[],Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation,Aspose.PSD.Rectangle,Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Longitud
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Guía
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Rectángulo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.PíxelesProfundidad
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.MáximosCanales
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Canales
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.MáscaraUsuario
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.RectánguloMáscara
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.MáscaraHoja
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.GuardarDatos(Aspose.PSD.StreamContainer)

# **APIs Eliminadas:**
- Ninguna

## **Ejemplos de uso:**

**PSDNET-128. Soporte del mecanismo de Filtros Inteligentes**

{{< highlight csharp >}}
            string sourceFilte = "r2_SmartFilters.psd";
            string outputPsd = "out_r2_SmartFilters.psd";

            void AssertAreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Los objetos no son iguales.");
                }
            }

            using (var image = (PsdImage)Image.Load(sourceFilte))
            {
                SmartObjectLayer smartObj = (SmartObjectLayer)image.Layers[1];

                // editar filtros inteligentes
                GaussianBlurSmartFilter gaussianBlur = (GaussianBlurSmartFilter)smartObj.SmartFilters.Filters[0];

                // verificar valores del filtro
                AssertAreEqual(3.1, gaussianBlur.Radius);
                AssertAreEqual(BlendMode.Dissolve, gaussianBlur.BlendMode);
                AssertAreEqual(90d, gaussianBlur.Opacity);
                AssertAreEqual(true, gaussianBlur.IsEnabled);

                // actualizar valores del filtro
                gaussianBlur.Radius = 1;
                gaussianBlur.BlendMode = BlendMode.Divide;
                gaussianBlur.Opacity = 75;
                gaussianBlur.IsEnabled = false;
                AddNoiseSmartFilter addNoise = (AddNoiseSmartFilter)smartObj.SmartFilters.Filters[1];
                addNoise.Distribution = NoiseDistribution.Uniform;

                // agregar nuevos elementos de filtro
                var filtros = new List<SmartFilter>(smartObj.SmartFilters.Filters);
                filtros.Add(new GaussianBlurSmartFilter());
                filtros.Add(new AddNoiseSmartFilter());
                smartObj.SmartFilters.Filters = filtros.ToArray();

                // aplicar cambios
                smartObj.SmartFilters.UpdateResourceValues();

                // Aplicar filtros
                smartObj.SmartFilters.Filters[0].Apply(image.Layers[2]);
                smartObj.SmartFilters.Filters[4].ApplyToMask(image.Layers[2]);

                image.Save(outputPsd);
            }

            using (var image = (PsdImage)Image.Load(outputPsd))
            {
                SmartObjectLayer smartObj = (SmartObjectLayer)image.Layers[1];

                GaussianBlurSmartFilter gaussianBlur = (GaussianBlurSmartFilter)smartObj.SmartFilters.Filters[0];

                // verificar valores del filtro
                AssertAreEqual(1d, gaussianBlur.Radius);
                AssertAreEqual(BlendMode.Divide, gaussianBlur.BlendMode);
                AssertAreEqual(75d, gaussianBlur.Opacity);
                AssertAreEqual(false, gaussianBlur.IsEnabled);

                AssertAreEqual(true, smartObj.SmartFilters.Filters[5] is GaussianBlurSmartFilter);
                AssertAreEqual(true, smartObj.SmartFilters.Filters[6] is AddNoiseSmartFilter);
            }
{{< /highlight >}}

**PSDNET-414. Soporte de Fxid/FEidResource**

{{< highlight csharp >}}
            string inputFilePath = "psdnet414_3.psd";
            string output = "out_psdnet414_3.psd";

            int resLength = 1144;
            int maskLength = 369;

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Los objetos no son iguales.");
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

            // comprobar después de guardar
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

**PSDNET-556. Error al cargar AliasStructure**

{{< highlight csharp >}}
            string srcFile = "Aspose.psd";
            string outputPsd = "out_Aspose.psd";
            string outputPng = "out_Aspose.png";

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Los objetos no son iguales.");
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
                        textLayer.UpdateText("Test", Aspose.PSD.Color.Black);
                    }
                }

                image.Save(outputPsd);
                image.Save(outputPng, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
            }
{{< /highlight >}}

**PSDNET-948. Cambio de Fuente y Color para TextLayer PSD**

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

**PSDNET-971. Agregar habilidad para crear personalmente una capa con una máscara de vector**

{{< highlight csharp >}}
        public void CreatingVectorPathExample()
        {
            string fileName = "PathExample2.psd";

            string outputPsd = "out_CreatingVectorPathExampleTest.psd";
            string outputPng = "out_CreatingVectorPathExampleTest.png";

            using (var psdImage = (PsdImage)Image.Load(fileName))
            {
                VectorDataProvider.RemoveVectorPathDataFromLayer(psdImage.Layers[2]);

                // crear objeto VectorPath para una capa existente sin datos de camino de vector.
                VectorPath vectorPath = VectorDataProvider.CreateVectorPathForLayer(psdImage.Layers[1]);

                // Establecer el color de relleno del camino vectorial
                vectorPath.FillColor = Color.MediumPurple;

                // agregar nueva forma
                PathShape newShape = new PathShape();
                newShape.Points.Add(new BezierKnot(new PointF(65, 175), true));
                newShape.Points.Add(new BezierKnot(new PointF(65, 210), true));
                newShape.Points.Add(new BezierKnot(new PointF(190, 210), true));
                newShape.Points.Add(new BezierKnot(new PointF(190, 175), true));
                vectorPath.Shapes.Add(newShape);

                // actualizar datos del camino en la capa
                VectorDataProvider.UpdateLayerFromVectorPath(psdImage.Layers[1], vectorPath, true);


                // crear objeto VectorPath para una nueva capa.
                FillLayer layer2 = FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color);
                layer2.DisplayName = "Layer 2";
                psdImage.AddLayer(layer2);
                VectorPath vectorPath2 = VectorDataProvider.CreateVectorPathForLayer(layer2);

                // Establecer el color de relleno del camino vectorial
                vectorPath2.FillColor = Color.IndianRed;

                // agregar nueva forma
                PathShape newShape2 = new PathShape();
                newShape2.Points.Add(new BezierKnot(new PointF(50, 150), true));
                newShape2.Points.Add(new BezierKnot(new PointF(100, 200), true));
                newShape2.Points.Add(new BezierKnot(new PointF(0, 200), true));
                vectorPath2.Shapes.Add(newShape2);

                // actualizar datos del camino en la capa
```csharp
                VectorDataProvider.UpdateLayerFromVectorPath(layer2, vectorPath2, true);

                psdImage.Save(outputPsd);
                psdImage.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
            }
        }
```