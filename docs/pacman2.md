## GUI frontend for package managers
 
1. [GNOME Software](https://gitlab.gnome.org/GNOME/gnome-software)
    - Works on: any distro using GNOME (Fedora, Ubuntu, Debian, openSUSE, Arch, etc.)
    - Supports: system packages (via PackageKit), Flatpak, Snap (with plugin)

2. [KDE Discover](https://github.com/KDE/discover)
    - Works on: any distro using KDE Plasma
    - Supports: system packages (via PackageKit), Flatpak, Snap, firmware updates (fwupd)

3. [Synaptic Package Manager](https://github.com/mvo5/synaptic)
    - Works on: any Debian-based distro (Ubuntu, Linux Mint, MX Linux), but is system-agnostic enough to run elsewhere if APT exists.
    - Backend: APT (.deb)

4. [Octopi](https://github.com/aarnt/octopi)
    - Works on: Arch-based distros
    - Backend: pacman (via libalpm)

5. [Pamac](https://github.com/manjaro/pamac)
    - Works on: Arch-based distros
    - Backend: pacman (via libpamac)

6. [Bauh](https://github.com/vinifmor/bauh)
    - Works on: Most distros
    - Supports: Flatpak, Snap, AppImage, AUR, WebApps

## Flatpak
[Flatpak](https://flatpak.org/) is a utility for software deployment and package management for Linux.

#### How it differs from Distro's package manager.
- Only Desktop Applications
- [Sandboxed Applications](https://en.wikipedia.org/wiki/Sandbox_(computer_security))
- Takes more space than Native Applications (the first few flatpak installations)

#### When you should use Flatpak.
- You want the latest version of an app, but you distro didn't update.
- You like trying new apps safely without risking your system.
- You don’t want to mess with [dependencies](https://www.reddit.com/r/learnprogramming/comments/15sq6o6/can_someone_help_explain_software_dependencies/)

#### When you might not need Flatpak
- If you prefer apps that fully integrate with your system
- If you have very limited disk space

[NEXT](DE.md)