---
title: Licencování
type: docs
weight: 60
url: /cs/java/licencovani/
---

## **Omezení verze evaluace**
Můžete stáhnout evaluaci verze Aspose.PSD pro Java ze [stažení stránky](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). Evaluace verze poskytuje stejné funkce jako plně licencovaná verze komponenty s několika omezeními. Po zakoupení Aspose.PSD stačí použít licenci k odstranění jakýchkoli omezení z nainstalované evaluace.

Evaluace verze Aspose.PSD pro Java poskytuje plnou funkčnost produktu, s pouhými dvěma omezeními:

- **Vodoznak na každém obrázku**: Každý obrázek, který uložíte, upravíte nebo exportujete, má vodoznak s textem "Evaluace pouze. Vytvořeno pomocí Aspose.PSD. Copyright 2018-2019 Aspose Pty Ltd.". U menších obrázků, kde by se celý vodoznak nevešel, jsou místo toho přidány dvě diagonální čáry přes obrázek.
- **Žádná podpora základní kreslicí funkcionality**: V režimu evaluace nelze načíst nebo uložit pixely obrázku. Pro kreslení obrázků použijte místo toho pokročilou kreslicí funkcionalitu. Toto omezení ovlivňuje funkčnost závislou na základní kreslicí funkcionalitě. Aspose.PSD pro Java vám umožňuje registrovat vlastní formát souboru. Tato funkce však závisí na základní kreslicí funkcionalitě, takže nemá smysl ji používat v režimu evaluace, protože nemůžete měnit obsah těchto souborů.

{{% alert color="primary" %}}

Pokud chcete otestovat Aspose.PSD pro Java bez omezení evaluace, požádejte o dočasnou licenci na 30 dní. Podívejte se na [Jak získat dočasnou licenci?](https://purchase.aspose.com/temporary-license) pro více informací.

{{% /alert %}}
## **O licenčním souboru**
Jakmile jste spokojení se svou evaluací Aspose.PSD, můžete zakoupit licenci na [Aspose webu](https://purchase.aspose.com/default.aspx). Seznamte se s různými nabízenými typy předplatného. Pokud máte nějaké otázky, neváhejte kontaktovat [obchodní tým Aspose](https://company.aspose.com/contact).

Každá licence od Aspose obsahuje jednoleté předplatné na softwarové aktualizace. Po prvním roce prodlužte své předplatné, abyste nadále dostávali nejnovější funkce a opravy. Technická podpora je zdarma a neomezená a poskytuje se jak licencovaným uživatelům, tak uživatelům v evaluaci prostřednictvím našich [podpůrných fór](https://forum.aspose.com/).

Licence je XML soubor obsahující detaily, jako je název produktu, počet licencovaných vývojářů, datum vypršení předplatného a další. Soubor je digitálně podepsaný, takže jej neupravujte: i nepředvážným přidáním dalšího zalomení řádku je soubor neplatný.

Po koupi Aspose.PSD potřebujete licenci použít před tím, než vytvoříte, upravíte nebo jinak manipulujete s obrázky. Licenci je třeba nastavit pouze jednou pro aplikaci nebo proces, který vyvíjíte.
## **Aplikace licence**
Můžete stáhnout evaluaci verze **Aspose.PSD** pro Java ze [své stažení stránky](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). Evaluační verze poskytuje naprosto stejné možnosti jako licencovaná verze produktu. Kromě toho se evaluační verze jednoduše stává licencovanou, když zakoupíte licenci a přidáte pár řádků kódu k aplikaci licence.

Jakmile jste spokojení se svou evaluací **Aspose.PSD**, můžete [zakoupit licenci](http://www.aspose.com/Purchase/Components/Default.aspx) na stránce Aspose. Seznamte se s různými nabízenými typy předplatného. Pokud máte nějaké otázky, neváhejte kontaktovat tým obchodníků Aspose.

Každá licence od Aspose obsahuje jednoleté předplatné na bezplatné aktualizace na nové verze nebo opravy, které vyjdou během této doby. Technická podpora je zdarma a neomezená a poskytuje se jak licencovaným uživatelům, tak uživatelům v evaluaci.

{{% alert color="primary" %}}

Pokud chcete otestovat **Aspose.PSD** bez omezení evaluace, požádejte o dočasnou licenci na 30 dní. Podívejte se na [Jak získat dočasnou licenci?](http://www.aspose.com/corporate/how-to-get-temporary-license.aspx) pro více informací.

{{% /alert %}}
### **Nastavení licence**
Licence je obyčejný textový XML soubor obsahující detaily, jako je název produktu, počet licencovaných vývojářů, datum vypršení předplatného a další. Soubor je digitálně podepsaný, takže jej neupravujte; dokonce i náhodné přidání dalšího zalomení řádku do souboru jej neplatným.

Před použitím **Aspose.PSD** musíte nastavit licenci, pokud chcete obejít jeho omezení evaluace. Licence je třeba nastavit pouze jednou pro aplikaci nebo proces.

Licenci lze načíst ze streamu nebo souboru na následujících místech:

1. Explicitní cesta.
1. Složka obsahující Aspose.PSD.jar.

Použijte metodu [License](http://www.aspose.com/api/java/psd/com.aspose.psd/classes/License).setLicense k licencování komponenty. Často nejjednodušší způsob, jak nastavit licenci, je umístit licenční soubor do stejné složky jako Aspose.PSD.jar a specifikovat pouze název souboru bez cesty, jak je znázorněno v následujícím příkladu:
#### **Příklad 1**
V tomto příkladu **Aspose.PSD** pokusí najít licenční soubor ve složce obsahující JAR aplikace.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense("Aspose.PSD.Java.lic");

{{< /highlight >}}
#### **Příklad 2**
Inicializuje licenci ze streamu.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense(new java.io.FileInputStream("Aspose.PSD.Java.lic"));

{{< /highlight >}}
### **Ověření licence**
Je možné ověřit, zda byla licence nastavena správně či nikoliv. Třída License obsahuje pole isLicensed, které vrátí true, pokud byla licence adekvátně nastavena.

**Java**

{{< highlight csharp >}}

 License license = new License();

license.setLicense("Aspose.PSD.Java.lic");

if (License.isLicensed()) {

    System.out.println("Licence byla nastavena!");

}

{{< /highlight >}}
## **Kde aplikovat licenci ve vaší aplikaci**
Kde aplikujete licenci, závisí na typu aplikace, kterou vyvíjíte. Postupujte podle těchto jednoduchých pravidel:

- Licence je třeba nastavit pouze jednou pro doménu aplikace. Volání License.setLicense vícekrát není škodlivé, ale plýtvá časem procesoru.
- Nastavte licenci před voláním jakýchkoli tříd Aspose.PSD.
- **Java aplikace**: Zavolejte License.SetLicense v startovním kódu.
- **Třída knihovny**: Zavolejte License.setLicense z statického konstruktoru třídy, která používá Aspose.PSD. Statický konstruktor se spustí předtím, než je vytvořena instance vaší třídy, což zajišťuje správné nastavení licence Aspose.PSD.
## **Používání více produktů Aspose**
Pokud ve vaší aplikaci používáte více než jeden produkt Aspose, například Aspose.PSD a Aspose.Cells, zde jsou několik užitečných tipů.

- **Nastavte licenci pro každý produkt Aspose samostatně**. I když máte jediný licenční soubor pro všechny komponenty, například 'Aspose.Total.lic', je stále nutné volat License.setLicense samostatně pro každý produkt Aspose ve vaší aplikaci.
- **Použijte plně qualifikovaný název třídy licence**. Každý produkt Aspose má třídu License ve svém jmenném prostoru. Například Aspose.PSD má com.aspose.psd.license.License a Aspose.Cells má com.aspose.cells.License. Použití plně qualifikovaného názvu třídy zabrání jakémukoli zmatení ohledně toho, k jakému produktu je licence aplikovaná.

