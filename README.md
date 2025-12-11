# Git-Einführung

In diesem Projekt wirst du Git-Grundlagen üben: Dateien erstellen,
Änderungen nachverfolgen, Commits erstellen und kleine Konflikte
verstehen.

Arbeite Schritt für Schritt die Aufgaben durch.

## Vorarbeit

1. Installiere Git: https://git-scm.com
2. Installiere Sourcetree: https://www.sourcetreeapp.com
3. Erstelle dir einen Github-Account: https://github.com
4. Erstelle dir ein SSH-Schlüsselpaar (private und public Key) falls
   du nicht schon eins hast
   - https://docs.github.com/de/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
   - lade deinen public Key in deinen Github-Account hoch

## Übungen

### Lokales Repo (Repository): initialisieren

Öffne ein Terminal (Eingabeaufforderung) und navigiere zum
`git-einführung`-Ordner.

Tippe dann

```
git init
```

### Lokales Repo: Erste Commits

In diesem Git-Übungsprojekt wirst du mehrere Dateien erstellen und
Änderungen committen.

Zunächst aber schauen wir uns den aktuellen Stand an:

```bash
git status
```

Hier sollten nun die drei Dateien liegen, die noch nicht in Git
"registriert" sind. 

Fange mit `personal.md` an, öffne sie und trage deine Daten ein (Name,
Abteilung, Position), speichere die Datei und committe mit

```bash
git add personal.md 
```


```bash
git commit -m "Add personal information of ...".
```

- "Add": Füge das Folgende dem nächsten Commit hinzu
- "Commit": Erstelle einen Commit mit allen geaddeten Änderungen

Öffne dann `projekt.md`, ergänze den Absatz über Herausforderungen
und schaue dir jetzt den Status mit `git status` an. Die Minus- und
Pluszeilen zeigen die Veränderung von der alten Version zur jetzigen.
Das nennt man einen *"Diff"*. Adde und committe deine Änderungen.

Anschließend kannst du mit 

```bash
git log
```

alle Commits anzeigen lassen und Änderungen zwischen zwei Commits mit

```
git diff <Commit1> <Commit2>
```
 
sehen.

### Remote Repo: Push und Pull / Clone

#### Push

Bislang sind die Änderungen und Commits nur lokal. Um sie in der Cloud
(z. B. auf Github) zu sichern und auch das Arbeiten im Team zu
ermöglichen, müssen wir das Repo (bzw. die Änderungen/Commits) auf ein
remote Repository "pushen".

Noch weiß Git nicht, *wohin* das Repo geschoben werden soll, daher
führt ein einfaches Aufrufen von `git push` zu einer Fehlermeldung.

- Aufgabe 1:

  Erstelle in Github ein neues Repositorium. Kopiere die nötigen
  Schritte unter "…or push an existing repository from the command
  line" (`git remote add ...`) und füge sie in deinem Terminal aus.

Von nun an sollte ein einfaches `git push` genügen.

#### Clone

Wenn Du ein fremdes Repository bei dir lokal bearbeiten möchtest,
musst du es zunächst "klonen":

```bash
git clone git@github.com:kaaninho/git-intro.git
```

Jetzt kannst du darin Dinge ändern, Commits erstellen usw.

Ein Push geht nur, wenn die Besitzerin dies erlaubt.

Aufgabe: Lass dir von deiner Nachbarin den git-Link zu ihrem Repo
geben und klone das Repo. Schaue dir ihre bisherigen Commits an (`git
log`).

#### Pull

Um Änderungen (z. B. von Teamkolleg:innen) vom remote auf dein lokales
Repo zu ziehen, benutze `git pull`.

Aufgabe 1: Sage deiner Nachbarin, sie soll einen neuen Commit
erstellen und pushen. Hole dann zu deinem lokalen Repo die Änderungen
mit `git pull`. Schaue dann nach, ob die Änderungen nun auch bei dir
lokal vorhanden sind.

#### Push

Bitte deine Nachbarin, dich ihrem Team in Github hinzuzufügen, sodass
du auch pushen kannst (Settings -> Collaborators).

Ergänze bei ihr im `personal.md`-Dokument ihre E-Mail-Adresse,
committe und pushe das Ergebnis. Lasse sie wiederum die Änderungen
holen.

#### Merge - und Merge-Konflikte

ist leichter mit einer grafischen Oberfläche zu bearbeiten, daher:
Wechsel zu Sourcetree.

## Sourcetree

Sourcetree ist ein grafisches Programm, das einem Git-Handling erleichtert.

Hier kannst du committen, pushen, pullen, klonen, ohne ein Terminal
verwenden zu müssen. Zudem gibt es eine schöne *Graph-Ansicht* der
Commits/Historie und die Diffs sehen besser aus!

Schauen wir uns gemeinsam an.

### Merge

Nun ändert ihr gleichzeitig an derselben Datei etwas: Eine von euch
ändert die Abteilung, die andere ändert die Position. Nun committet
und pusht beide - bei einer wirds nicht klappen! (wieso?)

Die Zweite muss nun zuerst die neuesten Änderungen bei sich
integrieren (in Git sagt man dazu *"mergen"*). `git pull` macht das
automatisch für einen. danach sollte ein `git push` wieder
funktionieren.

#### Merge-Konflikte

Manche Änderungen kann Git nicht automatisch "reparieren" bzw. mergen.
Dann kommt es zu einem Merge-Konflikt. Das wollen wir jetzt ansehen:

Ändert wieder beide dieselbe Datei: Dieses Mal dieselbe Zeile (z. B.
den Namen), und versucht zu committen + pushen.

Behebt anschließend den Merge-Konflikt gemeinsam.
