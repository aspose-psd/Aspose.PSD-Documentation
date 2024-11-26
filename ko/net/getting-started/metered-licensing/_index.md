---
title: 미터링 라이선싱
type: 문서
weight: 80
url: /ko/net/metered-licensing/
description: PSD Photoshop C# 라이브러리를 사용하면 미터링 키를 적용할 수 있으며, 이는 새로운 라이선싱 메커니즘이며 기존 라이선싱 방법과 함께 사용될 것입니다.
---

{{% alert color="primary" %}} 

Aspose.PSD는 미터링 키를 적용할 수 있게 합니다. 이는 새로운 라이선싱 메커니즘입니다. 새로운 라이선싱 메커니즘은 기존 라이선싱 방법과 함께 사용됩니다. API 기능 사용에 따라 청구 받고 싶은 고객은 미터링 라이선싱을 사용할 수 있습니다. 자세한 내용은 [미터링 라이선싱 FAQ](https://purchase.aspose.com/faqs/licensing/metered) 섹션을 참조하십시오.

{{% /alert %}} 
## **미터링 라이선싱**
다음은 Metered 클래스를 사용하는 간단한 단계입니다.

1. Metered 클래스의 인스턴스를 만듭니다.
1. setMeteredKey 메서드에 공개 및 비공개 키를 전달합니다.
1. 처리를 수행합니다 (작업 수행).
1. Metered 클래스의 getConsumptionQuantity 메서드를 호출합니다.
1. 지금까지 사용한 API 요청의 양/수량이 반환됩니다.

다음은 미터링 공개 및 비공개 키를 설정하는 방법을 보여주는 샘플 코드입니다.

{{< highlight java >}}

 // PSD Metered 클래스의 인스턴스 생성

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// setMeteredKey 속성에 액세스하여 공개 및 비공개 키를 매개변수로 전달합니다.

metered.SetMeteredKey("*****", "*****");



// API를 호출하기 전에 미터링 데이터 양 가져오기

decimal amountbefore = Aspose.PSD.Metered.GetConsumptionQuantity();



// 정보 표시

Console.WriteLine("사용 전 소비 양: " + amountbefore.ToString());

// API를 호출한 후 미터링 데이터 양 가져오기

decimal amountafter = Aspose.PSD.Metered.GetConsumptionQuantity();



// 정보 표시

Console.WriteLine("사용 후 소비 양: " + amountafter.ToString());

{{< /highlight >}}
