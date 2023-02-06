<p align="center" width="100%">
    <img width="25%" src="./sherpa.png">
</p>

# sh:erpa

### Personal Assistant from the shell

A tool for notes taking and daily activity, as I tried Notion and Obsidian but needed something simple, flexible and straight forward from the terminal ...so experimenting.

It's a personnal project and still in early days, but feel free to give it a try. It's always good to have a sh:erpa helping you to reach your higher goals faster and safer.  

---

## Install

Clone the program in the home folder: 

```bash
cd ~
git clone git@github.com:AndiKod/sherpa.git
```
Add that folder to the path by adding that line to **/home/username/.bashrc** : 

```bash
export PATH=$PATH:/home/username/sherpa/bin
```
Restart your terminal and press `s`. Welcome.

Edit defaults in ~/sherpa/bin/s  
`s config` will open that file with Vim
`s config-nano` the same but with Nano  

Plug sh:erpa into a content directory. The recommended way is to clone [Calepin](https://github.com/AndiKod/calepin), write plain markdown in md/ and view it in your browser as html with zero config. 

On the first run of `s`, sh:erpa creates the dot-files and store the default route as `~/.config/sherpa/routes/k1` pointing on $HOME/Documents as a placeholder.

Type `s route k1` to edit the content in Vim.

It can be virtually any folder, you can use sh:erpa with 11ty, astro, vue/svelte/react, whateverJS and serve to your browser (if needed).

```bash
# ~/.config/sherpa/routes/k1  

defRoot="/home/user/Documents"         # Where .git is
defDirectory="/home/user/Documents"    # Globally the /src folder
defContent="/home/user/Documents"      # The .md content folder 
```

Your personal sh:erpa is ready to help you managing documents.


### Defaults


Sherpa uses [Ranger](https://github.com/ranger/ranger) as default file explorer; be sure to have it installed. Vim is the default editor. It's a powerful combo, but you can configure it diferently if needed.

As main browser, I have Waterfox with Vim keybinds from [Vimium-FF](https://addons.mozilla.org/en-US/firefox/addon/vimium-ff). It synergize well together, as you can forget your mouse and experience a natural flow and privacy, without moving your hands away from the keyboard.

---

#### System specific defaults

sh:erpa check if he is called from Windows WSL and identify anyting else as Linux but it could be MacOS.

- To find a program in Linux, type `which program` and you'll get something like `/usr/bin/program`. You can use that in the config.

- For Windows, right click on the program's icon in the launcher > more > show in folder ...then on the shortcut r-click > settings and you'll find the path to the .exe


## sh:erpa Modules

Embracing the Unix phylosophy, sh:erpa use plain text files, does one simple taks at the time ...and is extensible. Below are the first modules to play around with and compose your own experience. Obviously, the FreeSoftware is prefered, but bring in whatever you like.

The quick list of available commands is in /docs/commands. Use the `?` s-command to read them in the terminal.  


### The s Dashboard

At any moment, press just `s` and get:

- An ASCII Art tile (maybe alternate ones later)
- Date, Hour, Greeting in random languages
- The list of your uncompleted Todos
- Status of tour Git repo, if you have work to save
- The author/name of the actual Git remote origin
- Your actual "climbing" Route paths (root, src, content) 

Sections of this screen could be customised in the future.
With simple bash commands, you could create your own widgets or "s commands", as I'm looking into ways to simplify the process.

### Quick Edits

- Edit bin/s with Vim or Nano to configure or tweak your sh:erpa 
- Edit .bashrc in the $defEditor
- Edit vimrc or nvim's init (next) 

### Going Places

Aliases changing the actual working directory, and "Go to:"  

- root: From where we use Git inside our project 
- src: If using sh:erpa with a JamStack framework, you got it
- content: Where all your actual .md content pages are 
- sherpa: The sherpa folder with the Templates, the Docs, bin/s
- dotDir: Config folder, data files, registers ...

New custom aliases could be soon added via the config file.

### List Things

- Short commands to list in tree form the content of:
root, content, sherpa, dotDir, templates, docs, data, registers 

### Routes

- Create new named route (sets of default paths)
- Edit the content or Rename/Remove the file  
- Take the route, set it as your active one 

### Todos

- Create
- Complete
- reActivate todos 
- Manage todo Lists
- *[Search, filter, ...with Unix tools]*

### Bookmarks

- Create
- List
- Tag 
- Open
- *[Search, filter, ...with Unix tools]*


### Files Operations
 
- Create files from Templates
- Write text into a file without opening it (quick notes) 
- Open file with chosen default editor or alternatives
- Read the content of a file, inside the terminal
- Open .md files in the Browser as .html with no config (Calepin)
- Preview file contents within Ranger file explorer
- *[Search, filter, manage files ...with Unix tools]*

### Handle URLs & WebSearch

- Open in browser anything starting with "http..."
- Open in Browser anyting ending in .com .org ...
- Search on DuckDuckGo from the terminal 

### Basic Git Operaitions 

- Auto status check on the "s dashboard"
- Full git status from anywhere
- Push all with `toGit "msg"` oneliner
- Pull with `fromGit` oneliner 


### Folders

- Create folders with $defRoot as starting point
- Rename folders. Works also with files, like `rename old new`
- *[Infos and manage ...with Unix tools]*


### RSS Reader

By default it looks for https://newsboat.org 

- Open the reader, refresh and happy reading
- Add a feed from the command line
- Launch the urls file in Vim & edit your feeds

### Help Pages

- The traditional --help flag, with English/French menu

### Version & Infos

- The other  -v or --version traditional flags


---



-Andrei- 
