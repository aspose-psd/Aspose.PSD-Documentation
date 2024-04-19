### Resize
This command resizes image with scale (in %) or new width and height and converts to output format. Result is saved to output file or folder (if output path is folder, the result file name will be "result.*output_format*"). You have ability to leave output format option unset, it will use extension of the output file, if output path is folder, it will use extension of the input file.

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
**Use from command line (with scale):**

``` 
Aspose.PSD.Micro-Apps resize --input photo1.jpg --output resized.png --scale 200 --format png --license Aspose.Total.Product.Family.lic
```

**Use from code (with scale):**

``` csharp
var options = new Aspose.PSD.ConsoleApps.CommandLineOptions.ResizeOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "resized.png",
    Scale = 200,
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.Total.Product.Family.lic";
}

Aspose.PSD.ConsoleApps.Services.ResizeService.Resize(options);
```

**Use from command line (with new width and height):**

``` 
Aspose.PSD.Micro-Apps resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.Total.Product.Family.lic
```

**Use from code (with new width and height):**

``` csharp
var options = new Aspose.PSD.ConsoleApps.CommandLineOptions.ResizeOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "resized.png",
    Width = 200,
    Height = 340,
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.Total.Product.Family.lic";
}

Aspose.PSD.ConsoleApps.Services.ResizeService.Resize(options);
```
