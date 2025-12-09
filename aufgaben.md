# Git-Einführung - Übungen


## Lokales Repo

In diesem Git-Übungsprojekt wirst du mehrere Dateien erstellen und
Änderungen committen.

Öffne zuerst `personal.md` und trage deine Daten ein (Name,
Abteilung, Position), speichere die Datei und committe mit 

```bash
git add personal.md 
```


```bash
git commit -m "Add personal information of ...".
```


Erstelle anschließend `projekt.md` mit Angaben zu Projektname,
Projektbeschreibung, Start- und Enddatum und committe die Datei mit

```bash
git add projekt.md

git commit -m "Add project information"
```

Öffne dann `beschreibung.md` und ergänze den Absatz über
Herausforderungen und committe ebenso

Anschließend kannst du mit 

```bash
git log
```

alle Commits anzeigen lassen und Änderungen zwischen zwei Commits mit

```
git diff <Commit1> <Commit2>
```
 
sehen.
