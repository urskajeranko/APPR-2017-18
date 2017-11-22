# Analiza podatkov s programom R, 2017/18

Repozitorij z gradivi pri predmetu APPR v študijskem letu 2017/18

## Analiza izbranih držav glede na prevladujočo državno religijo

V svoji projektni nalogi bom preučila vplive šestih svetovnih religij na sedem izbranih držav, pri čemer bo ena od držav zastopala neverujoče. Ker so gospodarstva držav, njihov razvoj ter uspešnost v svetu odvisna predvsem od drugih dejavnikov (npr. od zgodovine naroda, osamosvojitve države, naravnogeografske lege, naravnih virov, ...), se bom bolj osredotočila na populacijo in njene značilnosti, ki so bolj odvisne od državne religije.

Države, ki jih bom preučevala, sem izbrala tako, da v čim večji meri zastopajo določeno religijo oz. čim večji delež prebivalstva pripada tej veri. Tako sem kot predstavnico katolištva izbrala Italijo, protestantizma Veliko Britanijo, pravoslavcev Romunijo, islam zastopa Iran, hinduizem seveda Indija in budizem Tajska. Kot predstavnico neverujočih sem določila Kitajsko, saj se je po raziskavi iz leta 2014 kar 90 % prebivalstva opredelilo kot ateist ali neverujoči.

Vplive religij bom analizirala skozi naslednje indikatorje:
* rodnost
* izobrazba
* revščina
* ločitve
* BDP per capita po kupni moči

Viri tabel
* rodnost, izobrazba, BDP: http://databank.worldbank.org/data/reports.aspx?Code=NY.GDP.PCAP.CD&id=1ff4a498&report_name=Popular-Indicators&populartype=series&ispopular=y
* revščina: https://ourworldindata.org/extreme-poverty/#the-evolution-of-extreme-poverty-country-by-country, http://appsso.eurostat.ec.europa.eu/nui/submitViewTableAction.do
* ločitve: https://en.wikipedia.org/wiki/Divorce_demographyhttp://appsso.eurostat.ec.europa.eu/nui/submitViewTableAction.do

## Program

Glavni program in poročilo se nahajata v datoteki `projekt.Rmd`. Ko ga prevedemo,
se izvedejo programi, ki ustrezajo drugi, tretji in četrti fazi projekta:

* obdelava, uvoz in čiščenje podatkov: `uvoz/uvoz.r`
* analiza in vizualizacija podatkov: `vizualizacija/vizualizacija.r`
* napredna analiza podatkov: `analiza/analiza.r`

Vnaprej pripravljene funkcije se nahajajo v datotekah v mapi `lib/`. Podatkovni
viri so v mapi `podatki/`. Zemljevidi v obliki SHP, ki jih program pobere, se
shranijo v mapo `../zemljevidi/` (torej izven mape projekta).

## Potrebni paketi za R

Za zagon tega vzorca je potrebno namestiti sledeče pakete za R:

* `knitr` - za izdelovanje poročila
* `rmarkdown` - za prevajanje poročila v obliki RMarkdown
* `shiny` - za prikaz spletnega vmesnika
* `DT` - za prikaz interaktivne tabele
* `maptools` - za uvoz zemljevidov
* `sp` - za delo z zemljevidi
* `digest` - za zgoščevalne funkcije (uporabljajo se za shranjevanje zemljevidov)
* `readr` - za branje podatkov
* `rvest` - za pobiranje spletnih strani
* `reshape2` - za preoblikovanje podatkov v obliko *tidy data*
* `dplyr` - za delo s podatki
* `gsubfn` - za delo z nizi (čiščenje podatkov)
* `ggplot2` - za izrisovanje grafov
* `extrafont` - za pravilen prikaz šumnikov (neobvezno)
