## Beginning - The terminal
The terminal is the first and last thing in linux. You don't really have to use it, but you aren't a penguin user if you don't. 

### What is a terminal?
A terminal is a program that lets you interact with your computer by typing commands instead of clicking. It’s a text-based control panel or the Command Line Interference (CLI). You don’t need to memorize everything—just a few core ideas and commands.

**Why use a CLI when we have GUIs?**  
- It’s direct and fast.  
- It’s scriptable and automatable.  
- It’s predictable and consistent across systems.  
- It’s ideal for remote work and servers.  
- It exposes powerful features without hunting through menus.

For more info see [this](https://dev.to/arthvhanesa/5-reasons-why-command-line-interface-cli-is-more-efficient-than-gui-mh2)

## Using the terminal.
Open it with:
- Ubuntu: Ctrl + Alt + T
- Most distros: Search “Terminal” in the app launcher.

A black window opens. That’s it. That’s the terminal.

### Installing Programs
Lets start with installing [vlc media player](https://www.videolan.org/). Type the following into the terminal and press `ENTER` to run.
</br>If you and copy-pasting you need to use `CTRL`+`SHIFT`+`V` to paste into the terminal and `CTRL`+`SHIFT`+`C` to copy **from** the terminal.

Debian/Ubuntu/Linux Mint
```
sudo apt install vlc
```
Fedora/RHEL 
```
sudo dnf install vlc
```
Arch/Manjora/EndaevourOS
```
sudo pacman -S vlc
```
it will ask you to type your password and verify installation by typing `y`. Don't be afaid when you see a lot of text. That's normal.


### Cheetsheet
```
pwd          # where am I?
ls           # list files
cd           # change directory
mkdir        # create folder
touch        # create file
cp           # copy
mv           # move/rename
rm           # remove/delete
sudo         # run as admin
apt install  # install software (Ubuntu)
nano         # edit files
```


