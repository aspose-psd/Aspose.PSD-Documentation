---
title: Installatie
type: docs
weight: 50
url: /nl/installatie/
description: Installeer de PSD-bestandsindelingbibliotheek met behulp van NuGet of de Package Manager-console.
---

## **Aspose.PSD voor .NET installeren via NuGet**
NuGet is de eenvoudigste manier om Aspose API's voor .NET te downloaden en te installeren. Open Microsoft Visual Studio en de NuGet-pakketbeheerder. Zoek naar "aspose" om de gewenste Aspose API te vinden. Klik op "Installeren", de geselecteerde API wordt gedownload en in uw project geïmporteerd.

![todo:image_alt_text](installation_1.png)
## **Aspose.PSD installeren of bijwerken met behulp van de Package Manager-console**
U kunt de onderstaande stappen volgen om de [Aspose.PSD API](https://www.nuget.org/packages/Aspose.psd/) te refereren via de package manager-console:

1. Open uw oplossing/project in Visual Studio.
1. Selecteer Tools -> Library Package Manager -> Package Manager Console in het menu om de pakketbeheerconsole te openen.

![todo:image_alt_text](installation_2.png)

Typ de opdracht "**Install-Package Aspose.Psd**" en druk op enter om de nieuwste volledige versie in uw applicatie te installeren. U kunt ook de suffix "**-prerelease**" toevoegen aan de opdracht om aan te geven dat de nieuwste release inclusief hotfixes ook moet worden geïnstalleerd.

![todo:image_alt_text](installation_3.png)

U zult zien dat de tip **"Aspose.PSD installeren"** onderaan het venster verschijnt, wat aangeeft dat de download bezig is.

![todo:image_alt_text](installation_4.png)

Nadat deze is gedownload, ziet u de volgende bevestigingsberichten. Als u niet bekend bent met de [Aspose EULA](https://company.aspose.com/legal/eula) is het een goed idee om de licentie te lezen die wordt verwezen in de URL.

![todo:image_alt_text](installation_5.png)

U zou nu moeten zien dat Aspose.PSD met succes aan uw applicatie is toegevoegd en gerefereerd.

![todo:image_alt_text](installation_6.png)

In de pakketbeheerconsole kunt u ook de opdracht “**Update-Package Aspose.Psd**” gebruiken en op enter drukken om te controleren op updates voor het Aspose.Psd-pakket en deze te installeren indien aanwezig. U kunt ook de suffix "-prerelease" toevoegen om de nieuwste release bij te werken.
## **Overwegingen bij het uitvoeren in een gedeelde serveromgeving**
Het wordt aanbevolen dat alle Aspose .NET-componenten worden uitgevoerd met een Full Trust permissieset. Dit komt doordat Aspose .NET-componenten soms toegang nodig hebben tot registerinstellingen en bestanden die zich bevinden op andere locaties dan de virtuele directory, bijvoorbeeld voor het lezen van lettertypen enzovoort. Bovendien zijn Aspose.NET-componenten gebaseerd op kern .NET systeemklassen, waarvoor ook Full Trust permissie nodig kan zijn om te kunnen werken in bepaalde gevallen.

Internet Service Providers die meerdere applicaties hosten van verschillende bedrijven handhaven meestal het beveiligingsniveau Medium Trust. In het geval van .NET 2.0, kan zo'n beveiligingsniveau bepaalde beperkingen instellen die de mogelijkheid van Aspose Words om correct te functioneren kunnen beïnvloeden.

- **RegistryPermission** is niet beschikbaar. Dit betekent dat u geen toegang heeft tot het register, wat nodig is om geïnstalleerde lettertypen op te sommen bij het renderen van documenten.
- **FileIOPermission** is beperkt. Dit betekent dat u alleen toegang heeft tot bestanden in de hiërarchie van de virtuele directory van uw applicatie. Dit betekent potentieel dat lettertypen niet kunnen worden gelezen tijdens de export.

Om deze redenen wordt aangeraden dat Aspose.PSD wordt uitgevoerd met Full Trust permissies. U kunt merken dat sommige functies van de bibliotheek zullen werken bij het uitvoeren van verschillende taken in Medium Trust, terwijl andere (zoals het renderen) niet werken, mogelijk door oproepen naar GDI+ beeldverwerking.

## **Werken met .NET Core DLL's geïnstalleerd via MSI-pakket**


**Let op:** als u een .Net Standard dll gebruikt die is geïnstalleerd via een MSI-pakket, dient u de benodigde afhankelijkheden toe te voegen om te werken met de .Net Standard-versie.

|**Screenshot van Visual Studio-afhankelijkheden**|**CsProj-bestandsfragment:**|
| :- | :- |
|![todo:image_alt_text](installation_7.png)|<ItemGroup><p></p><p>`    `<PackageReference Include="System.Drawing.Common" Version="4.5.1" /></p><p>`    `<PackageReference Include="System.Text.Encoding.CodePages" Version="4.5.0" /></p><p></p></ItemGroup>|

## **Systeemvereisten**
### **Ondersteunde besturingssystemen:**
- Microsoft Windows 2000 Professional en Server (SP2 aanbevolen)
- Microsoft Windows XP Professional en Home Edition
- Microsoft Windows 2003 Server
- Microsoft Windows Vista
- Microsoft Windows 2008 Server
- Microsoft Windows 2008 Server R2
- Microsoft Windows 7
- Microsoft Windows 8
- Microsoft Windows 10
- Microsoft Windows 11
### **Ondersteunde platforms:**
- Windows-formulieren
- Web-formulieren
- Visual Studio 2005
- Visual Studio 2008
- Visual Studio 2010
- Visual Studio 2012
- Visual Studio 2013
- Visual Studio 2015
- Visual Studio 2017
- Visual Studio 2019
- Visual Studio 2022

Aspose.PSD werkt voor zowel de x86- als x64-versies van de hierboven genoemde besturingssystemen.
### **Ondersteunde frameworks:**
Aspose.PSD voor .NET ondersteunt .NET-framework als volgt:

- .NET Framework-versie 2.0 of hoger
- .NET Standard 2.0
