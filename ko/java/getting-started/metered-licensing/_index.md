---
title: 미터링 라이선스
type: 문서
weight: 70
url: /ko/java/metered-licensing/
---

{{% alert color="primary" %}} 

Aspose.PSD는 개발자가 미터링 키를 적용할 수 있도록 합니다. 이것은 새로운 라이선스 메커니즘입니다. 새로운 라이선스 메커니즘은 기존의 라이선스 방법과 함께 사용될 것입니다. API 기능의 사용에 따라 청구를 원하는 고객은 미터링 라이선스를 사용할 수 있습니다. 자세한 내용은 [Metered Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered) 섹션을 참조하십시오.

{{% /alert %}} 
## **미터링 라이선스**
다음은 Metered 클래스를 사용하는 간단한 단계입니다.

1. Metered 클래스의 인스턴스를 생성합니다.
1. setMeteredKey 메서드에 공개 및 비공개 키를 전달합니다.
1. 처리를 수행합니다 (작업 실행).
1. Metered 클래스의 getConsumptionQuantity 메서드를 호출합니다.
1. 지금까지 사용한 API 요청의 양/수량을 반환합니다.

다음은 미터링 공개 및 비공개 키를 설정하는 방법을 보여주는 샘플 코드입니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Licensing-MeteredLicensing-MeteredLicensing.java" >}}
