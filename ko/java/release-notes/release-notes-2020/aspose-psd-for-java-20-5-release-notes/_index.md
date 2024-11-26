---
title: Aspose.PSD for Java 20.5 - 릴리스 노트
type: docs
weight: 40
url: /ko/java/aspose-psd-for-java-20-5-release-notes/
---

{{% alert color="primary" %}} 이 페이지에는 [Aspose.PSD for Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/)에 대한 릴리스 노트가 포함되어 있습니다. {{% /alert %}} 

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDJAVA-188|문서 변환 진행 상황 지원|기능|
|PSDJAVA-197|채널 당 16 비트와 함께 Grayscale ColorMode PSD 이미지 저장 지원|기능|
|PSDJAVA-198|Nvrt 리소스 (Invert 조정 레이어 리소스) 지원|기능|
|PSDJAVA-200|레이어 그룹용 레이어 마스크 지원|기능|
|PSDJAVA-195|16 비트 채널에 Grayscale ColorMode PSD 이미지를 16비트 RGB PSD 형식으로 저장하는 문제 해결|버그|
|PSDJAVA-196|16 비트 채널에 Grayscale ColorMode PSD 이미지를 8 비트 채널 Grayscale PSD 형식으로 저장하는 문제 해결|버그|
|PSDJAVA-199|ITextPortion을 통한 텍스트 정렬이 우측에서 왼쪽으로 인해 작동하지 않습니다. 출력 파일이 손상됩니다.|버그|
|PSDJAVA-201|Lab Color 및 8 비트/채널이 포함된 특정 Psd 파일을 열려고 할 때 예외 발생|버그|
# **공개 API 변경**
# **추가된 API:**
- 없음
## **제거된 API:**
- 없음
# **사용 예시:**

**PSDJAVA-188. 문서 변환 진행 상황 지원**

{{< highlight java >}}

 // 로딩 및 저장 작업의 진행 핸들러 사용 예제

// 프로그램은 다른 저장 옵션을 사용하여 진행 이벤트를 발생시킵니다.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// 콘솔에 진행 정보를 작성하는 진행 핸들러 생성

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s / %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Apple.psd 로딩 중 ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// 로딩 진행을 보이도록 진행 핸들러 바인딩

loadOptions.setProgressEventHandler(localProgressEventHandler);

// 특정 로딩 옵션을 사용하여 PSD를 로드

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Apple.psd 를 PNG 형식으로 저장하는 중 ----------");

    PngOptions pngOptions = new PngOptions();

    // 출력 이미지를 색상화하고 투명하지 않게 만듭니다.

    pngOptions.setColorType(PngColorType.Truecolor);

    // 저장 진행을 보이도록 진행 핸들러 바인딩

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // 특정 특성으로 PSD를 PNG로 변환

    image.save(outputStream, pngOptions);

    System.out.println("---------- Apple.psd 를 PSD 형식으로 저장하는 중 ----------");

    PsdOptions psdOptions = new PsdOptions();

    // 출력 PSD를 칼라화합니다.

    psdOptions.setColorMode(ColorModes.Rgb);

    // 각 색상 (빨강, 녹색, 파랑)과 복합채널에 대해 채널 설정

    psdOptions.setChannelsCount((short)4);

    // 저장 진행을 보이도록 진행 핸들러 바인딩

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // 특성을 가진 PSD 복사본 저장

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. 채널 당 16 비트와 함께 Grayscale ColorMode PSD 이미지 저장 지원**

{{< highlight java >}}

 // 특정 레이어에 대해 다른 색상 모드, 채널 당 비트 수, 채널 수 및 압축을 적용한 예제입니다.

// 지역 범위에서 접근 가능하게 하는 메서드

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String file,

            short colorMode,

            short channelBitsCount,

            short channelsCount,

            short compression,

            int layerNumber)

    {

        String filePath = file + ".psd";

        String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +

                channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);

        String exportPath = file + postfix + ".psd";

        String pngExportPath = file + postfix + ".png";

        // 미리 정의된 16비트 Grayscale PSD 로드

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // 레이어 둘레의 회색 내부 테두리를 그립니다.

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // 특성을 가진 PSD 복사본 저장

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(colorMode);

            psdOptions.setChannelBitsCount(channelBitsCount);

            psdOptions.setChannelsCount(channelsCount);

            psdOptions.setCompressionMethod(compression);

            image.save(exportPath, psdOptions);

        }

        finally

        {

            image.dispose();

        }

        // 저장된 PSD를 로드

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // 저장된 PSD를 그레이스케일 PNG 이미지로 변환

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // 여기에는 예외가 발생하지 않아야 함

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. Nvrt 리소스 (Invert 조정 레이어 리소스) 지원**

{{< highlight java >}}

 // Invert 조정 레이어의 NvrtResource를 찾는 예제.

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// Invert 조정 레이어가 포함된 미리 정의된 PSD 로드

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Invert 조정 레이어의 리소스를 찾아보기

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // NvrtResource를 찾음

                    nvrtResource = (NvrtResource)layerResource;

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-200. 레이어 그룹용 레이어 마스크 지원**

{{< highlight java >}}

 // 레이어 그룹 용 레이어 마스크 지원 예제. 프로그램은 PSD를 로드하고 저장하여

// 예외를 발생시키지 않습니다.

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// 레이어 그룹에 대한 레이어 마스크가 포함된 미리 정의된 PSD 로드

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // 로드한 PSD를 PNG로 변환

    input.save(outputPng, new PngOptions());

    // PSD의 복사본 저장

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. 채널 당 16 비트와 함께 Grayscale ColorMode PSD 이미지를 16비트 채널 RGB PSD 형식으로 저장하는 문제 해결**

{{< highlight java >}}

 // 16비트 Grayscale PSD를 16비트 RGB로 변환한 다음

// 16비트 그레이스케일이지만 래스터 이미지로 다시 변환하는 예제.

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// 미리 정의된 16비트 Grayscale PSD 로드

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // 레이어 둘레에 회색 내부 테두리 그리기

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // 색상모드를 RBG로 변경한 특성을 가진 PSD 복사본 저장

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Rgb);

    psdOptions.setChannelBitsCount((short)16);

    psdOptions.setChannelsCount((short)4);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// 저장된 PSD를 로드

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // 저장된 PSD를 그레이스케일 PNG 이미지로 변환

    image1.save(pngExportPath, pngOptions); // 여기에는 예외가 발생하지 않아야 함

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. 채널 당 16 비트와 함께 Grayscale ColorMode PSD 이미지를 8비트 채널 Grayscale PSD 형식으로 저장하는 문제 해결**

{{< highlight java >}}

 // 16비트 Grayscale PSD를 8비트 Grayscale로 변환한 다음

// 8비트 그레이스케일 래스터 이미지로 다시 변환하는 예제.

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// 미리 정의된 16비트 Grayscale PSD 로드

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // 레이어 둘레에 회색 내부 테두리 그리기

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // 채널 수를 8비트로 변경한 특성을 가진 PSD 복사본 저장

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Grayscale);

    psdOptions.setChannelBitsCount((short)8);

    psdOptions.setChannelsCount((short)2);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// 저장된 PSD를 로드

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // 저장된 PSD를 그레이스케일 PNG 이미지로 변환

    image1.save(pngExportPath, pngOptions); // 여기에는 예외가 발생하지 않아야 함

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. ITextPortion을 통한 텍스트 정렬이 우측에서 왼쪽으로 인해 작동하지 않습니다. 출력 파일이 손상됩니다.**

{{< highlight java >}}

 // ITextPortion을 통한 오른쪽에서 왼쪽으로 텍스트 레이어 정렬 예제. 프로그램이

// 로드된 PSD의 기존 RTL 텍스트 레이어를 수정하고 수정된 문서의 복사본을 저장합니다.

String sourceFileName = "bidi.psd";

String outputFileName = "bidiOutput.psd";

// RTL 텍스트 레이어가 포함된 미리 정의된 PSD 로드

PsdImage image = (PsdImage)Image.load(sourceFileName);

try

{

    // 레이어로부터 텍스트 포션을 얻기

    TextLayer layer = (TextLayer)image.getLayers()[2];

    ITextPortion[] portions = layer.getTextData().getItems();

    // 텍스트 정렬 변경

    portions[0].getParagraph().setJustification(2);

    // 레이어에 변경 사항 적용

    layer.getTextData().updateLayerData();

    // 수정된 PSD 복사본 저장

    image.save(outputFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-201. Lab Color 및 8 비트/채널을 포함한 특정 Psd 파일을 여는 동안 예외 발생**

{{< highlight java >}}

 // LAB 색상 모드에서 8비