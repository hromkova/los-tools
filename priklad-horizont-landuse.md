---
layout: page
title: Horizont a využití území
subtitle: Modelový příklad výpočtu horizontu v Brně
---

Tento modelový příklad ukazuje, jak pomocí nástrojů **LoS Tools** vypočítat pohledový horizont a zjistit, na jakém typu využití území horizont leží.

Příklad je připravený pro území Brna a využívá předpřipravený model pro QGIS Processing Toolbox.

## Cíl příkladu

Cílem je zjistit:

- kde se z vybraného pozorovacího bodu nachází pohledový horizont,
- jak daleko horizont v jednotlivých směrech leží,
- jaký typ využití území se nachází pod vypočítaným horizontem.

Výsledkem bude mapa a tabulka, ve které lze pro jednotlivé směry vyhodnotit například to, zda horizont leží v ploše lesa, zástavby, průmyslového areálu, zemědělské půdy nebo jiné kategorie využití území.

## Co budete potřebovat

Pro tento příklad budete potřebovat:

1. QGIS 3.44,
2. nainstalovaný plugin LoS Tools,
3. modelová data pro území Brna,
4. připravený QGIS Processing model.

## Ke stažení

### Modelová data

Pro výpočet použijte připravený digitální model povrchu Brna a další podklady:

<a href="https://github.com/hromkova/los-tools/releases/download/data-dmp-brno-2019-v1/dmp_brno_19.zip" target="_blank" rel="noopener noreferrer">Stáhnout modelová data DMP Brno 2019</a>

## QGIS Processing model

Pro tento příklad je připravený QGIS Processing model, který spojí jednotlivé kroky výpočtu do jednoho postupu.

<a href="https://github.com/hromkova/los-tools/raw/refs/heads/main/downloads/models/horizon_landuse.zip" target="_blank" rel="noopener noreferrer">Stáhnout QGIS model jako ZIP</a>

Po stažení ZIP soubor rozbalte. V QGIS potom přidejte soubor `horizon_landuse.model3` do Processing Toolboxu do části Add Model to Toolbox.

## Jak přidat model do QGIS

Po stažení modelu jej přidejte do QGIS takto:

1. Otevřete QGIS.
2. Otevřete panel **Processing Toolbox**.
3. V horní části panelu klikněte na ikonu modelů nebo otevřete **Processing Modeler**.
4. Zvolte možnost pro otevření nebo přidání existujícího modelu.
5. Vyberte stažený soubor modelu.
6. Model se zobrazí v panelu **Processing Toolbox** ve skupině **Models**.

<!-- TODO: Později sem vložit screenshot přidání modelu do Processing Toolboxu. -->

## Co model dělá

Připravený model skládá několik kroků do jednoho postupu.

Model postupně:

1. načte pozorovací bod,
2. použije výšku pozorovatele nad povrchem,
3. vytvoří body kolem pozorovatele,
4. vytvoří linie viditelnosti,
5. vypočítá horizontní body,
6. vytvoří horizontní linii,
7. připraví tabulku s výsledky,
8. přiřadí k horizontu informace o využití území.

Díky tomu uživatel nemusí spouštět každý dílčí nástroj samostatně.

## Vstupní parametry modelu

Při spuštění modelu je potřeba nastavit několik vstupů.

| Parametr | Význam |
|---|---|
| `viewpoint` | bod pozorovatele |
| `raster` | digitální model povrchu |
| `id` | identifikátor pozorovacího bodu |
| `offset` | výška pozorovatele nad povrchem |
| `landuse` | polygonová vrstva využití území |

Názvy parametrů se mohou v QGIS zobrazovat podle toho, jak jsou pojmenované v modelu.

## Nastavení použité v modelu

Model je připravený tak, aby byl vhodný pro první vyzkoušení na datech Brna.

Použité nastavení:

| Parametr | Hodnota / princip |
|---|---|
| výškový model | DMP Brno 2019, převzorkovaný na 1 m |
| výška pozorovatele | hodnota z pole `offset` |
| pozorovací bod | bodová vrstva `viewpoint` |
| směry výpočtu | body vytvořené kolem pozorovatele |
| výstup | horizontní body, horizontní linie a tabulka |
| využití území | přiřazení podle polygonové vrstvy land use |

<!-- TODO: Doplnit konkrétní hodnoty parametrů podle finálního nastavení modelu, například počet směrů, vzdálenost výpočtu nebo interval azimutu. -->

## Jak model spustit

1. Otevřete QGIS.
2. Načtěte modelová data.
3. V panelu **Processing Toolbox** najděte připravený model.
4. Spusťte model dvojklikem.
5. Vyberte vstupní vrstvy a parametry.
6. Zvolte umístění výstupů.
7. Klikněte na **Run**.
8. Po dokončení zkontrolujte výstupy v mapě.

<!-- TODO: Později sem vložit krátké video nebo screenshot spuštění modelu. -->

## Výstupy modelu

Model vytvoří několik výstupů.

| Výstup | Co znamená |
|---|---|
| `horizon_points` | body, ve kterých byl nalezen horizont |
| `horizon_line` | linie spojující vypočítané horizontní body |
| `horizon_table` | tabulka s hodnotami pro další vyhodnocení |

Výstupní tabulka může obsahovat například:

| Pole | Význam |
|---|---|
| `azimuth` | směr pohledu ve stupních |
| `distance` | vzdálenost horizontu od pozorovatele |
| `observer_id` | identifikátor pozorovacího bodu |
| `landuse` | typ využití území pod horizontem |

## Jak číst výsledek

Data pro využití území lze stáhnout pro území města Brna na stránkách <a href="https://land.copernicus.eu/en/products/urban-atlas?tab=land_coverland_use " target="_blank" rel="noopener noreferrer">Urban Atlasu</a>

## Jak číst výsledek

Výsledek ukazuje, kde se v jednotlivých směrech nachází horizont.

Pokud je horizontní bod propojený s vrstvou využití území, lze zjistit, co danou část horizontu tvoří. Může jít například o:

- les,
- obytnou zástavbu,
- průmyslovou zástavbu,
- zemědělskou půdu,
- travní porost,
- vodní plochu,
- ostatní plochy.

Takový výstup pomáhá lépe interpretovat, co uživatel v krajině skutečně vnímá jako pohledový horizont.

## Na co si dát pozor

Před spuštěním modelu zkontrolujte:

- zda je plugin LoS Tools správně nainstalovaný,
- zda je výškový rastr načtený v QGIS,
- zda pozorovací bod leží v rozsahu rastru,
- zda mají vstupní data stejný souřadnicový systém,
- zda vrstva využití území pokrývá oblast vypočítaného horizontu,
- zda je správně nastavená výška pozorovatele.

## Další krok

Po dokončení výpočtu pokračujte stránkou:

[Jak číst výsledky](pruvodce/vysledky.md)
