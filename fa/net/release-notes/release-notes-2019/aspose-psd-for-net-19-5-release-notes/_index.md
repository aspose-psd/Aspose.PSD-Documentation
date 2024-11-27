---
title: راهنمای انتشار Aspose.PSD برای .NET 19.5
type: مستندات
weight: 80
url: /fa/net/aspose-psd-for-net-19-5-release-notes/
---

{{% alert color="primary" %}}

این صفحه حاوی یادداشت‌های انتشار برای Aspose.PSD برای .NET نسخه 19.5 می‌باشد:

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته بندی**|
| :- | :- | :- |
|PSDNET-133|افزودن پشتیبانی لایه‌های پر کردن: الگو|ویژگی|
|PSDNET-138|پشتیبانی از منبع PtFl|ویژگی|
|PSDNET-129|پیاده‌سازی صحیح روش برش برای فایل‌های PSD|ویژگی|
|PSDNET-140|پشتیبانی از منبع Vsms|ویژگی|
|PSDNET-121|لایه‌های قابل مشاهده در زیرپوشه قابل مشاهده در پوشه پنهان پردازش می‌شود، اما نباید|خطا|
|PSDNET-119|PSD (حالت RGB با 16 بیت بر کانال) به درستی به JPG تبدیل نمی‌شود|خطا|

## **تغییرات API عمومی**
# **API‌های اضافه شده:**
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

# **API‌های حذف شده:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)

## **نمونه‌های استفاده:**
**PSDNET-133. افزودن پشتیبانی لایه‌های پر کردن: الگو**

{{< highlight java >}}

 // افزودن پشتیبانی لایه‌های پر کردن: الگو

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

                          throw new Exception("تصویر PSD به غلط خوانده شده است");

                      }

                  // ویرایش 

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

**PSDNET-138. پشتیبانی از منبع PtFlResource**

{{< highlight java >}}

 // پشتیبانی از منبع PtFlResource

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

                        // خواندن

                        PtFlResource resource = (PtFlResource)res;

                        if (

                            resource.Offset.X != -46 || 

                            resource.Offset.Y != -45 || 

                            resource.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5\0" ||

                            resource.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares\0" ||

                            resource.AlignWithLayer != true ||

                            resource.IsLinkedWithLayer != true ||

                            !(Math.Abs(resource.Scale - 50) < tolerance)) {

                                throw new Exception("منبع PtFl به غلط خوانده شده است");

                            }

                        // ویرایش

                        resource.Offset = new Point(-11, 13);

                        resource.Scale = 200;

                        resource.AlignWithLayer = false;

                        resource.IsLinkedWithLayer = false;

                        fillLayer.Resources = fillLayer.Resources;

                        // اگر اطلاعات الگویی در PattResource وجود ندارد، می‌توانیم آن را اضافه کنیم.

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

**PSDNET-129. پیاده‌سازی درست روش برش برای فایل‌های PSD**

{{< highlight java >}}

             // پیاده‌سازی روش برش صحیح برای فایل‌های PSD.

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

**PSDNET-140. پشتیبانی از منبع VsmsResource**

{{< highlight java >}}

 // پشتیبانی از منبع VsmsResource

        static void ExampleOfVsmsResourceSupport()

        {

            string sourceFileName = "EmptyRectangle.psd";

            string exportPath = "EmptyRectangle_changed.psd";

            var im = (PsdImage)Image.Load(sourceFileName);

            using (im)

            {

                var resource = GetVsmsResource(im);

                // خواندن

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

                        throw new Exception("منبع Vsms به غلط خوانده شده است");

                }

                var pathFillRule = (PathFillRuleRecord)resource.Paths[0];

                var initialFillRule = (InitialFillRuleRecord)resource.Paths[1];

                var subpathLength = (LengthRecord)resource.Paths[2];

                // Path fill rule doesn't contain any additional information

                if (pathFillRule.Type != VectorPathType.PathFillRuleRecord || 

                initialFillRule.Type != VectorPathType.InitialFillRuleRecord ||

                initialFillRule.IsFillStartsWithAllPixels != false ||

                subpathLength.Type != VectorPathType.ClosedSubpathLengthRecord ||

                subpathLength.IsClosed != true ||

                subpathLength.IsOpen != false) 

                {

                    throw new Exception("مسیرهای منبع Vsms به غلط خوانده شده است");

                }

                // ویرایش

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

                throw new Exception("منبع Vsms یافت نشد");

            }

            return resource;

        }   

{{< /highlight >}}

**PSDNET-121: لایه‌های قابل مشاهده در زیرپوشه قابل مشاهده در پوشه پنهان پردازش می‌شود، اما نباید**

{{< highlight java >}}

 // لایه‌های قابل مشاهده در زیرپوشه قابل مشاهده در پوشه پنهان پردازش می‌شود، اما نباید

            string sourceFileName = "ALotOfFolders.psd.psd";

            string outputFilePathJpg = "outALotOfFolders.jpg";

            string outputFilePathPsd = "outALotOfFolders.psd";

            var options = new PsdLoadOptions();

     - "outRgb.jpg", new JpegOptions() { Quality = 100 });

            }

{{< /highlight >}}


**PSDNET-119. PSD (حالت RGB با 16 بیت بر کانال) به درستی به JPG تبدیل نمی‌شود**

{{< highlight java >}}

  // Psd به درستی به jpg تبدیل نمی‌شود

            string sourceFileName = "in.psd";

            string exportPath = "outRgb.jpg";

            var options = new PsdLoadOptions();

            using (PsdImage image = (P