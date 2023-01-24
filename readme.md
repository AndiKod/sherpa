<p align="center" width="100%">
    <img width="25%" src="./sherpa.png">
</p>

# sh:erpa

### Personal Assistant from the shell

A tool made to cover needs around managing/editing documents and daily activity, as I tried Notion and Obsidian but needed something more direct, flexible and straight forward ...so experimenting.

UNIX shell, via Bash, have everything you need to quickly create, manage and access information within documents. Sh:erpa is more or less a wrapper around existing CLI programs and tools ... with custom short commands. See them as building blocks for creating your own vibe. Just a starting point as for now.

It's a personnal project and still in early days, but feel free to give it a try. It's always good to have a sh:erpa helping you to reach your higher goals faster and safer.  

---

## Install


Clone the program itself: `cd ~` then `git clone git@github.com:AndiKod/sherpa.git`. It will create the /home/username/sherpa folder. 

Edit the `~/.bashrc` file and add that folder to the path `export PATH=$PATH:/home/username/sherpa/bin`. Restart your terminal.

Plug sh:erpa into a content directory. Here I use it inside an Astro project. It can be an empty folder or whatever. sh:erpa will just use those defaults. 
```bash
# in /home/user/sherpa/bin/s  

# --- Basic Config --- #

sherpaDir="/home/andrei/sherpa"  
dotDir="/home/andrei/.config/sherpa"
defRoot="/home/andrei/code/astro-sherpa"
defDirectory="/home/andrei/code/astro-sherpa/src/contents"
defImages="/home/andrei/code/astro-sherpa/public/assets"
defEditor="/usr/bin/vim"
```

You can now use short `s` commands and do things like: write text inside a file without even opening it, search something on DuckDuckGo and load it in your browser, push/pull to git from wherever you are, find lines with g/re/p, ...

Your personal sh:erpa is ready to help you managing documents.


### Defaults


Sherpa uses the wonderful [Ranger](https://github.com/ranger/ranger) as default file explorer; be sure to have it installed. Vim is the default editor. It's a powerful combo, but you can configure it diferently if needed.

As main browser, I have Firefox with Vim keybinds from [Vimium-FF](https://github.com/ranger/ranger) and [Bottom UI](https://github.com/ergenekonyigit/firefox-bottom-ui) visual theme. 

It synergize well together, as you can forget your mouse and experience a natural flow, without moving your hands away from the keyboard.

---

#### System specific defaults

Inside the `~/sherpa/bin/s` file: 

```bash  
# --- Linux defaults ---
defBrowser="firefox"
defEditor="vim"
defExplorer="ranger"
defExplorerBis="nautilus"

# --- Programs qualified paths ---
# cmd: $ which nautilus  output: /usr/bin/nautilus
Vim="/usr/bin/vim"
Ranger="/usr/bin/ranger"
Nautilus="/usr/bin/nautilus"
Sublime="/snap/bin/subl"
Nano="/usr/bin/nano"
ed="/usr/bin/ed"
neoVim="/usr/bin/nvim"

# Alternative programs [+] Options
editPlus=("Nano" "Sublime" "neoVim" "ed")
dirPlus=("Nautilus" "Sublime")
```

My WSL defaults:

```
# --- Windows Defaults --- #
defBrowser="/mnt/e/Programmes/FirefoxNightly/firefox.exe"
defEditor="/usr/bin/vim"
defExplorer="/usr/bin/ranger"

# --- Programs qualified paths ---
Vim="/usr/bin/vim"
Ranger="/usr/bin/ranger"
WinExplorer="/mnt/c/Windows/explorer.exe"
Sublime="/mnt/e/Programmes/Sublime3/subl.exe"
Nano="/bin/nano"
ed="/bin/ed"
neoVim="/usr/bin/nvim"

# Alternative programs [+] Options
editPlus=("Nano" "Sublime" "neoVim" "ed")
dirPlus=("WinExplorer" "Sublime")
```

To locate the .exe files, find a shortcut app icon, right click and check the path. Type the path in a WSL terminal to see if it works.

### Mac users

As bash can run from MacOS, as of now sh:erpa will identify the OS as Linux(detected as anything 'not Microsoft') , so you can tweak default paths there, and eventually the #!/bin/bash shebang, to make it fit your machine and programs.


## Commands

Quick list of available commands so far:
Type `s ?` to print them in the terminal 


Simply `s` with no arguments, will be a dashboard. For now just a greeting, the hour and if any, todos. Still thinking about what to display on it.


`s config`: Open the bin/s file in Vim to change the default routes, and plug sh:herpa in any directory we want. 
`s config-nano`: You guessed it, it's the same but with nano.

### Directories

- `s cd`: ChangeDirectory to $defDirectory. Useful to get auto-complete when typing files/dir names. 

- `s ls`: List your sherpa folder content from wherever you are

- `s la`: Same but showing also .hidden files 

- `s ll`: Same as ls but with permissions details and sizes

- `s (dirname|path)`: Will open the directory in the default explorer. Enter the name of a folder from your sherpa root like `s myFolder` or a full path like `s /home/whatever`

- `s (dirname|path) +`: Will show a menu with alternative progams to open the folder with. Default is Nautilus on Linux, and WindowsExplorer if installed in WSL, or SublimeText.

- `s newDir dirname`: Create the dirname forlder inside the main sherpa folder. A wraper around `mkdir` so you can `s newDir proj1/subFolder`. 

- `s rename dirname newDirname`: To rename a folder's name  


### Files

- `s ls`: Like *la* or *ll* will list available files in the root

- `s c file.ext`: Will display the content of the file in the terminal, to take a look at it. Like `s c todo.md` and see what's left. Can be set as alias in .bashrc with `alias todos="s c todos.md"`. Now you just type 'todos' for the same result.

- `s file.ext`: Will open the file in the default editor.

- `s file.ext +`: Will show a menu with alternative editors (also configurable). By default, it have Nano, Sublime, neoVim, ed.

- `s newFile file.ext`: Creates a file from the sherpa root. /sub/folder/file.ext will create it in the ~/Documents/sherpa/sub/folder directory.

- `s file.ext "Some text"`: Will write "Some text" at the end of the file.ext file without even opening it ;) Like `s todo.md "- [] Learn bash"`

- `s rename file.ext newfile.ext`: Well, it renames the file


### Web links Related

- `s https://domain.com/some/page`: Will open the page in the default browser (defaults to Firfox, but you can set yours). If the browser is opened, the page will load in a new tab.

- `s whatever.com`: Works the same. By default it checks if the string ends in .com .net .org .io, but can be extended.

- `s ddg "tiny kitten"`: Search for "tiny kitten" on DuckDuckGo and load the page in the default browser or a new tab of it.

### Git basics

- `s gitStatus`: Shows if something was modified

- `s toGit "Commit message"`: Will save (push) to the remote repo' all changed files, along with the message.

- `s fromGit`: The other way around. Updating from Git, if something was modified from elsewhere (like github in a mobile browser). 

You can stay up-to-date at home or "on the go" from your private git repository. Or sync between the desktop and the laptop, whatever you need.


### Locate lines of text with g/re/p 

- `s grep pattern file`: Will extract the lines conaining *pattern* from *file* or files (from the sherpa folder root) or any file with full path. The content is stored in a grep register ($dotDir/registers/grep.txt) and printed on screen from there.

- `s loc "something" todo.md`: do the same, it "locates" and print any line containing "something" in the todo.md file.

You can write notes in some notes.md file, and every now and then use `s notes.md "todo:: Do this thing asap."` to add it in that file and keep adding other things. `s loc "todo::" notes.md` will show all the todos from that file at once, wherever in the text they are. We can tag lines with whatever else, like link:: and retrive them. Endless creative solutions.



...to be updated, some commands are not yet documented here.

---

Insert contact, thanks, links, other stuff here.

-Andrei- 
