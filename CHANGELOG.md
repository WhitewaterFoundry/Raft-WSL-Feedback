# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [25.07.1] - 2025-07-01

### Changed

* Improved startup time and overall application fluency, especially noticeable on lower-end PCs and ARM64 devices.

### Fixed

* Fixed PowerToys plugin installation so it works correctly across all systems.

### Added

* The PowerToys plugin is now available on ARM64 devices for the first time.
* Synchronized the plugin version with the supported PowerToys version.

## [25.06.1] - 2025-06-13

### Added

* Support for snapshots in **VHD format** for WSL2 distros when supported by the installed WSL version. This improves snapshot speed and allows larger distro backups.
* Support for **importing distros in VHD format** via the *Import from file* feature.
* Support for **Oracle Linux 9.5**, **Arch Linux**, **Fedora Linux 42**, **AlmaLinux OS 10**, and **AlmaLinux OS Kitten 10**.

### Changed

* Improved the snapshot creation process:

  * Now returns to the *Create Snapshot* dialog if an error occurs.
  * Displays a confirmation message when a snapshot is successfully created.
* Enhanced usability: the *Create Snapshot* dialog now warns immediately if the snapshot name is already in use.

### Fixed

* Fixed a **regression** that allowed creation of snapshots with **duplicate names**.
* Fixed a bug introduced in **WSL 2.5.x** where the *Import from file* progress dialog would not close after completion.

## [25.0.1] - 2025-01-04

### Added

* New option Export to file, allows to take a compressed snapshot of your distro, that can be imported later using the Import from file option.

### Changed

* Improved compatibility with the upcoming WSL version 2.4.8 and new architecture
* Detects when the WSL inbox version needs to be updated in Windows 11 24h2
* Improved the WSL installation on a clean install

### Fixed

* An issue that prevented in some cases to correctly detect the default distro

## [24.10.0] - 2024-10-28

### Changed

* Updated the AlmaLinux support and now correctly launches the new Windows Terminal profile.

### Fixed

* A regression that launched the default WSL distro on the commands Update and Open in File Explorer regardless the selected distro.

## [24.08.1] - 2024-08-11

### Added

* A new distro view, tailored for users that have only a few distros installed
* Support for launching WSL Settings if you have wsl version 2.3.11 or newer (still in preview)
* Support for Oracle Linux 9.4
* Support for Oracle Linux 8.9
* Support for Oracle Linux 8.10
* Support for openSUSE Leap 15.6
* Support for openSUSE Tumbleweed on ARM64
* Support for SUSE 15 SP6

### Changed

* Now Raft correctly launches the Windows Terminal profile for Ubuntu

## [24.04.6] - 2024-04-20

### Fixed

* A race condition that keeps the application from launching in some hardware configurations

### Added

* Support for Oracle Linux 9.3

### Changed

* Upgraded to .NET 8
* Improved a bit the launch time
* Added more distros to the generated Windows Terminal profiles

## [23.11.1] - 2023-11-01

### Fixed

* Crash at launch in localized versions of Windows (like Spanish)
* Fix an incompatibility with the latest version of PowerToys 0.75

### Added

* Support for dark theme in the PowerToys plugin

## [23.10.1] - 2023-10-22

### Added

* A warning will appear if Raft detects that the wsl command is behaving slowly.
* Support for Oracle Linux 9.2 and 8.8
* Support for openSUSE Leap 15.5
* Support for SUSE 15 SP5

### Changed

* Now you can move your backups using File Explorer, together with the backupdatabase.yaml; tell Raft the new location, and everything will be adjusted.
* Now, if you compress your .tar file using gzip, Raft will notice that and work with the compressed backup.
* Improved the logo for Kali Linux.
* Greatly improve responsiveness when wsl gets slow.
* Now, Raft calls the wsl engine fewer times to improve responsiveness and energy.

### Fixed

* There were some missing icons for PowerToys run

## [23.6.0] - 2023-06-26

### Fixed

* Improve responsiveness when wsl gets slow.

## [23.5.2] - 2023-06-04

### Fixed

* A regression when the WSL version shown in the toolbar was always 1 regardless the actual default version.

## [23.5.1] - 2023-05-29

### Added

* Support for Pengwin Enterprise 9

### Fixed

* Fix an issue when incorrectly was classifying custom RedHat distros as Fedora

## [23.4.0] - 2023-04-05

### Added

* Include AlmaLinux for ARM64

## [22.7.4] - 2022-07-25

### Added

* Import any distro from a TAR file
* Partial Arch Linux support
* Partial CBL Mariner support
* Support for AlmaLinux 9
* Support for openSUSE Leap 15.4
* Support for SUSE 15 SP4
* Support for Oracle Linux 8.6

### Changed

* Every distro that is Debian or Fedora based is recognized based on the IDLIKE field of os-release

### Deprecated

* Support for openSUSE Leap 15.3
* Support for SUSE 15 SP3
* Support for Oracle Linux 8.5

## [22.5.4] - 2022-05-15

### Added

* Support for Ubuntu (Preview)
* Support for AlmaLinux 8 WSL

### Changed

* Improved the layout to accommodate more distros with the minimal width of the window.
* Removed the descriptions of the distros; these can be seen in the Microsoft Store by double-clicking the distro icon.

## [22.5.1] - 2022-05-08

### Added

* Support for Ubuntu 22.04 LTS

### Changed

* Icons for Ubuntu and Ubuntu 20.04
* Improved the trial period not requiring payment method

### Fixed

* Windows Terminal icons for Oracle Linux

## [22.2.3] - 2022-02-27

### Changed

* PowerToys plugin now targets .NET 6

### Fixed

* The Raft icon in the PowerToys Settings now shows correctly

## [22.2.1]

* Improved Oracle Linux Support

## [22.2.0]

* Fix an incompatibility issue with PowerToys 0.55.0. Now the required version of PowerToys is >= 0.55.0
* Preliminary support for Oracle Linux

## [21.12.1]

* Improve performance reducing the redundant calls to the WSL API

## [21.11.12]

* Add errors occurred trying to install the PowerToys plugin to the Command Output Window
* Improved look and feel of Settings and Snapshot screens to align better to Windows 11 design
* Fixed a regression with PowerToys Plugin
* Fixed a crash when there are no distros installed
* Improve compatibility with "Windows Subsystem for Linux Preview - Microsoft Store Edition"

## [21.11.5]

* Redesigned to match the newest Microsoft styles. Looks great on Windows 11 and Windows 10
* NEW: Now, you can shut down the entire WSL by pressing a button. Helpful if you changed the .wslconfig file.
* NEW: Now you can run a distro as root
* Allow selecting the default distro directly in the toolbar
* When you install a distro, you'll see a small dialog box instead of the whole Microsoft Store window.
* The snapshots screen was redesigned to improve the usability
* Fixed an incompatibility with PowerToys 0.45+
* The distro context menu was reordered for better usability. Now the terminate distro action is more accessible.
* Added openSUSE Tumbleweed
* Added Pengwin Enterprise 8
* Improved Pengwin Enterprise and Fedora Remix logos, especially in with the dark theme.
* Fixed a crash on startup when there is no Internet connection
* Fixed a crash when WSL is not installed
