# TestData moje


## Testovací data - Email
Data v textové podobě
https://github.com/Radek4k/TestData/blob/main/adresa.data

## Testovací data - Adresa (ČR+SR)
###### Popis a zdroje
* https://cs.wikipedia.org/wiki/Ozna%C4%8Dov%C3%A1n%C3%AD_ulic_a_ve%C5%99ejn%C3%BDch_prostranstv%C3%AD
* číslo domu - popisné, orientační, evidenční https://www.katastr365.cz/aktuality/blog/domovni-cisla/#:~:text=Popisn%C3%A9%20%C4%8D%C3%ADslo%20d%C5%AFm%20popisuje%2C%20je,a%20zanik%C3%A1%20s%20existenc%C3%AD%20nemovitosti.
* https://www.cuzk.cz/Uvod/Produkty-a-sluzby/RUIAN/1-Editacni-agendovy-system-ISUI/Casto-kladene-dotazy-k-RUIAN-(FAQ)/FAQ-ulice,-cislovani-srpen2015.aspx - Maximum ulice je 48 znaků.
* Zajímavosti názvů obcí v České republice https://www.czso.cz/csu/czso/zajimavosti_nazvu_obci_v_ceske_republice 

###### Negativní testy
```
[Prázdné pole]
Počet znaků jak málo (2) tak hodně (100) - raději zkontrolovat zda 100 je OK = 48+ulice+čárkyMezery+PSČ+čísloPop /TODO převést na dat/
Specialny znaky (@,#,$,%), Unicode characters 🦄
🦄 42, Liberec 460 01
Na konci vesmíru 42, 🦄 460 01
Znaky které se běžně nepoužívají v CZ/SR
Üۺڲ
Neplatná/neexistující adresa /TODO převést na dat/
<script>alert("Hello!");</script>@example.com
```

###### Pozitivní testy
```
Křenová 72, Písek, 32415
Křenová 1295/72, Písek, 32415
P.O.box (P. O. BOX 72) 
Nábřeží Svazu protifašistických bojovníků 20, Ostrava-Poruba, 708 00
Aš 1, 32415
poštovní přihrádka 72, 273 01, KAMENNÉ ŽEHROVICE
P. O. BOX 72, 273 01, KAMENNÉ ŽEHROVICE
Hartmanice 1, Hartmanice 34201
Hartmanice 1, Hartmanice 56992
```


