---
title: Známé Problémy
type: docs
weight: 40
url: /cs/net/zname-problemy/
---

## **.NET Compact Framework**
- Bylo zjištěno, že na některých konkrétních verzích Windows, jako je například Windows Mobile 5.0-6.0, nejsou kompaktní rámce podepsány certifikátem (nebo dvojitě podepsanými certifikáty) a nedaří se je načíst správně (je vyvoláno TypeLoadException). Pro překonání tohoto problému musí uživatel odstranit jakýkoli certifikát a poté použít aktualizovaný soubor shromáždění. Všimněte si, že toto provádíte na vlastní riziko, a nezaručujeme správnou funkčnost v důsledku této změny souboru shromáždění. Dále nevydáváme shromáždění bez podpisu, jelikož by to mohlo představovat potenciální bezpečnostní hrozbu. Místo toho by zákazníci měli, pokud je to možné, se vyvarovat používání tak starých operačních systémů a/nebo upgradovat operační systém na novější edice či service packy, které vyřeší problém s podepisováním certifikátů.

