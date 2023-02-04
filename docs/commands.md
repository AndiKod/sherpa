# --- sh:erpa s commands --- #

Just quick reminders, will be more info elsewhere.

Nav:   jklm OR arrows
Quit:  press q 

---

### Project
load projectName     source the paths to active project  

### Todos
       undone todos listed on s dashboard
lT     list all todos
cT n   complete todo line n 
aT n   activate todo line n  

### Bookmarks
lbm  list all Bookmarks
abm  add bookmark 

### Links
acme.com              opens in $defBrowser
http://acme.com/foo   idem

### Git
               brief Git Status on Dashboard
toGit "msg"    push to origin, with msg (or default if absent)  
fromGit        pull from the repo 
gitStatus      well, the repo's full Status

### Files
newFile               verbose prompt from template 
nF template file      sweet'n'short
to/file              open in $EDITOR
to/file +            open in alt EDITOR 
to/file "string"     write to the file
to/file $note        write multiline msg
c to/file            file preview (cat)
la                   ls .hiden files  
ll                   ls with details 
serve                 launch the /md files as website in Browser

### Folders
newDir                create new Dir from $defSrc
/to/dir               open Dir in $defExplorer
/to/dir +             open Dir in alt $Explorer
rename old new        rename Folder or File   

### Going Places
root     navigate to $defRoot
src      navigate to defSrc (rename defDirectory)
content  navigate to the md folder
dotDir   bavigate to the dot folder
sherpa   navigate to the sherpa folder

### Quick edits
config         open bin/s in Vim
