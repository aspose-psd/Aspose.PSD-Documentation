---
title: Licensing
type: docs
weight: 60
url: /java/licensing/
---

## **Evaluation Version Limitations**
You can download an evaluation version of Aspose.PSD for Java from the [download page](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). The evaluation version provides the same features as the fully licensed version of the component with a couple of restrictions. When you buy Aspose.PSD, simply applying the license removes any restrictions from the installed evaluation.

The evaluation version of Aspose.PSD for Java provides full product functionality, with only two limitations:

- **A watermark on each image**: Any image you save, modify or export has a watermark reading "Evaluation Only. Created with Aspose.PSD. Copyright 2018-2019 Aspose Pty Ltd.". Small images, where the full watermark won't fit, has two diagonal lines across the image instead.
- **No support for core drawing functionality**: In evaluation mode, image pixels cannot be loaded or saved to the image. To draw images, use the advanced drawing functionality instead. This limitation affects functionality that depends on the core drawing functionality. Aspose.PSD for Java allows you to register your own file format. However, this feature depends on the core drawing functionality so it makes no sense to use it in evaluation mode because you can not change the content of those files.

{{% alert color="primary" %}} 

If you want to test Aspose.PSD for Java without the evaluation limitations, request a 30-day temporary license. Please refer to [How to get a Temporary License?](https://purchase.aspose.com/temporary-license) for more information.

{{% /alert %}} 
## **About the License File**
Once you are happy with your evaluation of Aspose.PSD, you can purchase a license on [Aspose website](https://purchase.aspose.com/default.aspx). Make yourself familiar with the different subscription types offered. If you have any questions, do not hesitate to contact [Aspose's sales team](https://company.aspose.com/contact).

Every Aspose license comes with a one-year subscription for software upgrades. After the first year, renew your subscriptions to continue getting the latest features and fixes. Technical support is free and unlimited and is provided to both licensed and evaluation users through our [Support Forums](https://forum.aspose.com/).

The license is an XML file that contains details such as the product name, number of licensed developers, subscription expiry date and so on. The file is digitally signed, so do not modify it: even inadvertently adding an extra line break invalidates the file.

After buying Aspose.PSD, you need to apply the license before you create, edit or otherwise manipulate images. If you forget to apply the license, any output images will have an evaluation watermark. 
You only need to set the license once per application or process that you develop.
## **Applying the License**
You can download an evaluation version of **Aspose.PSD** for Java from [its download page](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). The evaluation version provides absolutely the same capabilities as the licensed version of the product. Furthermore, evaluation version simply becomes licensed when you purchase a license and add a couple of lines of code to apply the license.

Once you are happy with your evaluation of **Aspose.PSD**, you can [purchase a license](http://www.aspose.com/Purchase/Components/Default.aspx) at the Aspose website. Make yourself familiar with the different subscription types offered. If you have any questions, do not hesitate to contact the Aspose sales team.

Every Aspose license carries a one-year subscription for free upgrades to any new versions or fixes that come out during this time. Technical support is free and unlimited and provided both to licensed and evaluation users.

{{% alert color="primary" %}} 

If you want to test **Aspose.PSD** without evaluation version limitations, request a 30-day temporary license. Please refer to [How to get a Temporary License?](http://www.aspose.com/corporate/how-to-get-temporary-license.aspx) for more information.

{{% /alert %}} 
### **Setting a License**
The license is a plain text XML file that contains details such as the product name, number of developers it is licensed to, subscription expiry date and so on. The file is digitally signed, so do not modify the file; even the inadvertent addition of an extra line break into the file will invalidate it.

You need to set a license before utilizing **Aspose.PSD** if you want to avoid its evaluation limitations. You are only required to set a license once per application or process.

The license can be loaded from a stream or file in the following locations:

1. Explicit path.
1. The folder that contains the Aspose.PSD.jar.

Use the [License](http://www.aspose.com/api/java/psd/com.aspose.psd/classes/License).setLicense method to license the component. Often the easiest way to set a license is to put the license file in the same folder as Aspose.PSD.jar and specify just the file name without path as shown in the following example:
#### **Example 1**
In this example **Aspose.PSD** will attempt to find the license file in the folder that contain the JARs of your application.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense("Aspose.PSD.Java.lic");

{{< /highlight >}}
#### **Example 2**
Initializes a license from a stream.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense(new java.io.FileInputStream("Aspose.PSD.Java.lic"));

{{< /highlight >}}
### **Validate the License**
It is possible to validate if the license has been set properly or not. The License class has the isLicensed field that will return true if license has been properly set.

**Java**

{{< highlight csharp >}}

 License license = new License();

license.setLicense("Aspose.PSD.Java.lic");

if (License.isLicensed()) {

    System.out.println("License is Set!");

}

{{< /highlight >}}
## **Where to Apply a License in your Application**
Where you apply a license depends on the type of application you are developing. Follow these simple rules:

- The license only needs to be set once per application domain. Calling License.setLicense multiple times is not harmful but wastes processor time.
- Apply the license before calling any Aspose.PSD classes.
- **Java applications**: call License.SetLicense in the startup code.
- **Class library**: call License.setLicense from a static constructor of the class that uses Aspose.PSD. The static constructor executes before an instance of your class is created, making sure that the Aspose.PSD license is properly set.
## **Using Multiple Aspose Products**
If you use more than one Aspose product in your application, for example Aspose.PSD and Aspose.Cells, here are a few useful tips.

- **Apply the license for each Aspose product separately**. Even if you have a single license file for all components, for example 'Aspose.Total.lic', you still need to call License.setLicense separately for each Aspose product in your application.
- **Use a fully qualified license class name**. Each Aspose product has a License class in its namespace. For example, Aspose.PSD has com.aspose.psd.license.License and Aspose.Cells has com.aspose.cells.License. Using a fully qualified class name avoids any confusion about which license is applied to which product.
