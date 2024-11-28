---
title: Aspose.PSD for Java 23.7 - 릴리스 노트
type: docs
weight: 40
url: /ko/java/aspose-psd-for-java-23-7-release-notes/
---

{{% alert color="primary" %}} 이 페이지에는 [Aspose.PSD for Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/)의 릴리스 노트가 포함되어 있습니다. {{% /alert %}}

| **키**     | **요약**                                                                                                                                      | **카테고리** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | PSD 파일의 각 레이어를 애니메이션 GIF 파일로 내보내는 기능 추가                                         | 기능 |
| PSDJAVA-503 | Shape 레이어의 Fill 속성을 vscg 리소스에서 할당                                        | 기능 |
| PSDJAVA-504 | 새로운 와프 유형 추가 (arc 및 arch)                                                                           | 기능 |
| PSDJAVA-505 | 속성 UpdateMetadata가 true로 설정되면 PSD 파일을 저장하는 애플리케이션 변경       | 기능 |
| PSDJAVA-510 | 와프 이미지의 계산 영역 증가                                                              | 기능 |
| PSDJAVA-511 | 흑백 조정 레이어가 반투명을 잘못 처리함                                           | 버그     |
| PSDJAVA-512 | SmartObject ReplaceContents(AllowWarpRepaint 옵션 활성화 시) 계산 후 2분 후에 중단      | 버그     |
| PSDJAVA-513 | 실제 LayerGroup의 좌측 및 상단 위치 가져오는 기능 추가                            | 버그     |
| PSDJAVA-514 | VogkResource를 포인트 단위로 구조화된 PSD 파일의 레이어 크기 조정이 잘못 작동함     | 버그     |
| PSDJAVA-515 | TextBound가 예상대로 작동하지 않음                                                | 버그     |
| PSDJAVA-516 | 기본 생성자를 사용하여 만든 레이어를 PSD 이미지에 추가하면 기본 리소스가 추가되지 않음 | 버그     |
| PSDJAVA-517 | animated GIF로 내보낼 때 Timeline.LoopesCount가 무시됨                             | 버그     |

## **공개 API 변경**
# **추가된 API:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **제거된 API:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **사용 예시:**

**PSDJAVA-502. PSD 파일의 각 레이어를 애니메이션 GIF 파일로 내보내는 기능 추가**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // 각 레이어에 대한 프레임 생성.
        int framesCount = psdImage.getLayers().length;
        Timeline timeline = psdImage.getTimeline();

        Frame[] frames = new Frame[framesCount];
        for (int i = 0; i < framesCount; i++) {
            frames[i] = new Frame();
            LayerState[] layerStates = new LayerState[framesCount];

            for (int j = 0; j < framesCount; j++) {
                layerStates[j] = new LayerState();
                layerStates[j].setEnabled(i == j);
            }
            frames[i].setLayerStates(layerStates);
        }

        timeline.setFrames(frames);

        // 현재 상태 업데이트
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

(이하 생략)