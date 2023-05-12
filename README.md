

# INSTRUCTIONS---HOW-TO-CONNECT-A-NEW-DEVICE (WINDOWS)
Hoe ik een nieuwe computer inricht voor gebruik met mijn GitHub account




Globals en SSH-key instellen
In onderstaande video wordt uitgelegd hoe je jouw Git globals (globale variabelen) kunt instellen en hoe je een SSH-key aanmaakt. Dit heb je nodig om jouw GitHub identiteit te koppelen aan jouw machine. Alle stappen (en commando's) in de video worden hieronder ook uitgelegd in tekst. Let op: als het installeren van Git nog niet gelukt is, kun je niet verder met de stappen in deze paragraaf. Vraag eerst om hulp bij een docent of SME'er.



https://vimeo.com/676188445/3acedd8c91?embedded=true&source=vimeo_logo&owner=48986772


## 1. Globals instellen
Log in op www.Github.com en check welk e-mailades en gebruikersnaam je voor dit account hebt gekozen. Stel dat onze GitHub gebruikersnaam pietpieters is en ons GitHub e-mailadres piet_pieters@gmail.com. Dan voeren we de volgende twee commando's in, in de terminal:

git config --global user.name "gerardheuvelman"

Druk nu op Enter. Er zal daarna niets gebeuren, je krijgt simpelweg een nieuwe regel te zien waarop je het volgende commando invoert:


git config --global user.email "gerardheuvelman@gmail.com"


Druk opnieuw op Enter. We krijgen wederom geen duidelijke bevestiging dat dit gelukt, of mislukt is. Dit controleren we daarom met het volgende commando:



git config --list


Je krijgt nu een lijst te zien. Blijf telkens opnieuw op Enter drukken, tot je aan het eind van de lijst bent en geen nieuwe variabelen meer te zien krijgt. Wees je ervan bewust dat je nu in een andere terminal-weergave zit. Als je zometeen weer commando's wil gaan invoeren, zul je uit deze weergave moeten stappen door het commando :q in te voeren en op Enter te drukken. Die q staat voor Quit. Als het goed is, heb je dit voorbij zien komen:



user.name=gerardheuvelman
user.email=gerardheuvelman@gmail.com


Stonden jouw gebruikersnaam en email-adres in de lijst? Dan is het gelukt! Je kunt nu verder met stap 2: SSH-key aanmaken.

Zie je géén gebruikersnaam of e-mailadres, of slechts één van de twee? Herhaal alle commando's in deze paragraaf dan, net zo lang tot de juiste informatie in de lijst staat.



## 2. SSH-key aanmaken en koppelen
Nu kunnen we een SSH-key aanmaken. Een SSH-key bestaat altijd uit twee delen: een public key en een private key. De private key staat op ons besturingssysteem en delen we met niemand. De public-key geven we door aan GitHub, zodat we niet bij elke data-uitwisseling hoeven te bewijzen wie we zijn (door gebruikersnamen en wachtwoorden in te voeren).



Open jouw IDE naar keuze. Open de terminal en maak een nieuwe SSH-key aan door het volgende commando in te voeren:



ssh-keygen -t ed25519


Druk vervolgens op Enter. Kijk goed naar de melding in de terminal. Hier hoort nu: "Generating public/private ed25519 keypair" te staan. Indien dit niet zo is, heb je een spelfout gemaakt en zul je het opnieuw moeten proberen.

De terminal zal je nu de volgende vraag stellen: "Enter file in which to save the key:". De standaard locatie die wordt voorgesteld, is in jouw gebruikers-map op de C-schijf. Hier gaan we mee akkoord, dus drukken we op Enter.
Vervolgens wordt je gevraagd om een passphrase (een soort wachtwoord) te bedenken. Dit biedt uiteraard meer veiligheid, maar zorgt er ook voor dat je iedere keer als je iets met Git doet, om je wachtwoord wordt gevraagd. Voor de opleiding is dit niet zo handig, dus voeren we geen passphrase in. Je hoeft alleen op Enter te drukken.
Ten slotte wordt je gevraagd de (lege) passphrase te bevestigen: "Enter same passphrase again: ". Dus vullen we niets in en drukken we nogmaals op Enter. Je krijgt nu een soort kunstwerkje te zien:



Open nu Windows verkenner > C-schijf > Gebruikers en vervolgens de map met de gebruikersnaam van jouw besturingssysteem. Hier vind je een map genaamd .ssh. Open deze map.
Je zult hier twee bestanden in vinden, waarvan je het id_ed25519.pub bestand wil openen met Kladblok. Dit doe je door met de rechtermuisknop op het bestand te klikken > Openen met... > Meer Apps > Kladblok.
Kopieer de volledige inhoud van dit bestand.
Log in op www.GitHub.com en ga vervolgens naar de instellingen (Settings > SSH & GPG keys). Druk dan op de grote groene knop met "New SSH key" en plak jouw public key in het grote veld. Geef jouw key ook een naam die beschrijft welk apparaat deze key gebruikt, zoals "Pieters Asus laptop" of "Pieters Desktop".
Druk op de knop "Add SSH key". Vervolgens zul je de SSH key tussen jouw keys zien staan. Dan is het gelukt!



---



# Globals en SSH-key instellen (MAC)
In onderstaande video wordt uitgelegd hoe je jouw Git globals (globale variabelen) kunt instellen en hoe je een SSH-key aanmaakt. Dit heb je nodig om jouw GitHub identiteit te koppelen aan jouw machine. Alle stappen (en commando's) in de video worden hieronder ook uitgelegd in tekst. Let op: als het installeren van Git nog niet gelukt is, kun je niet verder met de stappen in deze paragraaf. Vraag eerst om hulp bij een docent of SME'er.


https://vimeo.com/677146300/85c5813506?embedded=true&source=vimeo_logo&owner=48986772


## 1. Globals instellen
Log in op www.Github.com en check welk e-mailades en gebruikersnaam je voor dit account hebt gekozen. Stel dat onze GitHub gebruikersnaam pietpieters is en ons GitHub e-mailadres piet_pieters@gmail.com. Dan voeren we de volgende twee commando's in, in de terminal:



git config --global user.name "gerardheuvelman"


Druk nu op Enter. Er zal daarna niets gebeuren, je krijgt simpelweg een nieuwe regel te zien waarop je het volgende commando invoert:



git config --global user.email "gerardheuvelman@gmail.com"


Druk opnieuw op Enter. We krijgen wederom geen duidelijke bevestiging dat dit gelukt, of mislukt is. Dit controleren we daarom met het volgende commando:



git config --list


Je krijgt nu een lijst te zien. Blijf telkens opnieuw op Enter drukken, tot je aan het eind van de lijst bent en geen nieuwe variabelen meer te zien krijgt. Wees je ervan bewust dat je nu in een andere terminal-weergave zit. Als je zometeen weer commando's wil gaan invoeren, zul je uit deze weergave moeten stappen door het commando :q in te voeren en op Enter te drukken. Die q staat voor Quit. Als het goed is, heb je dit voorbij zien komen:



user.name=gerardheuvelman
user.email=gerardheuvelman@gmail.com

Stonden jouw gebruikersnaam en email-adres in de lijst? Dan is het gelukt! Je kunt nu verder met stap 2: SSH-key aanmaken.


Zie je géén gebruikersnaam of e-mailadres, of slechts één van de twee? Herhaal alle commando's in deze paragraaf dan, net zo lang tot de juiste informatie in de lijst staat.


## 2. SSH-key aanmaken en koppelen
Nu kunnen we een SSH-key aanmaken. Een SSH-key bestaat altijd uit twee delen: een public key en een private key. De private key staat op ons besturingssysteem en delen we met niemand. De public-key geven we door aan GitHub, zodat we niet bij elke data-uitwisseling hoeven te bewijzen wie we zijn (door gebruikersnamen en wachtwoorden in te voeren).



Open jouw IDE naar keuze. Open de terminal en maak een nieuwe SSH-key aan door het volgende commando in te voeren:



ssh-keygen -t ed25519


Druk vervolgens op Enter. Kijk goed naar de melding in de terminal. Hier hoort nu: "Generating public/private ed25519 keypair" te staan. Indien dit niet zo is, heb je een spelfout gemaakt en zul je het opnieuw moeten proberen.

De terminal zal je nu de volgende vraag stellen: "Enter file in which to save the key:". De standaard locatie die wordt voorgesteld, is in jouw gebruikers-map op de C-schijf. Hier gaan we mee akkoord, dus drukken we op Enter.
Vervolgens wordt je gevraagd om een passphrase (een soort wachtwoord) te bedenken. Dit biedt uiteraard meer veiligheid, maar zorgt er ook voor dat je iedere keer als je iets met Git doet, om je wachtwoord wordt gevraagd. Voor de opleiding is dit niet zo handig, dus voeren we geen passphrase in. Je hoeft alleen op Enter te drukken.
Ten slotte wordt je gevraagd de (lege) passphrase te bevestigen: "Enter same passphrase again: ". Dus vullen we niets in en drukken we nogmaals op Enter. Je krijgt nu een soort kunstwerkje te zien:



We kopiëren de public key door het volgende commando in te voeren:
pbcopy < ~/.ssh/id_ed25519.pub


Log in op www.GitHub.com en ga vervolgens naar de instellingen (Settings > SSH & GPG keys). Druk dan op de grote groene knop met "New SSH key" en plak jouw public key in het grote veld. Geef jouw key ook een naam die beschrijft welk apparaat deze key gebruikt, zoals "Pieters iMac" of "Pieters MacBook Pro (M1)".
Druk op de knop "Add SSH key". Vervolgens zul je de SSH key tussen jouw keys zien staan. Dan is het gelukt!



