---
title: Licence
type: docs
weight: 70
url: /cs/net/licensing/
description: Ohodnoťte knihovnu PSD Photoshop C# z NuGet a aplikujte licenci pomocí souboru nebo proudu pro odstranění jakýchkoli omezení z nainstalované evaluace.
---

## **Omezení zkušební verze**
Zkušební verzi Aspose.PSD pro .NET můžete stáhnout z [NuGetu](https://www.nuget.org/packages/Aspose.psd/). Zkušební verze poskytuje stejné funkce jako plně licencovaná verze komponenty s několika omezeními. Po zakoupení Aspose.PSD jednoduše aplikováním licence odstraníte jakákoli omezení z nainstalované evaluace. Zkušební verze Aspose.PSD pro .NET poskytuje plnou funkcionalitu produktu, s pouhými dvěma omezeními:

- **Vodoznak na každém obrázku**: Každý uložený, upravený nebo exportovaný obrázek má vodoznak s nápisem "Pouze pro evaluaci. Vytvořeno s Aspose.PSD. Copyright 2010-2018 Aspose Pty Ltd.". U malých obrázků, kde by se celý vodoznak nevešel, jsou na obrázku místo toho dvě diagonální čáry.
- **Žádná podpora pro základní kreslicí funkce**: V režimu evaluace nelze načítat nebo ukládat pixely obrázku. Pro kreslení obrázků použijte místo toho pokročilou kreslicí funkcionalitu. Toto omezení ovlivňuje funkčnost, která závisí na základní kreslicí funkcionalitě. Aspose.PSD pro .NET vám umožňuje registrovat vlastní formát souboru. Tato funkce však závisí na základní kreslicí funkcionalitě, takže dává smysl ji nepoužívat v režimu evaluace, protože nemůžete měnit obsah těchto souborů.

Pokud chcete otestovat Aspose.PSD pro .NET bez omezení evaluace, můžete požádat o dočasnou 30denní licenci. Pro více informací se podívejte na [Jak získat dočasnou licenci?] (https://purchase.aspose.com/temporary-license).
## **O licenčním souboru**
Jakmile jste spokojeni s evaluací Aspose.PSD, můžete zakoupit licenci na [Aspose webové stránce](https://purchase.aspose.com/default.aspx). Seznamte se s různými nabízenými typy předplatného. Pokud máte jakékoli dotazy, neváhejte kontaktovat [obchodní tým Aspose](https://company.aspose.com/contact). Každá licence od Aspose obsahuje jednoleté předplatné pro aktualizace softwaru. Po prvním roce obnovte svá předplatná, abyste pokračovali v získávání nejnovějších funkcí a oprav. Technická podpora je zdarma a neomezená a poskytuje se jak licencovaným, tak i uživatelům evaluace prostřednictvím našich [podpůrných fór] (https://forum.aspose.com/). Licence je XML soubor obsahující detaily jako název produktu, počet licencovaných vývojářů, datum vypršení předplatného a tak dále. Soubor je digitálně podepsán, takže ho neupravujte: dokonce i omylem přidání dalšího zalomení řádku soubor neplatný. Po koupi Aspose.PSD musíte licenci aplikovat před vytvořením, upravením nebo jiným manipulováním obrázků. Pokud zapomenete aplikovat licenci, výstupní obrázky budou obsahovat evaluční vodoznak. Licenci stačí nastavit pouze jednou pro každou aplikaci nebo proces, který vyvíjíte.
## **Kde aplikovat licenci ve vaší aplikaci**
Kde aplikovat licenci závisí na typu aplikace, kterou vyvíjíte. Postupujte podle těchto jednoduchých pravidel:

- Licenci použijte pouze jednou na doménu aplikace. Opakované volání License.SetLicense není škodlivé, ale zbytečně zatěžuje procesor.
- Aplikujte licenci před voláním jakýchkoli tříd Aspose.PSD pro .NET.
- **Aplikace Windows Forms nebo konzole**: zavolejte License.SetLicense v kódování spouštění, před použitím jakýchkoli tříd Aspose.PSD pro .NET.
- **ASP.NET aplikace**: zavolejte License.SetLicense z Global.asax.cs (Global.asax.vb) souboru, ve chráněné metody Application_Start. Tím je volána jednou při spuštění aplikace. Nezavádějte License.SetLicense z Page_Load metod, protože licence se načítá pokaždé, když je načtena webová stránka.
- **Silverlight aplikace**: zavolejte License.SetLicense z události Application_Startup v souboru App.xaml.cs (App.xaml.vb).
- **Třídy knihovny**: zavolejte License.SetLicense z statického konstruktoru třídy, která používá Aspose.PSD. Statický konstruktor se spustí před vytvořením instance vaší třídy, zajistí tedy, že licence Aspose.PSD je správně nastavena.
## **Aplikování licence**
Zkušební verzi Aspose.PSD si můžete snadno stáhnout z NuGet [stránky ke stažení](https://www.nuget.org/packages/Aspose.psd/). Zkušební verze poskytuje úplně stejné schopnosti jako licencovaná verze Aspose.PSD. Kromě toho se zkušební verze jednoduše stane licencovanou, když zakoupíte licenci a přidáte několik řádků kódu pro aplikaci licence.
### **Používání souboru nebo proudu**
Chcete-li se vyhnout práci s omezeními evaluace, musíte licenci nastavit před použitím Aspose.PSD. Licenci stačí nastavit pouze jednou na aplikaci (nebo proces).
### **Aplikování licence z souboru**
Nejjednodušší způsob, jak aplikovat licenci, je umístit licenční soubor do stejné složky jako Aspose.PSD.dll. Poté můžete v kódu místo plné cesty specifikovat název souboru.



{{< highlight java >}}

 // Vytvořte instanci licence a aplikujte licenci pomocí plné cesty

Aspose.PSD.License licence = new Aspose.PSD.License();

licence.SetLicense("Aspose.PSD.lic");



{{< /highlight >}}



Když zavoláte metodu SetLicense, název licence by měl být stejný jako název vašeho licenčního souboru. Například pokud změníte název licenčního souboru na "Aspose.PSD.lic.xml", měli byste tento název licence použít pro metodu SetLicense.
### **Aplikování licence pomocí proudu**
Je také možné načíst licenci z proudu, jak je uvedeno níže.



{{< highlight java >}}



// Vytvořte instanci licence a aplikujte licenci pomocí proudu

Aspose.PSD.License licence = new Aspose.PSD.License();

licence.SetLicense(můjStream);



{{< /highlight >}}
### **Kontrola stavu licence**
Třída Aspose.PSD.License má vlastnost IsLicensed, která vrátí true, pokud byla licence správně nastavena.



{{< highlight java >}}

 License licence = new License();

licence.SetLicense(cestaLicence);

if (license.IsLicensed)

{

    Console.WriteLine("Licence je nastavena!");

}

{{< /highlight >}}
### **Použití vloženého zdroje**
Praktický způsob zabalování licence s vaší aplikací a zajištění, že není ztracena, je zahrnutí jako vložený zdroj do jednoho z montáží, které volají Aspose.PSD. Pro zahrnutí licenčního souboru jako vloženého zdroje:

1. V programu Visual Studio .NET klepněte na**Soubor** a vyberte **Přidat existující položku**.
1. Začleněte licenční soubor (s příponou .lic) do projektu.
1. Vyberte soubor v Průzkumníku řešení.
1. V okně Vlastnosti nastavte volbu **Akce sestavení** na **Vložený zdroj**.

Není nutné volat metody GetExecutingAssembly nebo GetManifestResourceStream z třídy System.Reflection.Assembly v rámci Microsoft .NET Framework k přístupu k vložené licenci. Místo toho vložte soubor jako zdroj do projektu a poté předejte název licenčního souboru k metodě SetLicense. Třída License automaticky najde licenční soubor ve vložených zdrojích. Níže je uveden příklad, jak zahrnout licenci jako vložený zdroj a aplikovat ji na vaší aplikaci.



{{< highlight java >}}

 // Vytvořte instanci třídy Licence

Aspose.PSD.License licence = new Aspose.PSD.License();



// Předejte název vloženého licenčního souboru

licence.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}


### **Kontrola stavu licence**
Třída Aspose.PSD.License má vlastnost IsLicensed, která vrátí true, pokud byla licence správně nastavena.



{{< highlight java >}}

 License licence = new License();

licence.SetLicense(cestaLicence);

if (license.IsLicensed)

{

    Console.WriteLine("Licence je nastavena!");

}

{{< /highlight >}}
