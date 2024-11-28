---
title: 安装
type: 文档
weight: 40
url: /zh/java/installation/
---

## **从Maven仓库安装Aspose.PSD for Java**
Aspose在[Maven仓库](https://releases.aspose.com/java/repo/com/aspose/)上托管了所有Java API。您可以通过简单的配置在您的Maven项目中直接使用[Aspose.PSD for Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) API。

### **指定Maven仓库配置**
首先，您需要在您的Maven pom.xml中指定Aspose Maven仓库的配置/位置，如下所示：

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}

### **定义Aspose.PSD for Java API依赖**
然后在您的pom.xml中定义Aspose.PSD for Java API的依赖，如下所示：

{{< highlight java >}}

 <dependencies>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-psd</artifactId>
        <version>24.2</version>
        <classifier>jdk16</classifier>
    </dependency>
</dependencies>

{{< /highlight >}}

完成以上步骤后，Aspose.PSD for Java依赖将最终在您的Maven项目中定义。

## **支持的平台**
Aspose.PSD for Java支持最受欢迎的开发和部署平台。

|**功能**|**描述**|
| :- | :- |
|桌面应用程序|Aspose.PSD for Java可用于在MS Windows中开发桌面应用程序。|
|企业Web应用程序|Aspose.PSD for Java完全支持Web应用程序。|
|Linux/Unix|Aspose.PSD for Java是一个跨平台的API，可以在Linux和Unix环境中工作。|

## **支持的Java版本**
- JDK 1.6或更高版本
