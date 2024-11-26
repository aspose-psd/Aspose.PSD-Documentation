---
title: Raw Data Processing
type: docs
weight: 50
url: /ko/net/raw-data-processing/
---

## **Raw Data Processing**
Aspose.PSD API의 성능을 향상시키기 위해 2.4.0 버전에서 Raw Data Processing 방법을 도입했습니다. Raw Data Processing은 현재 내부에서 사용되며 외부 API를 통해 외부 라이브러리에서 전반적인 성능을 향상시키기 위해 사용할 수 있습니다. 처리 과정이 가끔 까다로울 수 있어 설명이 필요합니다. Raw Data Processing은 현재 BMP 형식에만 사용할 수 있습니다.

개발자들이 최상의 성능을 얻을 수 있도록 도와주기 위해 Aspose.PSD API는 외부 API를 통한 원시 데이터 처리 시스템을 제공합니다. 개발자는 원시 데이터 처리를 사용하기 위해 [LoadRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadrawdata/index) 및 [SaveRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/saverawdata) 메소드 패밀리를 호출합니다. 이러한 메소드는 [RawDataSettings](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings) 클래스를 사용하여 원하는 원시 데이터 형식을 설정해야 합니다. RawDataSettings 클래스를 사용하면 개발자가 원시 데이터 형식을 지정할 수 있습니다. 그러나 최상의 성능을 얻으려면 데이터가 저장된 형식을 사용해야 합니다. RasterImage 클래스에 정의된 RawDataSettings는 이미지의 원시 [데이터 형식](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings/properties/pixeldataformat)을 결정하는 데 도움을 줍니다. RawDataSettings 인스턴스를 LoadRawData 메소드에 전달하면 데이터가 변환을 적용하지 않고 반환되어 성능을 향상시킬 수 있습니다. 그 반대로 때로는 복잡해 질 수 있는 모든 가능한 원시 데이터 형식 레이아웃을 고려해야 합니다.

처리 과정을 간소화하려면 일부 성능 저하를 감수하고 이 클래스를 사용하여 원하는 RawDataSettings를 지정할 수 있습니다. 여기서 주의해야 할 점은 지정된 형식으로 원시 데이터를 반환할 수 없는 경우(예: CMYK 색 공간에서 RGB로의 변환이 2.4.0 버전에서 사용할 수 없을 때)나 이미지 형식에 대해 원시 데이터 처리를 사용할 수 없는 시나리오가 있는 경우입니다. LoadRawData 및 SaveRawData 메소드 패밀리를 사용할 수 있는지 확인하려면 [IsRawDataAvailable](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/israwdataavailable) 속성을 쿼리해야 합니다.
### **통찰**
RGB [픽셀 데이터 형식](https://reference.aspose.com/psd/net/aspose.psd/pixeldataformat)에 대한 색인(팔레트 기반) 및 RGB 기반 원시 데이터 형식을 사용할 수 있습니다. 색인 원시 데이터 형식은 0에서 2의 비트 수 - 1의 범위에 팔레트 항목 색인을 포함합니다. 색인 원시 데이터 형식은 픽셀 당 1, 2, 4및 8비트입니다. 나머지는 RGB 기반 원시 데이터 형식입니다. Raw 데이터를로드할 때 데이터를로드하기에 충분한 바이트가 있는지 주의해야 합니다. 그렇지 않으면 적절한 예외가 발생할 수 있습니다. 원시 데이터 크기를 측정하기 위해 필요한 바이트 배열 크기는 줄 크기를 필요한 줄 수로 곱한 결과에 따라 달라질 수 있습니다. 줄 크기는 원시 데이터 저장 형식에 따라 달라질 수 있습니다.

최상의 성능을 달성하려면 항상 [RasterImage.RawLineSize](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawlinesize) 속성 값과 같은 원시 데이터 줄 크기를 사용해야 합니다. 그러나 경우에 따라 원시 데이터 행에 추가 패딩을 추가하거나 제거해야 하는 경우가 있습니다. 그럴 때는 다른 줄 크기를 사용해야 할 수도 있습니다. 이미지 바운딩 사각형의 하위 집합이 필요한 경우, 인덱스 RGB 픽셀 형식에 대해 발생할 수 있는 비트 시프트를 고려해야 합니다. 예를 들어, 두 가지 경우를 살펴보겠습니다. 100x100 픽셀의 이미지가 있고 픽셀당 1비트의 원시 데이터 형식이 있습니다. (0)의 위치 및 차원인 원시 데이터 사각형을로드하고 싶은 경우, 또는 다른 방식으로 말하면 x=7 및 y=0에서 시작하는 2픽셀이 필요한 경우가 있습니다. 이 경우 다음 데이터 레이아웃을 받게 됩니다:



![todo:image_alt_text](raw-data-processing_1.png)

이것은 첫 번째 바이트에 7개의 원하지 않는 픽셀이 있고, 두 번째 바이트에 1개의 원하는 픽셀이 있음을 의미합니다. 그리고 다음으로 1개의 원하는 픽셀과 7개의 원하지 않는 픽셀이 포함되어 있습니다. 이렇게 하지 않고 어떻게 2픽셀을 하나의 바이트로 넣지 않고 데이터 이동을 수행하지 않았나요? 답은 간단합니다. 성능을 유지하기 위해서입니다. 모든 내부 처리는 일반적으로 첫 번째 픽셀에서 시작하여 마지막 사용 가능한 픽셀로 끝납니다. 픽셀 하위 집합이 필요한 드물고, 그 픽셀이 이후에 어떻게 처리될지 모르기 때문에 이동은 성능을 떨어뜨리며 코드를 불필요하게 복잡하게 만듭니다. 요구 픽셀이 시작할 올바른 비트를 추정하도록 항상 유념하세요. 올바른 비트를 계산하는 데 간단한 공식을 사용할 수 있습니다: (rect.Left * 비트 수) % 8.
### **색인 RGB 색상 변환**
가능한 최상의 성능을 얻으려면 항상 동일한 소스 및 대상 원시 데이터 설정, 픽셀 형식 및 줄 크기를 사용해야 합니다. 그러나 때로는 데이터 변환이 필요할 수도 있습니다. 예를 들어, 1비트 픽셀 RGB 이미지를로드하여 2비트 픽셀로 저장하거나 4비트 RGB 이미지를로드하여 색 범위를 2비트 픽셀로 줄일 수 있습니다. 이 경우 색상 변환이 적용되어야 합니다. 색인 RGB 이미지를 변환하는 것은 때로는 까다롭고 설정을 적용하지 않으면 수행되지 않을 수 있습니다. 소스 색상 범위가 대상 색 공간에 매핑되는 방법을 결정해야 합니다. 이 작업을 수행하기 위해 다양한 [모드](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods)가 있습니다:

- 팔레트 매핑(DitheringMethods.PaletteConversion)
- 원시 데이터 매핑(DitheringMethods.PaletteIgnore)
- 사용자 정의 변환(DitheringMethods.CustomConverter)

팔레트 변환을 사용할 때 소스 색 공간은 가능한 한 대상 색 공간과 가장 유사하게 일치하려고 시도합니다. 예를 들어 다음과 같은 색상이 있는 4비트 이미지를 가정해 보겠습니다:
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
[3] RGB=51, 51, 51
[4] RGB=68, 68, 68
[5] RGB=85, 85, 85
[6] RGB=102, 102, 102
[7] RGB=119, 119, 119
[8] RGB=136, 136, 136
[9] RGB=153, 153, 153
[10] RGB=170, 170, 170
[11] RGB=187, 187, 187
[12] RGB=204, 204, 204
[13] RGB=221, 221, 221
[14] RGB=238, 238, 238
[15] RGB=255, 255, 255

소스 이미지는 다음과 같습니다:



![todo:image_alt_text](raw-data-processing_2.png)

그리고 4비트 이미지를 다음의 팔레트 색상이 정의된 1비트 이미지로 변환합니다:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

팔레트 변환 모드에서 변환기는 소스 색을 읽어 대상 팔레트의 [GetNearestColorIndex](https://reference.aspose.com/psd/net/aspose.psd/icolorpalette/methods/getnearestcolorindex/index) 메소드를 사용하여 대상 인덱스를 결정합니다. 팔레트의 GetNearestColorIndex 메소드가 범위를 벗어나는 인덱스를 줄 경우 [RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex) 속성 값이 사용됩니다. 이렇게 하면 소스 색이 강도 값에 대해 가능한 가장 가까운 대상 색에 대응됩니다. 다음 결과를 확인할 수 있습니다:


![todo:image_alt_text](raw-data-processing_3.png)

원시 데이터 매핑 모드에서는 다른 시나리오가 사용됩니다. 소스 및 대상 색 팔레트가 무시되고 소스 인덱스가 대상 인덱스로 매핑됩니다. 값이 대상 범위로 매핑할 수 없을 경우(비트 수를 줄일 때) RasterImage.RawFallbackIndex 속성 값이 사용됩니다. 이 값은 기본적으로 0이며 대상 팔레트의 첫 번째 색에 대응됩니다. 이 속성 값이 대상 범위를 벗어나면 적절한 예외가 발생합니다. 해당 이미지에 표현할 수 있는 결과가 덜 예측 가능하고 다음 이미지에서 확인할 수 있습니다:


![todo:image_alt_text](raw-data-processing_4.png)

팔레트 변환 모드는 색 매핑 문제에 대한 더 정확한 해결책이지만 올바른 팔레트 매핑을 추정하기 위해 계산을 수행해야 하므로 조금 더 오랜 시간이 걸릴 수 있습니다. 반면, 원시 매핑 모드는 조금 더 빠르게 수행되어 정확한 색 매핑이 중요하지 않은 경우에 사용될 수 있습니다. 예를 들어, 소스 색 팔레트가 잘린 경우나 추가 비트를 사용하지 않은 경우에 안전하게 비트 수를 줄일 수 있는 경우가 있습니다.

이러한 접근 방식 중 하나를 사용하려면 RasterImage 클래스의 RawDitheringMethod 속성을 사용하세요. 기본적으로 최상의 결과를 얻기 위해 팔레트 무시 및 팔레트 변환 디더링 방법이 사용되지 않을 수 있습니다. 이미지를로드하고 원래 픽셀 데이터의 일부를 수정했다면 새 데이터가 캐시로 이동하고 캐시는 가능한 모든 형식 32ARGB(2.4.0 기준, 변경될 수 있음)으로 데이터를 저장합니다. 이 형식을 사용하여 로드된 이미지와 저장된 이미지의 가능한 다른 색 범위와 관렬된 문제를 극복합니다. 또한 팔레트 무시 및 팔레트 변환 디더링 방법은 이미지가 RGB 모드로 로드되고 색인 모드로 또는 그 반대로 변환되는 경우에도 무시됩니다.
### **사용자 정의 색상 변환기**
때로는 표준 색상 변환 방법만으로는 충분하지 않을 수 있습니다. 색상 변환 루틴을 사용할 때 완전한 자유도를 얻기 위해 사용자 정의 알고리즘을 사용하려고 할 수 있습니다. 소스와 대상 이미지의 픽셀 형식이 모두 색인 RGB 형식인 경우 더 간단한 인터페이스, [IIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/iindexedcolorconverter)를 사용할 수 있습니다. RasterImage.RawIndexedColorConverter 속성을 IIndexedColorConverter 인터페이스의 인스턴스로 설정하고 [DitheringMethods](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods).CustomConverter을 RawDitheringMethod 속성 값으로 사용해야 합니다. 이 조합이 적용되면 모든 색인 색 변환이 지정된 IIndexedColorConverter 인스턴스를 통해 수행됩니다. 사용자 지정 인덱스 색상 변환기에는 다음과 같은 메소드가 정의되어 있습니다:



{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



변환이 필요할 때 호출되는 FillIndexedtoIndexedMap 메소드입니다. 맵 배열의 길이는 모든 가능한 소스 형식 항목 수입니다. 이 배열을 채워 소스 색 팔레트 항목을 대상 팔레트 항목으로 매핑해야 합니다. 대상 인덱스 값이 0에서 (비트 수 - 1) 범위에 있어야 하며, 그렇지 않으면 적절한 예외가 발생합니다.

더 세부적인 색 변환 시나리오를 수행해야 하는 경우 [RasterImage.RawCustomColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawcustomcolorconverter) 속성을 [IColorConverter](https://reference.aspose.com/psd/net/aspose.psd/icolorconverter) 인터페이스의 인스턴스로 설정해야 합니다. RawCustomColorConverter 속성은 항상 RawIndexedColorConverter 속성을 재정의하며 둘 다 설정된 경우에는 인덱스