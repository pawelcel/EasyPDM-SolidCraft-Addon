# Changelog

All notable changes to EasyPDM for SolidCraft are documented in this file. Version 0.9.0 was
released with EasyPDM itself; see the
[EasyPDM changelog](https://github.com/pawelcel/EasyPDM/blob/main/CHANGELOG.md#090) for it.

## [Unreleased]

## [0.9.1]

**In short:** Log in, Log out and Download work again in newer SolidCraft versions, which refused them with "permission denied: read entry may not use the host import write-file".

Update: unpack the new companion zip over the old one, run `easypdm-companion setup-solidcraft` again and reinstall the plugin it writes (Preferences > Plugins), granting the same `file` command group and `outbox` folder.

### Fixed
- **"permission denied: read entry may not use the host import write-file".** Log in, Log out and Download were declared as read-only entries, yet each leaves its request for the companion in the outbox folder. SolidCraft now refuses file writes to read-only entries, whatever folders the plugin was granted, so they failed before doing anything. They are now declared as edit entries, like Upload; they still change nothing in the design. ([EasyPDM #9](https://github.com/pawelcel/EasyPDM/issues/9))

## [0.9.0]

**In short:** the first release of EasyPDM for SolidCraft from its own repository: the same plugin and companion as attached to [EasyPDM 0.9.0](https://github.com/pawelcel/EasyPDM/releases/tag/v0.9.0), now released here. Upload, Download, Log in and Log out in SolidCraft's Plugins menu, assemblies of linked designs, transparent previews, signing in through the browser. Needs SolidCraft 0.43 or later and an EasyPDM 0.9 server.

![SolidCraft's Plugins menu and ribbon with EasyPDM's Upload, Download, Log in and Log out](https://raw.githubusercontent.com/wiki/pawelcel/EasyPDM/images/solidcraft-plugins-menu.png)

![SolidCraft Preferences → Plugins with the EasyPDM plugin installed and turned on](https://raw.githubusercontent.com/wiki/pawelcel/EasyPDM/images/solidcraft-plugin-installed.png)

**Install:** download the companion zip for your system below (`win-x64` or `linux-x64`); it holds the companion program and the plugin, with nothing else to install. Then follow [installing step by step](https://github.com/pawelcel/EasyPDM-SolidCraft-Addon/wiki/Installation) on the wiki: log in, set up the plugin, install it in SolidCraft, start the companion with your login.

### Changed
- **A repository of its own**, moved out of EasyPDM (`EasyPDM.SolidCraft/` became the top level and `plugin/`, `EasyPDM.Companion/` became `companion/`) with its history, released on its own as the FreeCAD and SolidWorks integrations are.
