### Usage
**Use from command line:**

``` 
Aspose.PSD.Micro-Apps crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.Total.Product.Family.lic
```

**Use from code:**

``` csharp
var options = new Aspose.PSD.ConsoleApps.CommandLineOptions.CropOptions
{
    InputPath = "photo1.jpg",
    CropType = CropType.Rect,
    Left = 150,
    Top = 100,
    Width = 100,
    Height = 250,
    OutputPath = "cropped_photo.png",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.Total.Product.Family.lic";
}

Aspose.PSD.ConsoleApps.Services.CropService.Crop(options);
```
