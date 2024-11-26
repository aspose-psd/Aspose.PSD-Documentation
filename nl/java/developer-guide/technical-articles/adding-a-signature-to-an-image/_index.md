---
title: Het toevoegen van een handtekening aan een afbeelding
type: docs
weight: 10
url: /nl/het-toevoegen-van-een-handtekening-aan-een-afbeelding/
---

## **Het toevoegen van een handtekening**

Het toevoegen van een handtekening aan een afbeelding is soms vereist om de afbeeldingen digitaal te ondertekenen om vervalsing te voorkomen. Een andere gedachte zou kunnen zijn om de afbeelding meer te behandelen alsof deze in een galerij wordt getoond. Wat de reden ook is, de Aspose.PSD API's bieden de mogelijkheid om een handtekening aan een afbeelding toe te voegen met het eenvoudigste mechanisme zoals hieronder uitgelegd. Let op, dit voorbeeld maakt gebruik van de Graphics-klasse om een andere afbeelding met handtekening op het oppervlak van de originele afbeelding te tekenen. Om de werking te demonstreren, laden we een PSD-afbeelding van de schijf en tekenen we een andere afbeelding als handtekening op het oppervlak van de originele afbeelding met behulp van de DrawImage-methode van de Graphics-klasse. We slaan de resulterende afbeelding op in PNG-indeling met behulp van de PngOptions-klasse. Hieronder staat een voorbeeldcode die laat zien hoe je een handtekening aan een afbeelding toevoegt. De broncode van het voorbeeld is opgesplitst in delen om het gemakkelijk te volgen. Stap voor stap laat het voorbeeld zien hoe je:

- De primaire en secundaire (handtekening) afbeeldingen laadt.
- Maak en initialiseer een Grafisch object.
- Afbeelding tekenen met behulp van de DrawImage-methode van de Grafisch klasse.
- Resultaat opslaan in PNG-indeling.

### **Voorbeeldprogrammacode**

#### **Afbeeldingen laden**
Maak eerst instanties van de Image-klasse om de voorbeeldafbeeldingen van de schijf te laden.

#### **Een Grafisch object maken en initialiseren**
Nadat de afbeeldingen zijn geladen, maak en initialiser Graphics-class object terwijl je het object van de primaire afbeelding gebruikt.

#### **Secundaire afbeelding op de primaire afbeelding tekenen**
Vervolgens, gebruik de DrawImage-methode van de Graphics-klasse om de secundaire afbeelding op de primaire afbeelding toe te voegen. Er zijn verschillende overbelastingen van de DrawImage-methode die een object van de Image accepteren als eerste parameter, terwijl alle andere parameters overeenkomen met de locatie waar de afbeelding moet worden getekend. Voor de demonstratie gebruikt de volgende code de overloadversie van DrawImage die een object van de Point als tweede parameter accepteert en probeert de handtekening in de rechteronderhoek van de primaire afbeelding te tekenen.

#### **De afbeelding opslaan**
Sla tot slot de afbeelding terug naar de lokale schijf op als een PNG-bestand met behulp van de PngOptions-klasse.

#### **Voorbeeldcode**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-TekenAfbeeldingen-VoegHandtekeningToeAanAfbeelding-VoegHandtekeningToeAanAfbeelding.java" >}}
