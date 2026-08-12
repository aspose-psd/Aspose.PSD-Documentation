### Crop
This command crops image with provided options and converts to output format. Result is saved to output file or folder (if output path is folder, the result file name will be "result.*output_format*"). You can specify crop type (*--cropType*) with values such as: rectangular (*rect*) or circular (*circle*) (default is *rect*). Also, you have ability to leave output format option unset, it will use extension of the output file, if output path is folder, it will use extension of the input file.

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
**Use from command line (with all options):**

``` 
Aspose.PSD.Micro-Apps crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.Total.Product.Family.lic
```

**Use from code:**

``` csharp
var options = new Aspose.PSD.ConsoleApps.CommandLineOptions.CropOptions
{
    InputPath = "photo1.jpg",
    CropType = CropType.Rect,
    Left = 10,
    Top = 35,
    Width = 250,
    Height = 300,
    OutputPath = "cropped_photo.png",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.Total.Product.Family.lic";
}

Aspose.PSD.ConsoleApps.Services.CropService.Crop(options);
```




**Use from command line (with only nessesary options):**

``` 
Aspose.PSD.Micro-Apps crop --input photo1.jpg --output resut_folder --left 10 --top 35 --width 250 --height 300
```

**Use from code:**

``` csharp
var options = new Aspose.PSD.ConsoleApps.CommandLineOptions.CropOptions
{
    InputPath = "photo1.jpg",
    Left = 10,
    Top = 35,
    Width = 250,
    Height = 300,
    OutputPath = "result_folder"
};

Aspose.PSD.ConsoleApps.Services.CropService.Crop(options);
```
