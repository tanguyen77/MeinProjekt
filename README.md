# Mein Projekt
Einrichten des GitHub-Repositorys "MeinProjekt":
- Auf www.github.com mit meinem Benutzerkonto angemeldet und ueber "+ New" ein neues leeres Repository mit dem Namen "MeinProjekt" erstellt (git@github.com:tanguyen77/MeinProjekt.git). -> siehe screenshot01

Schritte zum Erstellen eines SSH-Schluessels:
- Ich hatte bereits einen SSH-Schluessel, dennoch waren ein paar Schritte vor dem Klonen durchzufuehren: specify the location of my SSH-key using "ssh-add ~/.ssh/id_rsa/id_github -> see screenshot03

Schritte zum lokalen Klonen des Repositorys, zum Konfigurieren von Git und zum Erstellen der initialen Commits:
- lokales Klonen des Repositorys: git clone git@github.com:tanguyen77/MeinProjekt.git
- Wechseln zum entsprechenden Ordner und ueberpruefen der aktuellen Konfigurationen: cd MeinProjekt/, git config --global user.name, git config --global user.email
- Erstellung des initialen Commits: echo "" > main.py, git add main.py, git commit -m "Initialer Commit"
- siehe screenshot03

Schritte zum Erstellen des "feature"-Branches, zum Hinzufuegen einer neuen Datei zu diesem Branch und zum Commiten der durchgefuehrten Aenderungen:
- Erstellen des "feature"-Branches und Wechsel auf diesen Branch: git checkout -b feature
- Hinzufuegen der neuen Datei: mkdir -p utils, echo "" > utils/database.py
- Commiten der durchgefuehrten Aenderungen: git add utils/database.py, git commit -m "Neue Funktion hinzugefuegt"
- siehe screenshot04

Schritte zum Mergen des "feature"-Branches in den "master"-Branch und zum Beheben des dabei auftretenden Merge-Konflikts:
- Merge-Konflikt erzwingen: auf "feature"-Branch $ echo "print('Hello, world\!')" > main.py, git add main.py, git commit -m "Hauptdatei aktualisiert"; git checkout master, $ echo "print('Hello, this is a random line\!')" > main.py, git add main.py, git commit -m "Hauptdatei aktualisiert"
- Mergen des "feature"-Branches in den "master"-Branch: git merge feature
- Beheben des auftretenden Merge-Konflikts: nano main.py, Bearbeiten des Datei-Inhalts, git add main.py, git commit
- siehe screenshot04, screenshot05


