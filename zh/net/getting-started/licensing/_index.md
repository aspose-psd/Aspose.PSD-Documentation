---
title: 许可
type: 文档
weight: 70
url: /zh/net/licensing/
description: 评估PSD Photoshop C#库从NuGet，并应用许可证使用文件或流以删除已安装评估的任何限制。
---

## **评估版本限制**
您可以从[NuGet](https://www.nuget.org/packages/Aspose.psd/)下载Aspose.PSD for .NET的评估版本。评估版本提供与组件完全许可版本相同的功能，但有一些限制。当您购买Aspose.PSD时，简单应用许可证即可去除已安装评估的任何限制。Aspose.PSD for .NET的评估版本提供完整的产品功能，只有两个限制：

- **每个图像上的水印**：您保存、修改或导出的任何图像都带有水印："仅供评估。使用Aspose.PSD创建。版权所有2010-2018 Aspose Pty Ltd." 在小图像上，完整水印无法适应，代之以两条对角线穿过图像。
- **不支持核心绘图功能**：在评估模式下，图像像素无法加载或保存到图像。要绘制图像，请改用高级绘图功能。该限制会影响依赖核心绘图功能的功能。Aspose.PSD for .NET允许您注册自己的文件格式。但是，此功能依赖于核心绘图功能，因此在评估模式下使用它是没有意义的，因为您无法更改这些文件的内容。

如果您想要测试Aspose.PSD for .NET而不受评估限制，请申请一个30天的临时许可证。有关更多信息，请参阅[如何获取临时许可证？](https://purchase.aspose.com/temporary-license)。
## **关于许可文件**
一旦您对Aspose.PSD的评估满意，您可以在[Aspose网站](https://purchase.aspose.com/default.aspx)购买许可证。熟悉提供的不同订阅类型。如果您有任何问题，请随时联系[Aspose的销售团队](https://company.aspose.com/contact)。每个Aspose许可证都附带一年的软件升级订阅。第一年后，请续订您的订阅以继续获得最新功能和修复程序。技术支持是免费且无限的，并且为已许可和评估用户提供了支持论坛上[的支持论坛](https://forum.aspose.com/)。许可证是一个包含产品名称、许可开发人数、订阅到期日期等详细信息的XML文件。该文件经过数字签名，因此不要修改它：即使意外添加额外的换行符也会使文件失效。购买Aspose.PSD后，您需要在创建、编辑或以其他方式操纵图像之前应用许可证。如果您忘记应用许可证，任何输出图像都将带有评估水印。您只需在每个应用程序或过程中设置一次许可证。
## **在应用程序中的何处应用许可证**
应用许可证的位置取决于您正在开发的应用程序类型。遵循以下简单规则：

- 每个应用程序域仅应用一次许可证。调用License.SetLicense多次不会造成伤害，但会浪费处理器时间。
- 在调用任何Aspose.PSD for .NET类之前应用许可证。
- **Windows窗体或控制台应用程序**：在使用任何Aspose.PSD for .NET类之前，在启动代码中调用License.SetLicense。
- **ASP.NET应用程序**：从Global.asax.cs（Global.asax.vb）文件的Application_Start受保护方法中调用License.SetLicense。这样，在应用程序启动时调用一次。不要从Page_Load方法内部调用License.SetLicense，否则每次加载网页时都会加载许可证。
- **Silverlight应用程序**：从App.xaml.cs（App.xaml.vb）文件中的Application_Startup事件中调用License.SetLicense。
- **类库**：从使用Aspose.PSD的类的静态构造函数中调用License.SetLicense。静态构造函数在创建类实例之前执行，确保正确设置了Aspose.PSD许可证。
## **应用许可证**
您可以从NuGet的[下载页面](https://www.nuget.org/packages/Aspose.psd/)轻松获取Aspose.PSD的评估版本。评估版本提供的功能与已许可版本的Aspose.PSD完全相同。此外，只需购买许可证并添加几行代码来应用许可证，即可让评估版本转为已许可。
### **使用文件或流应用许可证**
如果要避免处理评估限制，您需要在使用Aspose.PSD之前设置许可证。每个应用程序（或进程）只需设置一次许可证。 
### **使用文件应用许可证**
将许可证文件放在与Aspose.PSD.dll相同的文件夹中是应用许可证的最简单方法。然后，您可以在代码中指定文件名，而不是完整路径。

{{< highlight java >}}

// 实例化一个许可证实例并使用完整路径应用许可证

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}

调用SetLicense方法时，许可证名称应与许可证文件名相同。例如，如果您将许可证文件名更改为"Aspose.PSD.lic.xml"，则应该在SetLicense方法中使用此许可证名称。
### **使用流应用许可证**
也可以从流中加载许可证，示例如下。

{{< highlight java >}}

// 实例化一个许可证实例并使用流应用许可证

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense(myStream);

{{< /highlight >}}

### **检查许可证状态**
Aspose.PSD.License类具有IsLicensed属性，如果许可证已正确设置，则将返回true。

{{< highlight java >}}

License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("许可证已设置！");

}

{{< /highlight >}}

### **使用嵌入式资源**
将许可证与应用程序一起打包，并确保不会丢失的一种有效方式是将其作为嵌入式资源包含在调用Aspose.PSD的程序集中。要将许可证文件包含为嵌入式资源：

1. 在Visual Studio .NET中，单击**文件**菜单，然后选择**添加现有项**。
1. 在项目中包括许可证文件（扩展名为.lic）。
1. 在解决方案资源管理器中选择文件。
1. 在属性窗口中，将**生成操作**设置为**嵌入式资源**。

在Microsoft .NET Framework中，无需调用System.Reflection.Assembly的GetExecutingAssembly或GetManifestResourceStream方法来访问嵌入式许可证，而是将文件作为项目中的资源嵌入，然后将许可证文件名传递给SetLicense方法。License类会自动在嵌入资源中找到许可证文件。下面的示例显示了如何将许可证作为嵌入式资源并将其应用到应用程序中。

{{< highlight java >}}

// 实例化License类

Aspose.PSD.License license = new Aspose.PSD.License();

// 传递嵌入许可证文件的名称

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}

### **检查许可证状态**
Aspose.PSD.License类具有IsLicensed属性，如果许可证已正确设置，则将返回true。

{{< highlight java >}}

License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("许可证已设置！");

}

{{< /highlight >}}
