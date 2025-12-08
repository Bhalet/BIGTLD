# Beginning - The terminal
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

# Using the terminal.
Open it with:
- Ubuntu: Ctrl + Alt + T
- Most distros: Search “Terminal” in the app launcher.

A black window opens. That’s it. That’s the terminal.

## Installing Programs
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

## The Interference
When you opened the terminal you saw some thing similar to this
```
[john@my-Lenovo-Laptop ~]$
```
- `john` is your username.
- `Lenovo-Laptop` is the name of you computer
- `~`is your current directory (location). *`~` stands for `/home/username`*.
- `$` indicates that the terminal is ready for interaction.

All comamand follow this pattern
```
$ [program/utility] [option/flag] [argument]
```
Don't worry if you dont understand. You will get used to it eventually.

## Managing files and folders (directories)
tutorial at [ubuntu](https://ubuntu.com/tutorials/command-line-for-beginners), [hostinger](https://www.hostinger.com/tutorials/linux-commands?) and [geekforgeeks](https://www.geeksforgeeks.org/linux-unix/basic-linux-commands/).
You only need to learn the following commands for now.


### Cheetsheet
```
pwd          # where am I?
ls           # list files
cd           # change directory
mkdir        # create folder
touch        # create file
cp           # copy
mv           # move/rename
echo         # repeat after me
cat          # What's in the file (text based only)
rm           # remove/delete
sudo         # run as admin
apt install  # install software (Ubuntu)
nano         # edit files
```

### Example usage.
Organising the Pictures in `~/Downloads/`
```
Downloads/
├─ program-1.0-2.tar.gz
├─ ramdom_video.mp4
├─ Ramdom-script.sh
├─ Waifu1_pose1.png
├─ Waifu2_pose1.jpeg
├─ Waifu1_pose2.jpg
├─ Waifu2_pose2.png
├─ pose3_waifu1.jpeg
```
1. **Go to `Downloads` folder**
```
cd ~/Downloads
```
2. **Make a list file to keep track of moved files**
```
touch ~/Documents/waifulist.txt
```
3. **Move images one file type at a time**
```
mv *.jpg ../Pictures/
ls ../Pictures/*.jpg >> ~/Documents/waifulist.txt

mv *.png ../Pictures/
ls ../Pictures/*.png >> ~/Documents/waifulist.txt

mv *.jpeg ../Pictures/
ls ../Pictures/*.jpeg >> ~/Documents/waifulist.txt
```
or **more Advance** and accurate
```
mv -v *{jpg,png,jpeg} ../Pictures >> ~/Documents/waifulist.txt
```
4. **Go to the Pictures folder**
```
cd ../Pictures
```
5. **Create folders for organization**
```
mkdir Waifu1
mkdir Waifu2

# or two in one command

mkdir Waifu1 Waifu2
```
6. **Move files into the appropriate folder**
```
mv -v ./*aifu1* ./Waifu1/
mv -v ./*aifu2* ./Waifu2/
```
7. **Open the list file to see what you moved**
```
nano ~/Documents/waifulist.txt
```
or print it into the terminal
```
cat ~/Documents/waifulist.txt
```

**Summary**  
If that felt like a lot, remember that it becomes quite easy and effiecient once you learn it
```
mv -v ~/Documents/*{jpg,png,jpeg} ../Pictures >> ~/Documents/waifulist.txt # move all images (including non-waifu)
cd ~/Pictures
mkdir ./Waifu1 ./Waifu2
mv -v ./*aifu1* ~./Waifu1/
mv -v ./*aifu2* ./Waifu2/
```


# Filesystem Hierarchy
I reccomend to learn the [Filesystem Hierarchy Standard](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard) from a ramdom Youtube video.


</br></br>
**NEXT [Optional](terminal2.md) or [Skip](pacman.md)**