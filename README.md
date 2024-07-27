# BitBot XL-workshop

## Forutsetninger
Før en kan jobbe med BitBot må en kjenne litt til editoren makecode og en bør ha litt kjenskap til 
- blokkene
- micro:bit
- overføring av program til micro:bit

### Editoren makecode

https://makecode.microbit.org/

* En kan risikere at noen av blokkene ikke er oversatt til norsk enda
* Man må legge til utvidelse for BitBot
  - Grå knapp `Utvidelser`
  - Søk på `bitbot`
  - Velg bitbot-utvidelsen
* I den nye gruppen med blokker `bitbot` kan vi ikke bruke noen av blokkene som står under `BitBot PRO` fordi vi har en BitBot XL.

### Micro:bit
Kidsa koder har en del oppgaver med micro:bit på sine sider: https://oppgaver.kidsakoder.no/microbit

Bør vise elementære blokker i editoren, særlig:
* Inndata
* Basis
* Løkker
* Sammenligninger

Overføring av program til micro:bit
* Pare micro:biten med maskinen for å overføre programmet direkte og ikke via filsystemet.


## Kjente problemstillinger
* På workshoper i Bergen klart ikke deltakerne med Chromebook å koble seg til hotellnettet
* Synking/overføring av program til micro:bit feilet for dem som brukte Safari på Mac, men løste seg hvis de byttet til chrome

## Best practices
* Slå av BitBot-en før du tar micro:biten ut, og sett micro:bit-en tilbake før du slår på igjen.
* Bruk en inndata-hendelse (f.eks. `Når knapp A trykkes`) slik at en unngår at bilen begynner å kjøre med en gang du slår den på.
* Det kan se ut som om dialogboksen for overføring fra editoren lukkes før programmet er helt overført til micro:biten. Vent til det gule lyset har sluttet å blinke med å ta ut USB-kabelen.

## Start med programmering av BitBot XL

Vi starter med å bli kjent med bilen, hvordan blokkene virker og hvordan bilen oppfører seg.
Se Oppgave_svinge-stoppe.md

# Utforming av bane
Det er mulig å lage baner med hvilken som helst utforming. Vi kan starte med en sirkel og ende med en bane som har svinger begge veier.

![width:200px](bane.jpg)

Dette forslaget til bane har 90°-svinger begge veier, en 180°-sving og en langside hvor det er mulig å kjøre

## Tape på hvitt papir
Har prøvd å bruke svart elektriker tape på papir klippet av en rull med hvit bordduk i papir. Erfaringen er at papiret vil krølle seg fordi tapen er elastisk og det er vanskelig å dra den ut og ned på papiret uten å strekke den for mye. Svingene er også en utfordring å få til uten å strekke tapen. Prøvde å krølle den og klippe spor på innsiden av svingen, men endte opp med å sette sammen svingene av små biter tape. Under prøvekjøring opplevde jeg at bilen kjørte av banen fordi det var mellomrom mellom tape-bitene etter å ha klippet dem i to for å rette ut det krøllete papiret.

## Tusj på hvitt papir
Etter forsøket med tape konkluderte jeg at å tegne banen med en bred, svart tusj på den hvite papirduken hadde vært et bedre alternativ. Husk i så fall at tusjen sannsynligvis trekker gjennom papiret og man derfor må ha noe under når man tegner.

## Tape rett på gulvet
Dersom du har et litt flatt, lyst gulv er det også mulig å tape rett på gulvet. Avhengig av overflaten på gulvet kan du oppleve at tapen løsner, særlig i svingene der det er mest spenn fordi tapen er strukket ut.