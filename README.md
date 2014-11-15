#Todo.txt add-on «Local»
	«Local» integration for todo.txt, which available you to create local todo lists.

## Setup
- [This article](https://github.com/ginatrapani/todo.txt-cli/wiki/Creating-and-Installing-Add-ons) in todo.txt repository helps you to start.
- If you want replace this command "blah-blah-blah/todo.sh local" to "tl" add to your `.bashrc` file this command `alias tl="blah-blah-blah/todo.sh local"`

## Usage

Imagine than you hava an alias for use usual `todo.sh` script, and use it as: `todo [arguments...]`. In this moment we are here: `/sites/onesite`, and it is a root directory for one of our sites.

#### Init
`todo local init` or `todo local i`  
If you want to create todo list just for this site, and with `todo.txt` file in there, just exec command above. In result we have:

- Folder for todo created: `/sites/onesite/todo`
- Config file added: `/sites/onesite/todo/todo.cfg`
- Todo file added: `/sites/onesite/todo/todo.txt`

#### Run command
`todo local [arguments...]`  
All actions what can send in usual todo.sh you can send in local todo list. For example, we can add a todo so: `todo local add "Just do this"`. We can list our local todos: `todo local list`, and what we want to do we can do with our local todo. :)

**Intresting:** if we go to the folder `/sites/onesite/js`, and then want to add a todo, we don't need to init local todo again. Just run command like this `todo local add "Fix some scripts"`, and todo will added into `/sites/onesite/todo/todo.txt`. No metter how deep you in the files tree, when you invoke to `todo local` it always find config file up in tree.

#### Destroy
`todo local destroy` or `todo local de`  
Remove local todo folder.

#### Reset
`todo local reset` or `todo local re`  
Remove and create again todo.cfg file if something went wrong with it.

#### Path
`todo local path` or `todo local pa`  
Show path to local todo.txt file.
