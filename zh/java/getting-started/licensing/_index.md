---
title: 许可
type: docs
weight: 60
url: /zh/java/licensing/
---

## **评估版本限制**
您可以从[下载页面](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/)下载 Aspose.PSD for Java 的评估版本。 评估版本提供与组件完全许可版本相同的功能，但有几个限制。购买 Aspose.PSD 后，仅需应用许可便可移除已安装评估版中的任何限制。

Aspose.PSD for Java 的评估版本提供完整的产品功能，但有两个限制：

- **每个图像上的水印**：您保存、修改或导出的任何图像都会带有水印，上面写着"Evaluation Only. Created with Aspose.PSD. Copyright 2018-2019 Aspose Pty Ltd." 对于较小的图像，如果水印无法完全显示，将会在图像上画两条对角线。
- **不支持核心绘图功能**：在评估模式下，无法加载或保存图像像素。要绘制图像，请改用高级绘图功能。此限制会影响依赖核心绘图功能的功能。 Aspose.PSD for Java 允许您注册自己的文件格式。但是，此功能依赖于核心绘图功能，因此在评估模式下使用它是毫无意义的，因为您无法更改这些文件的内容。

{{% alert color="primary" %}} 

如果要测试不受评估限制的 Aspose.PSD for Java，请申请一个为期30天的临时许可。请参阅[如何获取临时许可证？](https://purchase.aspose.com/temporary-license) 获取更多信息。

{{% /alert %}} 

## **许可文件信息**
一旦您满意对 Aspose.PSD 的评估，您可以在[Aspose 网站](https://purchase.aspose.com/default.aspx)购买许可证。熟悉提供的不同订阅类型。 如果您有任何疑问，请不要犹豫[联系 Aspose 销售团队](https://company.aspose.com/contact)。

每个 Aspose 许可证都附带一年的软件升级订阅。 首年后，您可以续订订阅以继续获得最新功能和修复程序。技术支持是免费且无限的，可提供给已许可和评估用户，通过我们的[支持论坛](https://forum.aspose.com/)。

许可证是一个包含产品名称、许可开发人员数量、订阅到期日期等详细信息的 XML 文件。 该文件经过数字签名，因此不要修改它：即使无意中添加额外的换行也会使文件无效。

购买 Aspose.PSD 后，您需要在创建、编辑或以其他方式操作图像之前应用许可证。 如果忘记应用许可证，输出的图像将带有评估水印。 您只需要在每个应用程序或进程中设置一次许可证。

## **应用许可证**
您可以从[其下载页面](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/)下载 Aspose.PSD for Java 的评估版本。 评估版本提供与产品许可版本完全相同的功能。 此外，购买许可证并添加几行代码应用许可证后，评估版本会自动转换为许可版本。

一旦您满意对 Aspose.PSD 的评估，您可以在 Aspose 网站上[购买许可证](http://www.aspose.com/Purchase/Components/Default.aspx)。 了解提供的不同订阅类型。 如果您有任何疑问，请不要犹豫联系 Aspose 销售团队。

每个 Aspose 许可证都提供一年的免费升级订阅，以获取此期间推出的任何新版本或修复程序。 技术支持是免费且无限的，向已许可和评估用户提供支持。

{{% alert color="primary" %}} 

如果您想测试不受评估版本限制的 Aspose.PSD，请申请一个为期30天的临时许可。请参阅[如何获得临时许可证？](http://www.aspose.com/corporate/how-to-get-temporary-license.aspx) 获取更多信息。

{{% /alert %}} 

### **设置许可证**
许可证是一个包含产品名称、许可的开发人员数量、订阅到期日期等详细信息的纯文本 XML 文件。 该文件经过数字签名，因此不要修改它；即使意外在文件中添加额外换行也会使其无效。

如果要避免 Aspose.PSD 的评估限制，必须在使用 Aspose.PSD 之前设置许可证。 每个应用程序或进程只需设置一次许可证即可。

许可证可以从以下位置的流或文件加载：

1. 显式路径。
1. 包含 Aspose.PSD.jar 的文件夹。

使用[License](http://www.aspose.com/api/java/psd/com.aspose.psd/classes/License).setLicense 方法为组件添加许可证。设置许可证的最简单方法通常是将许可文件放在与 Aspose.PSD.jar 相同的文件夹中，并仅指定文件名而不包含路径，如以下示例所示：

#### **示例 1**
在此示例中，Aspose.PSD 将尝试在包含应用程序 JAR 文件的文件夹中查找许可文件。

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense("Aspose.PSD.Java.lic");

{{< /highlight >}}

#### **示例 2**
从流初始化许可证。

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense(new java.io.FileInputStream("Aspose.PSD.Java.lic"));

{{< /highlight >}}

### **验证许可证**
可以验证许可证是否已正确设置。`License` 类具有字段 `isLicensed`，如果许可证已设置，则返回true。

**Java**

{{< highlight csharp >}}

 License license = new License();

license.setLicense("Aspose.PSD.Java.lic");

if (License.isLicensed()) {

    System.out.println("许可证已设置！");

}

{{< /highlight >}}

## **在应用程序中应用许可证的位置**
应用许可证的位置取决于您正在开发的应用程序的类型。 遵循以下简单规则：

- 每个应用程序域只需要设置一次许可证。多次调用 `License.setLicense` 不会有害，但会浪费处理器时间。
- 在调用任何 Aspose.PSD 类之前应用许可证。
- **Java 应用程序**： 在启动代码中调用 `License.SetLicense`。
- **类库**： 在使用 Aspose.PSD 的类的静态构造函数中调用 `License.setLicense`。 静态构造函数在创建类的实例之前执行，确保正确设置 Aspose.PSD 许可证。

## **使用多个 Aspose 产品**
如果您的应用程序中使用多个 Aspose 产品，例如 Aspose.PSD 和 Aspose.Cells，以下是一些有用的提示。

- **为每个 Aspose 产品单独应用许可证**。即使您有所有组件的单个许可文件，例如 'Aspose.Total.lic'，您仍然需要为应用程序中的每个 Aspose 产品单独调用 `License.setLicense`。
- **使用完全限定的许可证类名**。每个 Aspose 产品在其命名空间中都有一个 `License` 类。 例如，Aspose.PSD 有 `com.aspose.psd.license.License`，Aspose.Cells 有 `com.aspose.cells.License`。 使用完全限定的类名可以避免在应用于哪个产品的许可证上产生混淆。
