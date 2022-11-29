# Git

Git je sistem za kontrolu verzija. On nam pomaže da pratimo sve promene nekome projektu , takođe se koristi da bi moglo više ljudi istovremeno da rade na nekom projektu.
Šta to Git radi?
* On omogućava praćenje istorije promena, kako lokalno tako i u zajedničkom radnom okruženju. Prednost ovog praćenja je u tome što znamo šta je menjano, kada je menjano, ko ga je menjao i zašto ga je menjao. Dobra strana svega je što tako praćene izmene na kraju mogu biti spojene u jednu istoriju.
* S obzirom da je u pitanju distribuirani sistem za kontrolu verzije, svaki računar poseduje ceo repozitorijum koji se čuva lokalno, dok server služi za razmenu i saradnju između korisnika. Svaki računar ima kopiju podataka koja se čuva lokalno i koja se sinhronizuje sa serverom.

Važno je da odmah napomenemo da Git može u potpunosti biti korišćen od strane pojedinca, bez potrebe da se ikada konektuje na server i sarađuje sa drugima, ali da on to može jednostavno učiniti kada god mu to bude potrebno.`

U narednim paragrafima ću vam pokazati kako da započnemo sa korišćenjem Git-a:
# Git konfiguracija
Komanda `git config` je funkcija koja se koristi za postavljanje vrednosti Git konfiguracije na globalnom ili lokalnom nivou projekta. Ovi nivoi konfiguracije odgovaraju `.gitconfig` tekstualnim datotekama. Izvršavanje `git config`-a će izmeniti tekstualnu datoteku konfiguracije.
```
git config --global user.email "your_email@example.com
```
## Neke osnovne funkcije su:
* `git init` - Kreira prazno git skladište ili ponovo inicijalizuje već postojeće
* `git clone` - Klonira skladište u novi direktorijum (folder)
* `git add` - Dodaje fajl u _staging area_
* `git status` - Prikazuje sve fajlove koji treba da budu priloženi (engl. _commit_)
* `git diff` - Prikazuje sve razlike u fajlovima koji nisu još priloženi i onih koji su sačuvani
* `git commit` - Čuva promene u skladištu
* `git reset` - Vraća skladište u neko stanje iz prošlosti
* `git log` - Prikazuje istoriju svih promena trenutne grane
* `git revert` - Vraća neke promene iz prošlosti

U narednim paragrafima su prikazani primeri ovih funkcija
```
git init C:/Users/User01/Documents
git clone https://github.com/example.git
git add projectgit
git status
git diff
git commit -m "prvi priloženi fajl"
git reset zadatak.cs
git log
git revert projekat~1
```
## Branching & merging

Karakteristika Git-a koja ga zaista izdvaja od skoro svakog drugog sistema za kontrolu verzija je njegov koncept modela grananja. Git nam omogućava da imamo više lokalnih grana koje mogu biti potpuno nezavisne u odnosu jedna na drugu.
* `git branch` - Prikazuje sve postojeće grane, Kreira ili briše grane
* `git merge` - Spaja istoriju navedene grane sa istorijom trenutne grane
* `git pull` - Uzima i spaja promene sa trenutnog skladišta sa navedenim granama
* `git push` - Obnavlja promene na glavnom skladištu koristeći promene sa trenutnog skladišta
```
git branch my2.6.14 v2.6.14   (1)
git merge projekat_1 projekat_2
git pull origin next
git push origin master
```
<p align="center">
  <img src="http://nvie.com/img/git-model@2x.png">
</p>

### Secure shell network protocol
Secure shell network protocol ili ti sigurnosni šel protokol je kriptografski mrežni protokol koji se koristi za bezbedno upravljanje mrežnim uslugama preko nezaštićene mreže. Njegove najistaknutije aplikacije su prijavljivanje sa daljine i izvršavanje sa komandne linije.
```
localhost:~$ ssh -p <broj porta (ako ostavimo praznim biće port 22)> <korisničko ime>@<adresa servera>
```
<p align="center">
  <img src="https://www-assets.kolide.com/assets/inventory/device_properties/icons/ssh-keys-3aa34a73f9567f78ae7a573fa758b65e4d0309d1.png">
</p>
