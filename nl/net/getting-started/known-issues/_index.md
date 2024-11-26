---
title: Bekende problemen
type: docs
weight: 40
url: /nl/net/known-issues/
---

## **.NET Compact Framework**
- Het is opgemerkt dat op sommige specifieke Windows-versies, zoals Windows Mobile 5.0-6.0, de Compact Framework-assemblies die zijn ondertekend met een certificaat (of met dubbel ondertekende certificaten) niet werken zoals verwacht en niet correct kunnen worden geladen (een TypeLoadException wordt gegenereerd). Om het probleem te omzeilen, moet de gebruiker elk certificaat verwijderen en vervolgens de bijgewerkte assembly gebruiken. Houd er rekening mee dat u dit op eigen risico doet en wij garanderen geen correcte werking vanwege dergelijke wijzigingen aan de assembly. Wij leveren ook geen assemblies zonder handtekening, aangezien dit een potentieel beveiligingsrisico vormt. Klanten moeten in plaats daarvan proberen om geen gebruik te maken van dergelijke verouderde besturingssystemen, waar mogelijk, en/of het besturingssysteem upgraden naar nieuwere edities of servicepacks die het probleem met de certificaatondertekening oplossen.
