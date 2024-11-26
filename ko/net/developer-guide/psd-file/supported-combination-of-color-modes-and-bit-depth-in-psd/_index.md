---
title: PSD에서 지원되는 Color Modes 및 Bit Depth의 조합
type: docs
weight: 80
url: /ko/net/supported-combination-of-color-modes-and-bit-depth-in-psd/
---

## **설명**
Aspose.PSD는 Adobe Photoshop PSD 파일의 Color Mode 및 Bit Depth를 아무 조합으로도 열 수 있습니다. 이러한 파일을 열고 Low-Level API를 사용하여 파일의 내용을 수정할 수 있습니다. 그러나 일부 인기가 덜 한 특정 조합은 특정 문제가 발생할 수 있으며, 그 중 일부는 Color Modes 제한과 관련이 있습니다.

## **PSD의 읽기 전용 모드에서 지원되는 Color Modes And Bit Depth의 내보내기 조합**

| |비트맵|그레이스케일|색인화된|RGB|CMYK|멀티채널|듀오톤|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|깊이 1|예[](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|-|
|깊이 8|-|예|예|예|예|아니요 Q3-Q4|아니요 Q3-Q4|예[](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|깊이 16|-|예|-|예|예|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|아니요 (Q3-Q4)|
|깊이 32|-|예*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|예*|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|
\* 일부 경우에는 작은 문제가 있을 수 있습니다.

## **PSD의 편집 가능한 모드에서 지원되는 Color Modes 및 Bit Depth의 내보내기 조합**

| |비트맵|그레이스케일|색인화된|RGB|CMYK|멀티채널|듀오톤|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|깊이 1|예|-|-|-|-|-|-|-|
|깊이 8|-|예|아니요|예|예|아니요 Q3-Q4|아니요 Q3-Q4|예*|
|깊이 16|-|예|-|예|예*|-|-|아니요 (Q3-Q4)|
|깊이 32|-|아니요 (Q3-Q4)|-|아니요 (Q3-Q4)|-|-|-|-|
\* 일부 경우에는 작은 문제가 있을 수 있습니다.

특정 Color Mode/Bit Depth 조합의 지원이 필요한 경우 [Aspose 포럼](https://forum.aspose.com/c/psd)에 게시할 수 있습니다.
