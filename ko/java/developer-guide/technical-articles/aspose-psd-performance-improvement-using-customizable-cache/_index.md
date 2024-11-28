---
title: Aspose.PSD의 사용자 정의 캐시를 활용한 성능 향상
type: docs
weight: 30
url: /ko/java/aspose-psd-performance-improvement-using-customizable-cache/
---

## **사용자 정의 캐시로 성능 향상**
Aspose.PSD는 임시 데이터 저장을 위해 캐싱을 사용합니다. 이 메커니즘은 사용하기 쉽고 사용자 정의가 가능하며 투명합니다. 이미지 처리 중 성능 문제가 없도록 보장합니다. 이 문서에서는 Aspose.PSD API를 사용하여 캐시를 사용자 정의하는 방법을 설명합니다.

### **캐시의 사용자 정의**
프로세스가 임시 데이터 저장이 필요할 때 해당 저장소는 캐시에 할당됩니다. 캐시는 메모리나 디스크에 공간을 할당할 수 있으며 사용자에 의해 설정됩니다. 임시 데이터가 더 이상 필요하지 않을 때 해당 공간은 해제됩니다. 할당된 공간의 통계는 언제든지 확인할 수 있습니다. Aspose.PSD가 캐시를 어떻게 할당하고 사용하는지를 사용자가 사용자 정의할 수 있습니다. 이 섹션에서는 각 설정과 그 기본값을 설명하며, 아래 코드 조각들은 설정 방법을 보여줍니다.

### **캐시가 할당되는 위치 설정**
캐시 공간이 할당되는 방식을 사용자 정의하려면 CacheType 속성을 설정하면 됩니다. 기본적으로 캐시는 메모리에 할당되며, 메모리에 더 이상 공간이 없을 때 디스크에 할당됩니다. 이 동작은 Auto 모드로 캡쳐됩니다. Auto 모드는 유연하며 성능을 극대화합니다. 다른 모드에는 다음이 있습니다:

- CacheOnDiskOnly 모드: 디스크에만 할당.
- CacheInMemoryOnly 모드: 메모리에만 할당.

CacheOnDiskOnly 모드를 선택하면 성능이 저하될 수 있습니다.

### **캐시의 크기 설정**
MaxDiskSpaceForCache 및 MaxMemoryForCache 속성을 설정하여 디스크나 메모리에 할당될 수 있는 최대 공간(바이트)을 설정합니다. 기본적으로 두 값은 0으로 설정되어 상한선이 없음을 의미합니다.

### **캐시 재할당 제어**
새 캐시가 할당될 때 메모리에 충분한 공간이 없을 경우(MaxMemoryForCache 속성에 지정된대로), 캐시는 디스크에 할당됩니다. 디스크에 충분한 공간이 없는 경우 예외가 발생합니다. 캐시 할당 과정은 메모리에서 디스크로 이동하지만 그 반대로는 이동하지 않습니다. ExactReallocateOnly 속성을 사용하여 메모리 재할당을 제어합니다. 재할당은 미리 할당된 캐시의 경우 가장 가능성이 높습니다. 시스템이 할당된 공간이 충분하지 않을 것으로 판단하면 재할당될 수 있습니다. ExactReallocateOnly가 기본값 False로 설정된 경우, 공간은 같은 매체로 재할당됩니다. True로 설정된 경우, 재할당은 지정된 최대 공간을 초과할 수 없습니다. 이 경우, 기존에 할당된 메모리 캐시(재할당이 필요한 경우)가 해제되고 디스크에 확장된 공간이 할당됩니다.

### **프로그램 샘플**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.java" >}}
