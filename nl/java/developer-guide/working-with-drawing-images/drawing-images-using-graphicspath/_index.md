---
title: Het tekenen van afbeeldingen met behulp van GraphicsPath
type: docs
weight: 30
url: /nl/java/het-tekenen-van-afbeeldingen-met-behulp-van-graphicspath/
---

## **Het tekenen van afbeeldingen met behulp van GraphicsPath**
De GraphicsPath-klasse is verantwoordelijk voor het maken en onderhouden van een grafisch pad. De GraphicsPath heeft geen verwijzing naar een afbeelding en verandert de afbeelding zelf niet, in plaats daarvan kan het worden beschouwd als een object dat metagegevens bevat die de paden beschrijven die de Graphics-klasse kan tekenen. De GraphicsPath-klasse maakt gebruik van figuren; elke figuur is samengesteld uit een reeks verbonden lijnen en curven of een geometrische vormprimitief. Elke vorm kan worden opgesplitst in vormsegmenten. U kunt verschillende figuren of vormen toevoegen, verwijderen en wijzigen in een GraphicsPath-object. Wanneer het GraphicsPath volledig is beschreven, gebruikt u de bijbehorende methoden van de Graphics-klasse (DrawPath en Fill Paths) om over de paden te tekenen of ze in te vullen. De Graphics-klasse neemt elk vormsegment en tekent het om het uiteindelijke beeld te produceren.
### **Tekenafbeeldingen met behulp van de GraphicsPath-klasse**
Hieronder volgt een voorbeeld dat het gebruik van de GraphicsPath-klasse demonstreert. De broncode van het voorbeeld is opgesplitst in verschillende delen om het eenvoudig en gemakkelijk te volgen te houden. Stap voor stap tonen de voorbeelden u hoe u:

- Een afbeelding maakt.
- Een Graphics-object initialiseert.
- Het oppervlak schoonmaakt.
- Een instantie van GraphicsPath maakt.
- Een figuur maakt.
- Vormen toevoegt aan de figuur.
- Een array van figuren maakt.
- Padtekst tekent.
- Pad opvult.

### **Het tekenen van afbeeldingen met GraphicsPath: Programmeervoorbeelden**
#### **GraphicsPath: Maak een afbeelding**
Begin met het maken van een afbeelding met behulp van een van de methoden die worden beschreven in het maken van bestanden.
#### **GraphicsPath: Initialiseer een Graphics-object**
Maak en initialiseer een Graphics-object door het Image-object door te geven aan de constructor.
#### **GraphicsPath: Maak het oppervlak leeg**
Maak het grafische oppervlak leeg door de Clear-methode van de Graphics-klasse aan te roepen en geef een Kleur door als parameter. Deze methode vult het grafische oppervlak met de opgegeven kleur.
#### **GraphicsPath: Maak een instantie van de GraphicsPath**
Maak een instantie van GraphicsPath met GraphicsPath ingesteld op Standaard door standaard. Deze modus bepaalt hoe het interieur van een gesloten figuur moet worden gevuld. De andere mogelijke GraphicsPath-waarde is Winding.
#### **GraphicsPath: Maak een figuur**
Maak een instantie van de Figure-klasse. Zoals eerder besproken kan een figuur vormen bevatten en vormen bevinden zich in de Aspose.PSD.Shapes-namespace.
#### **GraphicsPath: Voeg vormen toe aan de figuur**
De Add Shapes-methode die wordt blootgesteld door de Figure-klasse, stelt u in staat om vormen toe te voegen aan de figuur. In de onderstaande codevoorbeelden worden verschillende vormen toegevoegd aan een Figure-object.
#### **GraphicsPath: Voeg figuren toe aan een array**
Meerdere figuren kunnen aan een GraphicsPath-object worden toegevoegd met behulp van de AddFigures-methode die wordt blootgesteld door de GraphicsPath-klasse. Deze methode accepteert een array van figuren als parameter.
#### **GraphicsPath: Teken de paden**
Teken de GraphicsPath met behulp van de DrawPath-methode die wordt blootgesteld door de Graphics-klasse. De methode accepteert twee parameters. Het eerste parameter is een object van de Pen-klasse, die de kleur, breedte en stijl van het pad bepaalt. Het tweede parameter is het object van de GraphicsPath-klasse dat het pad zelf vertegenwoordigt.
#### **GraphicsPath: Vul paden in**
U kunt een pad vullen door een GraphicsPath-object door te geven aan de Fill Paths-methode die wordt blootgesteld door de Graphics-klasse. De Fill Paths-methode vult het pad in volgens de vulmodus (standaard of winding) die momenteel is ingesteld voor het pad. Als het pad open figuren heeft, wordt het pad ingevuld alsof die figuren gesloten waren.

De Fill Paths-methode accepteert twee parameters. Het eerste parameter is een object van een brush-klasse uit de Aspose.PSD.Brushes-namespace. Het tweede parameter is het pad zelf. Voor dit voorbeeld gebruikt u de HatchBrush, die een rechthoekige penseel is met een schaakbordpatroon, een voorgrondkleur en een achtergrondkleur. Stel voordat u het HatchBrush-object doorgeeft aan de Fill Paths-methode, de eigenschappen ervan in.
### **GraphicsPath: Volledige broncode**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}



Alle klassen die IDisposable implementeren, worden geïnstantieerd in een Using-statement om ervoor te zorgen dat ze correct worden verwijderd.
