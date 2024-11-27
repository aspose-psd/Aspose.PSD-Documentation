---
title: Aspose.PSD за .NET 20.4 - Бележки за версията
type: docs
weight: 90
url: /bg/net/aspose-psd-za-net-20-4-belejki-za-versiyata/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за версията на [Aspose.PSD за .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Обобщение**|**Категория**|
| :- | :- | :- |
|PSDNET-567|Поддръжка на ресурса 'Данни за произход на вектора'|Функционалност|
|PSDNET-373|Поддръжка на lclrResource (Настройка на цвета на листа)|Функционалност|
|PSDNET-563|Поддръжка на свойствата от данните на LengthRecord. (Операции върху пътеки (булеви операции), индекс на формата в слоя, брой на записите за кръгови възли)|Функционалност|
|PSDNET-425|Поддръжка на ресурса Image Section #1010 Заден план на цвета|Функционалност|
|PSDNET-530|Добавяне на слоеве за попълване по време на изпълнение|Функционалност|
|PSDNET-424|Поддръжка на ресурса Image Section #1009 Информация за границите|Функционалност|
|PSDNET-592|Поддръжка на слоеве във файловете във формат AI|Функционалност|
|PSDNET-256|Поддръжка за четене и редактиране на ефекта на слоя с градиентен оверлей|Функционалност|
|PSDNET-257|Изчертаване на ефекта на слоя с градиентен оверлей|Функционалност|
|PSDNET-585|Промените в свойството BlendMode на GradientOverlayEffect не се показват в Photoshop|Проблем|
|PSDNET-561|Оправяне на запазването на PSD изображение с Grayscale ColorMode и 16 бита на канал към формата на Grayscale PSD|Проблем|
|PSDNET-560|Оправяне на запазването на PSD изображение с Grayscale ColorMode и 16 бита на канал към формата PNG|Проблем|

## **Промени в публичното API**
# **Добавени API:**
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
# **Премахнати API:**
- Нито един

## **Примери за използване:**
**PSDNET-567. Поддръжка на ресурса 'Данни за произход на вектора'**

{{< highlight java >}}

         // Поддръжка на ресурса VogkResource

        static void ПримерЗаПоддръжкаНаРесурсаВогкРесурс()

        {

            string имеНаФайла = "VectorOriginationDataResource.psd";

            string имеЗаИзходноФайлаНаФайл = "out_VectorOriginationDataResource_.psd";

            using (var изображениеПсд = (PsdImage)Image.Load(имеНаФайла))

            {

                var ресурс = GetVogkResource(изображениеПсд);

                // Четене

                if (ресурс.ShapeOriginSettings.Length != 1 ||

                    !ресурс.ShapeOriginSettings[0].IsShapeInvalidated ||

                    ресурс.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    throw new Exception("Има грешка при четене на VogkResource.");

                }

                // Редактиране

                ресурс.ShapeOriginSettings = new[]

                {

                    ресурс.ShapeOriginSettings[0],

                    new VectorShapeOriginSettings(true, 1)

                };

                изображениеПсд.Save(имеЗаИзходноФайлаНаФайл);

            }

        }

        static VogkResource GetVogkResource(PsdImage image)

        {

            var layer = image.Layers[1];

            VogkResource resource = null;

            var resources = layer.Resources;

            for (int i = 0; i < resources.Length; i++)

            {

                if (resources[i] is VogkResource)

                {

                    resource = (VogkResource)resources[i];

                    break;

                }

            }

            if (resource == null)

            {

                throw new Exception("Ресурсът VogkResource не е намерен.");

            }

            return resource;

        }   

{{< /highlight >}}

**PSDNET-373. Поддръжка на lclrResource (Настройка на цвета на листа)**

{{< highlight java >}}

         static void ПроверкаНаЦветоветеНаЛистИОбръщане(SheetColorHighlightEnum[] цветовеЗаЛистове, PsdImage изображение)

        {

            int бройСлоеве = изображение.Layers.Length;

            for (int индексНаСлой = 0; индексНаСлоеве < бройСлоеве; индексНаСлой++)

            {

                Layer слой = изображение.Layers[индексНаСлой];

                LayerResource[] ресурси = слой.Resources;

                foreach (LayerResource слойРесурс in ресурси)

                {

                    // Ресурсът lcrl винаги е наличен в списъка с ресурси на psd файл.

                    LclrResource ресурс = слойРесурс as LclrResource;

                    if (ресурс != null)

                    {

                        if (ресурс.Color != цветовеЗаЛистове[индексНаСлой])

                        {

                            throw new Exception("Цветът на листа е прочетен грешно");

                        }

                        // Обръщане на цветовете на листовете. Задаване на оцветяването на слой.

                        ресурс.Color = цветовеЗаЛистове[бройСлоеве - индексНаСлой - 1];

                        break;

                    }

                }

            }

        }

            string източенФайлПът = "AllLclrResourceColors.psd";

            string изходенФайлПът = "AllLclrResourceColorsReversed.psd";

            // Във файла цветовете на слоевете за оцветяване са в този ред

            SheetColorHighlightEnum[] цветовеЗаЛистове = new SheetColorHighlightEnum[] {

                SheetColorHighlightEnum.Red,

                SheetColorHighlightEnum.Orange,

                SheetColorHighlightEnum.Yellow,

                SheetColorHighlightEnum.Green,

                SheetColorHighlightEnum.Blue,

                SheetColorHighlightEnum.Violet,

                SheetColorHighlightEnum.Gray,

                SheetColorHighlightEnum.NoColor

            };            

            // Цветовете на листа се използват за визуално оцветяване на слоевете. 

            // Например можете да актуализирате някои слоеве в PSD и след това да оцветите с цвят слоя, който искате да привлече вниманието.

            using (PsdImage изображение = (PsdImage)Image.Load(източенФайлПът))

            {

                ПроверкаНаЦветоветеНаЛистИОбръщане(цветовеЗаЛистове, изображение);

                изображение.Save(изходенФайлПът, new PsdOptions());

            }

            using (PsdImage изображение = (PsdImage)Image.Load(изходенФайлПът))

            {

                // Цветовете трябва да бъдат обръщани

                Array.Reverse(цветовеЗаЛистове);

                ПроверкаНаЦветоветеНаЛистИОбръщане(цветовеЗаЛистове, изображение);

            }

{{< /highlight >}}

**PSDNET-563. Поддръжка на свойствата от данните на LengthRecord. (Операции върху пътеки (булеви операции), индекс на формата в слоя, брой на записите за кръгови възли)**

{{< highlight java >}}

            string имеНаФайла = "PathOperationsShape.psd";

            using (var им = (PsdImage)Image.Load(имеНаФайла))

            {

                VsmsResource ресурс = null;

                foreach (var layerResource in им.Layers[1].Resources)

                {

                    if (layerResource is VsmsResource)

                    {

                        ресурс = (VsmsResource)layerResource;

                        break;

                    }

                }

                LengthRecord lengthRecord0 = (LengthRecord)ресурс.Paths[2];

                LengthRecord lengthRecord1 = (LengthRecord)ресурс.Paths[7];

                LengthRecord lengthRecord2 = (LengthRecord)ресурс.Paths[11];

                // Тук променяме начина на комбиниране между формите.

                lengthRecord0.PathOperations = PathOperations.ExcludeOverlappingShapes;

                lengthRecord1.PathOperations = PathOperations.IntersectShapeAreas;

                lengthRecord2.PathOperations = PathOperations.SubtractFrontShape;

                им.Save("out_" + имеНаФайла);

            }

{{< /highlight >}}

**PSDNET-425. Поддръжка на ресурса Image Section #1010 Заден план на цвета**

{{< highlight java >}}

             string изходенФайл = "изходен.psd";

            using (var изображение = (PsdImage)Image.Load(изходенФайл))

            {

                ResourceBlock[] ресурсиНаИзображението = изображение.ImageResources;

                BackgroundColorResource ресурсНаЗаденПланНаЦвета = null;

                foreach (var ресурсНаИзображението in ресурсиНаИзображението)

                {

                    if (ресурсНаИзображението is BackgroundColorResource)

                    {

                        ресурсНаЗаденПланНаЦвета = (BackgroundColorResource)ресурсНаИзображението;

                        break;

                    }

                }

                // актуализация на BackgroundColorResource

                ресурсНаЗаденПланНаЦвета.Color = Color.DarkRed;

                изображение.Save(изходенФайл);

            }

{{< /highlight >}}

**PSDNET-530. Добавяне на слоеве за попълване по време на изпълнение**

{{< highlight java >}}

             string outputPsd = "output.psd";

            using (var image = new PsdImage(100, 100))

            {

                FillLayer colorFillLayer = FillLayer.CreateInstance(FillType.Color);

                colorFillLayer.DisplayName = "Color Fill Layer";

                image.AddLayer(colorFillLayer);

                FillLayer gradientFillLayer = FillLayer.CreateInstance(FillType.Gradient);

                gradientFillLayer.DisplayName = "Gradient Fill Layer";

                image.AddLayer(gradientFillLayer);

                FillLayer patternFillLayer = FillLayer.CreateInstance(FillType.Pattern);

                patternFillLayer.DisplayName = "Pattern Fill Layer";

                patternFillLayer.Opacity = 50;

                image.AddLayer(patternFillLayer);

                image.Save(outputPsd);

            }

{{< /highlight >}}

**PSDNET-424. Поддръжка на ресурса Image Section #1009 Информация за границите**

{{< highlight java >}}

             string sourceFile = "input.psd";

            string outputFile = "output.psd";

            using (var image = (PsdImage)Image.Load(sourceFile))

            {

                ResourceBlock[] imageResources = image.ImageResources;

                BorderInformationResource borderInfoResource = null;

                foreach (var imageResource in imageResources)

                {

                    if (imageResource is BorderInformationResource)

                    {

                        borderInfoResource = (BorderInformationResource)imageResource;

                        break;

                    }

                }

                // update BorderInformationResource

                borderInfoResource.Width = 0.1;

                borderInfoResource.Unit = PhysicalUnit.Inches;

                image.Save(outputFile);

            }

{{< /highlight >}}

**PSDNET-592. Поддръжка на слоеве във файловете във формат AI**

{{< highlight java >}}

         void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "form_8_2l3_7.ai";

        string outputFileName = "form_8_2l3_7_export";

        using (AiImage image = (AiImage)Image.Load(sourceFileName))

        {

            AiLayerSection layer0 = image.Layers[0];

            AssertIsTrue(layer0 != null, "Layer 0 should be not null.");

            AssertIsTrue(layer0.Name == "Layer 4", "The Name property of the layer 0 should be Layer 4");

            AssertIsTrue(!layer0.IsTemplate, "The IsTemplate property of the layer 0 should be false.");

            AssertIsTrue(layer0.IsLocked, "The IsLocked property of the layer 0 should be true.");

            AssertIsTrue(layer0.IsShown, "The IsShown property of the layer 0 should be true.");

            AssertIsTrue(layer0.IsPrinted, "The IsPrinted property of the layer 0 should be true.");

            AssertIsTrue(!layer0.IsPreview, "The IsPreview property of the layer 0 should be false.");

            AssertIsTrue(layer0.IsImagesDimmed, "The IsImagesDimmed property of the layer 0 should be true.");

            AssertIsTrue(layer0.DimValue == 51, "The DimValue property of the layer 0 should be 51.");

            AssertIsTrue(layer0.ColorNumber == 0, "The ColorNumber property of the layer 0 should be 0.");

            AssertIsTrue(layer0.Red == 79, "The Red property of the layer 0 should be 79.");

            AssertIsTrue(layer0.Green == 128, "The Green property of the layer 0 should be 128.");

            AssertIsTrue(layer0.Blue == 255, "The Blue property of the layer 0 should be 255.");

            AssertIsTrue(layer0.RasterImages.Length == 0, "The pixels length property of the raster image in the layer 0 should equals 0.");

            AiLayerSection layer1 = image.Layers[1];

            AssertIsTrue(layer1 != null, "Layer 1 should be not null.");

            AssertIsTrue(layer1.Name == "Layer 1", "The Name property of the layer 1 should be Layer 1");

            AssertIsTrue(layer1.RasterImages.Length == 1, "The length property of the raster images in the layer 1 should equals 1.");

            AiRasterImageSection rasterImage = layer1.RasterImages[0];

            AssertIsTrue(rasterImage != null, "The raster image in the layer 1 should be not null.");

            AssertIsTrue(rasterImage.Pixels != null, "The pixels property of the raster image in the layer 1 should be not null.");

            AssertIsTrue(string.Empty == rasterImage.Name, "The Name property of the raster image in the layer 1 should be empty");

            AssertIsTrue(rasterImage.Pixels.Length == 100, "The pixels length property of the raster image in the layer 1 should equals 100.");

            image.Save(outputFileName + ".psd", new PsdOptions());

            image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

        }

{{< /highlight >}}

**PSDNET-256. Поддръжка за четене и редактиране на ефекта на слоя с градиентен оверлей**

{{< highlight java >}}

             // Creates/Gets and edits the gradient overlay effect in a layer.

            using (var psdImage = this.LoadFile("psdnet256.psd", new PsdLoadOptions() { LoadEffectsResource = true }))

            {

                BlendingOptions layerBlendOptions = psdImage.Layers[1].BlendingOptions;

                GradientOverlayEffect gradientOverlayEffect = null;

                // Search GradientOverlayEffect in a layer.

                foreach (ILayerEffect effect in layerBlendOptions.Effects)

                {

                    gradientOverlayEffect = effect as GradientOverlayEffect;

                    if (gradientOverlayEffect != null)

                    {

                        break;

                    }

                }

                if (gradientOverlayEffect == null)

                {

                    // You can create a new GradientOverlayEffect if it not exists.

                    gradientOverlayEffect = layerBlendOptions.AddGradientOverlay();

                }

                // Add a bit of transparency to the effect.

                gradientOverlayEffect.Opacity = 200;

                // Change the blend mode of gradient effect.

                gradientOverlayEffect.BlendMode = BlendMode.Hue;

                // Gets GradientFillSettings object to configure gradient overlay settings.

                GradientFillSettings settings = gradientOverlayEffect.Settings;

                // Setting a new gradient with two colors.

                settings.ColorPoints = new IGradientColorPoint[]

                {

                    new GradientColorPoint(Color.GreenYellow, 0, 50),

                    new GradientColorPoint(Color.BlueViolet, 4096, 50),

                };

                // Sets an inclination of the gradient at an angle of 80 degrees.

                settings.Angle = 80;

                // Scale gradient effect up to 150%.

                settings.Scale = 150;

                // Sets type of gradient.

                settings.GradientType = GradientType.Linear;

                // Make the gradient opaque by setting the opacity to 100% at each transparency point.

                settings.TransparencyPoints[0].Opacity = 100;

                settings.TransparencyPoints[1].Opacity = 100;

                psdImage.Save("psdnet256.psd_output.psd");

            }

{{< /highlight >}}

**PSDNET-257. Изчертаване на ефекта на слоя с градиентен оверлей. Функционалност**

{{< highlight java >}}

             string srcFile = "gradientOverlayEffect.psd";

            string outputPng = "output.png";

            string outputPsd = "output.psd";

            using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))

            {

                psdImage.Save(outputPng, new PngOptions());

                psdImage.Save(outputPsd);

            }

{{< /highlight >}}

**PSDNET-585. Промените в свойството BlendMode на GradientOverlayEffect не се показват в Photoshop**

{{< highlight java >}}

             string srcFile = "psdnet585.psd";

            string outFile = "out_psdnet585.psd";

            using (var psdImage = (PsdImage)Image.Load(srcFile))

            {

                var gradientOverlayEffect = psdImage.Layers[1].BlendingOptions.AddGradientOverlay();

                gradientOverlayEffect.BlendMode = BlendMode.Subtract;

                psdImage.Save(outFile);

                // After saving open 'outFile' manually in Photoshop and check Blend Mode in 'Gradient Overlay' effect settings of 'Layer 1'.

            }

{{< /highlight >}}

**PSDNET-561. Оправяне на запазването на PSD изображение с Grayscale ColorMode и 16 бита на канал към формата на Grayscale PSD**

{{< highlight java >}}

         string sourceFileName = "grayscale16bit.psd";

        string exportFileName = "grayscale16bit_output.psd";

        PsdOptions psdOptions = new PsdOptions()

                                    {

                                        ColorMode = ColorModes.Grayscale, ChannelBitsCount = 16, ChannelsCount = 2

                                    };

        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

        {

            RasterCachedImage raster = image.Layers[0];

            Aspose.PSD.Graphics graphics = new Graphics(raster);

            int width = raster.Width;

            int height = raster.Height;

            Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

            graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1),  rect);

            image.Save(exportFileName, psdOptions);

        }

        string pngExportPath = Path.ChangeExtension(exportFileName, "png");

        using (PsdImage image = (PsdImage)Image.Load(exportFileName))

        {

            // Here should be no exception.

            image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

        }

{{< /highlight >}}

**PSDNET-560. Оправяне на запазването на PSD изображение с Grayscale ColorMode и 16 бита на канал към формата PNG**

{{< highlight java >}}

         string sourceFileName = "grayscale16bit.psd";

        string exportPath = "grayscale_output.png";

        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

        {

            image.Save(exportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

        }

{{< /highlight >}}