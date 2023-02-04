<p align="center" width="100%">
    <img width="25%" src="./sherpa.png">
</p>

# sh:erpa

### Personal Assistant from the shell

A tool for notes taking and daily activity, as I tried Notion and Obsidian but needed something simple, flexible and straight forward from the terminal ...so experimenting.

It's a personnal project and still in early days, but feel free to give it a try. It's always good to have a sh:erpa helping you to reach your higher goals faster and safer.  

---

## Install


Clone the program itself: `cd ~` then `git clone git@github.com:AndiKod/sherpa.git`. It will create the /home/username/sherpa folder. 

Edit the `~/.bashrc` file and add that folder to the path `export PATH=$PATH:/home/username/sherpa/bin`. Restart your terminal and press `s`. Welcome.

Edit defaults in ~/sherpa/bin/s  
`s config` will open that file with Vim
`s config-nano` the same but with Nano  

Plug sh:erpa into a content directory. The recommended way is to clone [Calpin](https://github.com/AndiKod/calepin) ,write plain markdown and view it in your browser as html with zero config. 

It can be virtually any folder, you can use sh:erpa with 11ty, astro, vue/svelte/react, whatever use .md content and serve it to your browser (if needed).

If you cloned the Calepin in your Documents folder, you could have something like this:

```bash
# ~/sherpa/bin/s  

project="calepin"
```
Add the corresponding paths to the profile   

```bash
# ~/.config/sherpa/projects/calepin

defRoot="/home/user/Documents/calepin" 
defDirectory="/home/user/Documents/calepin"
defContent="/home/user/Documents/calepin/md"
```
If your sh:erpa is plugged into a JamStack static site generator, the defDirectory would point to something like the `/src` folder.

Your personal sh:erpa is ready to help you managing documents.


### Defaults


Sherpa uses [Ranger](https://github.com/ranger/ranger) as default file explorer; be sure to have it installed. Vim is the default editor. It's a powerful combo, but you can configure it diferently if needed.

As main browser, I have Waterfox with Vim keybinds from [Vimium-FF](https://addons.mozilla.org/en-US/firefox/addon/vimium-ff). It synergize well together, as you can forget your mouse and experience a natural flow and privacy, without moving your hands away from the keyboard.

---

#### System specific defaults

The script check if he is called from Windows WSL and identify anyting else as Linux but it could be MacOS version of Bash calling.

`s config` or `s config nano` will open ~/sherpa/bin/s in Vim or Nano, ready to customise paths to forders or programs.

- To find a program in Linux, type `which program` and you'll get something like `/usr/bin/program`. You can use that in the config.

- For Windows, right click on the program's icon in the launcher > more > show in folder ...then on the shortcut r-click > settings and you'll find the path to the .exe binary. Use that in the WSL part of the config.


## sh:erpa Modules

Embracing the Unix phylosophy, sh:erpa use plain files, does one simple taks at the time ...and is extensible. Below are the first modules to play around with and compose your own workflow. As much as possible, the FreeSoftware is prefered.

The quick list of available commands is in /docs/commands. Use the `?` s-command to read them in the terminal.  


### Projects

- Create porject profiles (sets of default paths)
- Set the default one in the config  
- Load project from the terminal to switch workspace  

### Todos

- Create
- Complete
- reActivate todos 
- Manage todo Lists
*[Search, filter, ...with Unix tools]*

### Bookmarks

- Create
- List
- Tag 
- Open
*[Search, filter, ...with Unix tools]*

### Direct Links

- Open in browser anything starting with "http..."
- Open in Browser anyting ending in .com .org ...

### Git  

- Auto status check on the "s dashboard"
- Full git status from anywhere
- Push all with `toGit "msg"` oneliner
- Pull with `fromGit` oneliner 

### Files 

- Create files from default or custom Templates
- Write text into a file without opening it (quick notes) 
- Open file with chosen default editor or alternatives
- Read the content of a file, inside the terminal
- Open .md files in the Browser as .html with zero config (Calpin)
- Preview file contents withing Ranger file explorer
- *[Search, filter, manage files ...with Unix tools]*

### Folders

- Create folders with $defRoot as starting point
- List content (from anywhere) normal, .hidden files, detailed
- Rename folders. Works also with files, like `rename old new`
- *[Infos and manage ...with Unix tools]*

### Going Places

Aliases changing the actual working directory, and "go to"  

- root: From where we use Git inside our project 
- src: If using sh:erpa with a JamStack framework, you got it
- content: Where all your actual .md content pages are 
- sherpa: The sherpa folder with the Templates, the Docs, bin/s
- dotDir: Config folder, data files, registers ...

### RSS Reader

By default it looks for https://newsboat.org 

- Open the reader, refresh and happy reading
- Add a feed from the command line
- Launch the urls file in Vim & edit your feeds

### Edit Stuff

- Open bin/s with Vim or Nano to configure or tweak your sh:erpa 

---



-Andrei- 
