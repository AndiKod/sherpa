# Les commandes "s " de sh:erpa 

Navig:   jklm OU flèches

Quiter:  appuyer sur q 

---

## Modifs Rapides

- config       : Ouvre bin/s dans Vim
- config-nano  : La même mais dans Nano
- bashrc       : Ouvre ~/.bashrc avec $defEditor     

## se Téléporter 

Change le répertoire actif du terminal vers:

- root     : $defRoot: La racine du projet (.git,...)
- src      : $defDirectory ou le dossier "src/"
- content  : La ou l'on garde les fichiers .md  
- dotDir   : ~/.config/sherpa avec Routes, Templates,...
- sherpa   : ~/sherpa avec les Docs, bin, etc ...

## Lister des choses

Affiche le contenu d'un dossier, sous forme d'arborescence

- l-root    : $defRoot, à la Racine du dossier principal
- l-md      : Nos fichiers de contenu, souvent en .md  
- l-sherpa  : Contenu du $sherpaDir (Docs, etc)
- l-dotDir  : Contenu du $dotDir (Templates, data, etc)  
- l-tpl     : Les Templates dans $dotDir/templates 
- l-docs    : Fichiers documentation dans $sherpaDir/docs
- l-data    : Les bases texte du $dotDir/data


## Routes

- routes                 Routes disponibles  
- route x                Editer la route x  
- takeRoute x            Activer la route x 
- newRoute               Créer une nouvelle route  
- rnRoute x y            Renommer une route 
- delRoute x             Effacer (delete) une route 


### Todos

- (juste s)   Liste des Todo encore à faire
- todo        Ajouter une Todo  
- lT          Lister toutes les Todos (faites ou pas)
- cT n        Compléter la Todo de la ligne n  
- aT n        reActiver la Todo de la ligne n  

### Bookmarks

- bm    Lister tous les Bookmarks
- nbm   Nouveau bookmark 

### Liens et Recherches

- acme.com              Le lien s'ouvre dans $defBrowser
- http://acme.com/foo   Idem
- ddg "Chatton mimi"    Cherche un chatton mimi, sur DuckDuckGo

### Git

- (juste s)      Bref résumé de l'état du dépot
- gitStatus      Le détail de ce qui a été modifié, ajouté,...
- sync           Sauvegarde (push) si besoin, sinon (pull)
- toGit "msg"    Sauvergarder vers Git avec un "msg"
- fromGit        Récupérer la version la plus récente

### Autour des Fichiers  

- newFile              Créer un fichier depuis un modèle (dynamic)
- nF template file     Pareil mais en une seule ligne  
- to/file              Depuis $defRoot, ouvre le fichier en édition
- to/file +            Menu pour choisir un EDITOR alternatif 
- to/file "string"     Ecrire dans un fichier, sans l'ouvrir
- to/file $note        Ecrire le contenu d'une variable
- c to/file            Apperçu d'un fichier, dans le terminal  
- la                   Lister les fichiers cachés, .files  
- ll                   Lister le contenu avec des détails

### Dossiers

- newDir                Créer un nouveau dossier (depuis root) 
- /to/dir               Ouvre le dossier dans $defExplorer
- /to/dir +             Ouvre le dossier dans l'$Explorer alt'
- rename old new        Renomme un dossier ou fichier (depuis root) 
### RSS

- rss    Ouvre Newsboat (à installer d'abord)
- af     Ajoute un flux RSS  
- ef     Editer le fichier des flux RSS disponibles  



