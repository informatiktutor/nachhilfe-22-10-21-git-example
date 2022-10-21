```
git init  # Neues Repo im aktuellen Ordner erstellen

git status  # Aktuelle Änderungen anzeigen#

git add datei.txt  # datei.txt zum Commit vormerken
git add ordner/    # "ordner" zum Commit vormerken

git commit -m "Nachricht"  # Commiten

git log  # Vergangene commits ansehen

git remote add origin https://github.com/informatiktutor/nachhilfe-22-10-21-git-example.git

git push -u origin main
```

Statt dem HTTPS-Remote sollte ein SSH-Remote verwendet werden!

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account

U: Untracked  
A: ? (zum Commit vorgemerkt)  
M: Modified

Logs:

```
jonas@mustang:~/git$ ls -la
insgesamt 28
drwxr-xr-x 2 jonas jonas  4096 21. Okt 09:25 .
drwxr-xr-x 5 jonas jonas  4096 21. Okt 09:24 ..
-rw-r--r-- 1 jonas jonas 20352 21. Okt 09:26 api-result.json
jonas@mustang:~/git$ codium -n .
jonas@mustang:~/git$ git init
Hinweis: Als Name für den initialen Branch wurde 'master' benutzt. Dieser
Hinweis: Standard-Branchname kann sich ändern. Um den Namen des initialen Branches
Hinweis: zu konfigurieren, der in allen neuen Repositories verwendet werden soll und
Hinweis: um diese Warnung zu unterdrücken, führen Sie aus:
Hinweis: 
Hinweis:        git config --global init.defaultBranch <Name>
Hinweis: 
Hinweis: Häufig gewählte Namen statt 'master' sind 'main', 'trunk' und
Hinweis: 'development'. Der gerade erstellte Branch kann mit diesem Befehl
Hinweis: umbenannt werden:
Hinweis: 
Hinweis:        git branch -m <Name>
Leeres Git-Repository in /home/jonas/git/.git/ initialisiert
jonas@mustang:~/git$ git branch -m main
jonas@mustang:~/git$ git branch
jonas@mustang:~/git$ git log
fatal: Ihr aktueller Branch 'main' hat noch keine Commits.
jonas@mustang:~/git$ git status
Auf Branch main

Noch keine Commits

Unversionierte Dateien:
  (benutzen Sie "git add <Datei>...", um die Änderungen zum Commit vorzumerken)
        README.md
        api-result.json

nichts zum Commit vorgemerkt, aber es gibt unversionierte Dateien
(benutzen Sie "git add" zum Versionieren)
jonas@mustang:~/git$ git add README.md 
jonas@mustang:~/git$ git status
Auf Branch main

Noch keine Commits

Zum Commit vorgemerkte Änderungen:
  (benutzen Sie "git rm --cached <Datei>..." zum Entfernen aus der Staging-Area)
        neue Datei:     README.md

Unversionierte Dateien:
  (benutzen Sie "git add <Datei>...", um die Änderungen zum Commit vorzumerken)
        api-result.json

jonas@mustang:~/git$ git commit -m "Initial commit"
[main (Root-Commit) de2f177] Initial commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
jonas@mustang:~/git$ git status
Auf Branch main
Unversionierte Dateien:
  (benutzen Sie "git add <Datei>...", um die Änderungen zum Commit vorzumerken)
        api-result.json

nichts zum Commit vorgemerkt, aber es gibt unversionierte Dateien
(benutzen Sie "git add" zum Versionieren)
jonas@mustang:~/git$ git log
commit de2f177fcd941794c561715da98b796d2ee4190e (HEAD -> main)
Author: Jonas van den Berg <24623262+vonas@users.noreply.github.com>
Date:   Fri Oct 21 09:31:27 2022 +0200

    Initial commit
jonas@mustang:~/git$ git add README.md 
jonas@mustang:~/git$ git commit -m "Make changes"
[main 49d0548] Make changes
 1 file changed, 14 insertions(+)
jonas@mustang:~/git$ git add api-result.json 
jonas@mustang:~/git$ git commit -m "Day 1"
[main eff248a] Day 1
 1 file changed, 829 insertions(+)
 create mode 100644 api-result.json
jonas@mustang:~/git$ git add api-result.json 
jonas@mustang:~/git$ git commit -m "Day 2"
[main c2ffd98] Day 2
 1 file changed, 5 deletions(-)
jonas@mustang:~/git$ 

git commit -m "Nachricht"^C
jonas@mustang:~/git$ git remote add origin https://github.com/informatiktutor/nachhilfe-22-10-21-git-example.git
jonas@mustang:~/git$ git push -u ori^Cn main
jonas@mustang:~/git$ man git.push
Kein Handbucheintrag für git.push vorhanden
jonas@mustang:~/git$ man git
jonas@mustang:~/git$ man git-push
jonas@mustang:~/git$ ^C
jonas@mustang:~/git$ git push -u origin main^C
jonas@mustang:~/git$ git branch
* main
jonas@mustang:~/git$ git push -u origin main
Username for 'https://github.com': vonas
Password for 'https://vonas@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentifizierung fehlgeschlagen für 'https://github.com/informatiktutor/nachhilfe-22-10-21-git-example.git/'
jonas@mustang:~/git$ git push -u origin main
Username for 'https://github.com': vonas
Password for 'https://vonas@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentifizierung fehlgeschlagen für 'https://github.com/informatiktutor/nachhilfe-22-10-21-git-example.git/'
jonas@mustang:~/git$
```
