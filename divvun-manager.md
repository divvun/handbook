# Package managers for end-users

## Overview

## Divvun Installer - "one-click" simplified installer

This tool is the main entry path for new users of the Divvun tools. The expected onboarding path is that the user:

- Navigates to divvun.org
- Selects to download Divvun Installer either for macOS or Windows
- Opens the downloaded application
- Selects their language from the provided dropdown list
- Clicks "Install"
- Closes the installer

This process should install the relevant keyboards and spellers for the given language, and enable the relevant items for the current user where possible.

Users can delete this installer once they're done -- it replaces a "setup.exe" or equivalent, much like the Firefox installer is just a miniature Firefox downloader.

### Microsoft Office handling

If Microsoft Office is detected, the user will be explained that the speller will be installed.

If it is detected but an incompatible version, the user will be informed that they need to upgrade MS Office for it to work.

If MS Office is detected but it is a new, and unknown version, the user will be prompted to send debug information to Divvun so that we can enable compatibility with that version.

If no MS Office is detected, the user will be informed that if they install MS Office in the future, that spellers will exist and they can use them.

## Divvun Manager - resident updater application and service



## Historical information

Divvun Manager was historically known as Divvun Installer until the release of the 2.x series. To simplify communication to users, a new "Divvun Installer" was created that is ofter referred to as the "one-click" installer, as this process radically simplifies the installation process for end-users, while not diminishing functionality for power users or sysadmins when using the Divvun Manager tooling.

Divvun Installer 1.x is no longer supported and any requests for assistance relating to this tool should be responded with requiring the user to upgrade to 2.x via the new Divvun Installer.