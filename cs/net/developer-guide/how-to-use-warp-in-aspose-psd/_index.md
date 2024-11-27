---
title: Jak použít vlnění v Aspose.PSD
type: docs
weight: 40
url: /cs/jak-pouzit-vlneni-v-aspose-psd/
---

## **Část 1 – Vykreslování souboru PSD s efektem Vlnění**

Photoshop uloží vykreslený obraz po aplikaci efektu Vlnění. Naše knihovna dokáže reprodukovat nebo znovu vykreslit obrázek s efektem Vlnění. Pro povolení této funkce jednoduše nastavte příznak AllowWarpRepaint v nastavení při otevírání souboru PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentace-Aspose-PSD-Vlnění-Vykreslování-1.cs" >}}

Výsledek:
![Aspose.PSD pro .NET Výsledek Vlnění 1](warp1.png)

Kromě vykreslování efektu Vlnění pro SmartLayers, naše knihovna také podporuje Vlnění pro TextLayers. Implementační kód zůstává stejný, jediný rozdíl spočívá v názvu souboru.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentace-Aspose-PSD-Vlnění-Vykreslování-2.cs" >}}

Výsledek:
![Aspose.PSD pro .NET Výsledek Vlnění 2](warp2.png)

**! Poznámka: ** V současné době naše knihovna podporuje vykreslování jak vlastního Vlnění (kde uživatelé manipulují body sítě), tak všechny standardní typy Vlnění.
* - V současné době naše knihovna podporuje vlastní Vlnění s standardní sítí a aktivně pracujeme na rozšíření naší podpory tak, aby zahrnovala všechny typy sítí v blízké budoucnosti.


## **Část 2 – Modifikace efektu Vlnění**

Naše knihovna vám umožňuje nejen vykreslovat, ale také modifikovat (přidávat) efekt Vlnění.
Tyto úpravy jsou usnadněny funkcemi třídy **WarpParams**.

| **Funkce**  | **Popis**                                                         | 
|:-------------|:----------------------------------------------------------------------------|
| Hranice       | Vrátí hranice zkřiveného obrazu.                                     |
| MeshPoints   | Pole bodů, přičemž každý bod představuje vrchol mřížky zkreslení. |
| Hodnota        | Hodnota efektu vlnění pro nevlastní efekty vlnění.                   |
| WarpRotates  | Výčet, který definuje směr nevlastních efektů vlnění.           |
| WarpStyles   | Výčet, který definuje typ efektu vlnění.                            |

Příklad kódu níže ukazuje, jak určit typ efektu Vlnění pro chytrou vrstvu a upravit typ a intenzitu zkreslení efektu.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentace-Aspose-PSD-Vlnění-Vykreslování-3.cs" >}}

Výsledek:
![Aspose.PSD pro .NET Výsledek Vlnění 3](warp3.png)

## **Část 3 – Přidání efektu Vlnění**

Příklad kódu níže ukazuje, jak přidat standardní efekt Vlnění do chytré vrstvy.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentace-Aspose-PSD-Vlnění-Vykreslování-4.cs" >}}

Výsledek:
![Aspose.PSD pro .NET Výsledek Vlnění 4](warp4.png)

Příklad kódu níže ukazuje, jak přidat efekt vlastního Vlnění do chytré vrstvy.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentace-Aspose-PSD-Vlnění-Vykreslování-5.cs" >}}

Výsledek:
![Aspose.PSD pro .NET Výsledek Vlnění 5](warp5.png)

Příklad kódu níže ukazuje, jak přidat efekt Vlnění do textové vrstvy. 
**! Poznámka:** Podle standardů Photoshopu je efekt Vlnění pro textové vrstvy obvykle omezen na standardní typ. Naše knihovna však podporuje použití dvou typů efektů Vlnění. Vezměte prosím na vědomí, že takové soubory nemusí plně kompatibilní s Photoshopem.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentace-Aspose-PSD-Vlnění-Vykreslování-5.cs" >}}

Výsledek:
![Aspose.PSD pro .NET Výsledek Vlnění 6](warp6.png)

Neustále zdokonalujeme a rozšiřujeme možnosti našeho efektu Vlnění, zaměřujeme se na zlepšení jeho rychlosti, kvality a podporované funkcionality. Zůstaňte informováni s našimi měsíčními aktualizacemi o nejnovějších vývojích.
Váš tým Aspose.PSD
