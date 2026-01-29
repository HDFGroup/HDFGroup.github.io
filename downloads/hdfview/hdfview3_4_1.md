---
title: HDFView 3.4.1
---

<img alt="HDFView Logo" align=right width=300 src="/assets/img/hdfview.png">

# HDFView 3.4.1

## Release Information

| Version | HDFView 3.4.1 |
| Release Date | ![GitHub release (latest by date)](https://img.shields.io/github/v/release/HDFGroup/HDFView?label=HDFView&color=white) | ![GitHub Release Date](https://img.shields.io/github/release-date/HDFGroup/HDFView?label=&color=white) |
| Additional Release Information | [CHANGELOG](https://github.com/HDFGroup/hdfview/blob/release/hdfview-3.4.1/docs/UsersGuide/CHANGELOG.md) |
| | [Release Announcement](https://www.hdfgroup.org/2026/01/30/release-of-hdfview-3-4-1-newsletter-208) |
| | [Known Problems](#known-problems-in-this-release) |

## Documentation

| File | Type |
| ---- | ---- |
| [UsersGuide.tar.gz](https://github.com/HDFGroup/hdfview/releases/download/v3.4.1/UsersGuide.tar.gz) | Documentation (HTML, Unix) |
| [UsersGuide.zip](https://github.com/HDFGroup/hdfview/releases/download/v3.4.1/UsersGuide.zip) | Documentation (HTML, Windows) |

## Download

HDFView 3.4.1 source and binaries are available [here](https://github.com/HDFGroup/hdfview/releases/tag/v3.4.1)

HDFView 3.4.1 was built and tested with HDF5-2.0.0, HDF 4.3.1, and openjdk 21. 

This release provides two ways to install the HDFView pre-built binary distribution for a platform:
* Using an application image. This method simply requires extracting the downloaded HDFView-3.4.1App\*.tar.gz or .zip file in the chosen install location.

* Running an installer. This method runs an installer (eg .exe) that sets up file associations and menu items.

Once you have uncompressed the downloaded pre-built binary file, refer to the provided README file for details.

See Known Problems if you encounter any issues.

## Known Problems In This Release

* **PATH pointing to other HDF4/5 installations**: If the environment path points to a directory including HDF4/5 installations, then these installations may be loaded by HDFView instead of the bundled HDF4/5 versions, causing the application to fail to launch with a "failed to launch JVM" error. This can be resolved by either removing those directories from the PATH, or removing the HDF4/5 installations from that directory.

* **Large Dataset Handling**: HDFView currently cannot nicely handle large datasets when using the default display mode, as the data is loaded in its entirety. To view large datasets, it is recommended to right click on a data object and use the "Open As" menu item, where a subset of data to view can be selected.

* **Object/Region References in Compound Types**: Object/region references can't be opened by a double-click or by right-clicking and choosing "Show As Table/Image" when inside a compound datatype.

* **Export Dataset in Read-Only Mode**: If a file is opened in read-only mode, right-clicking on a dataset in the tree view and choosing any of the options under the "Export Dataset" menu item will fail with a message of 'Unable to export dataset: Unable to open file'. The current workaround is to re-open the file in read/write mode.

* **Recent Files Button on Mac**: The 'Recent Files' button does not work on Mac due to a cross-platform issue with SWT.

* **PaletteView Selection**: Selecting and changing individual points in PaletteView for an image palette is broken.

* **Source Rebuild Requirements**: Logging and optional HDF4 requires rebuilds from source.

* **Mac File Display**: Automatically opening HDFView and displaying a file selected still does not display the file on a mac.
