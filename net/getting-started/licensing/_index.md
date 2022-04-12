---
title: Licensing
type: docs
weight: 70
url: /net/licensing/
description: Evaluate PSD Photoshop C# Library from NuGet and apply the license using file or stream to remove any restrictions from the installed evaluation.
---

## **Evaluation Version Limitations**
You can download an evaluation version of Aspose.PSD for .NET from the [NuGet](https://www.nuget.org/packages/Aspose.psd/). The evaluation version provides the same features as the fully licensed version of the component with a couple of restrictions. When you buy Aspose.PSD, simply applying the license removes any restrictions from the installed evaluation. The evaluation version of Aspose.PSD for .NET provides full product functionality, with only two limitations:

- **A watermark on each image**: Any image you save, modify or export has a watermark reading "Evaluation Only. Created with Aspose.PSD. Copyright 2010-2018 Aspose Pty Ltd.". Small images, where the full watermark won't fit, has two diagonal lines across the image instead.
- **No support for core drawing functionality**: In evaluation mode, image pixels cannot be loaded or saved to the image. To draw images, use the advanced drawing functionality instead. This limitation affects functionality that depends on the core drawing functionality. Aspose.PSD for .NET allows you to register your own file format. However, this feature depends on the core drawing functionality so it makes no sense to use it in evaluation mode because you can't change the content of those files.

If you want to test Aspose.PSD for .NET without the evaluation limitations, request a 30-day temporary license. Please refer to [How to get a Temporary License?](https://purchase.aspose.com/temporary-license) for more information.
## **About the License File**
Once you are happy with your evaluation of Aspose.PSD, you can purchase a license on [Aspose website](https://purchase.aspose.com/default.aspx). Make yourself familiar with the different subscription types offered. If you have any questions, do not hesitate to contact [Aspose's sales team](https://company.aspose.com/contact). Every Aspose license comes with a one-year subscription for software upgrades. After the first year, renew your subscriptions to continue getting the latest features and fixes. Technical support is free and unlimited and is provided to both licensed and evaluation users through our [Support Forums](https://forum.aspose.com/). The license is an XML file that contains details such as the product name, number of licensed developers, subscription expiry date and so on. The file is digitally signed, so do not modify it: even inadvertently adding an extra line break invalidates the file. After buying Aspose.PSD, you need to apply the license before you create, edit or otherwise manipulate images. If you forget to apply the license, any output images will have an evaluation watermark. You only need to set the license once per application or process that you develop.
## **Where to Apply a License in your Application**
Where you apply a license depends on the type of application you are developing. Follow these simple rules:

- Only apply the license once per application domain. Calling License.SetLicense multiple times is not harmful but wastes processor time.
- Apply the license before calling any Aspose.PSD for .NET classes.
- **Windows Forms or Console applications**: call License.SetLicense in the startup code, before using any Aspose.PSD for .NET classes.
- **ASP.NET applications**: call License.SetLicense from the Global.asax.cs (Global.asax.vb) file, in the Application_Start protected method. This way, it is called once when the application starts. Do not call License.SetLicense from within the Page_Load methods or the license will be loaded every time a web page is loaded.
- **Silverlight applications**: call License.SetLicense from the Application_Startup event in the App.xaml.cs (App.xaml.vb) file.
- **Class library**: call License.SetLicense from a static constructor of the class that uses Aspose.PSD. The static constructor executes before an instance of your class is created, making sure that the Aspose.PSD license is properly set.
## **Applying a License**
You can easily download an evaluation version of Aspose.PSD from NuGet [download page](https://www.nuget.org/packages/Aspose.psd/). The evaluation version provides absolutely the same capabilities as the licensed version of Aspose.PSD. Furthermore, evaluation version simply becomes licensed when you purchase a license and add a couple of lines of code to apply the license.
### **Using a File or a Stream**
If you want to avoid working with evaluation limitations, you need to set a license before using Aspose.PSD. You only need to set a license once per application (or process).
### **Applying a license from a file**
The easiest way to apply a license is to put the license file in the same folder as the Aspose.PSD.dll. Then you can specify the file name in the code instead of a full path.



{{< highlight java >}}

 // Instantiate an instance of license and apply the license using a full path

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense("Aspose.PSD.lic");



{{< /highlight >}}



When you call the SetLicense method, the license name should be same as that of your license file name. For example, if you change the license file name to "Aspose.PSD.lic.xml" you should use this license name for the SetLicense method.
### **Applying a license using a stream**
It is also possible to load a license from a stream as demonstrated below.



{{< highlight java >}}



// Instantiate an instance of license and apply the license using a stream

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense(myStream);



{{< /highlight >}}
### **Checking the license status**
The Aspose.PSD.License class has the IsLicensed property that will return true if license has been properly set.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("License is Set!");

}

{{< /highlight >}}
### **Using an Embedded Resource**
A practical way of packaging the license with your application and making sure it is not lost, is to include it as an embedded resource into one of the assemblies that calls Aspose.PSD. To include the license file as an embedded resource:

1. In Visual Studio .NET, click the **File** menu and select **Add Existing Item**.
1. Include the license file (extension .lic) in the project.
1. Select the file in the Solution Explorer.
1. In the Properties window, set **Build Action** to **Embedded Resource**.

It's not necessary to call the System.Reflection.Assembly's GetExecutingAssembly or GetManifestResourceStream methods in the Microsoft .NET Framework to access an embedded license. Instead, embed the file as a resource in the project and then pass the license file name to the SetLicense method. The License class automatically finds the license file in the embedded resources. The example below shows how to include the license as an embedded resource and apply it to your application.



{{< highlight java >}}

 // Instantiate the License class

Aspose.PSD.License license = new Aspose.PSD.License();



// Pass the name of the embedded license file

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}


### **Checking the license status**
The Aspose.PSD.License class has the IsLicensed property that will return true if license has been properly set.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("License is Set!");

}

{{< /highlight >}}
