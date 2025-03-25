# BitBot XL-workshop

Velkommen til workshop med BitBit XL og micro:bit. Du skal programmere micro:bit-en til å styre bilen. Det er litt fritt program, men vi har laget to "oppgaver" som utgangspunkt for dagens workshop.

## 12:00 - 13:30 Workshop del 1

1. Det blir en kort introduksjon til editoren [makecode](https://makecode.microbit.org/), micro:bit og BitBit-en
1. Dere skal lage et enkelt program og overføre til micro:biten.
1. Dere starter på [oppgave 1](./Oppgave_svart-stripe.md) som er å få bilen til å bruke sensoren sin til å følge en svart linje.

## 13:30 - 14:15 Lunch


## 14:15 - 16.00 Workshop del 2

1. Jobbe videre med selvkjøringen. Det er forskjellige baner med økende vanskelighetsgrader.
1. Låne en microbit til og bruke den som fjernkontroll til å kjøre bilen 
1. Bruke avstandssensoren slik at den bremser eller står stille dersom noe står mindre enn 5 cm fra bilen.

# Komme i gang med microbit:
Bruk nettleser, helst Chrome. Editor er på adressen: https://makecode.microbit.org

1. Start et nytt prosjekt og gi det et navn. 
1. Klikk på tannhjulet oppe til høyre og sett riktig språk
1. I menyen av blokker, velg utvidelser og søk opp `bitbot`.
1. Du skal nå ha fått en egen gruppe med blokket under `bitbot`
1. Merk at ingen av blokkene under `BitBot PRO` kan brukes fordi de tilhører en annen bilmodell.

### Få bilen til å kjøre:
For å bruke riktig bilmodell, legg blokken `velg BitBot modell ..``Ved start` og velg `XL` i listen av tilgjengelige modeller.

For at ikke programmet skal starte med en gang bilen slås på, bruker vi blokken `Når knapp 'A' trykkes`. Til å begynne med skal du få filen til å kjøre framover med fart 30% i 2 sekunder (2000 millisekunder) og så svinge til høyre med fart 30% i 2 sekunder.

### Overføre program:
1. Koble til microbit-en
1. Trykk på de tre `...` til høyre for `Last ned`-knappen og velg `Connect device` og `neste`.
1. Trykk på `Pair`-knapp
1. I vinduet som kommer opp, velg 'bbc micro:bit' og knappen `connect`

Dette er for å sette opp en kobling mellom PC-en og microbit-en og trengs å gjøres bare første gang du kobler til en microbit. For å overføre programmet fra nettleseren til microbit-en, trenger du bare å trykke på knappen `Last ned`.

Når det gule lyset bakpå microbitten slutter å blinke, er programmet overført.

Sett microbiten i bilen, slå på bilen og trykk på 'A'-knappen.

### Ekstraoppgaver:
1. Klarer du å få bilen til å kjøre framover, svinge (ca) 90<sup>o</sup>?
2. Eksperimenter og finn ut hva som er forskjellen på blokkene `snu til høyre med x% i y millisekund` og `kjør venste motor framover med fart x%`. 


# Oppgave 1: Følge svart linje
Nå skal du programmere bilen til å følge en svart linje. I menyen av blokker, under `BitBot`ligger `Sensorer og styring`. Der er en blokk for venstre og høyre `Linjesensor`. Den blokken brukes inne i blokken for `Sammenligning` under `Logikk`. 

BitBit-en har to linjesensorer under, en på hver side. Målet er å starte å kjøre med den svarte stripen rett under bilen. Hvis høyre linjesensor blir `1`, betyr det at høyre side av bilen er oppå linjen. Du må da svinge litt til høyre for å få linjen midt under bilen igjen.

Utfordringen er å få bilden til å kjøre raskest mulig gjennom banen, men kjører du for fort kan du kjøre ut av banen. Du kan også justere på hvor mye du svinger når linjesensoren markerer at du er oppå linjen. Svinger du for lite havner du straks på linjen igjen og må svinge mange ganger, noe som tar tid.

Målet er å få bilen til å kjøre rundt hele den store banen. Øv gjerne på en av de mindre i starten inntil du begynner å få det til.

### Ekstraoppgave:
1. Klarer du å få bilen til å kjøre enda litt raskere og likevel holde seg på linjen?

# Oppgave 2: Avstandssensor
Bilen har også en avstandssensor. Den kan måle antall cm til et hinder foran seg. `Les ultralydsensor som cm` passer inn i sammenligningsblokken slik som linjesensoren. Kan du utvide programmet ditt slik at bilen stopper hvis noe er minder enn 5 cm fra den og kjører ellers?

# Oppgave 3: Fjernkontroll
For å løse denne oppgaven trenger du en microbit til. Under `Radio` er det en del blokker som kan brukes for å kommunisere mellom microbitene. En microbit står i bilen og mottar beskjed om å kjøre eller ikke, den andre microbiten holder du i hånden og styrer med.

Du må lage to programmer, ett til bilen og ett som er fjernkontroll. 

### Fjernkontrollen
Vi starter med fjernkontrollen:
Lage et nytt prosjekt som du kaller `fjernstyring-kontroll`
1. `Ved start` må du bruke blokken `radio sett gruppe x` hvor x er et tall du må velge selv og som ingen andre bruker samtidig. Husk å også sette hvilken modell av BitBit du bruker.
1. Send tekst-kommandoer til bilen når knappene trykke ved å bruke blokken `radio send tekst`. Bilen skal lese teksten som kommer og starte eller stoppe å kjøre avhengig av hvilken tekst som er mottatt.

```
Hvis `knapp A+B trykkes` så
   send tekst "begge"
ellers hvis `knapp A trykkes` så 
   send tekst "hoyre"
ellers hvis `knapp B trykkes` så 
   send tekst "venstre"
ellers hvis `logo er nedtrykket` så 
   send tekst "stopp"
```

### Mottaker i bilen
Lage et nytt prosjekt som du kaller `fjernstyring-bil`. Programmet skal reagere på kommandoene som den mottar. Svinge til venste gjøres ved å først bruke blokken `kjør venstre motor framover med fart 0%`og `kjør høyre motor framover med fart 30%`.

1. `Ved start` må du bruke blokken `radio sett gruppe x` hvor x det samme tallet som du brukte i fjernekontrollen. Husk å også sette hvilken modell av BitBit du bruker.
1. Bruk radio-blokken `når radio mottar receivedString`. `receivedString` er en variabel som inneholder kommandoen sendt fra fjernkontrollen og kan brukes i en sammenligningsblokk.

```
Hvis 'venstre' = receivedString så 
   sving venstre
ellers hvis 'hoyre' = receivedString så 
   sving høyre
ellers hvis 'begge' = receivedString så 
   kjør framover
ellers hvis 'stopp' = receivedString så
   brems 
```

Last programmene ned på hver sin microbit og kjør...

### Ekstraoppgaver:
1. Kan du også bruke lysene på armene til bilen? De kan f.eks. blinke blått som en politibil.
2. Du kan også legge på en sirene som om bilen har utrykning.