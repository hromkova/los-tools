# Jaká data jsou potřeba

Pro výpočet horizontu pomocí LoS Tools potřebujete několik vstupních dat.

Základem je výškový model a bod, ze kterého se bude viditelnost počítat.

## 1. Výškový model

Výškový model určuje tvar terénu nebo povrchu.

Pro analýzy viditelnosti lze použít například:

- **DEM / DMR** – digitální model reliéfu,
- **DSM / DMP** – digitální model povrchu.

Digitální model reliéfu obvykle popisuje samotný terén.  
Digitální model povrchu zahrnuje také objekty na povrchu, například budovy nebo vegetaci.

Pro analýzy pohledových horizontů je často vhodný právě digitální model povrchu.

## 2. Bod pozorovatele

Bod pozorovatele určuje místo, odkud se počítá viditelnost.

Může to být například:

- vyhlídkové místo,
- věž,
- rozhledna,
- okraj zástavby,
- místo plánovaného záměru,
- libovolný bod v krajině.

Doporučené atributy bodu pozorovatele:

| Pole | Význam |
|---|---|
| `id` | jedinečný identifikátor bodu |
| `name` | název pozorovacího místa |
| `offset` | výška pozorovatele nad terénem |

## 3. Cílové nebo směrové body

Cílové body určují, kam se mají vést linie viditelnosti.

Mohou představovat konkrétní objekty nebo směry, ve kterých chceme hledat horizont.

Doporučené atributy cílových nebo směrových bodů:

| Pole | Význam |
|---|---|
| `id` | jedinečný identifikátor cílového bodu |
| `observer_id` | ID pozorovatele, ke kterému bod patří |
| `offset` | výška cíle nad terénem |
| `azimuth` | směr pohledu ve stupních |

## 4. Vrstva využití území

Pro pokročilejší příklady lze použít také polygonovou vrstvu využití území.

Ta umožní zjistit, na jakém typu plochy leží vypočítaný horizont.

Například zda horizont leží v ploše:

- lesa,
- zemědělské půdy,
- obytné zástavby,
- průmyslové zástavby,
- vodní plochy,
- travního porostu,
- ostatních ploch.

## Modelová data DMP Brno 2019

Pro vyzkoušení nástrojů je k dispozici modelový datový balíček:

[Stáhnout DMP Brno 2019](https://github.com/hromkova/los-tools/releases/download/data-dmp-brno-2019-v1/dmp_brno_19.zip)

Balíček obsahuje kompletní digitální model povrchu pro území Brna.

Použitá data:

- zdroj: data.Brno,
- datová sada: Digitální model povrchu / Digital Surface Model,
- rok: DMP 2019,
- předzpracování: převzorkování z rozlišení 0,25 m na 1 m,
- nástroj: GDAL Warp (reproject),
- metoda převzorkování: Bilinear.

Rozlišení 1 m bylo zvoleno proto, aby výpočet netrval příliš dlouho a zároveň bylo pro analýzy viditelnosti dostatečně podrobné.

## Další krok

Pokračujte stránkou:

[Základní pojmy](pojmy.md)
