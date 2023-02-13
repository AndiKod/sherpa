# sh:erpa s commands

Nav:   jklm OR arrows

Quit:  press q 

---

## Quick edits

- config  : Open bin/s in Vim
- bashrc  : Open ~/.bashrc in $defEditor     

## Going Places

- root     : $defRoot: The main root folder (git,...)
- src      : $defDirectory (will be renamed) 
- content  : The .md actual content files 
- dotDir   : The one with Routes, Templates, Registers...
- sherpa   : $HOME/sherpa with Docs, default Templates, bin

## List Things

- l-root    : $defRoot folder content
- l-md      : Content files in $defContent
- l-sherpa  : $sherpaDir folder content
- l-dotDir  : $dotDir folder content  
- l-tpl     : Templates in $dotDir/templates 
- l-docs    : Available docs in $sherpaDir/docs
- l-data    : Content of $dotDir/data


## Routes

- routes                 List available routes  
- route x                Edit the x route  
- takeRoute x            Source the paths to activate route 
- newRoute               Create a new named routes  
- rnRoute x y            Renames the x route to y
- delRoute x             Delete the x route  


### Todos

- (just s)    Uncompleted todos listed on s dashboard
- todo        Add a new one 
- lT          List all todos
- cT n        Complete todo line n 
- aT n        Activate todo line n  

### Bookmarks

- bm    List all Bookmarks
- nbm   New bookmark 

### Links

- acme.com              Opens in $defBrowser
- http://acme.com/foo   Idem
- ddg "Cute kitten"     Search a "Cute kitten" on DuckDuckGo

### Git

- (just s)       Brief Git Status on Dashboard
- gitStatus      Well, the repo's full Status
- sync           Either push (if needed) or pull (just in case) 
- toGit "msg"    Push to origin, with msg (or default if absent)  
- fromGit        Pull from the repo 

### Files

- newFile              Verbose prompt from template 
- nF template file     Sweet'n'short
- to/file              Open in $EDITOR (while in $defRoot)
- to/file +            Menu with alt EDITORS 
- to/file "string"     Write/Append text to the file
- to/file $note        Write the content of note="lineA\nlineB"
- c to/file            File preview (less file)  
- la                   ls .hiden files  
- ll                   ls with details 

### Folders

- newDir                Create new Dir from $defSrc
- /to/dir               Open Dir in $defExplorer
- /to/dir +             Open Dir in alt $Explorer
- rename old new        Rename Folder or File   

### RSS

- rss    Open Newsboat (if installed)
- af     Add a new RSS feed
- ef     Edit feeds (opens the 'urls' file) 



