# Installation

> [!CAUTION]
> Backup important files (Required) and use a seperate ssd/hdd for GNU/Linux installation

## Distro Choosing

**Youtube**
- [ExplainingComputers](https://www.youtube.com/watch?v=e2wB9r1SYrY)
- [NeuralNine](https://www.youtube.com/watch?v=gqsWwyiUaZI)

**Sites**
- [Distrochooser](https://distrochooser.de/) **<-- RECOMMENDED**
- [linuxnewbieguide.org](https://linuxnewbieguide.org/overview-of-chapters/chapter-3-choosing-a-linux-distribution/) <--Reading

## Installation

**Youtube**
- [Chris Titus Tech](https://www.youtube.com/watch?v=CJ41KZ0fBMc)
- [Micheal Horn](https://www.youtube.com/watch?v=_BoqSxHTTNs)

# Getting Familiar with the Desktop

> [!NOTE]
> I provided this section because some people say that linux feels unfamiliar

The desktop user interference **might** slightly/moderately vary depending on the [Desktop Environment](DE.md) and [Distribution](https://en.wikipedia.org/wiki/Linux_distribution), but almost all have a traditional desktop layout.


insert missing


# Software

## Packaging

| Type              | File Extension(s)     | Analogous in Windows        | Description |
|-------------------|-----------------------|-----------------------------|-------------|
| Installer Package | `.deb`, `.rpm`        | `.msi`, `.exe` (installer)  | Native Linux package formats used by package managers (APT, DNF, Zypper). Installed system-wide with dependency resolution. |
| Portable Archive  | `.tar.gz`, `.tar.xz`  | `.zip`, `.7z`               | Compressed archives containing prebuilt binaries or source code. Typically extracted and run manually, no automatic dependency handling. |
| AppImage          | `.AppImage`           | Portable `.exe`             | Self-contained executable that runs without installation. Includes most dependencies and can be run from any location. |
| Flatpak           | `.flatpak`, `.flatpakref` | Microsoft Store / MSIX | Sandbox-based application format. Distributes apps with bundled dependencies, supports permissions and system isolation. |
