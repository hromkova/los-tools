# Modelové příklady

Modelové příklady ukazují, jak lze LoS Tools použít v praxi.

První verze webu obsahuje návrh příkladů. Podrobné návody, screenshoty a vzorové projekty QGIS budou doplněny postupně.

## Příklad 1: Horizont kolem jednoho pozorovatele

Základní příklad pro začátečníky.

Cílem je vypočítat horizont kolem jednoho pozorovacího bodu a zobrazit výslednou horizontní linii v mapě.

Uživatel se naučí:

- načíst výškový model,
- načíst bod pozorovatele,
- připravit směry pohledu,
- spustit výpočet,
- zobrazit horizontní body nebo horizontní linii.

## Příklad 2: Je vybraný cíl viditelný?

V tomto příkladu uživatel ověří, zda je konkrétní bod viditelný z pozorovacího místa.

Cílem může být například:

- věž,
- vrchol,
- rozhledna,
- stavba,
- jiný výrazný bod v krajině.

Výsledek ukáže, zda mezi pozorovatelem a cílem existuje volná linie viditelnosti.

## Příklad 3: Porovnání více pozorovacích míst

Tento příklad slouží k porovnání horizontů z několika různých pozorovacích bodů.

Lze tak zjistit, ze kterého místa je výhled otevřenější, kde je horizont blíže a kde je pohled více omezený.

## Příklad 4: Horizont a využití území

Pokročilejší modelový příklad.

Cílem je vypočítat horizont a zjistit, na jakém typu využití území horizont leží.

Například zda je horizont tvořen:

- lesem,
- zemědělskou půdou,
- obytnou zástavbou,
- průmyslovou zástavbou,
- vodní plochou,
- travním porostem,
- ostatními plochami.

## Princip postupu

1. Vypočítají se horizontní body.
2. Horizontní body se prostorově spojí s polygonovou vrstvou využití území.
3. Ke každému horizontnímu bodu se přiřadí typ využití území.
4. Výsledek se zobrazí v mapě a atributové tabulce.

Doporučený výstup:

| Azimut | Vzdálenost horizontu | Typ využití území |
|---|---:|---|
| 0° | 1250 m | les |
| 45° | 980 m | obytná zástavba |
| 90° | 1430 m | zemědělská půda |

## Modelová data

Pro vyzkoušení příkladů lze použít DMP Brno 2019:

[Stáhnout DMP Brno 2019](https://github.com/hromkova/los-tools/releases/download/data-dmp-brno-2019-v1/dmp_brno_19.zip)

## Další krok

Pokud narazíte na problém, pokračujte stránkou:

[Časté problémy](faq.md)
