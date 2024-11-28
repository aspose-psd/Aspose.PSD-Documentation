---
title: Отчет о релизе Aspose.PSD для .NET 19.5 
type: docs
weight: 80
url: /ru/net/aspose-psd-для-net-19-5-отчет-о-релизе/
---

{{% alert color="primary" %}} 

Эта страница содержит отчет о релизе для Aspose.PSD для .NET 19.5.

{{% /alert %}} 

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-133|Добавлена поддержка слоев заливки: Узор|Новая функция|
|PSDNET-138|Поддержка PtFlResource|Новая функция|
|PSDNET-129|Реализация корректного метода обрезки для файлов PSD|Новая функция|
|PSDNET-140|Поддержка VsmsResource|Новая функция|
|PSDNET-121|Видимые слои в видимой подпапке в невидимой папке отображаются, но не должны|Ошибка|
|PSDNET-119|PSD (RGB режим 16 бит на канал) неправильно конвертирован в JPG|Ошибка|

## **Изменения в публичном API**
# **Добавленные API:**
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
# **Удаленные API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)

## **Примеры использования:**
**PSDNET-133. Добавить поддержку слоев заливки: Узор**

{{< highlight java >}}

 // Добавить поддержку слоев заливки: Узор

    string sourceFileName = "PatternFillLayer.psd";

    string exportPath = "PatternFillLayer_Edited.psd";

    double tolerance = 0.0001;

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

         foreach (var layer in im.Layers)

         {

             if (layer is FillLayer)

             {

                  FillLayer fillLayer = (FillLayer)layer;

                  PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;

                  if (fillSettings.HorizontalOffset != -46 || 

                      fillSettings.VerticalOffset != -45 || 

                      fillSettings.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5"||

                      fillSettings.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares" ||

                      fillSettings.AlignWithLayer != true ||

                      fillSettings.Linked != true ||

                      fillSettings.PatternHeight != 64 ||

                      fillSettings.PatternWidth != 64 ||

                      fillSettings.PatternData.Length != 4096 ||

                      Math.Abs(fillSettings.Scale - 50) > tolerance) 

                      {

                          throw new Exception("PSD Image was read wrong");

                      }

                  // Редактирование 

                  fillSettings.Scale = 300;

                  fillSettings.HorizontalOffset = 2;

                  fillSettings.VerticalOffset = -20;

                  fillSettings.PatternData = new int[]

                  {

                       Color.Red.ToArgb(), Color.Blue.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Red.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Blue.ToArgb(),  Color.Red.ToArgb()

                  };

                  fillSettings.PatternHeight = 3;

                  fillSettings.PatternWidth = 3;

                  fillSettings.AlignWithLayer = false;

                  fillSettings.Linked = false;

                  fillSettings.PatternId = Guid.NewGuid().ToString();

                  fillLayer.Update();

                  break;

             }

         }

         im.Save(exportPath);

    }

{{< /highlight >}}

**PSDNET-138. Поддержка PtFlResource**

{{< highlight java >}}

  // Поддержка PtFlResource

    string sourceFileName = "PatternFillLayer.psd";

    string exportPath = "PtFlResource_Edited.psd";

    double tolerance = 0.0001;

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

         foreach (var layer in im.Layers)

         {

             if (layer is FillLayer)

             {

                var fillLayer = (FillLayer)layer;

                var resources = fillLayer.Resources;

                foreach (var res in resources)

                {

                    if (res is PtFlResource)

                    {

                        // Чтение

                        PtFlResource resource = (PtFlResource)res;

                        if (

                            resource.Offset.X != -46 || 

                            resource.Offset.Y != -45 || 

                            resource.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5\0" ||

                            resource.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares\0" ||

                            resource.AlignWithLayer != true ||

                            resource.IsLinkedWithLayer != true ||

                            !(Math.Abs(resource.Scale - 50) < tolerance)) {

                                throw new Exception("PtFl Resource was read incorrect");

                            }

                        // Редактирование

                        resource.Offset = new Point(-11, 13);

                        resource.Scale = 200;

                        resource.AlignWithLayer = false;

                        resource.IsLinkedWithLayer = false;

                        fillLayer.Resources = fillLayer.Resources;

                        // У нас нет данных о шаблоне в PattResource, поэтому мы можем их добавить.

                        var fillSettings = (PatternFillSettings)fillLayer.FillSettings;

                        fillSettings.PatternData = new int[]

                        {

                            Color.Black.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                        };

                        fillSettings.PatternHeight = 1;

                        fillSettings.PatternWidth = 4;

                        fillSettings.PatternName = "$$$/Presets/Patterns/VerticalLine=Vertical Line New\0";

                        fillSettings.PatternId = Guid.NewGuid().ToString() + "\0";

                        fillLayer.Update();

                    }

                    break;

                }

                break;

            }

         }

         im.Save(exportPath);

    } 

{{< /highlight >}}

**PSDNET-129. Реализация корректного метода обрезки для файлов PSD**

{{< highlight java >}}

             // Реализация корректного метода обрезки для файлов PSD

            string sourceFileName = "1.psd";

            string exportPathPsd = "CropTest.psd";

            string exportPathPng = "CropTest.png";

            using (RasterImage image = Image.Load(sourceFileName) as RasterImage)

            {

                image.Crop(new Rectangle(10, 30, 100, 100));

                image.Save(exportPathPsd, new PsdOptions());

                image.Save(exportPathPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-140. Поддержка VsmsResource**

{{< highlight java >}}

 // Поддержка VsmsResource

        static void ПримерПоддержкиVsmsResource()

        {

            string sourceFileName = "EmptyRectangle.psd";

            string exportPath = "EmptyRectangle_changed.psd";

            var im = (PsdImage)Image.Load(sourceFileName);

            using (im)

            {

                var resource = GetVsmsResource(im);

                // Чтение

                if (resource.IsDisabled != false ||

                    resource.IsInverted != false ||

                    resource.IsNotLinked != false ||

                    resource.Paths.Length != 7 ||

                    resource.Paths[0].Type != VectorPathType.PathFillRuleRecord ||

                    resource.Paths[1].Type != VectorPathType.InitialFillRuleRecord ||

                    resource.Paths[2].Type != VectorPathType.ClosedSubpathLengthRecord ||

                    resource.Paths[3].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    resource.Paths[4].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    resource.Paths[5].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked||

                    resource.Paths[6].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked)

                {

                        throw new Exception("VsmsResource was read wrong");

                }

                var pathFillRule = (PathFillRuleRecord)resource.Paths[0];

                var initialFillRule = (InitialFillRuleRecord)resource.Paths[1];

                var subpathLength = (LengthRecord)resource.Paths[2];

                // Правило заполнения пути не содержит дополнительной информации

                if (pathFillRule.Type != VectorPathType.PathFillRuleRecord || 

                initialFillRule.Type != VectorPathType.InitialFillRuleRecord ||

                initialFillRule.IsFillStartsWithAllPixels != false ||

                subpathLength.Type != VectorPathType.ClosedSubpathLengthRecord ||

                subpathLength.IsClosed != true ||

                subpathLength.IsOpen != false) 

                {

                    throw new Exception("VsmsResource paths were read wrong");

                }

                // Редактирование

                resource.IsDisabled = true;

                resource.IsInverted = true;

                resource.IsNotLinked = true;

                var bezierKnot = (BezierKnotRecord)resource.Paths[3];

                bezierKnot.Points[0] = new Point(0, 0);

                bezierKnot = (BezierKnotRecord)resource.Paths[4];

                bezierKnot.Points[0] = new Point(8039798, 10905191);

                initialFillRule.IsFillStartsWithAllPixels = true;

                subpathLength.IsClosed = false;

                im.Save(exportPath);

            }         

        }

        static VsmsResource GetVsmsResource(PsdImage image)

        {

            var layer = image.Layers[1];

            VsmsResource resource = null;

            var resources = layer.Resources;

            for (int i = 0; i < resources.Length; i++)

            {

                if (resources[i] is VsmsResource)

                {

                    resource = (VsmsResource)resources[i];

                    break;

                }

            }

            if (resource == null)

            {

                throw new Exception("VsmsResource not found");

            }

            return resource;

        }

{{< /highlight >}}

**PSDNET-121: Видимые слои в видимой подпапке в невидимой папке отображаются, но не должны**

{{< highlight java >}}

 // Видимые слои в видимой подпапке в невидимой папке отображаются, но не должны

            string sourceFileName = "ALotOfFolders.psd.psd";

            string outputFilePathJpg = "outALotOfFolders.jpg";

            string outputFilePathPsd = "outALotOfFolders.psd";

            var options = new PsdLoadOptions();

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, options))

            {

                image.Save(outputFilePathPsd, new PsdOptions(image));

                image.Save(outputFilePathJpg, new JpegOptions() { Quality = 100 });

            }

{{< /highlight >}}

**PSDNET-119. PSD (RGB режим 16 бит на канал) неправильно конвертирован в JPG**

{{< highlight java >}}

  // Psd неправильно конвертирован в jpg

            string sourceFileName = "in.psd";

            string exportPath = "outRgb.jpg";

            var options = new PsdLoadOptions();

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, options))

            {

                image.Save(exportPath, new JpegOptions() { Quality = 100 });

            }

{{< /highlight >}}