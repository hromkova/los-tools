# Testovací data

Na této stránce jsou ke stažení modelová data pro vyzkoušení nástroje LoS Tools v QGIS.

## DMP Brno 2019

Pro modelové příklady je připraven digitální model povrchu pro území Brna.

Data byla převzorkována z původního prostorového rozlišení 0,25 m na 1 m, aby výpočty netrvaly příliš dlouho a zároveň byla zachována dostatečná podrobnost pro analýzy viditelnosti.

[Stáhnout DMP Brno 2019](https://github.com/hromkova/los-tools/releases/download/data-dmp-brno-2019-v1/dmp_brno_19.zip)

## Zdroj dat

Vstupní data byla stažena z portálu data.Brno, datová sada:

**Digitální model povrchu / Digital Surface Model**

Použitá data: **DMP 2019**

## Předzpracování

Data byla v prostředí QGIS převzorkována z původního prostorového rozlišení 0,25 m na 1 m pomocí nástroje **GDAL Warp (reproject)**, s použitím resamplingové metody **Bilinear**.

## Poznámka k velikosti dat

Soubor je větší, protože obsahuje kompletní DMP pro území Brna. Stažení proto může chvíli trvat.
