# flatpak - org.onlyoffice.desktopeditors

## Overview

ONLYOFFICE Desktop Editors is a free office suite that combines text,
spreadsheet and presentation editors allowing to create, view and edit
documents stored on your Windows/Linux PC or Mac without an Internet connection.
It is fully compatible with Office Open XML formats: .docx, .xlsx, .pptx.

**Important** Because of our release process and important check we perform - flatpak
package always released little bit after deb/rpm/exe packages.
And sometimes we skip major release if hotfix is coming

## Quick Setup

### Install via flathub.org

1. Install flatpak runtime on your system according to [instruction](https://flatpak.org/setup/)
2. Install application via

   ```shell script
   flatpak install flathub org.onlyoffice.desktopeditors
   ```

3. Rum the application

    ```shell script
   flatpak run org.onlyoffice.desktopeditors
   ```

### Build application manually

All steps tested on Ubuntu 18.04

1. Clone this repo:

   ```shell script
   git clone https://github.com/flathub/org.onlyoffice.desktopeditors
   cd org.onlyoffice.desktopeditors
   ```

2. Install `flatpak` and `flatpak-builder` according to [instruction](https://flatpak.org/setup/)

3. Install a runtime and the matching SDK

   ```shell script
   flatpak install flathub org.freedesktop.Platform//22.08 \
                   org.freedesktop.Sdk//22.08 \
                   io.atom.electron.BaseApp//20.08 \
                   org.electronjs.Electron2.BaseApp//22.08
   ```

4. Build and install the application

   ```shell script
   flatpak-builder build org.onlyoffice.desktopeditors.json --force-clean --install
   ```

5. Run the application

   ```shell script
   flatpak run org.onlyoffice.desktopeditors
   ```
