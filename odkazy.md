---
layout: page
title: Odkazy
subtitle: Užitečné zdroje pro LoS Tools, QGIS, modelová data a citace
---

## LoS Tools

Oficiální stránka pluginu: [LoS Tools](https://cahik.cz/projects/lostools)

Repozitář pluginu LoS Tools: [JanCaha/qgis_los_tools](https://github.com/JanCaha/qgis_los_tools)

Dokumentace pluginu: [Dokumentace LoS Tools](https://jancaha.github.io/qgis_los_tools/)

Stránka pluginu v repozitáři QGIS pluginů: [LoS Tools – QGIS Plugins](https://plugins.qgis.org/plugins/los_tools/)


## Web LoS Tools Lab

Tento výukový web je dostupný zde: [LoS Tools Lab na GitHub Pages](https://hromkova.github.io/los-tools/)

Repozitář tohoto webu: [hromkova/los-tools](https://github.com/hromkova/los-tools)

## Jak citovat

Tato část shrnuje doporučené citace webu, pluginu LoS Tools, softwaru QGIS a použitých datových zdrojů.

Citace je vhodné upravit podle citační normy požadované fakultou nebo ústavem.

### Citace tohoto výukového webu

Pokud v práci odkazujete na tento výukový web jako celek, můžete použít například:

```text
HROMKOVÁ, Lenka. LoS Tools Lab: Návody, modelová data a příklady využití nástrojů LoS Tools v QGIS. GitHub Pages, 2026. Dostupné z: https://hromkova.github.io/los-tools/
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

---

## Výšková data

Pro modelový příklad byl použit digitální model povrchu pro území Brna z portálu data.Brno.

Původní datová sada:

[Data.Brno – Digitální model povrchu / Digital Surface Model](https://data.brno.cz/datasets/mestobrno::digit%C3%A1ln%C3%AD-model-povrchu-digital-surface-model-/about)

Pro účely výukového příkladu byla použita upravená verze dat. Původní výšková data byla převzorkována na nižší prostorové rozlišení (1 m), aby byla vhodnější pro stažení, práci v QGIS a opakování modelového výpočtu v rámci výuky.

Upravená modelová data použitá v tomto příkladu:

[Stáhnout DMP Brno 2019 – upravená modelová data](https://github.com/hromkova/los-tools/releases/download/data-dmp-brno-2019-v1/dmp_brno_19.zip)

Doporučená citace původních dat:

```text
Statutární město Brno. Digitální model povrchu / Digital Surface Model. Data.Brno, 2019. Licence CC BY 4.0. Dostupné z: https://data.brno.cz/datasets/mestobrno::digit%C3%A1ln%C3%AD-model-povrchu-digital-surface-model-/about
```

Doporučený popis úpravy dat:

```text
Pro účely modelového výpočtu byla použita upravená verze datové sady Digitální model povrchu / Digital Surface Model, poskytované Statutárním městem Brnem prostřednictvím portálu data.Brno. Data byla převzorkována na nižší prostorové rozlišení a publikována jako modelová data pro výukové účely.
```

*Poslední aktualizace: květen 2026.*
