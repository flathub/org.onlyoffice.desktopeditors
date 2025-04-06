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

1. Install `flatpak` runtime on your system according to [instruction](https://flathub.org/setup)
2. Install application via

   ```shell script
   flatpak install flathub org.onlyoffice.desktopeditors
   ```

3. Rum the application

    ```shell script
   flatpak run org.onlyoffice.desktopeditors
   ```

### Build application manually

1. Clone this repo:

   ```shell script
   git clone https://github.com/flathub/org.onlyoffice.desktopeditors
   cd org.onlyoffice.desktopeditors
   ```

2. Install `flatpak` runtime on your system according to [instruction](https://flathub.org/setup)
3. Add the Flathub repo user-wide

   ```shell script
   flatpak remote-add --if-not-exists --user flathub https://dl.flathub.org/repo/flathub.flatpakrepo
   ```

4. Install `org.flatpak.Builder` according to [instruction](https://docs.flathub.org/docs/for-app-authors/submission#build-and-install)

   ```shell script
   flatpak install -y flathub org.flatpak.Builder
   ```

5. Build and install the application

   ```shell script
   flatpak run org.flatpak.Builder --force-clean --sandbox --user --install --install-deps-from=flathub --ccache --mirror-screenshots-url=https://dl.flathub.org/media/ --repo=repo builddir org.onlyoffice.desktopeditors.json
   ```

6. Run the application

   ```shell script
   flatpak run org.onlyoffice.desktopeditors
   ```
