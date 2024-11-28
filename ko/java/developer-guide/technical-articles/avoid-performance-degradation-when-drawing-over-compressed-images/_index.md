---
title: 압축 이미지 위에 그림 그릴 때 성능 저하 방지
type: docs
weight: 40
url: /ko/java/avoid-performance-degradation-when-drawing-over-compressed-images/
---

## **압축 이미지 위에 그림 그릴 때 성능 저하 방지**
압축된 이미지 위에 매우 복잡한 그래픽 작업을 수행해야 하는 경우가 있습니다. Aspose.PSD가 이미지를 동적으로 압축하고 해제해야 할 때 성능 저하가 발생할 수 있습니다. 압축된 이미지 위에 그림을 그리는 것 또한 성능에 부정적인 영향을 끼칠 수 있습니다.

### **해결책**
성능 저하를 방지하기 위해서는 그래픽 작업을 수행하기 전에 이미지를 압축되지 않은 raw 형식으로 변환하는 것을 권장합니다.

### **파일 경로 사용**
다음 예제에서는 PSD 이미지가 압축되지 않은(raw) 형식으로 변환되고 디스크에 저장됩니다. 그리고 그래픽 작업이 수행되기 전에 압축이 풀린 이미지를 다시 로드합니다. BMP 및 GIF 파일에도 동일한 기술이 적용됩니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}

### **스트림 개체 사용**
다음 코드 스니펫은 PSD 이미지가 압축되지 않은(raw) 형식으로 변환되고 Stream을 사용하여 디스크에 저장되는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}
