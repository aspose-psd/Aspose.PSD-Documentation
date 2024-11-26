---
title: Aspose.PSD 성능 향상을 위한 사용자 정의 캐시
type: docs
weight: 20
url: /ko/net/aspose-psd-performance-improvement-using-customizable-cache/
---

## **사용자 정의 캐시로 성능 향상**
[Aspose.PSD](https://products.aspose.com/psd/family)는 임시 데이터 저장을 위해 캐싱을 사용합니다. 이 메커니즘은 사용하기 쉬우며 사용자 정의가 가능하며 투명합니다. 이미지 처리 중에 성능 문제가 없도록 보장합니다. 이 문서에서는 .NET용 Aspose.PSD API를 사용하여 캐시를 사용자 정의하는 방법을 설명합니다.

### **캐시 사용자 정의**
프로세스가 임시 데이터 저장 공간이 필요할 때, 해당 공간은 캐시에 할당됩니다. 캐시는 메모리나 디스크 상에 있을 수 있으며 사용자에 의해 설정됩니다. 임시 데이터가 더 이상 필요하지 않을 때 그 공간은 해제됩니다. 할당된 공간의 통계는 언제든지 검토할 수 있습니다. Aspose.PSD가 어떻게 캐시를 할당하고 사용하는지를 사용자 정의할 수 있습니다. 이 섹션에서는 다양한 설정과 그 기본값을 설명하고 아래의 코드 스니펫은 어떻게 사용할 수 있는지 보여줍니다.

### **캐시 할당 위치 설정**
캐시 공간이 할당되는 방식을 사용자 정의하려면 [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype) 속성을 설정하세요. 기본적으로 캐시는 메모리에 할당되며 더 이상 메모리에 공간이 없으면 디스크에 할당됩니다. 이러한 동작은 Auto 모드에 의해 캡처됩니다. Auto 모드는 유연하며 성능을 최대화합니다. 다른 모드도 있습니다:

- CacheOnDiskOnly 모드: 오직 디스크에만 할당
- CacheInMemoryOnly 모드: 오직 메모리에만 할당

CacheOnDiskOnly 모드를 선택하면 성능이 저하될 수 있습니다.

### **캐시의 크기 설정**
[MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) 및 [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache) 속성을 설정하여 디스크나 메모리에 할당할 수 있는 최대 공간(바이트)을 설정하세요. 기본적으로 두 값은 0으로 설정되어 있어 상한선이 없음을 의미합니다.

### **캐시 재할당 제어**
새 캐시가 할당될 때에 메모리에 충분한 공간이 없는 경우(MaxMemoryForCache 속성에 지정된대로), 캐시는 디스크에 할당됩니다. 디스크에 충분한 공간이 없는 경우, 예외가 throw됩니다. 캐시 할당 프로세스는 메모리에서 디스크로 이동하지만 그 반대는 안됩니다. [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) 속성은 메모리 재할당을 제어하는 데 사용됩니다. 재할당은 미리 할당된 캐시의 경우 가장 가능성이 높습니다. 할당된 공간이 충분하지 않을 것으로 판단될 때 일어날 수 있습니다. ExactReallocateOnly 속성이 기본값 False로 설정되어 있으면, 공간은 동일한 매체로 재할당됩니다. True로 설정하면, 재할당은 최대 지정된 공간을 초과할 수 없습니다. 이 경우 이미 할당된 메모리 캐시(재할당이 필요한)는 해제되고 디스크에 확장된 공간이 할당됩니다.

### **프로그램 샘플**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.cs" >}}
