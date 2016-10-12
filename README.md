# Rymdskeppet
Using Git
=========

## Scenario - Koll på repot! ##
```
#!bash
git status # Berättar hur ert repo ser ut. Vet ni inte vad ni skall skriva, skriva detta.
git log # Printar ut historiken/commiter i repot.
git diff # Visar icke commitade ändringar.
```


## Scenario - Göra en commit! ##
```
#!bash
git status # Visar vilka ändrade filer som kommer commitas.
git diff # Visar icke commitade ändringar.
git add # Lägg till filer ni vill commita. Skriv filerna en efter en eller . för att lägga till alla ändringar. 
git commit # Skapar en commit med ändringar.
git show # Visar senast commitade ändringar.
```
## Scenario - Lägga till i tidigare commit! ##
```
#!bash
git add
git commit --amend # Lägger till ändringar i senaste commit
```

## Scenario - Hämta ner! ##
```
#!bash
git stash # Lägger temporärt undan ändringarna
git pull
git stash pop # Tar fram de undanlagda ändringarna
```
## Scenario - Skicka upp! ##

```
#!bash
git status # Kontrollera att allt som skall commitas är commitat.
git add # Om ni inte har commitat allt, lägg till
git commit # Och commita
git log # Kontrollera att ert commit meddelande är korrekt.
git show # Kontrollera att koden ni commitat är fin och era kollegor kommer älska er.
git push
```
## Scenario - Lösa merge! ##


Såhär kan din typiska mergekonflikt i Java se ut:
```
#!java

    public Driver() {
<<<<<<< HEAD // This is your changes
        name = "Sven";
======= // This is their changes
        name = "name?";
>>>>>>> src-branch
    }
```
* Lös konflikterna
* Kör testerna
* Kör följande i git


```
#!bash

git add src/model/Driver.java # Lägger till filen som har haft en mergekonflikt för att indikera att den är löst
git commit # Säger till git att mergen är färdig
```
**OBS!** Kör inte ```git pull``` innan merge-ändringen är commitad.
