---
title: Aspose.PSD .NET 전체 매뉴얼용 어댑터
type: docs
weight: 10
url: /ko/net/adapters/full-manual
keywords: 어댑터 전체 매뉴얼 PSD PSB AI WebP SVG PNG JPEG TIFF GIF BMP 빠른 시작 가이드
description: Aspose.PSD 어댑터 전체 매뉴얼입니다.
---

## 개요

Aspose.PSD 어댑터를 사용하여 Aspose.PSD 기능을 확장하는 방법에 대한 전체 매뉴얼입니다. 어댑터는 Aspose.PSD와 다른 Aspose 제품을 완벽하게 통합하여 추가 통합 코드 작성 없이 파일을 다양한 지원되지 않는 형식으로 손쉽게 내보낼 수 있도록 하는 특별한 Nuget 패키지입니다.

## 라이선스 적용

어댑터에 대한 라이선스 적용에 대한 전체 [기사](/psd/ko/net/adapters/license)를 확인해 주세요.

{{% alert color="primary" %}}
어댑터를 사용하려면 Aspose.PSD 및 어댑티의 라이선스 모두 필요합니다.
{{% /alert %}}

라이선스는 다음 샘플을 사용하여 적용할 수 있습니다:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapters-CSharp-License.cs" >}}

프로젝트의 초기화 모듈에서 한 번에 라이선스를 적용하는 것이 좋습니다.

## Aspose.PSD 어댑터 참조

먼저 [Nuget](https://www.nuget.org/aspose.psd.adapters.imaging)에서 Aspose.PSD.Adapters.Imaging을 참조하거나 [Aspose 릴리스 페이지](https://releases.aspose.com/psd/net/)에서 다운로드하십시오 (어댑터는 현재 메인 릴리스 아티팩트에 분리된 이진으로 포함되어 있습니다).

![필요한 참조](references.png)

추가로 다른 패키지들을 참조해야 할 수도 있습니다.


## 어댑티의 로더 및 익스포터 활성화

### 어댑터 활성화
어댑터를 사용해야 하는 경우 다음 코드를 사용하십시오:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Enable-Adapters.cs" >}}


### 어댑터 비활성화
개발 과정에서 Aspose.PSD 로더를 사용하고 다른 코드 부분에서 어댑티의 로더를 사용해야 하는 경우 어댑터를 비활성화해야 할 수 있습니다. 이 경우 다음 코드를 사용하십시오:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Disable-Adapters.cs" >}}


## 어댑터를 사용하여 이미지 로드

어댑터를 사용하면 SVG 또는 WebP와 같은 Aspose.PSD에서 지원되지 않는 인기있는 형식을 로드할 수 있습니다.

### 간단한 사용
로드하기 위해 다음 코드를 사용하십시오:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Add-Imaging-Adapters-Loading-Unsupported-Formats.cs" >}}


### 복잡한 이미지 처리를 위한 중간 사용
어댑티가 제공하는 추가 옵션을 지정해야 하는 경우 다음 예제를 확인하십시오:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapters-CSharp-Full-Manual-Complex-Loading.cs" >}}


SVG 이미지를 사용하여 모든 이미징 기능을 사용하고 한 번의 메서드 호출로 내보낼 수 있습니다.

## 어댑터를 사용하여 이미지 내보내기

Aspose.PSD에서 지원되지 않는 형식을 [열지 않아도](/ko/net/adapters/load-unsupported-formats) [내보내야 하는](/ko/net/adapters/export-to-unsupported-formats) 많은 상황이 있습니다. 이런 경우 익스포터를 활성화하고 다음 코드를 사용하십시오:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Add-Imaging-Adapters-Exporting-to-Unsupported-Formats.cs" >}}


## 결론

Aspose.PSD 어댑터를 사용하여 파일을 로드하고 내보내는 것은 개발자에게 혁신을 가져다줍니다. 이 강력한 Nuget 패키지를 사용하면 Aspose.PSD를 다른 Aspose 제품과 완벽하게 통합하여 추가 통합 코드 작성 없이 지원되지 않는 파일 형식을 열고 작업하는 것이 이전보다 쉬워집니다. Aspose.PSD 어댑터를 사용하면 추가 코드나 수동 변환 프로세스 없이 시간과 노력을 절약할 수 있습니다. 파일을 로드하거나 내보내는 경우 Aspose.PSD 어댑터는 프로젝트에 새로운 가능성을 열어주는 편리하고 효율적인 솔루션을 제공합니다. Aspose.PSD 어댑터의 힘을 경험하고 개발 프로세스를 더 나은 수준으로 이끌어 보세요.
