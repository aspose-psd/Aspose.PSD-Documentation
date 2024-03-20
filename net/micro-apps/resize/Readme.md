### Usage
**Use from command line:**

``` 
Aspose.PSD.Micro-Apps resize --input photo1.jpg --output resized.png --resizeFactor 200 --format png --license Aspose.Total.Product.Family.lic
```

**Use from code:**

``` csharp
var options = new Aspose.PSD.ConsoleApps.CommandLineOptions.ResizeOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "resized.png",
    ResizeFactor = 200,
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.Total.Product.Family.lic";
}

Aspose.PSD.ConsoleApps.Services.ResizeService.Resize(options);
```
