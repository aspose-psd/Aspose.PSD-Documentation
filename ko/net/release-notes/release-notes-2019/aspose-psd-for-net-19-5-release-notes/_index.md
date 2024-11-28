---
title: Aspose.PSD for .NET 19.5 - 릴리스 노트
type: docs
weight: 80
url: /ko/net/aspose-psd-for-net-19-5-release-notes/
---

{{% alert color="primary" %}} 

Aspose.PSD for .NET 19.5에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}} 

|**키**|**요약**|**범주**|
| :- | :- | :- |
|PSDNET-133|채우기 레이어: 패턴 지원 추가|기능|
|PSDNET-138|PtFlResource 지원|기능|
|PSDNET-129|PSD 파일에 대한 올바른 자르기 메서드 구현|기능|
|PSDNET-140|VsmsResource 지원|기능|
|PSDNET-121|보이지 않는 폴더의 보이는 하위 폴더에 있는 레이어는 렌더링되지만 하지 않아야 함|버그|
|PSDNET-119|PSD (각 채널 당 16 비트의 RGB 모드)를 제대로 JPG로 변환하지 않음|버그|

## **공개 API 변경**
# **추가된 API:**
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
# **제거된 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)

## **사용 예시:**
**PSDNET-133. 채우기 레이어: 패턴 지원 추가**

{{< highlight java >}}

 // 채우기 레이어: 패턴 지원 추가

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

                  // 편집

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

**PSDNET-138. PtFlResource 지원**

{{< highlight java >}}

  // PtFlResource 지원

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

                        // 읽기

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

                        // 편집

                        resource.Offset = new Point(-11, 13);

                        resource.Scale = 200;

                        resource.AlignWithLayer = false;

                        resource.IsLinkedWithLayer = false;

                        fillLayer.Resources = fillLayer.Resources;

                        // PattResource에 패턴 데이터가 없으므로 추가할 수 있음.

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

**PSDNET-129. PSD 파일에 대한 올바른 자르기 메서드 구현**

{{< highlight java >}}

             // PSD 파일에 대한 올바른 자르기 메서드 구현.

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

**PSDNET-140. VsmsResource 지원**

{{< highlight java >}}

 // VsmsResource 지원

        static void VsmsResourceSupportExample()

        {

            string sourceFileName = "EmptyRectangle.psd";

            string exportPath = "EmptyRectangle_changed.psd";

            var im = (PsdImage)Image.Load(sourceFileName);

            using (im)

            {

                var resource = GetVsmsResource(im);

                // 읽기

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

                // 경로 채우기 규칙에는 추가 정보가 포함되어 있지 않음

                if (pathFillRule.Type != VectorPathType.PathFillRuleRecord || 

                initialFillRule.Type != VectorPathType.InitialFillRuleRecord ||

                initialFillRule.IsFillStartsWithAllPixels != false ||

                subpathLength.Type != VectorPathType.ClosedSubpathLengthRecord ||

                subpathLength.IsClosed != true ||

                subpathLength.IsOpen != false) 

                {

                    throw new Exception("VsmsResource paths were read wrong");

                }

                // 편집

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



**PSDNET-121: 보이지 않는 폴더의 보이는 하위 폴더에 있는 레이어는 렌더링되지만 하지 않아야 함**

{{< highlight java >}}

 // 보이지 않는 폴더의 보이는 하위 폴더에 있는 레이어는 렌더링되지만 하지 않아야 함

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



**PSDNET-119. PSD (각 채널 당 16 비트의 RGB 모드)를 제대로 JPG로 변환하지 않음**

{{< highlight java >}}

  // PSD가 제대로 jpg로 변환되지 않음

            string sourceFileName = "in.psd";

            string exportPath = "outRgb.jpg";

            var options = new PsdLoadOptions();

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, options))

            {

                image.Save(exportPath, new JpegOptions() { Quality = 100 });

            }

{{< /highlight >}}