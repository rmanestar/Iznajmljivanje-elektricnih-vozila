# Iznajmljivanje električnih vozila
Projekt izrađen u sklopu kolegija: Uzorci dizajna

## Opis projekta

Izrada sustava za iznajmljivanje električnih vozila u obliku konzolne aplikacije. U aplikaciji je potrebno koristiti uzorke dizajna koji su opisani u GoF (Gang of Four) knjizi. Dopušteno je koristiti razne uzorke, međutim, cilj je na temelju opisa projekta identificirati i implementirati "najbolje" uzorke za opisane djelove projekta. Odabir programskog jezika koji će biti korišten za izradu aplikacije prepušten je studentima (Java ili C#). Projekt ima tri faze, a u svakoj fazi se aplikacija  nadograđuje s raznim funkcionalnostima i uzorcima. Kod predaje faze projekta potrebno je priložiti dijagram klasa koji prikazuje korištene uzorke dizajna i tablicu koja sadrži listu korištenih uzoraka. Za svaki uzorak u tablici potrebno je opisati zašto je baš taj uzorak korišten i u kojem dijelu aplikacije je implementiran.

### Prva faza
U ovoj fazi bilo je potrebno postaviti temelj aplikacije (učitavanje i sadržaja datoteka, definiranje potrebnih klasa, implementacija i provjera ispravnosti naredba koje se mogu izvršavati u aplikaciji i sl.). U opisu projekta je definirano da tvrtka iznajmljuje različite vrste vozila (električne bicikle, romobile, motore, automobile i sl.), svaka vrsta vozila ima određeni broj primjeraka što čini vozni park u određenoj lokaciji. Svako vozilo ima sljedeće osobine: vrijeme punjenja prazne baterije (0%-100%), domet. Tvrtka ima više poslovnica (lokacija) na kojima korisnici/klijenti mogu unajmiti ili vratiti vozilo. Svaka lokacija ima inicijalni broj raspoloživih primjeraka vozila za pojedinu vrstu vozila (definirano u konfiguracijskoj datoteci). Broj raspoloživih primjeraka ne može biti veći od broja mjesta za punjenje te vrste vozila na lokaciji. Korisnik može imati samo jedan aktivni najam, odnosno dok korisnik ne vrati prvo vozilo ne može unajmiti drugo vozilo. Vozilo se može vratiti na bilo koju lokaciju ukoliko na toj lokaciji postoji slobodno mjesto za tu vrstu vozila.

Kod vraćanja vozila s aktivnog najma se preuzima ukupan broj prijeđenih kilometara za određeno vozilo te se izračunava potrošnja baterije na bazi prijeđenog broja kilometara i dometa vrste vozila (u km). Nakon vraćanja vozila potrebno mu je napuniti bateriju. Punjenje baterije provodi se linearno tako da se potrebno vrijeme punjenja baterije vozila izračunava na temelju trenutnog stanja baterije (u %) i vremena punjenja prazne baterije. Vozilo nije moguće unajmiti ako mu baterija nije u potpunosti puna.

Za svaku vrstu vozila postoji cjenik koji se temelji na najmu, broju sati najma i broju prijeđenih kilometara. Kod vraćanja vozila izračunava se trošak najma (najam, broj započetih sati najma, broj prijeđenih kilometara).

Svaka aktivnost (najam, vraćanje, provjera) polazi od virtualnog vremena. Virtualno vrijeme jedne aktivnosti mora biti veće od virtualnog vremena prethodne aktivnosti. Virtualno vrijeme ažurira se nakon izvođenja aktivnosti.

Konfiguracijske datoteke:
1. Vozila - popis vrsta vozila i njihove osobine
2. Lokacije - popis lokacija i njihove osobine
3. Lokacije_Kapaciteti - broj mjesta za pojedine vrste vozila i broj raspoloživih vrsta vozila po lokaciji
4. Cjenik - iznos najma, iznos po satu najma i po prijeđenom km po pojedinoj vrsti vozila
5. Osobe - popis osoba s njihovim osobinama
6. Aktivnosti - aktivnosti za skupni način rada. Aktivnosti koje su zapisane u datoteci se mogu koristiti i kod interaktivnog načina rada (manualnim upisom aktivnosti).


Aplikacija ima dva načina rada:
- Interaktivni način rada
- Skupni način rada

Interaktivni način rada podrazumijeva manualno upisivanje naredba od strane korisnika u aplikaciju, dok se u skupnom načinu rada aktivnosti koje želimo izvršiti učitavaju iz datoteke.

Detaljni opis faze dostupan je ovdje.

Tablica uzoraka:
<p align="center">
  <img width="800" height="500" src="https://user-images.githubusercontent.com/45578967/134831258-ceae0f67-6d45-4f6a-a317-7872cb00b050.png">
</p>

Dijagram klasa:
<p align="center">
  <img width="1000" height="500" src="https://user-images.githubusercontent.com/45578967/134831218-56ec7094-1b9c-4830-bba1-46ba42a6c0e6.png">
</p>

### Druga faza
Detaljni opis faze dostupan je ovdje.

Tablica uzoraka:
<p align="center">
  <img width="800" height="800" src="https://user-images.githubusercontent.com/45578967/134832445-7b992bee-6803-479b-bacd-68d923627282.png">
</p>

Dijagram klasa:
<p align="center">
  <img width="1000" height="600" src="https://user-images.githubusercontent.com/45578967/134832527-e0f7f755-8011-41fb-907d-5773d87def0d.png">
</p>

### Treća faza
Detaljni opis faze dostupan je ovdje.

Tablica uzoraka:
<p align="center">
  <img width="800" height="1000" src="https://user-images.githubusercontent.com/45578967/134832767-2df7e317-e763-47de-a679-b9ab6de16f43.png">
</p>

Dijagram klasa:
<p align="center">
  <img width="1000" height="600" src="https://user-images.githubusercontent.com/45578967/134832831-56ecee8a-e9ba-4aee-80f4-f0ed66cbb26b.png">
</p>
