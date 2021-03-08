# TestData moje


## Testovací data - Email
Data v textové podobě
https://github.com/Radek4k/TestData/blob/main/adresa.data

###### Popis a zdroje
* zdroje RFC
* https://en.wikipedia.org/wiki/Email_address
* RFC 3696: https://tools.ietf.org/html/rfc3696
* RFC 5321: https://tools.ietf.org/html/rfc5321
* RFC 5322: https://tools.ietf.org/html/rfc5322
* RFC 6530: https://tools.ietf.org/html/rfc6530
* List of top level domain from IANA https://data.iana.org/TLD/tlds-alpha-by-domain.txt
* https://cs.wikipedia.org/wiki/Seznam_internetov%C3%BDch_dom%C3%A9n_nejvy%C5%A1%C5%A1%C3%ADho_%C5%99%C3%A1du
* https://gist.github.com/cjaoude/fd9910626629b53c4d25
* Jaká je max velikost domény 1. řádu?
** 63 znaků


###### Pozitivní testy (platný emaily)
```
x@e.cz
test@gmail.chucknorris
beznyemail@seznam.cz
Abc\@def@example.com
Fred\ Bloggs@example.com
user+mailbox@example.com
!#$%&'*+-/=?^_`.{|}~@seznam.cz
customer/department=shipping@example.com
$A12345@example.com
!def!xyz%abc@example.com
_somename@example.com
test@eeee.museum
test@DcS5Ce1wUj0Pfvo5CAgiVh4gBHc8yUp0MnwbvuemgUzbb00aonBnmOgE3Xn7WHIZlcoutniv2O5A7w1fzuJDcJ6gZQL8012OCqdislZj1v0uIzKUtrgP95aRpPuU9IVEF6nlBY0QssQetFxF4mbocgiKcEutWdGYWnB6YzgUQ69Bw89Yo4EjbSeROWS8GHwFqfZLxgWk5uJiQnIIG1cBfsSxPIccF3govaXeGXZ3NA7bkeQu1mrOkqQo.museum
email@example.com.au
mail@neco.example.com
mail@nic.neco.example.com
“x@x.cz ”
me@example.com
a.nonymous@example.com
name+tag@example.com
name\@tag@example.com – this is a valid email address containing two @ symbols.
spaces\ are\ allowed@example.com
"spaces may be quoted"@example.com
!#$%&'*+-/=.?^_`{|}~@[1.0.0.127]
!#$%&'*+-/=.?^_`{|}~@[IPv6:0123:4567:89AB:CDEF:0123:4567:89AB:CDEF]
testmail@háčkyčárky.cz
me(this is a comment)@example.com
comments are discouraged but not prohibited by RFC2822.
```

###### Negativní testy
```
[prázdné pole]
spatnyemailseznam.cz
x@.cz
x@e.z
x@e.
@e.cz
x@.cz
x@gmail.com, x+1@gmail.com, x+2@gmail.com, x+test@gmail.com
x@xcz
x    @x.cz
x@x .cz
x@x     .cz (zkusit neviditelné znaky)
🦄@e.cz (nepovolené znaky)
<script>alert("Hello!");</script>@example.com
text=%3Cscript%3Ealert%28%22Hello%21%22%29%3B%3C%2Fscript%3E%40example.com
```

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


