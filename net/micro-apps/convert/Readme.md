### Convert
This command converts image(s) to provided output format. Output is always compressed to .zip file, so you need to specify output folder or path to .zip file.

Supported formats:
- psd
- pdf
- jpg
- jpeg
- jp2
- j2k
- gif
- png
- bmp
- tiff


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

Aspose.PSD.ConsoleApps.Services.ConversionService.Convert(options);
```
