# LaboReeks Git
## **Labo 2**

In ons tweede labo gaan we aan de slag met een **remote repository**.

We gaan hier zelf onze lokale repository aanmaken en de remote er manueel aan koppelen.
In de volgende labo's zullen we het onszelf mat makkelijker maken en simpelweg de remote repository *clonen* om een lokale gekoppelde repo te bekomen.

Je dient alle wijzigingen steeds te maken in je lokale repository (op je pc) en vervolgens via de nodige commando's ook in de remote repository (op GitHub) te brengen. 

#### **Aanvullende toets op Leho**
Na het afwerken van dit labo heb je op Leho een aanvullende toets met betrekking tot het labo en de leerstof gekoppeld aan het labo.
Je kan/mag de aanvullende toets steeds afleggen gebruik makend van alle bronnen (cursusmateriaal, labo, online bronnen, ...).

### **Deel 1: Lokale repo aanmaken en linken met de remote repo**

- [ ] Open de Git Bash Console op de locatie waar je dit labo wil gaan uitwerken.
      Dit kan via een rechtermuisklik op de locatie in kwestie en vervolgens de keuze **Git Bash Here** te selecteren.
>**Tip!** Indien deze optie niet beschikbaar is dan heb je een stap in de aanbevolen installatie van git overgeslaan.

- [ ] Gebruik het gepaste git commando om lokaal een folder **labo2** aan te maken mét git versiebeheer.
>**Tip!** Controleer dat je lokale repo de naam **main** gebruikt voor de default branch (meer hierover later).
Indien je in je Git Bash prompt **master** ziet staan i.p.v. **main**, dan zal je in de problemen komen bij het koppelen van je lokale repo aan de remote.
Pas in dat geval je lokale configuratie aan met het commando `git config --global init.defaultBranch main` en herneem deze stap:
verwijder de map **labo2** en maak een nieuwe lokale repo met diezelfde naam, want de settings hebben geen effect op bestaande repos!

- [ ] Ga via de console (met het juiste commando) in de nieuw aangemaakte map **labo2** (je lokale repo).
>**Tip!** Controleer voor je verder werkt of je al dan niet in de juiste git repository zit! Je kan dit snel visueel vaststellen in je console.

- [ ] Ga na met een git commando dat er aan deze lokale repo nog **geen** remote gekoppeld is.
- [ ] Zorg er nu voor dat je eigen (**deze**) remote repository, die je van ons kreeg op GitHub, gekoppeld wordt aan je zelf aangemaakte lokale repo.
      Hiervoor gebruik je weer een gepast git commando. Kies als alias voor de remote de naam *origin*.
- [ ] Controleer nog eens of het koppelen gelukt is (met hetzelfde commando dat je hierboven reeds gebruikte om initieel na te gaan dat er nog geen remote gekoppeld was).

- [ ] Voer een git commando uit om te controleren dat je in je lokale git geschiedenis nog geen enkele commit hebt zitten.

- [ ] Zorg **voor** je verdere stappen onderneemt dat je nu eerst je lokale git repository gaat updaten met de huidige inhoud van deze remote GitHub repository. Gebruik hiervoor het juiste git commando.

>**Tip!** Het is normaal dat je hier waarschijnlijk een melding zal krijgen dat je extra argumenten moet verschaffen bij het gebruikte commando, omdat de lokale en remote *main* branches nog niet aan elkaar gekoppeld zijn (meer over branches volgt in het volgende cursusdeel). Kijk goed naar de hints die je van git krijgt, en zoek uit hoe je de nodige extra argumenten kan meegeven. Indien je hier andere foutmeldingen of errors tegenkomt dan is er vermoedelijk iets foutgelopen in je lokale repository. Verwijder de folder waar je aan de slag bent en start even opnieuw, dat is de makkelijkste manier.

- [ ] Voer een git commando uit om te controleren dat je nu lokaal ook dezelfde commit(s) in de geschiedenis terugvindt als deze op je remote repo.

### **Deel 2: Gitignore**

- [ ] Maak een .gitignore bestand aan in de root van dit labo (lokaal).

- [ ] Zorg ervoor dat overheen de volledige git repository alle bestanden met extensie **tmp** niet opgenomen worden in git. Plaats de zin **temporary files are excluded** net boven de regel die je hiervoor gemaakt hebt, deze regel wordt als commentaar aanzien.

- [ ] Maak gebruik van passende git commando's om het .gitignore bestand te commiten naar je lokale repo.
>**Tip!** Denk aan de conventies rondom naamgeving van de commit messages!

- [ ] Voeg een regel toe aan de .gitignore die de folder **temp** zal gaan negeren. Plaats de zin **temporary folder is excluded** net boven de regel die je hiervoor gemaakt hebt, deze regel wordt als commentaar aanzien.
>**Tip!** Vergeet de wijzigingen niet op te slaan na je aanpassingen!

- [ ] Maak gebruik van passende git commando's om het .gitignore bestand te commiten naar git.
>**Tip!** Denk aan de conventies rondom naamgeving van de commit messages!

- [ ] Bekijk even de structuur van de reeds aanwezige **docs** folder.
Je zal zien dat deze o.a. vier subfolders bevat, elk verwijzend naar een fase (phase1, phase2, phase3 & phase4). 
Voeg eerst en vooral volgende regel commentaar toe in je .gitignore: **All phases except phase1 are ignored**.
Vervolgens voorzie je de nodige regels waardoor je alle bestanden in de map phase2, phase3 & phase4 zal negeren, maar deze in de map phase1 niet!

>**Tip!** Het is de bedoeling dat eventueel later toegevoegde mappen phase5, phase6, etc. **ook** genegeerd zullen worden door git.
Tracht dus efficient gebruik te maken van de .gitignore functionaliteit en niet door elke genegeerde phase folder op een afzonderlijke regel toe te voegen.

>**Tip!** Je zal hiervoor hoogstwaarschijnlijk 2 regels nodig hebben. Vergeet de wijzigingen niet op te slaan na je aanpassingen!

- [ ] Maak gebruik van passende git commando's om het .gitignore bestand te commiten naar git.
>**Tip!** Denk aan de conventies rondom naamgeving van de commit messages!

- [ ] Kopieer onderstaande lijst van commando's *(in 1 keer)*. Plak deze vervolgens in je console. Na uitvoeren zal deze blijven staan op de **git status** regel. Voer deze ook uit (enter).

```
clear
touch file01.tmp
touch file02.temp
touch docs/temp/garbage.txt
touch docs/temp/tmp.txt
touch docs/file01.tmp
touch docs/file01.temp
touch docs/phase1/file01.md
touch docs/phase1/phase1.md
touch docs/phase1/phase2.md
touch docs/phase1/phase3.md
touch docs/phase2/file01.md
touch docs/phase2/phase1.md
touch docs/phase2/phase2.md
touch docs/phase2/phase3.md
touch docs/phase3/file01.md
touch docs/phase3/phase1.md
touch docs/phase3/phase2.md
touch docs/phase3/phase3.md
touch docs/phase4/file01.md
touch docs/phase4/phase1.md
touch docs/phase4/phase2.md
touch docs/phase4/phase3.md
touch docs/phase1.md
touch docs/phase2.md
touch docs/phase3.md
clear
git status
```

- [ ] Controleer of de juiste bestanden (volgens de beschrijving hierboven) genegeerd worden door git.
      Gebruik hiervoor het gepaste git commando.
>**Tip!** Indien je merkt dat je gitignore regels niet correct zijn, pas deze dan verder aan tot je kan bevestigen dat (enkel) de juiste bestanden genegeerd worden! 

- [ ] Indien je het gitignore bestand nog verder hebt aangepast, zorg er dan voor dat deze aanpassingen opgenomen worden in je lokale git repo **zonder** dat de andere toegevoegde bestanden reeds opgenomen worden (deze moeten dus nog even in de working directory blijven staan).
  
- [ ] Synchroniseer je lokale git geschiedenis naar de remote repo, met het juiste git commando.
>**Tip!** Dit is de eerste keer dat we iets van de lokale repo naar de remote doorsturen. Je zal dus moeten opgeven dat we naar de **main** branch willen syncen. Zorg ervoor dat deze keuze **onthouden wordt**, m.a.w. dat de lokale en remote main branches aan elkaar gekoppeld worden, zodat we straks kunnen syncen zonder de remote branch nog te moeten specifiëren.

- [ ] Zorg er nu voor dat de andere toegevoegde bestanden opgenomen worden in je lokale git repo.
      Uiteraard gaat het dan enkel om deze die niet genegeerd worden door git wegens de gitignore-regels.

- [ ] Synchroniseer nogmaals naar de remote repo.
>**Tip!** Als je bij de vorige synchronisatie de link correct gelegd hebben naar de remote **main** branch, zou je die hier dus niet meer op hoeven te geven. Gebruik een zo kort mogelijk commando!

