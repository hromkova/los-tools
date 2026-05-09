---
layout: page
title: Modelové příklady
subtitle: Ukázky využití LoS Tools v QGIS
---

## Příklad: Horizont a využití území

Cílem je vypočítat horizont a zjistit, na jakém typu využití území horizont leží. Například zda je horizont tvořen
- lesem,
- zemědělskou půdou,
- obytnou zástavbou,
- průmyslovou zástavbou,
- vodní plochou,
- travním porostem,
- ostatními plochami.

Výsledkem bude mapa a tabulka, ve které lze pro jednotlivé směry vyhodnotit například to, zda horizont leží v ploše lesa, zástavby, průmyslového areálu, zemědělské půdy nebo jiné kategorie využití území.

## Co budete potřebovat

Pro tento příklad budete potřebovat:
1. <a href="https://www.qgis.org/download/" target="_blank" rel="noopener noreferrer">QGIS</a>
2. nainstalovaný <a href="https://plugins.qgis.org/plugins/los_tools/" target="_blank" rel="noopener noreferrer">plugin LoS Tools</a>
3. stažená <a href="https://github.com/hromkova/los-tools/releases/download/data-dmp-brno-2019-v1/dmp_brno_19.zip" target="_blank" rel="noopener noreferrer">modelová data DMP Brno 2019</a>
4. stažený <a href="https://github.com/hromkova/los-tools/raw/refs/heads/main/downloads/models/horizon_landuse.zip" target="_blank" rel="noopener noreferrer">QGIS Processing model</a>

## Jak přidat model do QGIS

Po stažení ZIP soubor rozbalte. 
V QGIS potom přidejte soubor `horizon_landuse.model3` do Processing Toolboxu do části Add Model to Toolbox:

1. Otevřete QGIS.
2. Otevřete panel **Processing Toolbox**.
3. V horní části panelu klikněte na ikonu modelů nebo otevřete **Processing Modeler**.
4. Zvolte možnost pro otevření nebo přidání existujícího modelu.
5. Vyberte stažený soubor modelu.
6. Model se zobrazí v panelu **Processing Toolbox** ve skupině **Models**.

## Co model dělá

Připravený model skládá několik kroků do jednoho postupu.

Model postupně:

1. načte pozorovací bod,
2. použije výšku pozorovatele nad povrchem (1,6 m, odpovídá výšce očí průůěrně vysokého člověka),
3. vytvoří body kolem pozorovatele (360°),
4. vytvoří linie viditelnosti (po 1°),
5. na těchto liniích vypočítá body horizontu,
6. vytvoří linii horizontu,
7. připraví tabulku s výsledky (s vertkálním úhlem horizontu),

Díky tomu uživatel nemusí spouštět každý dílčí nástroj samostatně.

## Jak model spustit

1. Otevřete QGIS.
2. Načtěte modelová data.
3. V panelu **Processing Toolbox** najděte připravený model.
4. Spusťte model dvojklikem.
5. Vyberte vstupní vrstvy a parametry.
6. Zvolte umístění výstupů.
7. Klikněte na **Run**.
8. Po dokončení zkontrolujte výstupy v mapě.

   
## Vstupní parametry modelu

Při spuštění modelu je potřeba nastavit několik vstupů.

| Parametr | Význam |
|---|---|
| `viewpoint` | bod pozorovatele |
| `raster` | digitální model povrchu |
| `id` | identifikátor pozorovacího bodu |
| `offset` | výška pozorovatele nad povrchem |
| `landuse` | polygonová vrstva využití území |

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

## Data pro využití území

Data pro využití území lze stáhnout pro území města Brna na stránkách <a href="https://land.copernicus.eu/en/products/urban-atlas?tab=land_coverland_use " target="_blank" rel="noopener noreferrer">Urban Atlasu</a>

Následně lze body horizontu pomocí nástroje Intersection propojit s Urban Atlasem.

## Jak číst výsledek

Výsledek ukazuje, kde se v jednotlivých směrech nachází horizont a na jakém typu využití území leží. 

## Na co si dát pozor

Před spuštěním modelu zkontrolujte:

- zda je plugin LoS Tools správně nainstalovaný,
- zda je výškový rastr načtený v QGIS,
- zda pozorovací bod leží v rozsahu rastru,
- zda mají vstupní data stejný souřadnicový systém,
- zda vrstva využití území pokrývá oblast vypočítaného horizontu,
- zda je správně nastavená výška pozorovatele.

## Další krok

Pokud narazíte na problém, pokračujte stránkou:

[Časté problémy](faq.md)
