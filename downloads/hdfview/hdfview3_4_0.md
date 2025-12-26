---
title: HDFView 3.4.0
---

<img alt="HDFView Logo" align=right width=300 src="/assets/img/hdfview.png">

# HDFView 3.4.0

## Release Information

| Version | HDFView 3.4.0 |
| Release Date | 12/31/2025 |
| Additional Release Information | [Release Notes](https://github.com/HDFGroup/hdfview/blob/v3.4.0/docs/RELEASE.txt) |
| | [Release Announcement](https://www.hdfgroup.org/) | 
| | [Known Problems](#known-problems-in-this-release) |

## Documentation

| File | Type |
| ---- | ---- |
| [UsersGuide.tar.gz](https://github.com/HDFGroup/hdfview/releases/download/v3.4.0/UsersGuide.tar.gz) | Documentation (HTML, Unix) |
| [UsersGuide.zip](https://github.com/HDFGroup/hdfview/releases/download/v3.4.0/UsersGuide.zip) | Documentation (HTML, Windows) |

## Download

HDFView 3.4.0 source and binaries are available [here](https://github.com/HDFGroup/hdfview/releases/tag/v3.4.0)

HDFView 3.4.0 was built and tested with HDF5-2.0.0, HDF 4.3.1, and openjdk 21. 

This release provides two ways to install the HDFView pre-built binary distribution for a platform:
* Using an application image. This method simply requires running the provided executable to obtain the software.
* Running an installer. This method runs an installer (eg .exe) that sets up file associations and menu items.

Once you have uncompressed the downloaded pre-built binary file, refer to the provided README file for details.

See Known Problems if you encounter any issues.

## Known Problems In This Release

* Workaround for issue with launching HDFView: A path issue which causes HDFView to fail to launch can be resolved by using the included batch script in the binary under the app folder.
* If installing HDFView with the installer method, please be aware that the installer does NOT overwrite "hardcoded" associations.  If there is a pre-existing user-defined file association, you must manually associate the extension with the HDFView application.

Please see the [Release Notes](https://github.com/HDFGroup/hdfview/blob/v3.4.0/docs/RELEASE.txt) for more information on known problems.
