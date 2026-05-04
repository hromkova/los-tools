---
layout: page
title: Odkazy
subtitle: Užitečné zdroje pro LoS Tools, QGIS, modelová data a citace
---

## LoS Tools

Oficiální stránka pluginu:

[LoS Tools](https://cahik.cz/projects/lostools)

Repozitář pluginu LoS Tools:

[JanCaha/qgis_los_tools](https://github.com/JanCaha/qgis_los_tools)

Dokumentace pluginu:

[Dokumentace LoS Tools](https://jancaha.github.io/qgis_los_tools/)

Stránka pluginu v repozitáři QGIS pluginů:

[LoS Tools – QGIS Plugins](https://plugins.qgis.org/plugins/los_tools/)

## QGIS

Oficiální web QGIS:

[QGIS](https://www.qgis.org/)

Stažení QGIS:

[Stáhnout QGIS](https://www.qgis.org/download/)

## Modelová data

Modelová data DMP Brno 2019:

[Stáhnout DMP Brno 2019](https://github.com/hromkova/los-tools/releases/download/data-dmp-brno-2019-v1/dmp_brno_19.zip)

## Zdroj výškových dat

Data byla stažena z portálu data.Brno, datová sada:

Digitální model povrchu / Digital Surface Model

[Data.Brno – Digitální model povrchu](https://data.brno.cz/datasets/mestobrno::digit%C3%A1ln%C3%AD-model-povrchu-digital-surface-model-/about)

## Data využití území

Pro přiřazení typu využití území k vypočteným horizontním bodům lze použít data Urban Atlas.

[Urban Atlas – Copernicus Land Monitoring Service](https://land.copernicus.eu/en/products/urban-atlas?tab=land_coverland_use)

## Web LoS Tools Lab

Tento výukový web je dostupný zde:

[LoS Tools Lab na GitHub Pages](https://hromkova.github.io/los-tools/)

Repozitář tohoto webu:

[hromkova/los-tools](https://github.com/hromkova/los-tools)

## Jak citovat

Tato část shrnuje doporučené citace webu, pluginu LoS Tools, softwaru QGIS a použitých datových zdrojů.

Citace je vhodné upravit podle citační normy požadované fakultou nebo katedrou.

### Citace tohoto výukového webu

Pokud v práci odkazujete na tento výukový web jako celek, můžete použít například:

```text
HROMKOVÁ, Lenka. LoS Tools Lab: Návody, modelová data a příklady využití nástrojů LoS Tools v QGIS. GitHub Pages, 2026. Dostupné z: https://hromkova.github.io/los-tools/
```

### Citace modelového příkladu

Pokud v práci odkazujete přímo na modelový příklad výpočtu horizontu a využití území, použijte konkrétní stránku:

```text
HROMKOVÁ, Lenka. LoS Tools Lab: Horizont a využití území. GitHub Pages, 2026. Dostupné z: https://hromkova.github.io/los-tools/priklad-horizont-landuse.html
```

### Citace pluginu LoS Tools

Plugin LoS Tools je vhodné citovat podle doporučení autora pluginu:

```text
Jan Caha (2025). LoS Tools. QGIS Plugin version 2.0. https://jancaha.github.io/qgis_los_tools/
```

BibTeX zápis uvedený autorem pluginu:

```bibtex
@Manual{,
  title = {LoS Tools}. QGIS Plugin version 2.0,
  author = {Jan Caha},
  year = {2025},
  url = {https://jancaha.github.io/qgis_los_tools/}
}
```

V textu práce lze plugin zmínit například takto:

> Pro výpočet linií viditelnosti a pohledového horizontu byl použit plugin LoS Tools pro QGIS (Caha, 2025).

### Citace QGIS

QGIS je vhodné uvést jako software použitý pro zpracování prostorových dat, spuštění Processing modelu a vizualizaci výsledků.

Příklad citačního zápisu:

```text
QGIS Development Team. QGIS Geographic Information System. Open Source Geospatial Foundation Project. Dostupné z: https://www.qgis.org/
```

### Citace použitých dat

U datových zdrojů je vhodné uvést název datové sady, poskytovatele, rok nebo verzi dat, licenci, datum stažení a URL.

Pro modelový příklad se jedná zejména o:

- digitální model povrchu Brna,
- data Urban Atlas,
- modelová data stažená z repozitáře LoS Tools Lab.

Příklad zápisu pro výšková data:

```text
Digitální model povrchu / Digital Surface Model. Data.Brno, 2019. Dostupné z: https://data.brno.cz/datasets/mestobrno::digit%C3%A1ln%C3%AD-model-povrchu-digital-surface-model-/about
```

Příklad zápisu pro data využití území:

```text
Urban Atlas. Copernicus Land Monitoring Service. Dostupné z: https://land.copernicus.eu/en/products/urban-atlas
```

### Doporučený metodický zápis do bakalářské práce

Následující text lze použít jako výchozí formulaci pro metodickou část práce:

```text
Výpočet byl proveden v prostředí QGIS 3.44 pomocí pluginu LoS Tools. Plugin byl citován podle doporučení autora pluginu (Caha, 2025). Pro modelový výpočet byl použit připravený QGIS Processing model publikovaný na výukovém webu LoS Tools Lab. Jako výškový vstup byl použit digitální model povrchu Brna 2019 převzorkovaný na prostorové rozlišení 1 m. Vypočtené horizontní body byly následně prostorově propojeny s polygonovou vrstvou využití území Urban Atlas.
```

---

*Poslední aktualizace: květen 2026.*
