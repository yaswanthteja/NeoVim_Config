
# Prerequisites

- NEOVim ViA Chocolatey 

 - Vim-plug

- [NODE.JS](https://nodejs.org/en/download/)

- [Git](https://git-scm.com/downloads)


Open your powershell with Admin previliges and copy the commands and run on your power shell terminal


```
 Get-ExecutionPolicy

 Set-ExecutionPolicy AllSigned
 
 Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

 choco install neovim -y


```



- [Chocolatey](https://chocolatey.org/install)

Now add path to environment vriables 

The path to be added in the environment variables:

C:\ProgramData\chocolatey\

The path for configuration files
C:\Users\YourUsername\AppData\Local\nvim\init.vim

Create a  folder 'nvim' in this location

C:\Users\YourUser Name\AppData\Local\

Example: 

C:\Users\YourUserName\AppData\Local\nvim


## Vim Plugs

### Install Plugins 

Open your Powershell and run this command. try to run powershell with Admin Privileges 

### Run this in your power shell
```
iwr -useb https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim |`
    ni "$(@($env:XDG_DATA_HOME, $env:LOCALAPPDATA)[$null -eq $env:XDG_DATA_HOME])/nvim-data/site/autoload/plug.vim" -Force

```
Now open nvim folder you created earlier and create a file `init.vim` and Inside nvim create autoload folder and inside autoload folder create another folder plugged

or simply open your powershell 

navigate to the nvim folder by using "cd"command 
```
cd C:\Users\YourUserName\AppData\Local\nvim
```
Now type the command 


```
nvim init.vim
```
Now copy the code from [here](https://github.com/yaswanthteja/NeoVim_Config/blob/master/init.vim)
now press i in keyboard to be in   insert mode and paste that code here and click 'ESC' button and ':wq' button to save and exit the file 

Now create a folder called autoload and plugged

```
cd C:\Users\YourUserName\AppData\Local\nvim
mkdir autoload/plugged

```
If we Want to add Other plugins 

open `init.vim` file and do this 

## How to Add Plugins 
call plug#begin('C:\Users\YourUsername\AppData\Local\nvim\autoload\plugged')


Plug 'https://github.com/scrooloose/nerdtree'

call plug#end()


we need to add the Plugins Between call plug#begin and call plug#end.
After Plug  we need to place the ' link'


## Install autocomplete intellisense  and other plugins in neovim

if you clone my repository  in the nvim folder in this loction "C:\Users\YourUserName\AppData\Local\nvim"  

   YourUserName = username 

you just need to open your powershell and type  `nvim`

and nvim opens here 

now you need to type 
```
:PlugInstall
```
after installing the files you need to press ":q!"



- [COC github repository](https://github.com/neoclide/coc.nvim)

if you want to install some more plugins from COC
open nvim and follow

```
:CocInstall coc-pluginname
```
You can install multiple autocompletion plugins using coc by just looking up for them on the internet. Some of my favorites are:

coc-tabnine
coc-tsserver
coc-json
coc-tabnine
coc-python
coc-java


#  Install neovide

copy the commands and paste in your Terminal

```
Set-ExecutionPolicy RemoteSigned -scope Currentuser
iwr -useb get.scoop.sh | iex
scoop install git
scoop bucked add extras https://github.com/ScoopInstaller/Extras
scoop install neovide

```

[Nerd fonts website](https://nerdfonts.com/font-downloads)

This is the [configuration](https://github.com/hamiecod/dotfiles/blob/main/.config/nvim/init.vim) i've  reffered  to make this neovim 

















- [Themes](https://github.com/vim-airline/vim-airline/wiki/Screenshots)



- [Some Examples](https://github.com/artart222/CodeArt)
