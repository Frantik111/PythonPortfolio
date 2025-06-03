# PythonPortfolio
Projekty kódované pythonom

## xml
- tvorba custom xml feedu pre merchant center z csv súboru
- upgates.cz vytváral nedostatočný xml feed, preto som pristúpil k ustom riešeniu
- v súčastnosti je manuálne python kód spúštaný podľa potreby, v pláne je ho umiestniť na aws - ec2 (doker)

## django
- pre potreby firmy a nespokojnosti s VBA excel objednávkami (vibe coding v 2023 - modularne okno s verifikaciou a spracovaním údajov)
- biznis bootstrap design
- app customer_import
  - pomocou jupiterstudio vyčistené csv údaje z idoklad.sk (odstránenie duplicít, atď...)
  - import pomocou pandas do model
- app customer
  - zoznam klientov s podrobnosťami o klientovi
  - pridanie odstránenie klientov
  - vyhľadávanie, filtrovanie
- app fotografie
  - upload fotografií (možnosť na mobile spraviť buttonom fotografiu)
  - štítkovanie fotografií tagmi
  - priečinková organizácia fotografií na základe pridelených tagov
- app values
  - navrhnuté ako settings pre django aplikáciu, išpirované visual studio settings
  - funkcia si vyžiada pár hodnôt
  - hodnoty sa vytvárajú a ukladajú do json formátu do modelu
  - hodnoty môžu mať rozličné typy údajov
- app wesche objednávky
  - slúži ako objednávkový systém čistenia a opravy kobercov a s tým spojenými službami


- finesy
  - štandardne dijango umiestnuje konfigurácie aplikácie do priečinku s rovnakým názvom ako je názov aplikácie, pre nespokojnosť bol premenovaný na settings
  - django seasons použítý na prenos variabilných hodnôt medzi jednotlivými appkami (id klienta z app customers do app objedávka )
  - custom user a použitie @login_required pre obmedzenie prístupu k funkciam
