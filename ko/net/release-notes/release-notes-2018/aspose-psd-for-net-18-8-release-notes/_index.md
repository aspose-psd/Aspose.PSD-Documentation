---
title: Aspose.PSD for .NET 18.8 - 릴리스 노트
type: docs
weight: 50
url: /ko/net/aspose-psd-for-net-18-8-release-notes/
---

|**Key**|**개요**|**카테고리**|
| :- | :- | :- |
|PSDNET-68|레이어 생성일시 속성 지원|기능|
|PSDNET-67|SheetColor 강조 기능 지원|기능|
|PSDNET-66|레이어를 서로 병합할 수 있는 기능|기능|
|PSDNET-65|텍스트 레이어 바운딩 상자 속성의 일부 지원 추가|기능|
|PSDNET-64|IopaResource 지원 추가|기능|
|PSDNET-56|PSD 형식에 대한 레이어 효과 지원|기능|
|PSDNET-55|.Net용 InterruptMonitor 지원|기능|
|PSDNET-50|레이어 플래튼화 가능성 추가|기능|
|PSDNET-49|레이어의 채우기 불투명도 속성 렌더링 추가|기능|
|PSDNET-43|곡선 조정 레이어 렌더링 구현|기능|
|PSDNET-42|곡선 조정 레이어 지원 추가|기능|
|PSDNET-41|수준 조정 레이어 렌더링 구현|기능|
|PSDNET-40|수준 조정 레이어 지원 추가|기능|
|PSDNET-37|채널 믹서 조정 레이어 지원 추가|기능|
|PSDNET-35|색조/채도 조정 레이어 지원 추가|기능|
|PSDNET-34|수출을 위한 노출 조정 레이어 렌더링 구현|기능|
|PSDNET-31|채널 믹서 조정 레이어를 위한 수출 렌더링 지원 추가|기능|
|PSDNET-26|클리핑 마스크 지원 추가|기능|
|PSDNET-13|레이어 마스크 지원 추가|기능|
|PSDNET-9|사진 필터 조정 레이어 지원 추가|기능|
|PSDNET-8|채널 믹서 조정 레이어 지원 추가|기능|
|PSDNET-7|노출 조정 레이어 지원 추가|기능|
|PSDNET-6|밝기/대비 조정 레이어 지원 추가|기능|
|PSDNET-5|조정 레이어의 부분적 지원 추가|기능|
|PSDNET-3|PSD NoBreak 텍스트 옵션 지원 추가|기능|
|PSDNET-2|런타임에 텍스트 레이어 추가 기능|기능|
|PSDNET-62|TIFF 코덱이 16비트 채널 이미지를 저장할 수 없음|개선|
|PSDNET-61|PSD 이미지 저장시 잘못된 이미지 색상 생성|개선|
|PSDNET-60|왼쪽 상단 모서리 좌표가 업데이트되지 않는 문제 수정|개선|
|PSDNET-59|텍스트 레이어 업데이트 중 예외 발생|개선|
|PSDNET-58|JPEG2000 이미지의 코덱 속성 공개화|개선|
|PSDNET-57|24bpp 옵션 설정을 고쳐 BMP로 내보내기|개선|
|PSDNET-46|CMYK PSD 변환시 조정 레이어가 무시되는 문제 해결|개선|

## **사용 예시:**
**PSDNET-68 레이어 생성일시 속성 지원**

{{< highlight java >}}

 // 레이어 생성일시 속성 사용 예시

string sourceFileName = "OneLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // 새로 생성된 레이어의 생성일시가 업데이트되었는지 확인

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 SheetColor 강조 기능 지원**

{{< highlight java >}}

 // SheetColorHighlight 속성 사용 예시

string sourceFileName = "SheetColorHighlightExample.psd";

string exportPath = "SheetColorHighlightExampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer1 = im.Layers[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, layer1.SheetColorHighlight);

    var layer2 = im.Layers[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, layer2.SheetColorHighlight);



    layer1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;



    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-66 레이어를 서로 병합할 수 있는 기능**

{{< highlight java >}}

 // 두 레이어 병합 예시

var sourceFile1 = "FillOpacitySample.psd";

var sourceFile2 = "ThreeRegularLayersSemiTransparent.psd";

var exportPath = "MergedLayersFromTwoDifferentPsd.psd" 

using (var im1 = (PsdImage)(Image.Load(sourceFile1)))

{

    var layer1 = im1.Layers[1];

    using (var im2 = (PsdImage)(Image.Load(sourceFile2)))

    {

        var layer2 = im2.Layers[0];

        layer1.MergeLayerTo(layer2);

	im2.Save(exportPath);	

    }

}

{{< /highlight >}}

**PSDNET-65 텍스트 레이어 바운딩 상자 속성의 일부 지원 추가**

{{< highlight java >}}

 // 텍스트 BoxBounds 예시

string sourceFileName = "LayerWithText.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    // 레이어의 크기는 렌더링 영역의 크기입니다

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    // TextBoundBox는 텍스트 레이어의 최대 크기입니다. 

    // 여기에 PS에서 텍스트가 맞추려고 할 것입니다

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 IopaResource 지원 추가**

{{< highlight java >}}

 // IopaResource 변경을 통한 Fill Opacity 속성 변경

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];



    var resources = layer.Resources;

    foreach (var resource in resources)

    {

        if (resource is IopaResource)

        {

            var iopaResource = (IopaResource)resource;

            iopaResource.FillOpacity = 200;

        }

    }



    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-56 PSD 형식에 대한 레이어 효과 지원**

{{< highlight java >}}

 using (

    PsdImage image =

        (PsdImage)

        Aspose.PSD.Image.Load(

            sourceFileName,

            new Aspose.PSD.ImageLoadOptions.PsdLoadOptions()

            {

                LoadEffectsResource = true,

                UseDiskForLoadEffectsResource = true

            }))

{

    image.Save(

                output,

                new Aspose.PSD.ImageOptions.PngOptions()

                {

                    ColorType =

                            Aspose.PSD.FileFormats.Png

                            .PngColorType

                            .TruecolorWithAlpha

                });

}

{{< /highlight >}}

**PSDNET-55 .Net용 InterruptMonitor 지원**

{{< highlight java >}}

         public void InterruptMonitorTest(string dir, string ouputDir)

        {

            ImageOptionsBase saveOptions = new ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            SaveImageWorker worker = new SaveImageWorker(dir + "big.psb", dir + "big_out.png", saveOptions, monitor);

            System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(worker.ThreadProc));

            try

            {

                thread.Start();

                // 전체 이미지 변환에 소요되는 시간보다 작아야 함.

                System.Threading.Thread.Sleep(3000);

                // 프로세스 중지

                monitor.Interrupt();

                System.Console.WriteLine("Interrupting the save thread #{0} at {1}", thread.ManagedThreadId, System.DateTime.Now);

                // 중지 대기...

                thread.Join();

            }

            finally

            {

                // 삭제할 파일이 존재하지 않으면 예외가 발생하지 않음.

                System.IO.File.Delete(dir + "big_out.png");

            }

        }

        /// <summary>

        /// 이미지 변환을 시작하고 중지를 대기함.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// 입력 이미지 경로.

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// 출력 이미지 경로.

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// 중지 모니터.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// 저장 옵션.

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// <see cref="SaveImageWorker" /> 클래스의 새 인스턴스를 초기화함.

            /// </summary>

            /// <param name="inputPath">입력 이미지 경로.</param>

            /// <param name="outputPath">출력 이미지 경로.</param>

            /// <param name="saveOptions">저장 옵션.</param>

            /// <param name="monitor">중지 모니터.</param>

            public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// 다른 형식으로 이미지 변환을 시도함. 중단을 처리함. 

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("Expected interruption.");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("The save thread #{0} finishes at {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

                        System.Console.WriteLine(e);

                    }

                    catch (System.Exception e)

                    {

                        System.Console.WriteLine(e);

                    }

                    finally

                    {

                        Multithreading.InterruptMonitor.ThreadLocalInstance = null;

                    }

                }

            }

        }

{{< /highlight >}}

**PSDNET-50 레이어를 플래튼화할 수 있는 기능**

{{< highlight java >}}

 // 전체 PSD 플래튼화

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattened.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.FlattenImage();

    im.Save(exportPath);	 

}

// 다른 레이어와 합치기

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var bottomLayer = im.Layers[0];

    var middleLayer = im.Layers[1];

    var topLayer = im.Layers[2];

    var layer1 = im.MergeLayers(bottomLayer, middleLayer);

    var layer2 = im.MergeLayers(layer1, topLayer);

    // 합쳐진 레이어 설정

    im.Layers = new Layer[] { layer2 };



    im.Save(exportPath);	 

}

{{< /highlight >}}

**PSDNET-49 레이어의 채우기 불투명도 속성 렌더링 추가**

{{< highlight java >}}

 // Fill Opacity 속성 변경

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];

    layer.FillOpacity = 5;

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-43 Curves 조정 레이어 렌더링 구현**

{{< highlight java >}}

 // 커브 레이어 편집

string sourceFileName = "CurvesAdjustmentLayer";

string psdPathAfterChange = "CurvesAdjustmentLayerChanged";

string pngExportPath = "CurvesAdjustmentLayerChanged";

for (int j = 1; j < 2; j++)

{

    using (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

    {

        foreach (var layer in im.Layers)

	{

            if (layer is CurvesLayer)

            {

                 var curvesLayer = (CurvesLayer)layer;

                 if (curvesLayer.IsDiscreteManagerUsed)

                 {

                      var manager = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();

                      for (int i = 10; i < 50; i++)

                      {

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2));

                      }

                 }

                 else

                 {

                      var manager = (CurvesContinuousManager)curvesLayer.GetCurvesManager();

                      manager.AddCurvePoint(0, 50, 100);

                      manager.AddCurvePoint(0, 150, 130);

                 }

            }

        }

    }



    // PSD로 저장

    im.Save(psdPathAfterChange + j.ToString() + ".psd");
	


    // PNG로 저장

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath + j.ToString() + ".png", saveOptions);

}

{{< /highlight >}}

**PSDNET-42 Curves 조정 레이어 지원 추가**

{{< highlight java >}}

 // 커브 레이어 편집

string sourceFileName = "CurvesAdjustmentLayer";

string psdPathAfterChange = "CurvesAdjustmentLayerChanged";

for (int j = 1; j < 2; j++)

{

    using (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

    {

         foreach (var layer in im.Layers)

	 {

            if (layer is CurvesLayer)

            {

                 var curvesLayer = (CurvesLayer)layer;

                 if (curvesLayer.IsDiscreteManagerUsed)

                 {

                      var manager = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();

                      for (int i = 10; i < 50; i++)

                      {

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2));

                      }

                 }

                 else

                 {

                      var manager = (CurvesContinuousManager)curvesLayer.GetCurvesManager();
	
                      manager.AddCurvePoint(0, 50, 100);

                      manager.AddCurvePoint(0, 150, 130);

                 }

            }

	}

    }



    // PSD로 저장

    im.Save(psdPathAfterChange + j.ToString() + ".psd");
}

{{< /highlight >}}

**PSDNET-41 수준 조정 레이어 렌더링 구현**

{{< highlight java >}}

 // 수준 레이어 편집

string sourceFileName = "LevelsAdjustmentLayer.psd";

string psdPathAfterChange = "LevelsAdjustmentLayerChanged.psd";

string pngExportPath = "LevelsAdjustmentLayerChanged.png";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

        if (layer is LevelsLayer)

        {

            var levelsLayer = (LevelsLayer)layer;

            var channel = levelsLayer.GetChannel(0);

            channel.InputMidtoneLevel = 2.0f;

            channel.InputShadowLevel = 10;

channel.InputHighlightLevel = 230;

channel.OutputShadowLevel = 20;

channel.OutputHighlightLevel = 200;

}



// PSD로 저장

im.Save(psdPathAfterChange);



// PNG로 저장

var saveOptions = new PngOptions();

saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

im.Save(pngExportPath, saveOptions);

}


{{< /highlight >}}


**PSDNET-40 수준 조정 레이어 지원 추가**

{{< highlight java >}}

 // 수준 레이어 편집

string sourceFileName = "LevelsAdjustmentLayer.psd";

string psdPathAfterChange = "LevelsAdjustmentLayerChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

        if (layer is LevelsLayer)

        {

            var levelsLayer = (LevelsLayer)layer;

            var channel = levelsLayer.GetChannel(0);

            channel.InputMidtoneLevel = 2.0f;

            channel.InputShadowLevel = 10;

            channel.InputHighlightLevel = 230;

            channel.OutputShadowLevel = 20;

            channel.OutputHighlightLevel = 200;

        }

    }



    // PSD로 저장

    im.Save(psdPathAfterChange);

}

{{< /highlight >}}


**PSDNET-37 채널 믹서 조정 레이어 지원 추가**

{{< highlight java >}}



// RGB 채널 믹서

string sourceFileName = "ChannelMixerAdjustmentLayerRgb.psd";

string psdPathAfterChange = "ChannelMixerAdjustmentLayerRgbChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

         if (layer is RgbChannelMixerLayer)

         {

              var rgbLayer = (RgbChannelMixerLayer)layer;

              rgbLayer.RedChannel.Blue = 100;

              rgbLayer.BlueChannel.Green = -100;

              rgbLayer.GreenChannel.Constant = 50;

         }

    }



    im.Save(psdPathAfterChange);

}

// CMYK 채널 믹서

string sourceFileName = "ChannelMixerAdjustmentLayerCmyk.psd";

string psdPathAfterChange = "ChannelMixerAdjustmentLayerCmykChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

         if (layer is CmykChannelMixerLayer)

         {

             var cmykLayer = (CmykChannelMixerLayer)layer;

             cmykLayer.CyanChannel.Black = 20;

             cmykLayer.MagentaChannel.Yellow = 50;

             cmykLayer.YellowChannel.Cyan = -25;

             cmykLayer.BlackChannel.Yellow = 25;

         }

    }



    im.Save(psdPathAfterChange);

}





// 새 레이어 추가(CMYK 예시)

string sourceFileName = "CmykWithAlpha.psd";

string psdPathAfterChange = "ChannelMixerAdjustmentLayerCmykChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    var newlayer = im.AddChannelMixerAdjustmentLayer();

    newlayer.GetChannelByIndex(2).Constant = 50;

    newlayer.GetChannelByIndex(0).Constant = 50;



    im.Save(psdPathAfterChange);

}		

{{< /highlight >}}


**PSDNET-35 색조/채도 조정 레이어 지원 추가**

{{< highlight java >}}

 // 색조/채도 레이어 편집

string sourceFileName = "HueSaturationAdjustmentLayer.psd";

string psdPathAfterChange = "HueSaturationAdjustmentLayerChanged.psd";

using (var im = LoadFile(sourceFileName))

{

     foreach (var layer in im.Layers)

     {

           if (layer is HueSaturationLayer)

           {

                var hueLayer = (HueSaturationLayer)layer;

                hueLayer.Hue = -25;

                hueLayer.Saturation = -12;

                hueLayer.Lightness = 67;

                var colorRange = hueLayer.GetRange(2);

                colorRange.Hue = -40;

                colorRange.Saturation = 50;

                colorRange.Lightness = -20;

                colorRange.MostLeftBorder = 300;

           }

      }

      im.Save(psdPathAfterChange);

}



// 색조/채도 레이어 추가

string sourceFileName = "PhotoExample.psd";

string psdPathAfterChange = "PhotoExampleAddedHueSaturation.psd";



using (PsdImage im = LoadFile(sourceFileName))

{

     this.SaveForVisualTest(im, this.OutputPath, prefix + file, "before");

     var hueLayer = im.AddHueSaturationAdjustmentLayer();

     hueLayer.Hue = -25;

     hueLayer.Saturation = -12;

     hueLayer.Lightness = 67;

     var colorRange = hueLayer.GetRange(2);

     colorRange.Hue = -160;

     colorRange.Saturation = 100;

     colorRange.Lightness = 20;

     colorRange.MostLeftBorder = 300;



     im.Save(psdPathAfterChange);

}

{{< /highlight >}}