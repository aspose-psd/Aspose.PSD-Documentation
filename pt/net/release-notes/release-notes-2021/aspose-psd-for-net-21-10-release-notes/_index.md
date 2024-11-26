---
title: Notas de Lançamento do Aspose.PSD para .NET 21.10
type: docs
weight: 30
url: /pt/net/aspose-psd-for-net-21-10-release-notes/
---

{{% alert color="primary" %}} 

Esta página contém as notas de lançamento do [Aspose.PSD para .NET 21.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-128|Suporte ao mecanismo de Filtros Inteligentes|Funcionalidade|
|PSDNET-414|Suporte a Fxid/FEidResource|Funcionalidade|
|PSDNET-556|Erro ao carregar AliasStructure|Erro|
|PSDNET-948|Alterar Fonte e Cor para TextLayer PSD|Erro|
|PSDNET-971|Adicionar capacidade de criação personalizada de uma camada com uma máscara vetorial|Aprimoramento|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
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

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDNET-128. Suporte ao mecanismo de Filtros Inteligentes**

{{< highlight csharp >}}
            string sourceFilte = "r2_SmartFilters.psd";
            string outputPsd = "out_r2_SmartFilters.psd";

            void AssertAreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Os objetos não são iguais.");
                }
            }

            using (var image = (PsdImage)Image.Load(sourceFilte))
            {
                SmartObjectLayer smartObj = (SmartObjectLayer)image.Layers[1];

                // editar filtros inteligentes
                GaussianBlurSmartFilter gaussianBlur = (GaussianBlurSmartFilter)smartObj.SmartFilters.Filters[0];

                // verificar valores do filtro
                AssertAreEqual(3.1, gaussianBlur.Radius);
                AssertAreEqual(BlendMode.Dissolve, gaussianBlur.BlendMode);
                AssertAreEqual(90d, gaussianBlur.Opacity);
                AssertAreEqual(true, gaussianBlur.IsEnabled);

                // atualizar valores do filtro
                gaussianBlur.Radius = 1;
                gaussianBlur.BlendMode = BlendMode.Divide;
                gaussianBlur.Opacity = 75;
                gaussianBlur.IsEnabled = false;
                AddNoiseSmartFilter addNoise = (AddNoiseSmartFilter)smartObj.SmartFilters.Filters[1];
                addNoise.Distribution = NoiseDistribution.Uniform;

                // adicionar novos itens de filtro
                var filtros = new List<SmartFilter>(smartObj.SmartFilters.Filters);
                filtros.Add(new GaussianBlurSmartFilter());
                filtros.Add(new AddNoiseSmartFilter());
                smartObj.SmartFilters.Filters = filtros.ToArray();

                // aplicar alterações
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

                // verificar valores do filtro
                AssertAreEqual(1d, gaussianBlur.Radius);
                AssertAreEqual(BlendMode.Divide, gaussianBlur.BlendMode);
                AssertAreEqual(75d, gaussianBlur.Opacity);
                AssertAreEqual(false, gaussianBlur.IsEnabled);

                AssertAreEqual(true, smartObj.SmartFilters.Filters[5] is GaussianBlurSmartFilter);
                AssertAreEqual(true, smartObj.SmartFilters.Filters[6] is AddNoiseSmartFilter);
            }
{{< /highlight >}}

**PSDNET-414. Suporte a Fxid/FEidResource**

{{< highlight csharp >}}
            string inputFilePath = "psdnet414_3.psd";
            string output = "out_psdnet414_3.psd";

            int resLength = 1144;
            int maskLength = 369;

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Os objetos não são iguais.");
                }
            }

            using (var psdImage = (PsdImage)Image.Load(inputFilePath))
            {
                FXidResource fxidResource = (FXidResource)psdImage.GlobalLayerResources[3];

                AssertAreEqual(resLength, fxidResource.Length);
                foreach (var maskData in fxidResource.FilterEffectMasks)
                {
                    AssertAreEqual(maskLength, maskData.Length);
                }

                psdImage.Save(output);
            }

            // verificar após a gravação
            using (var psdImage = (PsdImage)Image.Load(output))
            {
                FXidResource fxidResource = (FXidResource)psdImage.GlobalLayerResources[3];

                AssertAreEqual(resLength, fxidResource.Length);
                foreach (var maskData in fxidResource.FilterEffectMasks)
                {
                    AssertAreEqual(maskLength, maskData.Length);
                }
            }
{{< /highlight >}}