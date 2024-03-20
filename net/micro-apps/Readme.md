# Aspose.PSD Micro Apps
Aspose.PSD Micro Applications supply high-level image processing scenarios useful for end-users.

Work over [Aspose.PSD .NET API](https://products.aspose.com/psd/net/).

### System Requirements
- .NET7 on Windows, Linux, MacOs;

- Aspose.PSD Micro application installed.

### Installation

Please issue the command :

```
dotnet tool install --global Aspose.PSD.Micro-Apps
```

If you've already installed the application - update supported via the command :

```
dotnet tool update --global Aspose.PSD.Micro-Apps --version 23.11.2
```

### Commands
- convert
- resize
- crop


### Usage
**Use from command line:**

``` 
Aspose.PSD.Micro-Apps convert --input photo_1.jpg photo_2.jpg photo_3.jpg photo_4.jpg photo_5.jpg photo_6.jpg --output result.zip --format png --license Aspose.Total.Product.Family.lic
```

**Use from code:**

``` csharp
var options = new Aspose.PSD.ConsoleApps.CommandLineOptions.ConversionOptions
{
    InputFiles = new List<string> { "photo_1.jpg", "photo_2.jpg", "photo_3.jpg", "photo_4.jpg", "photo_5.jpg", "photo_6.jpg" },
    OutputPath = "result.zip",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.Total.Product.Family.lic";
}

Aspose.PSD.ConsoleApps.Services.ConversionService.Convert(options.InputFiles, options.OutputPath, options.OutputFormat);
```
