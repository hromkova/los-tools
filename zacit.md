---
layout: page
title: Začít s LoS Tools
subtitle: Rychlý průvodce od instalace po první výpočet
---

Tato stránka vás provede základním postupem, jak začít pracovat s nástroji **LoS Tools** v QGIS.

Pokud s nástroji začínáte, postupujte krok za krokem. Nejdříve si udělejte představu, co nástroje umožňují zjistit, potom pokračujte instalací, přípravou dat a prvním výpočtem.

## 1. Co lze pomocí LoS Tools zjistit

LoS Tools pomáhají odpovědět například na otázky:

- kde se z vybraného místa nachází pohledový horizont,
- zda je konkrétní cíl viditelný,
- jak se liší horizonty z různých pozorovacích míst,
- na jakém typu využití území horizont leží.

Přehled typických úloh najdete zde:

[Modelové příklady](priklady.md)

<!-- TODO: Později sem lze vložit krátký obrázek nebo schéma výsledků. -->

## 2. Nainstalujte QGIS

LoS Tools fungují jako plugin v prostředí QGIS.

Nástroje jsou ověřené a spolehlivě fungují ve verzi **QGIS 3.44**.

<a href="https://www.qgis.org/download/" target="_blank" rel="noopener noreferrer">Stáhnout QGIS</a>

## 3. Nainstalujte plugin LoS Tools

Plugin můžete získat dvěma způsoby:

- z oficiálního webu pluginu,
- jako ZIP soubor z tohoto webu.

Podrobný postup instalace najdete zde:

[Instalace pluginu](pruvodce/instalace.md)

## 4. Najděte nástroje v QGIS

Po instalaci pluginu se nástroje **LoS Tools** zobrazí v QGIS v panelu **Processing Toolbox**.

Panel najdete obvykle v pravé části okna QGIS. Pokud ho nevidíte, zapněte ho v horním menu:

**Processing → Toolbox**

V panelu **Processing Toolbox** vyhledejte skupinu:

**LoS Tools**

Po rozbalení skupiny uvidíte jednotlivé části nástrojů, například:

- **Azimuths**,
- **Calculate Parameters Settings**,
- **Horizons**,
- **LoS Analysis**,
- **LoS Creation**,
- **Points Creation**,
- **Raster Editing**.

Pokud skupinu **LoS Tools** v panelu nevidíte, zkontrolujte, zda je plugin správně nainstalovaný a povolený ve správci zásuvných modulů.

<!-- TODO: Později sem vložit screenshot QGIS: Processing Toolbox → LoS Tools. -->
<!-- Doporučený soubor: assets/images/qgis-los-tools-processing-toolbox.png -->

## 5. Připravte modelová data

Pro první vyzkoušení je připravený digitální model povrchu Brna a další podklady.

Všechna dostupná data a soubory najdete zde:

[Ke stažení](stazeni.md)

Více o tom, jaká data jsou pro výpočet potřeba, najdete zde:

[Jaká data jsou potřeba](pruvodce/data.md)

## 6. Projděte si základní pojmy

Před prvním výpočtem je dobré vědět, co znamená:

- pozorovatel,
- cíl,
- linie viditelnosti,
- horizont,
- azimut,
- výška pozorovatele nad terénem.

[Základní pojmy](pruvodce/pojmy.md)

## 7. Spusťte první výpočet horizontu

Začněte jednoduchým výpočtem horizontu kolem jednoho pozorovacího bodu.

Tento krok vás provede načtením dat, přípravou vstupů a spuštěním základní analýzy.

[První výpočet horizontu](pruvodce/prvni-vypocet.md)

<!-- TODO: Později sem lze vložit krátké video: první výpočet horizontu v QGIS. -->

## 8. Zkontrolujte a přečtěte výsledky

Po výpočtu si výsledek zobrazíte v mapě a atributové tabulce.

Naučíte se rozpoznat:

- linie viditelnosti,
- horizontní body,
- horizontní linii,
- základní atributy výsledku.

[Jak číst výsledky](pruvodce/vysledky.md)

## 9. Pokračujte modelovými příklady

Až zvládnete první výpočet, můžete pokračovat dalšími modelovými příklady:

- horizont kolem jednoho pozorovatele,
- viditelnost vybraného cíle,
- porovnání více pozorovacích míst,
- horizont a využití území.

[Modelové příklady](priklady.md)
