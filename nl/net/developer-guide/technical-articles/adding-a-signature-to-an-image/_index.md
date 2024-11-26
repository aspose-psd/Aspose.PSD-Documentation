---
title: Het toevoegen van een handtekening aan een afbeelding
type: docs
weight: 70
url: /nl/het-toevoegen-van-een-handtekening-aan-een-afbeelding/
---

## **Het toevoegen van een handtekening**

Het toevoegen van een handtekening aan een afbeelding is soms nodig om de afbeeldingen digitaal te ondertekenen en vervalsing te voorkomen. Een andere gedachte kan zijn om de afbeelding meer te behandelen alsof deze in een galerij wordt getoond. Wat de reden ook is, de Aspose.PSD API's bieden de mogelijkheid om een handtekening toe te voegen aan een afbeelding met behulp van het eenvoudigste mechanisme zoals hieronder uitgelegd. Let op, dit voorbeeld maakt gebruik van de [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) klasse om een andere afbeelding met handtekening op het oppervlak van de oorspronkelijke afbeelding te tekenen. Om de handeling te demonstreren, zullen we een PSD-afbeelding vanaf schijf laden en een andere afbeelding als handtekening op het oppervlak van de oorspronkelijke afbeelding tekenen met behulp van de DrawImage methode van de Graphics klasse. We zullen de resulterende afbeelding opslaan in PNG-formaat met behulp van de [PngOptions](https://reference.aspose.com/psd/net/aspose.psd/imageoptions/pngoptions) klasse. Hieronder staat een voorbeeldcode die demonstreert hoe u een handtekening aan een afbeelding toevoegt. De voorbeeldbroncode is opgesplitst in delen om het gemakkelijk te volgen. Stap voor stap laat het voorbeeld zien hoe u:

- De primaire en secundaire (handtekening) afbeeldingen laadt.
- Een Graphics object aanmaakt en initialiseert.
- Een afbeelding tekent met behulp van de DrawImage methode van de Graphics klasse.
- Het resultaat opslaat in PNG-formaat.

### **Programmavoorbeelden**

#### **Afbeeldingen laden**

Maak eerst instanties van de Image klasse om de voorbeeldafbeeldingen vanaf schijf te laden.

#### **Een Graphics object aanmaken en initialiseren**

Na het laden van de afbeeldingen, maakt u een Graphics klasse object aan en initialiseert u deze terwijl u het object van de primaire afbeelding gebruikt.

#### **Een secundaire afbeelding toevoegen aan de primaire afbeelding**

Vervolgens kunt u met behulp van de DrawImage methode van de Graphics klasse de secundaire afbeelding toevoegen aan de primaire afbeelding. Er zijn verschillende overbelastingen van de DrawImage methode die een object van de Image als eerste parameter accepteren, terwijl alle andere parameters overeenkomen met de locatie waar de afbeelding moet worden getekend. Voor de demonstratie maakt de volgende code gebruik van de overbelastingversie van DrawImage die een object van het type Point als tweede parameter accepteert en probeert de handtekening in de rechteronderhoek van de primaire afbeelding te tekenen.

#### **Het opslaan van de afbeelding**

Sla ten slotte de afbeelding terug naar de lokale schijf op als een PNG-bestand met behulp van de PngOptions klasse.

#### **Vollledige broncode**

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddSignatureToImage-AddSignatureToImage.cs" >}}
