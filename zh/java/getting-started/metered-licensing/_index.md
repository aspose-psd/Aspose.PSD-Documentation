---
title: 计量许可
type: 文档
weight: 70
url: /zh/java/metered-licensing/
---

{{% alert color="primary" %}}

Aspose.PSD 允许开发人员应用计量密钥。这是一种新的许可机制。新的许可机制将与现有许可方法一起使用。那些希望根据 API 功能的使用情况进行计费的客户可以使用计量许可。有关更多详细信息，请参阅 [计量许可FAQ](https://purchase.aspose.com/faqs/licensing/metered) 部分。

{{% /alert %}}
## **计量许可**
以下是使用 Metered 类的简单步骤。

1. 创建 Metered 类的实例。
1. 通过 setMeteredKey 方法传递公钥和私钥。
1. 进行处理（执行任务）。
1. 调用 Metered 类的 getConsumptionQuantity 方法。
1. 它将返回到目前为止已消耗的 API 请求的金额/数量。

以下是演示如何设置计量公钥和私钥的示例代码。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Licensing-MeteredLicensing-MeteredLicensing.java" >}}

