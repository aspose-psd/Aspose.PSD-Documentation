---
title: JPEG를 위한 ICC 프로필을 통한 색 공간 변환
type: docs
weight: 60
url: /ko/net/color-space-conversion-for-jpeg-through-icc-profiles/
---

## **JPEG 형식을 위한 색상 관리**


이 기사는 Aspose.PSD API를 사용하여 JPEG 형식을 처리하는 동안 ICC 프로필을 사용하여 색 공간 관리를 수행하는 것을 논의합니다. JPEG의 내부 색 공간은 YCbCr이지만 이 [형식](https://reference.aspose.com/psd/net/aspose.psd/pixelformat)은 회색조, RGB, CMYK 및 YCCK 색 공간을 이미지 메타데이터를 저장하기 위해 사용할 수 있습니다. Aspose.PSD API는 주로 RGB 공간에서 작동하기 때문에 API는 JPEG 파일을 제대로 처리하기 위해 색 공간 변환을 수행해야 합니다. 회색조에서 RGB 및 YCbCr에서 RGB로의 변환은 수학적 변환을 통해 수행될 수 있지만 CMYK 및 YCCK 공간은 쉽게 RGB 공간으로 변환되지 않을 수 있습니다.

Aspose.PSD API는 CMYK 색 공간을 가지는 JPEG 이미지에 대한 직접적인 RGB에서 CMYK 색 변환을 수행해야 합니다. 반면에 YCCK 색 공간을 가지는 이미지는 RGB에서 CMYK에서 YCCK 색 변환을 필요로 합니다. 여기서 CMYK에서 YCCK로의 변환은 처음 세 개의 채널에 적용되는 [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601) 변환이 사용되며 k-채널은 그대로 둡니다. 요약하면, Aspose.PSD API는 CMYK 및 YCCK 이미지에 대한 RGB 및 CMYK 색 공간의 상호 변환을 수행해야 하며 이러한 변환은 색상 및 색상 변환을 도와주는 색의 속성을 설명하는 Look-Up 테이블인 ICC 프로필의 도움을 받아 수행됩니다.


## **ICC 프로필**
ICC 변환 메커니즘은 원본 색 공간을 장치 독립형 CIELAB 또는 CIEXYZ 색 공간으로 매핑하는 "프로필"을 사용합니다. Aspose.PSD는 이 두 색 공간을 사용하여 데이터를 필요한 색 공간으로 변환할 수 있고 추가 프로필을 사용합니다. 따라서 ICC 변환을 위해 사용자는 내부 CIE 색 공간으로 이동하기 위한 하나의 RGB 프로필과 CMYK 색 특성을 얻기 위한 하나의 CMYK 프로필 두 개를 제공해야 합니다. CMYK를 RGB로 변환하려면 프로필을 교체해야 합니다. 즉, 소스 프로필로 CMYK 프로필을 사용하고 대상 프로필로 RGB 프로필을 사용해야 합니다.
## **JPEG를 위한 ICC 프로필을 통한 색 변환**
Aspose.PSD API는 ICC 프로필을 지정하는 간단한 메커니즘을 제공하여 [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions) 클래스를 통해 ICC 프로필을 지정할 수 있습니다. 또한, Aspose.PSD는 SWOP, CMYK 및 sRGB의 샘플 프로필을 핵심에 내장하여 대부분의 일반적인 사용 사례에서 사용자는 특정 프로필을 찾아야 할 필요가 없습니다. 이러한 보정의 단점은 RGB에서 CMYK에서 RGB로의 변환 후 동일한 색상을 기대할 수 없다는 것입니다. 왜냐하면 호환되지 않는 색 공간과 다른 색상 프로필을 사용하여 RGB에서 CMYK에서 RGB로의 변환 후 같은 색상을 기대할 수 없기 때문입니다. 다음 코드 스니펫은 .NET API를 사용하여 Aspose.PSD를 사용하는 방법을 보여줍니다. 여기서 RGB 및 CMYK 색 프로필을 YCCK JPEG 이미지에 지정합니다. 아래 예제에서 RGB 및 CMYK 색 프로필은 변경되고 이미지가 YCCK 색 공간으로 저장됩니다. 이 [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile)과 [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) 속성은 YCCK 색 공간의 픽셀 데이터를 변경하는 데 사용됩니다. 다른 모든 색 공간은 색 데이터를 업데이트하기 위한 색 프로필을 가져오지 않습니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}


프로필을 설정하지 않은 경우 Aspose.PSD for .NET API는 기본 프로필을 대신 사용합니다. 아래 예제에서 대상 프로필 속성을 사용하여 대부분의 JPEG 이미지의 대상 색 공간을 변경합니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}
