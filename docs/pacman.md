# Package Manager

A package manager is a software tool that automates installing, upgrading, configuring, and removing software packages (programs, libraries) on a computer.


If you want the [wikipedia description](https://en.wikipedia.org/wiki/Package_manager)
</br>

> A package manager or package management system (PMS) is a collection of software tools that automates the process of installing, upgrading, configuring, and removing computer programs for a computer in a consistent manner. </br> package manager deals with packages, distributions of software and data in archive files. Packages contain metadata, such as the software's name, description of its purpose, version number, vendor, checksum (usually a cryptographic hash function), and a list of dependencies necessary for the software to run properly. Upon installation, metadata is stored in a local package database. Package managers typically maintain a database of software dependencies and version information to prevent software mismatches and missing prerequisites. They work closely with software repositories, binary repository managers, and app stores. </br> Package managers are designed to eliminate the need for manual installs and updates. This can be particularly useful for large enterprises whose operating systems (OSes) typically consist of hundreds or even tens of thousands of distinct packages.

## What package manager

What package manager you use depends on your distro

- `apt`/`dpkg` on Debian/Ubuntu. (Includes Kali, Linux_Mint, Pop_OS, Zorin_OS)
- `dnf`/`rpm` on RHEL/Fedora
- `zypper` on openSUSE
- `pacman` on Arch (Includes EndaevourOS, Manjora)

To see full guide on individual package manager (Optional)
```
man <package-manager>
# or
<package-manager> -h
<package-manager> --help
```

## Installing packages

Lets start with installing [vlc media player](https://www.videolan.org/). The following commands installs a specific package (vlc) and its dependencies

**Debian/Ubuntu**
```
sudo apt install vlc
```
**openSUSE**
```
zypper install vlc
```
**Fedora/RHEL** 
```
sudo dnf install vlc
```
**Arch**
```
sudo pacman -S vlc
```

> [!NOTE]  
> `pacman -S` will reinstall package. Use `pacman -S --needed` if you dont want to reinstall if it is already installed. `apt install` will not reinstall packages. Use `apt install --reinstall` to reinstall packages.

Multiple packages can be installed using a single command
```
sudo apt install vlc firefox fcitx5 neofetch
```

## Removing packages

Removing software is just as straightforward as installing it.  
Each package manager has its own flag for uninstalling packages.  
Here’s how you remove **vlc**:

**Debian/Ubuntu**
```
sudo apt remove vlc
```
If you also want to remove configuration files left on the system:
```
sudo apt purge vlc
```
**openSUSE**
```
sudo zypper remove vlc
```
**Fedora/RHEL**
```
sudo dnf remove vlc
```
**Arch**
```
sudo pacman -R vlc
```
If you want to remove dependencies installed *only* for this package:  
```
sudo pacman -Rs vlc
```

## Updating packages

Package managers can update both individual packages and the entire system.

### Update package lists (when applicable)

Some distros require refreshing their lists of available software.

**Debian/Ubuntu**  
```
sudo apt update
```
**openSUSE**
```
sudo zypper refresh
```
**Fedora/RHEL**
```
sudo dnf check-update
```
**Arch** (this is done automatically when updating)  
No separate “refresh” step is needed; `pacman -Syu` handles it.

### Upgrade installed packages

**Debian/Ubuntu**
```
sudo apt upgrade
```
**Fedora/RHEL**
```
sudo dnf upgrade
```
**Arch**
```
sudo pacman -Syu
```

## Searching for packages

If you're not sure what the package is called, use the search feature.

**Debian/Ubuntu**
```
apt search <name>
```
**openSUSE**
```
zypper search <name>
```
**Fedora/RHEL**
```
dnf search <name>
```
**Arch**
```
pacman -Ss
```

## Viewing package information

To inspect a package before installing it:

**Debian/Ubuntu**
```
apt show <package>
```
**openSUSE**
```
zypper info <package>
```
**Fedora/RHEL**
```
dnf info <package>
```
**Arch**
```
pacman -Si <package>
```

This helps you verify version, description, dependencies, and repository source.

**Next [Optional](pacman2.md) or [Skip](DE.md)**