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
