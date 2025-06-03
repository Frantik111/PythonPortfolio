# PythonPortfolio
Projekty kódované v pythone

## xml
- tvorba custom xml feedu pre merchant center z csv súboru
- upgates.cz vytváral nedostatočný xml feed, preto som pristúpil k custom riešeniu
- v súčastnosti je manuálne python kód spúštaný podľa potreby, v pláne je ho umiestniť na aws - ec2 (doker)

## django
- pre potreby firmy a nespokojnosti s VBA excel objednávkami (vibe coding v 2023 - modularne okno s verifikáciou a spracovaním údajov)
- biznis bootstrap design
- __app__ customer_import
  - pomocou jupiterstudio vyčistené csv údaje z idoklad.sk (odstránenie duplicít, atď...)
  - import pomocou pandas do model
- __app__ customer
  - zoznam klientov s podrobnosťami o klientovi
  - pridanie odstránenie klientov
  - vyhľadávanie, filtrovanie
- __app__ fotografie
  - upload fotografií (možnosť na mobile spraviť buttonom fotografiu)
  - štítkovanie fotografií tagmi
  - priečinková organizácia fotografií na základe pridelených tagov
- __app__ values
  - navrhnuté ako settings pre django aplikáciu, išpirované visual studio settings
  - funkcia si vyžiada pár hodnôt
  - hodnoty sa vytvárajú a ukladajú do json formátu do modelu
  - hodnoty môžu mať rozličné typy údajov
- __app__ wesche objednávky
  - slúži ako objednávkový systém čistenia a opravy kobercov a s tým spojenými službami
  - zoznam objednávok
  - zoznam kobercov v objednávke
  - procedúry aplikované na koberce pri čistení a oprave
  - custom formuláre
  - css @media print
- __app__ synchro sklad
  - dodavateľské feedy stiahnuté 2x z FTP, 1x z emailu
  - aktualizovaná databáza podľa EAN kódu (aj pre potreby časového vývoju skladovej dostupnosti)
  - doplnanie položiek na základe csv súboru
  - tvorba csv s aktuálnou skladovou dostuposťou pre upgates.sk
- finesy
  - štandardne dijango umiestňuje konfigurácie aplikácie do priečinku s rovnakým názvom, ako je názov aplikácie, pre nespokojnosť bol premenovaný na settings
  - django seasons použitý na prenos variabilných hodnôt medzi jednotlivými appkami (id klienta z app customers do app objedávka )
  - custom user a použitie @login_required pre obmedzenie prístupu k funkciám
- plány
  - po odkončení wasche nasadenie na AWS EC2 (docker)
  - tvorba skladu predajne pre zvýšenie efektivity
  - objednávky od klienta k dodávateľovi
  - pokladňa a fakturácia
  - CRM
