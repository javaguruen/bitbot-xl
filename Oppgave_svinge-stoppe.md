# Oppgave: Kjøre, svinge og stoppe
For å bli kjent med blokkene og bilen skal vi få den til å kjøre fram, svinger rundt et hinder, kjøre fram mot en vegg (eller mykt hinder) og stoppe foran den uten å krasje. Bilens sensor framover skal selv se når den nærmere seg veggen og stoppe 2-5 cm foran uten å kjøre inn i veggen.

<bilde av banen>

## Kjøring og svinging

BitBot har to blokker for å kjøre framover eller bakover:
- `kjør framover med fart X %` som kjører hele tiden i X % av maksfart
- `kjør framover med fart X % i Y millisekund`som kjører framover med X % av maksfarten, men stopper etter Y millisekund. 1000 millisekund er 1 sekund.
Begge disse blokkene kan brukes til å kjøre framover eller bakover avhengig av hva du velger i nedtrekkslisten.

Blokkene for `snu til ....` virker på samme måte som blokkene for å kjøre framover. De svinger enten hele tiden eller bare i det gitte antallet millisekunder.

For å stoppe bilen er det to valg:
- `stopp med bråstopp` lar bilen rulle til den stanser
- `stopp med brems` stopper bilen plutselig vha. elektronisk brems.

For å svinge er det en blokk `snu til venstre med fart X % i Y millisekunder`. Den svinger omtrent på stedet. Etter Y millisekunder står bilen stille.

BitBot har også mulighet for å kjøre med forskjellig fart på de to hjulene (eg. motoren til hjulene). Blokken `snu til venstre med fart X %` vil f.eks. sette farten til 0% på det venstre hjulet og X% på det høyre hjulet slik at den svinger på stedet. Når du bruker blokken `kjør framover med fart X%` settes lik fart på begge hjulene og den kjører rett fram. Med blokken `kjør venstre motor(er) framover med fart X%` kan du sette farten på kun ett av hjulene. Kombinasjonen `kjør venstre motor(er) framover med fart 30%` og `kjør høyre motor(er) framover med fart 60%` vil får bilen til å kjøre i en slak sving fordi høyre hjul kjører fortere enn venstre.


## Avstandsmåler
Ultralydsensoren vil måle framover og gi tilbake avstanden (i ønsket enhet) til nærmeste hindring. For å unngå å krasje inn i noe kan vi hele tiden måle avstand til nærmeste ting og stoppe bilen dersom avstanden er mindre enn f.eks. 5 cm.

Her skal du bruke blokkene:
- `gjenta for alltid` (Basis)
- `hvis` (Logikk)
- sammenligning av tall (Logikk)
- `les ultralydsenson som cm` (bitbot, Sensorer og styring)
- `stopp med bråstopp` (bitbot, Kjøring)