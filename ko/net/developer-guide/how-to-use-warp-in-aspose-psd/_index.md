---
title: Aspose.PSD에서 워프 사용하는 방법
type: docs
weight: 40
url: /ko/net/how-to-use-warp-in-aspose-psd/
---

## **부분 1 – 워프 효과가 적용된 PSD 파일 렌더링하기**

포토샵은 워프 효과를 적용한 후 렌더링된 이미지를 저장합니다. 저희 라이브러리는 워프 효과가 적용된 이미지를 재현하거나 다시 렌더링할 수 있습니다. 이 기능을 활성화하려면 PSD 파일을 열 때 설정에서 AllowWarpRepaint 플래그를 설정하면 됩니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-1.cs" >}}

결과:
![Aspose.PSD for .NET 워프 결과 1](warp1.png)

스마트 레이어에 대한 워프 효과를 렌더링하는 것 외에도, 저희 라이브러리는 텍스트 레이어에 대한 워프도 지원합니다. 구현 코드는 파일 이름을 제외하고 동일하며, 유일한 차이점은 파일 이름입니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-2.cs" >}}

결과:
![Aspose.PSD for .NET 워프 결과 2](warp2.png)

**! 참고:** 현재 저희 라이브러리는 사용자가 메시 포인트를 조작하는 사용자 지정 워프 및 모든 표준 워프 유형을 지원합니다.

## **부분 2 – 워프 효과 수정하기**

저희 라이브러리를 통해 워프 효과를 렌더링뿐만 아니라 수정(추가)할 수 있습니다.
이러한 수정 사항은 **WarpParams** 클래스의 기능을 통해 용이하게 이루어집니다.

| **기능**   | **설명**                                                    | 
|:----------|:--------------------------------------------------------|
| Bounds    | 워프된 이미지의 경계를 반환합니다.                          |
| MeshPoints| 각 포인트가 워프 메시의 정점을 나타내는 포인트 배열입니다. |
| Value     | 사용자 지정 워프 효과에 대한 워프 효과의 값입니다.        |
| WarpRotates| 표준 외 워프 효과의 방향을 정의하는 열거형입니다.         |
| WarpStyles| 워프 효과의 유형을 정의하는 열거형입니다.                 |

아래 코드 예제는 스마트 레이어의 워프 효과 유형을 결정하고 효과의 유형과 왜곡의 강도를 조절하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-3.cs" >}}

결과:
![Aspose.PSD for .NET 워프 결과 3](warp3.png)

## **부분 3 – 워프 효과 추가하기**

아래 코드 예제는 스마트 레이어에 표준 워프 효과를 추가하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-4.cs" >}}

결과:
![Aspose.PSD for .NET 워프 결과 4](warp4.png)

아래 코드 예제는 스마트 레이어에 사용자 지정 워프 효과를 추가하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-5.cs" >}}

결과:
![Aspose.PSD for .NET 워프 결과 5](warp5.png)

아래 코드 예제는 텍스트 레이어에 워프 효과를 추가하는 방법을 보여줍니다.
**! 참고:** 포토샵의 표준에 따라 텍스트 레이어의 워프 효과는 일반적으로 표준 유형으로 제한됩니다. 그러나 저희 라이브러리는 두 가지 유형의 워프 효과 사용을 지원합니다. 이러한 파일은 포토샵과 완전히 호환되지 않을 수 있음에 유의하십시오.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-5.cs" >}}

결과:
![Aspose.PSD for .NET 워프 결과 6](warp6.png)

저희는 워프 효과의 성능, 품질 및 지원 기능을 지속적으로 개선 및 확대하고 있으며 최신 개발 동향을 확인하려면 매월 릴리스를 확인해 주세요.
귀하의 Aspose.PSD 팀
