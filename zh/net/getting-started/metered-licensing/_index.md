---
title: 计量许可
type: docs
weight: 80
url: /zh/net/metered-licensing/
description: PSD Photoshop C＃库允许开发人员应用按量计费密钥，这是一种新的许可机制，将与现有许可方法一起使用。
---

{{% alert color="primary" %}} 

Aspose.PSD允许开发人员应用按量计费密钥。这是一种新的许可机制。这种新的许可机制将与现有许可方法一起使用。那些希望根据API功能的使用情况进行计费的客户可以使用计量许可。有关更多详细信息，请参阅[Metered Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered)部分。

{{% /alert %}} 
## **计量许可**
以下是使用Metered类的简单步骤。

1. 创建Metered类的实例。
1. 将公共和私钥传递给setMeteredKey方法。
1. 进行处理（执行任务）。
1. 调用Metered类的getConsumptionQuantity方法。
1. 它将返回到目前为止已消耗的API请求的金额/数量。

以下是演示如何设置按量计费公钥和私钥的示例代码。

{{< highlight java >}}

 // 创建PSD Metered类的实例

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// 访问setMeteredKey属性并将公共和私钥作为参数传递

metered.SetMeteredKey("*****", "*****");



// 在调用API之前获取计量数据量

decimal amountbefore = Aspose.PSD.Metered.GetConsumptionQuantity();



// 显示信息

Console.WriteLine("消费金额： " + amountbefore.ToString());

// 在调用API后获取计量数据量

decimal amountafter = Aspose.PSD.Metered.GetConsumptionQuantity();



// 显示信息

Console.WriteLine("消费金额： " + amountafter.ToString());

{{< /highlight >}}
