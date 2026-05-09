---
layout: page
title: Časté problémy
subtitle: Řešení nejběžnějších potíží při práci s LoS Tools
---

## Jak nainstalovat plugin LoS Tools?

Plugin je možné stáhnout z oficiální stránky LoS Tools:

[Oficiální stránka LoS Tools](https://cahik.cz/projects/lostools)

Postup instalace ZIP souboru v QGIS:

1. Otevřete QGIS.
2. V horním menu zvolte **Zásuvné moduly**.
3. Vyberte **Spravovat a instalovat zásuvné moduly**.
4. Přejděte na možnost **Instalovat ze ZIP**.
5. Vyberte stažený soubor `los_tools.zip`.
6. Klikněte na **Instalovat zásuvný modul**.
7. Po instalaci otevřete v QGIS panel **Processing Toolbox**.
8. Dílčí nástroje jsou součástí sady LoS Tools.

## Plugin v QGIS není vidět

Zkontrolujte:

- zda je plugin nainstalovaný,
- zda je plugin povolený ve správci zásuvných modulů,
- zda používáte doporučenou verzi QGIS,
- zda jste po instalaci restartovali QGIS,
- zda máte otevřený panel Processing Toolbox.

## Výpočet nejde spustit

Zkontrolujte:

- zda jsou vybrané všechny povinné vstupní vrstvy,
- zda vstupní vrstvy obsahují správné atributy,
- zda výškový rastr pokrývá celé zájmové území,
- zda mají data správný souřadnicový systém,
- zda nejsou některé vstupní vrstvy prázdné.

## Výpočet je příliš pomalý

Výpočet může být pomalý hlavně při použití velmi podrobného výškového modelu nebo velkého množství linií viditelnosti.

Pomoci může:

- použít hrubší rozlišení rastru,
- zmenšit počet směrů nebo cílových bodů,
- testovat nejprve na menším území,
- zkontrolovat, zda nejsou vstupní data zbytečně velká.

Modelový DMP Brno 2019 byl převzorkován na rozlišení 1 m právě proto, aby výpočty netrvaly příliš dlouho.

## Horizont se nevytvořil

Možné příčiny:

- linie viditelnosti nebyly správně vytvořeny,
- vstupní bod pozorovatele neleží v rozsahu výškového rastru,
- výškový rastr neobsahuje platné hodnoty,
- cílové nebo směrové body nejsou správně přiřazeny k pozorovateli.

## Výsledek vypadá zvláštně

Zkontrolujte hlavně:

- souřadnicový systém dat,
- jednotky souřadnicového systému,
- hodnotu výšky pozorovatele,
- správné nastavení offsetu,
- rozsah a kvalitu výškového rastru.

## Data mají špatný souřadnicový systém

Pro výpočty vzdáleností je vhodné používat projektovaný souřadnicový systém v metrech.

Pokud jsou data v různých souřadnicových systémech, převeďte je před výpočtem do společného systému.

## Výškový rastr nepokrývá celé území

Pokud některé linie viditelnosti vedou mimo rozsah rastru, výpočet nemusí fungovat správně.

Zkontrolujte, zda výškový model pokrývá celé území, ve kterém chcete horizont počítat.

## Zpět na hlavní stránku

[Domů](index.md)
