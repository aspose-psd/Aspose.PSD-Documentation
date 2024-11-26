---
title: JPEG를 위한 ICC 프로필을 통한 색 공간 변환
type: docs
weight: 50
url: /ko/java/color-space-conversion-for-jpeg-through-icc-profiles/
---

## **JPEG 형식을 위한 색 관리**


이 문서에서는 Aspose.PSD API를 사용하여 JPEG 형식을 처리하면서 ICC 프로필을 사용하여 색 공간 관리를 수행하는 방법에 대해 설명합니다. JPEG의 내부 색 공간은 YCbCr이지만 해당 형식은 이미지 메타데이터를 저장하기 위해 회색조, RGB, CMYK 및 YCCK 색 공간을 수용할 수도 있습니다. Aspose.PSD API는 주로 RGB 공간에서 작동하기 때문에 API는 JPEG 파일을 올바르게 처리하기 위해 색 공간 변환을 수행해야 합니다. 회색조에서 RGB 및 YCbCr에서 RGB 변환은 수학적 변환을 통해 수행할 수 있지만 CMYK 및 YCCK 공간은 쉽게 RGB 공간으로 변환할 수 없습니다.



Aspose.PSD API는 CMYK 색 공간을 가진 JPEG 이미지에 대해 직접 RGB에서 CMYK 색 변환을 수행해야 합니다. 반면에 YCCK 색 공간을 가진 이미지는 RGB에서 CMYK에서 YCCK 색 변환이 필요하며, CMYK에서 YCCK 변환은 첫 번째 세 개의 채널에 적용된 ITU-R BT.601 변환을 사용하고 k 채널을 건드리지 않습니다. 요약하자면, Aspose.PSD API는 CMYK 및 YCCK 이미지의 RGB 및 CMYK 색 공간의 상호 변환을 수행해야 하며, 이러한 변환은 색 및 색 변환에 도움을 주며 색의 속성을 설명하는 룩업 테이블인 ICC 프로필의 도움으로 수행됩니다.


## **ICC 프로필**
ICC 변환 메커니즘은 소스 색 공간을 장치 독립적인 CIELAB 또는 CIEXYZ 색 공간에 매핑하는 "프로필"을 사용합니다. Aspose.PSD는 데이터를 이러한 두 색 공간으로 변환하는 데 필요한 추가 프로필을 사용하며 ICC 변환을 위해 사용자는 두 개의 프로필을 제공해야 합니다. 따라서 CMYK를 RGB로 변환하려면 프로필을 스왑해야 합니다; 즉, CMYK 프로필을 소스 프로필로 사용하고 RGB 프로필을 대상 프로필로 사용해야 합니다.
## **ICC 프로필을 통한 JPEG의 색 변환**
Aspose.PSD API는 사용자에게 JpegOptions 클래스를 통해 ICC 프로필을 지정하기 쉬운 메커니즘을 제공하여 세부 정보를 숨깁니다. 또한 Aspose.PSD는 흔히 사용되는 경우에 대부분의 경우 사용자가 특정 프로필을 찾을 필요가 없는 SWOP CMYK 및 sRGB의 샘플 프로필을 포함하고 있기 때문에 해당 보정의 단점이 있습니다; 즉, RGB를 CMYK로 변환한 후 CMYK를 RGB로 변환한 후에도 동일한 색을 얻을 것으로 기대할 수 없어서 호환되지 않는 색 공간 및 다른 색 프로필로 인해 색 공간 변환은 되돌릴 수 없습니다. 다음 코드 스니펫은 Aspose.PSD를 사용한 자바 API 예제를 보여줍니다. 여기서 RGB 및 CMYK 색 프로필을 YCCK JPEG 이미지에 지정합니다. 아래 예제에서 RgbColorProfile 및 CmykColorProfile 속성은 YCCK 색 공간의 픽셀 데이터를 변경하는 데 사용됩니다. 다른 모든 색 공간은 컬러 데이터를 업데이트하기 위해 컬러 프로필을 가져오지 않습니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.java" >}}



프로필이 설정되지 않은 경우 Aspose.PSD를 사용하는 Java API는 기본 프로필을 사용할 것입니다. 아래 예제는 대부분의 JpegImages에 대한 대상 프로필 속성을 사용합니다.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.java" >}}
