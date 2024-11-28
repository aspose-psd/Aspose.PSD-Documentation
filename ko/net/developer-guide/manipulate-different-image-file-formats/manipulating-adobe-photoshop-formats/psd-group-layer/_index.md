---
title: Aspose.PSD를 사용한 그룹 레이어 예제(C#)
weight: 100
type: docs
description: C#을 통한 PSD 파일의 그룹 레이어 사용 방법
keywords: [레이어 그룹, 그룹 레이어, 레이어 추가, psd api, C#, 샤프, 코드 샘플]
url: ko/net/psd-group-layer/
---

## 개요

Aspose.PSD의 C#에서 그룹 레이어는 PSD 파일의 레이어를 효율적으로 조직화하고 조작할 수 있게 합니다. 폴더 레이어를 사용하면 여러 레이어를 그룹화하고 전체 그룹에 변형이나 효과를 적용할 수 있습니다.

이 예제는 `PsdImage.Create`를 사용하여 새 PSD 이미지를 생성하는 방법을 보여줍니다. 그런 다음 `PsdImage` 객체에서 `AddLayerGroup`를 사용하여 새 `LayerGroup` 객체를 생성합니다. 그룹 레이어는 "폴더"라는 이름으로 생성되며 0번 인덱스에 삽입되고 표시됩니다.

이후, `DisplayName` 속성이 설정된 두 개의 `Layer` 객체가 생성됩니다. 이러한 레이어들은 `AddLayer`를 사용하여 그룹 레이어에 추가됩니다.

그룹 내의 레이어들은 `LayerGroup` 객체의 `Layers` 속성을 통해 액세스할 수 있습니다. 이 예제는 그룹 내 첫 번째 및 두 번째 레이어의 표시 이름이 각각 "Layer 1" 및 "Layer 2"임을 확인합니다.

그룹 레이어를 수정한 후에는 `PsdImage` 객체의 `Save` 메서드를 사용하여 업데이트된 PSD 이미지를 저장합니다.

이 기본 예제는 Aspose.PSD for C#을 사용하여 그룹 레이어를 다루는 방법을 소개합니다. 이 라이브러리는 PSD 파일의 레이어를 조작하고 변형하기 위한 고급 기능을 제공합니다. 자세한 예제 및 기능은 Aspose.PSD for C# 문서를 참조하십시오.

다음은 Aspose.PSD for C#에서 그룹 레이어 사용법을 보여주는 샘플 코드입니다:

## 예제

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

자세한 정보 및 예제는 [Aspose.PSD for C# 문서](https://docs.aspose.com/psd/net/)를 방문해주십시오.

