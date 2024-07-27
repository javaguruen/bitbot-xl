# Oppgave: Følge svart stripe

i bitbot-gruppen av blokker, under `Sensorer og styring` ligger blokk for å lese høyre og venstre linjesensor. Linjesensoren vil gi tilbake verdiene 0 (ingen svart linje) eller 1 (svart linje). En lys-indikator oppå skinnen vil lyse når svart linje detekteres.

Målet er å få bilen til å følge den svarte linjen hele veien rundt banen helt av seg selv ved å selv korrigere kursen sin når den merker at den er på vei til å kjøre ut av banen. Når venstre sensor er oppå den svarte linjen må bilen svinge litt til venstre for å få linjen midt under bilen igjen. Tilsvarende for høyre sensor. 

Kombinasjonen av hvor fort bilen kjører og hvor mye/kraftig den svinger når den treffer linjen vil avgjøre hvor raskt den kommer seg rundt banen. Det er også lurt å teste bilen begge veier rundt banen slik at programmet ikke bare virker på venstre-svinger.

