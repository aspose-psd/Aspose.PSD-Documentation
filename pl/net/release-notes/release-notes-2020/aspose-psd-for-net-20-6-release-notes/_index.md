---
title: Aspose.PSD dla .NET 20.6 - Notatki dotyczące wydania
type: docs
weight: 70
url: /pl/net/aspose-psd-dla-net-20-6-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 20.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-606 |Obsługa zasobu LnkE|Funkcja|
|PSDNET-386 |Obsługa zasobu britResource (Zasób warstwy regulacji jasności/kontrastu)|Funkcja|
|PSDNET-219|Przeniesienie ustawienia DefaultReplacementFont do klasy ImageOptionsBase|Udoskonalenie|
|PSDNET-596|Grupa warstw z trybem mieszania innych niż PassThrough nie jest renderowana|Błąd|
|PSDNET-610|Wyjątek NullReference podczas próby konwersji określonego pliku Psd na obraz|Błąd|
|PSDNET-636|Zmiana rozmiaru plików PSD działa nieprawidłowo, jeśli jest maska w warstwie regulacji, która ma puste granice|Błąd|
|PSDNET-611|Wyjątek OverflowException podczas próby otwarcia określonego pliku Psd|Błąd|
|PSDNET-565|Obraz Psd w trybie RGB 16 bit/na kanał aktualizuje warstwy tylko w podglądzie|Błąd|
|PSDNET-652|Wyjątek podczas ładowania określonego pliku PSD z łączonym zasobem LnkE i właściwością adobeStockLicenseState|Błąd|
|PSDNET-640|Zmiany w masce warstwy PSD są odrzucane podczas zapisywania|Błąd|
|PSDNET-593|Zapisanie pliku AI w formacie Jpeg2000 nie działa|Błąd|
|PSDNET-638|Nieprawidłowa kolejność warstw po dodaniu grupy warstw do pustej grupy warstw|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.MaskRectangle
- P:Aspose.PSD.ImageOptionsBase.DefaultReplacementFont
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Type
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.OriginalFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.FileType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.FileCreator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.ChildDocId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.AssetModTime
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.AssetLockedState
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.IsLibraryLink
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.OriginalCompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.HasFileOpenDescriptor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Length
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.None
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFD
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFE
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFA
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.#ctor(System.Int32,System.Guid,System.String,System.String,System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.Date
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FileSize
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FullPath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.RelativePath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.ElementRef
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.ElementName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.AdobeStockId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.AdobeStockLicenseState
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.#ctor(System.Int32,System.Guid,System.String,System.String,System.String)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.IsEmpty
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.DataSourceCount
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.StringStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,System.String)
# **Usunięte API:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.DefaultReplacementFont

## **Przykłady użycia:**
**PSDNET-606. Obsługa zasobu LnkE**

{{< highlight java >}}

string message = "PrzykładObsługiZasobuLnkE działa niepoprawnie.";

void AssertIsTrue(bool condition)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

void AssertAreEqual(object actual, object expected)

{

    if (!object.Equals(actual, expected))

    {

        throw new FormatException(message);

    }

}

// Ten przykład demonstruje, jak pobrać i ustawić właściwości zasobu Photoshop Psd LnkE, który zawiera informacje o zewnętrznym połączonym pliku.

void PrzykladObslugiZasobuLnkE(

    string sciezkaPliku,

    int dlugosc,

    int dlugosc2,

    int dlugosc3,

    int dlugosc4,

    string pelnaSciezka,

    string data,

    double czasModyfikacji,

    string childDocId,

    bool zablokowany,

    string unikalneId,

    string nazwa,

    string oryginalnaNazwaPliku,

    string typPliku,

    long rozmiar)

{

    string nazwaPliku = Path.GetFileName(sciezkaPliku);

    string sciezkaWyjsciowa = @"Output\" + nazwaPliku;

    using (PsdImage obraz = (PsdImage)Image.Load(sciezkaPliku))

    {

        LnkeResource zasobLnke = null;

        foreach (var zasob in obraz.GlobalLayerResources)

        {

            zasobLnke = zasob as LnkeResource;

            if (zasobLnke != null)

            {

                AssertAreEqual(zasobLnke.Length, dlugosc);

                AssertAreEqual(zasobLnke.UniqueId, new Guid(unikalneId));

                AssertAreEqual(zasobLnke.FullPath, pelnaSciezka);

                AssertAreEqual(zasobLnke.Date.ToString(CultureInfo.InvariantCulture), data);

                AssertAreEqual(zasobLnke.AssetModTime, czasModyfikacji);

                AssertAreEqual(zasobLnke.AssetLockedState, zablokowany);

                AssertAreEqual(zasobLnke.FileName, nazwa);

                AssertAreEqual(zasobLnke.FileSize, rozmiar);

                AssertAreEqual(zasobLnke.ChildDocId, childDocId);

                AssertAreEqual(zasobLnke.Version, 7);

                AssertAreEqual(zasobLnke.FileType, typPliku);

                AssertAreEqual(zasobLnke.FileCreator, string.Empty);

                AssertAreEqual(zasobLnke.OriginalFileName, oryginalnaNazwaPliku);

                AssertAreEqual(zasobLnke.CompId, -1);

                AssertAreEqual(zasobLnke.OriginalCompId, -1);

                AssertIsTrue(zasobLnke.HasFileOpenDescriptor);

                AssertIsTrue(!zasobLnke.IsEmpty);

                AssertIsTrue(zasobLnke.Type == LinkResourceType.liFE);

                zasobLnke.FullPath =

                    @"file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png";

                AssertAreEqual(zasobLnke.Length, dlugosc2);

                zasobLnke.FileName = "rgb8_2x23.png";

                AssertAreEqual(zasobLnke.Length, dlugosc3);

                zasobLnke.ChildDocId = Guid.NewGuid().ToString();

                AssertAreEqual(zasobLnke.Length, dlugosc4);

                zasobLnke.Date = DateTime.Now;

                zasobLnke.AssetModTime = double.MaxValue;

                zasobLnke.FileSize = long.MaxValue;

                zasobLnke.FileType = "test";

                zasobLnke.FileCreator = "plik";

                zasobLnke.CompId = int.MaxValue;

                break;

            }

        }

        AssertIsTrue(zasobLnke != null);

        obraz.Save(sciezkaWyjsciowa, new PsdOptions(obraz));

    }

    using (PsdImage obraz = (PsdImage)Image.Load(sciezkaWyjsciowa))

    {

        obraz.Save(

            Path.ChangeExtension(sciezkaWyjsciowa, "png"),

            new PngOptions

            {

                ColorType = PngColorType.TruecolorWithAlpha

            });

    }

}

// Ten przykład demonstruje, jak pobrać i ustawić właściwości zasobu Photoshop Psd LnkE zawierającego informacje o zewnętrznie połączonym pliku JPEG.

this.PrzykladObslugiZasobuLnkE(

    @"..\..\..\Issues\IMAGINGNET-2375\photooverlay_5_new.psd",

    0x21c,

    0x26c,

    0x274,

    0x27c,

    @"file:///C:/Users/cvallejo/Desktop/photo.jpg",

    "05/09/2017 22:24:51",

    0,

    "F062B9DB73E8D124167A4186E54664B0",

    false,

    "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

    "photo.jpg",

    "photo.jpg",

    "JPEG",

    0x1520d);

// Ten przykład demonstruje, jak pobrać i ustawić właściwości zasobu Photoshop Psd LnkE zawierającego informacje o zewnętrznie połączonym pliku PNG.

this.PrzykladObslugiZasobuLnkE(

    "rgb8_2x2_linked.psd",

    0x284,

    0x290,

    0x294,

    0x2dc,

    @"file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

    "04/14/2020 14:23:44",

    0,

    "",

    false,

    "5867318f-3174-9f41-abca-22f56a75247e",

    "rgb8_2x2.png",

    "rgb8_2x2.png",

    "png",

    0x53);

// Ten przykład demonstruje, jak pobrać i ustawić właściwości zasobu Photoshop Psd LnkE zawierającego informacje o aktywie z bibliotek CC Libraries.

this.PrzykladObslugiZasobuLnkE(

    "rgb8_2x2_asset_linked.psd",

    0x398,

    0x38c,

    0x388,

    0x3d0,

    @"CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (Funkcja dostępna w Photoshopie CC 2015)",

    "01/01/0001 00:00:00",

    1588890915488.0d,

    "",

    false,

    "ec15f0a8-7f13-a640-b928-7d29c6e9859c",

    "rgb8_2x2_linked",

    "rgb8_2x2.png",

    "png",

    0);

{{< /highlight >}}


**PSDNET-201. Obsługa postępu konwersji dokumentu**

{{< highlight java >}}

string sciezkaPlikuZrodlowego = "Apple.psd";

Stream wyjscieStrumien = new MemoryStream();

ProgressEventHandler lokalnyObslugaZdarzenPostepu = delegate(ProgressEventHandlerInfo informacjePostepu)

{

      string wiadomosc = string.Format(

           "{0} {1}: {2} z {3}",

           informacjePostepu.Description,

           informacjePostepu.EventType,

           informacjePostepu.Value,

           informacjePostepu.MaxValue);

      Console.WriteLine(wiadomosc);

};

Console.WriteLine("---------- Wczytywanie Apple.psd ----------");

var opcjeWczytywania = new PsdLoadOptions() { ProgressEventHandler = lokalnyObslugaZdarzenPostepu };

using (PsdImage obraz = (PsdImage)Image.Load(sciezkaPlikuZrodlowego, opcjeWczytywania))

{

      Console.WriteLine("---------- Zapisywanie Apple.psd w formacie PNG ----------");

      obraz.Save(

           wyjscieStrumien,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = lokalnyObslugaZdarzenPostepu

           });

      Console.WriteLine("---------- Zapisywanie Apple.psd w formacie PSD ----------");

      obraz.Save(

           wyjscieStrumien,

           new PsdOptions()

           {

                 ColorMode = ColorModes.Rgb,

                 ChannelsCount = 4,

                 ProgressEventHandler = lokalnyObslugaZdarzenPostepu

           });

}

{{< /highlight >}}


**PSDNET-386. Obsługa zasobu britResource (Zasób warstwy regulacji jasności/kontrastu)**

{{< highlight java >}}

 /* Ten przykład przedstawia, jak można programistycznie zmienić zasób warstwy jasności/kontrastu obrazu Psd

   Jest to nisko poziomowe API Aspose.PSD. Możesz używać warstwy jasności/kontrastu przez jej API, co będzie o wiele łatwiejsze,

   ale bezpośrednia edycja zasobu Photoshopa daje Ci większą kontrolę nad zawartością pliku PSD.  */

string sciezka = @"BrightnessContrastPS6.psd";

string sciezkaWyjsciowa = @"BrightnessContrastPS6_output.psd";

using (PsdImage obraz = (PsdImage)Image