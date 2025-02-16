---
title: Software+Changes+from+Release+to+Release+for+HDF5+1.10
redirect from: 
  - display/HDF5/Software+Changes+from+Release+to+Release+for+HDF5+1.10
---

# Software Changes from Release to Release in HDF5 1.10

For a description of the major new features that were introduced, please see New Features in HDF5 Release 1.10.)

This page provides information on the changes that a maintenance developer needs to be aware of between successive releases of HDF5, such as:

* New or changed features or tools
* Syntax and behavioral changes in the existing application programming interface (API)
* Certain types of changes in configuration or build processes

Note that bug fixes and performance enhancements in the C library are automatically picked up by the C++, Fortran, and Java libraries.

The following information is included below.

* <a href="#compatibility">Compatibility and Performance Issues</a>
* <a href="#9versus8">Release 1.10.9 versus 1.10.8]</a>
* <a href="#8versus7">Release 1.10.8 versus 1.10.7</a>
* <a href="#7versus6">Release 1.10.7 versus 1.10.6</a>
* <a href="#6versus5">Release 1.10.6 versus 1.10.5</a>
* <a href="#5versus4">Release 1.10.5 versus 1.10.4, 1.10.3, and 1.10.2</a>
* <a href="#4versus3">Release 1.10.4 versus Release 1.10.3</a>
* <a href="#3versus2">Release 1.10.3 versus Release 1.10.2</a>
* <a href="#2versus1">Release 1.10.2 versus Release 1.10.1</a>
* <a href="#1versus0">Release 1.10.1 versus Release 1.10.0 (and 1.10.0-patch1)</a>
* <a href="#0versus8_16">Release 1.10.0 of March 2016 versus Release 1.8.16</a>

See [API Compatibility Reports for 1.10](/documentation/hdf5/latest/api-compat-macros.html) for information regarding compatibility with previous releases.

<h2 id="compatibility">Compatibility and Performance Issues</h2>

Not all HDF5-1.10 releases are compatible. Users should NOT be using 1.10 releases prior to HDF5-1.10.3. See the compatibility matrix below for details on compatibility between 1.10 releases:

| Release  | 1.10.5+ | 1.10.4 | 1.10.3 | 1.10.2 | 1.10.1 | 1.10.0-patch1 | 1.10.0 |
| -------- | ------- | ------ | ------ | ------ | ------ | ------------- | ------ |
| 1.10.5+ |         | Yes     | Yes     | No      | No      | No      | No
| 1.10.4  | Yes     |         | Yes     | No      | No      | No      | No
| 1.10.3  | Yes     | Yes     |         | No      | No      | No      | No
| 1.10.2  | No      | No      | No      |         | No      | No      | No

The following images show how performance has changed from release to release.

[cgns, HDF5 versions](images/cgns.png)

[writeLgNumDsets](images/writeLgNumDsets.png)

The release notes also list changes made to the library, but these notes tend to be more at a more detail-oriented level. The release notes may include new features, bugs fixed, supported configuration features, platforms on which the library has been tested, and known problems. The release note files are listed below and can be found at the top level of the HDF5 source code tree in the release\_docs directory.

|                               |                                                              |
| ----------------------------- | ------------------------------------------------------------ |
| **Release Notes**             | Technical notes regarding the current release of the HDF5 library (RELEASE.txt in the source code) |
| **HISTORY-1_10.txt**          | Release information for all HDF5-1.10 releases |
| **HISTORY-1_8_0-1_10_0.txt**  | Development history between the HDF5-1.8.0 and HDF5-1.10.0 releases |
| **HISTORY-1_8.txt**           | Release information for HDF5-1.8.0 through HDF5-1.8.21 releases |
| **HISTORY-1_0-1_8_0_rc3.txt** | Technical notes starting with HDF5-1.0.0 and ending with HDF5-1.8.0-rc3 (the state of the code prior to the HDF5-1.8.0 release) |

<h2 id="9versus8">Release 1.10.9 versus 1.10.8</h2>

### New and Changed Functions, Classes, Subroutines, Wrappers, and Macros
In the Java API


One Java wrapper was added:

H5.H5export\_dataset

### Compatibility Notes and Reports
See the [API compatibility report between 1.10.8 and 1.10.9]() for information regarding compatibility with the previous release.

<h2 id="8versus7">Release 1.10.8 versus 1.10.7</h2>

### New and Changed Functions, Classes, Subroutines, Wrappers, and Macros

#### In the C++ API

One C++ wrapper was added:
DataSet::operator=

### Compatibility Notes and Reports
See the [API compatibility report between 1.10.7 and 1.10.8]() for information regarding compatibility with the previous release.

<h2 id="7versus6">Release 1.10.7 versus 1.10.6</h2>

### New and Changed Functions, Classes, Subroutines, Wrappers, and Macros
#### In the C Interface (main library)

The following are new C functions in this release:

| Function                      | Description                                               |
| ----------------------------- | --------------------------------------------------------- |
| [H5Pget\_fapl\_splitter](/documentation/hdf5/latest/group___f_a_p_l.html#gaf6ac1c131acee33dfb878593dfefb4ac) | Retrieves information for a splitter file access property list    |
| [H5Pget\_fapl_splitter](/documentation/hdf5/latest/group___f_a_p_l.html#gaf6ac1c131acee33dfb878593dfefb4ac) | Retrieves information for a splitter file access property list    |
| [H5Pset\_fapl_splitter](/documentation/hdf5/latest/group___f_a_p_l.html#ga49f386ea235bb48128e54c962c499f07) | Sets the file access property list to use the splitter driver     |
| [H5Pget\_file_locking](/documentation/hdf5/latest/group___f_a_p_l.html#ga5de19a5a8ac23ca417aa2d49d708dc2d) | Gets the file locking property values |
| [H5Pset\_file_locking](/documentation/hdf5/latest/group___f_a_p_l.html#ga503e9ff6121a67cf53f8b67054ed9391) | Sets the file locking property values |
| [H5get\_free_list_sizes](/documentation/hdf5/latest/group___h5.html#ga2310d963a6f48ec12fda8c0c8bbefbbb) | Gets the current size of the free lists used to manage memory  |
| [H5Scombine_hyperslab](/documentation/hdf5/latest/group___h5_s.html#gae7578a93bb7b22989bcb737f26b60ad1) | Performs an operation on a hyperslab and an existing selection and returns the resulting selection |
| [H5Scombine_select](/documentation/hdf5/latest/group___h5_s.html#ga356600d12d3cf0db53cc27b212d75b08) | Combines two hyperslab selections with an operation, returning a dataspace with the resulting selection |
| [H5Smodify_select](/documentation/hdf5/latest/group___j_h5_s.html#ga814b2cb29fcdfe79892737f4337d0ef9) | Refines a hyperslab selection with an operation using a second hyperslab to modify it |
| [H5Sselect_adjust](/documentation/hdf5/latest/group___h5_s.html#ga64f08c187b899f2728d4ac016d44f890) | Adjusts a selection by subtracting an offset |
| [H5Sselect_copy](/documentation/hdf5/latest/group___h5_s.html#ga57e5eba2d1b282803835ba3f7e0b9bfa) | Copies a selection from one dataspace to another |
| [H5Sselect_intersect_block](/documentation/hdf5/latest/group___h5_s.html#ga51472bcb9af024675fba6294a6aefa5e) | Checks if current selection intersects with a block |
| [H5Sselect_project_intersection](/documentation/hdf5/latest/group___h5_s.html#ga1e914ba45afb15ded99a0afeaf124c04) | Projects the intersection of two source selections to a destination selection |
| [H5Sselect_shape_same](/documentation/hdf5/latest/group___h5_s.html#gafc6cafae877900ee060709eaa0b9b261) | Checks if two selections are the same shape |

#### In the C++ API

The following C++ wrappers were added:

| FileAccPropList::getFileLocking | See H5Pget\_FILE\_LOCKING for details |
| FileAccPropList::setFileLocking | See H5Pset\_FILE\_LOCKING for details |

### Compatibility Notes and Reports
See the [API compatibility report between 1.10.6 and 1.10.7](https://htmlpreview.github.io/?https://github.com/HDFGroup/hdf5doc/blob/master/html/ADGuide/Compatibility_Report/hdf5-1.10.7-interface_compatibility_report.html) for information regarding compatibility with the previous release.

<h2 id="6versus5">Release 1.10.6 versus 1.10.5</h2>

### New and Changed Functions, Classes, Subroutines, Wrappers, and Macros
#### In the C Interface (main library)

The following are new C functions in this release:

| Function              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [H5Pget\_fapl_hdfs](/documentation/hdf5/latest/group___f_a_p_l.html#gae59e7d8e0e8823e6dd6034b66418ed00) | Gets the information of the given Read-Only HDFS virtual file driver |
| [H5Pget\_fapl_ros3](/documentation/hdf5/latest/group___f_a_p_l.html#ga13e273711e160cbd58e60c701b4f50e6) | Gets the information of the given Read-Only S3 virtual file driver |
| [H5Pset\_fapl_hdfs](/documentation/hdf5/latest/group___f_a_p_l.html#ga970d077c8e712a4692f43fa4f38dde14) | Sets up Read-Only HDFS virtual file driver |
| [H5Pset\_fapl_ros3](/documentation/hdf5/latest/group___f_a_p_l.html#gaad28d8c24f236590193215c5ae7a8f18) | Sets up Read-Only S3 virtual file driver |
 
#### In the C++ API

The following C++ wrappers were added:

| Function              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| LinkCreatPropList::getCreateIntermediateGroup() const | See [H5Pget\_create_intermediate_group](/documentation/hdf5/latest/group___l_c_p_l.html#gaf7db1b7ce19703f30f1827b7c899c3b0) |
| LinkCreatPropList::setCreateIntermediateGroup(bool crt\_intmd\_group) const | See [H5Pset\_create_intermediate_group](/documentation/hdf5/latest/group___l_c_p_l.html#ga66c4c5d3f34e5cf65d00e47a5387383c) |

### Compatibility Notes and Reports
See the [API compatibility report between 1.10.5 and 1.10.6](https://htmlpreview.github.io/?https://github.com/HDFGroup/hdf5doc/blob/master/html/ADGuide/Compatibility_Report/hdf5-1.10.6-interface_compatibility_report.html) for information regarding compatibility with the previous release.

<h2 id="5versus4">Release 1.10.5 versus 1.10.4</h2>

### New and Changed Functions, Classes, Subroutines, Wrappers, and Macros
#### In the C Interface (main library)

The following are new C functions in this release:

| Function              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [H5Dget\_chunk_info](/documentation/hdf5/latest/group___h5_d.html#gaccff213d3e0765b86f66d08dd9959807) | Retrieves information about a chunk specified by the chunk index |
| [H5Dget\_chunk_info_by_coord](/documentation/hdf5/latest/group___h5_d.html#ga408a49c6ec59c5b65ce4c791f8d26cb0) | Retrieves information about a chunk specified by its coordinates |
| [H5Dget\_num_chunks](/documentation/hdf5/latest/group___h5_d.html#ga8e15897dcc5799d6c09806644b492d7a) | Retrieves number of chunks that have nonempty intersection with a specified selection |
| [H5Fget\_dset\_no_attrs_hint](/documentation/hdf5/latest/group___h5_f.html#gacbf3ba8b36750c42b49740567a9732c4) | Retrieves the setting for determining whether the specified file does or does not create minimized dataset object headers |
| [H5Fset\_dset\_no_attrs_hint](/documentation/hdf5/latest/group___h5_f.html#gafc0166070f920f037e6b1a5c66e5464c) |Sets the flag to create minimized dataset object headers |
| [H5Pget\_dset\_no_attrs_hint](/documentation/hdf5/latest/group___d_c_p_l.html#ga2fd4f0446a38186db8256cef4c97a970) |Retrieves the setting for determining whether the specified DCPL does or does not create minimized dataset object headers |
| [H5Pset\_dset\_no_attrs_hint](/documentation/hdf5/latest/group___d_c_p_l.html#gaf5ae8c0257c02e3fbe50bde70b1eb8be) |Sets the flag to create minimized dataset object headers |
 

The following changed in this release:

| Function              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [H5Oget\_info](/documentation/hdf5/latest/group___h5_o.html#gaf4f302a33faba9e1c2b5f64c62ca4ed5)<br>[H5Oget\_info_by_name](/documentation/hdf5/latest/group___h5_o.html#ga16d8ac07f9244cfccb42b5f309ca6b3c)<br>[H5Oget\_info_by_idx](/documentation/hdf5/latest/group___h5_o.html#gafe764884e1530f86079288dd5895a7bd)<br>[H5Ovisit](/documentation/hdf5/latest/group___h5_o.html#ga5ce86255fcc34ceaf84a62551cd24233)<br>[H5Ovisit_by_name](/documentation/hdf5/latest/group___h5_o.html#gab02a69e88b11404e7fd61f55344b186c) | In 1.10.3 the original functions were versioned to H5Oget\_info*1 and H5Ovisit*1 and the macros H5Oget\_info* and H5Ovisit* were created. This broke the API compatibility for a maintenance release. In HDF5-1.10.5, the macros introduced in HDF5-1.10.3 were removed. The H5Oget\_info*1 and H5Ovisit*1 APIs were copied to H5Oget\_Info* and H5Ovisit*. As an example, H5Oget\_info and H5Oget\_info1 are identical in this release. |

#### In the C++ API

The following C++ wrapper was added:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| H5Object::visit() | Wrapper for the C API H5Ovisit2. Recursively visit elements reachable from an HDF5 object and perform a common set of operations across all of those elements. See H5Ovisit2 for more information on this function. |

#### In the Fortran API

The following Fortran wrappers were added or changed:

| Function          | Description   |
| ----------------- | --------------|
| [h5fget\_dset\_no\_attrs\_hint\_f](/documentation/hdf5/latest/group___f_h5_f.html#gaceb86e903eddc57846c8a249ab5b0a66)<br> [h5fset\_dset\_no\_attrs\_hint\_f](/documentation/hdf5/latest/group___f_h5_f.html#gafda7e4a737f10a9be280afcdbf468e61)<br> [h5pget\_dset\_no\_attrs\_hint\_f](/documentation/hdf5/latest/group___f_h5_p.html#ga7cc4d157c8502632af18454424aa58d6)<br> [h5pset\_dset\_no\_attrs\_hint\_f](/documentation/hdf5/latest/group___f_h5_p.html#ga3b2e599c1c38c395d6d9b1cdddee4f6a) | Wrappers for the dataset object header minimization calls. See [H5Fget\_dset\_no_attrs_hint](/documentation/hdf5/latest/group___h5_f.html#gacbf3ba8b36750c42b49740567a9732c4), [H5Fset\_dset\_no_attrs_hint](/documentation/hdf5/latest/group___h5_f.html#gafc0166070f920f037e6b1a5c66e5464c), [H5Pget\_dset\_no_attrs_hint](/documentation/hdf5/latest/group___d_c_p_l.html#ga2fd4f0446a38186db8256cef4c97a970), and [H5Pset\_dset\_no_attrs_hint](/documentation/hdf5/latest/group___d_c_p_l.html#gaf5ae8c0257c02e3fbe50bde70b1eb8be). |
| [h5ovisit\_f](/documentation/hdf5/latest/group___f_h5_o.html#ga1aa4f84b78f029f048593b1ec0757a63)<br>[h5oget\_info\_by\_name\_f](/documentation/hdf5/latest/group___f_h5_o.html#ga40081a5f47dc7900a795c0df62791ff7)<br>[h5oget\_info\_f](/documentation/hdf5/latest/group___f_h5_o.html#gabdbe70d333edbc46cffd791495e3edea)<br>[h5oget\_info\_by\_idx\_f](/documentation/hdf5/latest/group___f_h5_o.html#ga6666adcfef409c0828390b75730f9987)<br>[h5ovisit\_by\_name\_f](/documentation/hdf5/latest/group___f_h5_o.html#gaed6f1ee04db6973cbffca2cf0c33348f)<br>| Added new Fortran 'fields' optional parameter. See [H5Ovisit2](/documentation/hdf5/latest/group___h5_o.html#gaa4ab542f581f4fc9a4eaa95debb29c9e), [H5Oget\_info_by_name2](/documentation/hdf5/latest/group___h5_o.html#ga0090da86c086c1c63a5acfaed39a035e), [H5Oget\_info2](/documentation/hdf5/latest/group___h5_o.html#ga06f896e14fe4fa940fbc2bc235e0cf74), [H5Oget\_info_by_idx2](/documentation/hdf5/latest/group___h5_o.html#ga85e15e65922874111da1a5efd5dd7bed), and [H5Ovisit_by_name2](/documentation/hdf5/latest/group___h5_o.html#ga9c155caf5499405fe403e1eb27b5beb6). |

 
The following Fortran utility function was added:

h5gmtime	 converts (C) 'time\_t' structure to Fortran DATE AND TIME storage format
 

A new Fortran derived type was added:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| c_h5o_info_t | This is  interoperable with C's h5o_info_t. This is needed for callback functions which pass C's h5o_info_t data type definition. |

See the Fortran signature for H5Oget\_INFO2.
 

In the Java wrapper

The following Java wrappers were added or changed:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| [H5Fset\_libver_bounds]() | See the C API  H5Fset\_libver_bounds for information on this function |
| [H5Fget\_dset\_no_attrs_hint](/documentation/hdf5/latest/group___h5_f.html#gacbf3ba8b36750c42b49740567a9732c4) | |
| [H5Fset\_dset\_no_attrs_hint]() | |
| [H5Pget\_dset\_no_attrs_hint]() | |
| [H5Pset\_dset\_no_attrs_hint]() | |

Wrappers for the dataset object header minimization calls  See [H5Fget\_dset\_no_attrs_hint](/documentation/hdf5/latest/group___h5_f.html#gacbf3ba8b36750c42b49740567a9732c4), [H5Fset\_dset\_no_attrs_hint](/documentation/hdf5/latest/group___h5_f.html#gafc0166070f920f037e6b1a5c66e5464c), [H5Pget\_dset\_no_attrs_hint](/documentation/hdf5/latest/group___d_c_p_l.html#ga2fd4f0446a38186db8256cef4c97a970), and H5Pset\_DSET\_NO\_ATTRS\_HINT for more information on these APIs.

### Compatibility Notes and Reports
See the [API compatibility report between 1.10.5 and 1.10.2/1.10.3/1.10.4](https://htmlpreview.github.io/?https://github.com/HDFGroup/hdf5doc/blob/master/html/ADGuide/Compatibility_Report/hdf5-1.10.6-interface_compatibility_report.html) for details.

<h2 id="4versus3">Release 1.10.4 versus 1.10.3</h2>

See the [API compatibility report between 1.10.4 and 1.10.3](https://htmlpreview.github.io/?https://github.com/HDFGroup/hdf5doc/blob/master/html/ADGuide/Compatibility_Report/hdf5-1.10.6-interface_compatibility_report.html) for details.

<h2 id="3versus2">Release 1.10.3 versus 1.10.2</h2>

New and Changed Functions, Classes, Subroutines, Wrappers, and Macros
In the C Interface (main library)

The following are new C functions in this release:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| H5Dread\_chunk]() | Moved from HDF5 High Level Optimizations library to core library |
| H5Dwrite\_chunk]() | Moved from HDF5 High Level Optimizations library to core library |
H5Oget\_INFO

H5Oget\_INFO1

H5Oget\_INFO2

The function H5Oget\_INFO was moved to [H5Oget\_info1](/documentation/hdf5/latest/group___h5_o.html#gaf3751684a6706e3ba49b863406011f80), and the macro H5Oget\_INFO was created that can be mapped to either H5Oget\_INFO1 or H5Oget\_INFO2. For HDF5-1.10 and earlier releases, H5Oget\_INFO is mapped to H5Oget\_INFO1 by default.
H5Oget\_info_by_idx

H5Oget\_info_by_idx1

H5Oget\_info_by_idx2

The function H5Oget\_info_by_idx was moved to [H5Oget\_info_by_idx1](/documentation/hdf5/latest/group___h5_o.html#ga7208d2cf198dcfc875603323841bffae), and the macro H5Oget\_info_by_idx was created that can be mapped to either H5Oget\_info_by_idx1 or H5Oget\_info_by_idx2. For HDF5-1.10 and earlier releases, H5Oget\_info_by_idx is mapped to H5Oget\_info_by_idx1 by default.
H5Oget\_info_by_name

H5Oget\_info_by_name1

H5Oget\_info_by_name2

The function H5Oget\_info_by_name was moved to [H5Oget\_info_by_name1](/documentation/hdf5/latest/group___h5_o.html#ga96ce408ffda805210844246904da2842), and the macro H5Oget\_info_by_name was created that can be mapped to either H5Oget\_info_by_name1 or H5Oget\_info_by_name2. For HDF5-1.10 and earlier releases, H5Oget\_info_by_name is mapped to H5Oget\_info_by_name1 by default.
H5Ovisit

H5Ovisit1

H5Ovisit2

The function H5Ovisit was moved to [H5Ovisit1](/documentation/hdf5/latest/group___h5_o.html#ga6efdb2a0a9fe9fe46695cc0f7bd993e7), and the macro H5Ovisit was created that can be mapped to either H5Ovisit1 or H5Ovisit2. For HDF5-1.10 and earlier releases, H5Ovisit is mapped to H5Ovisit1 by default.
H5Ovisit_by_name

H5Ovisit_by_name1

H5Ovisit_by_name2

The function [H5Ovisit_by_name](/documentation/hdf5/latest/group___h5_o.html#gab02a69e88b11404e7fd61f55344b186c) was moved to [H5Ovisit_by_name1](/documentation/hdf5/latest/group___h5_o.html#gaffacf3bd66f4fe074099eae1c80914f2), and the macro H5Ovisit_by_name was created that can be mapped to either H5Ovisit_by_name1 or H5Ovisit_by_name2. For HDF5-1.10 and earlier releases, H5Ovisit_by_name is mapped to H5Ovisit_by_name1 by default.
 

In the C High Level Interface

The following C functions were deprecated in this release:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| H5DO_read_chunk]() | Deprecated, moved to H5D_read_chunk |
| H5DO_write\_chunk]() | Deprecated, moved to H5D_write_chunk |
 

In the C++ API

Several C++ wrappers were added or modified to provide additional support. See the API Compatibility Report for details.

### Compatibility Notes and Report
See the [API compatibility report between 1.10.4 and 1.10.3](https://htmlpreview.github.io/?https://github.com/HDFGroup/hdf5doc/blob/master/html/ADGuide/Compatibility_Report/hdf5-1.10.6-interface_compatibility_report.html) for details.

<h2 id="2versus1">Release 1.10.2 versus 1.10.1</h2>

This section lists interface-level changes and other user-visible changes in behavior in the transition from HDF5 Release 1.10.1 to Release 1.10.2.

New and Changed Functions, Classes, Subroutines, Wrappers, and Macros
In the C Interface (main library)

The following are new C functions in this release:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| H5Dget\_chunk\_storage\_size]() | Returns storage amount allocated within a file for a raw data chunk in a dataset |
| H5Fget\_eoa]() | Retrieves the file's EOA |
| H5Fincrement\_filesize](/documentation/hdf5/latest/group___h5_f.html#gadbe82c1f6e16c21062fabd20b0ffccd4) | Sets the file's EOA to the maximum of (EOA, EOF) + increment |

| H5Fset\_libver\_bounds]() | Enables the switch of version bounds setting for a file |
| H5FDdriver\_query]() | Queries a VFL driver for its feature flags when a file is not available (not documented in Reference Manual) |
| H5Pget\_virtual\_prefix]() | Retrieves prefix applied to VDS source file paths |
| H5Pset\_virtual\_prefix]() | Sets prefix to be applied to VDS source file paths |
 

The following C functions changed in this release:

| H5Pset\_libver\_bounds]() | HDF5-1.10 was added to the range of versions |
| H5Pset\_virtual]() | A change was made to the method of searching for VDS source files |
| H5PL\*]() | The parameters for many of the H5PL APIs were renamed |
 

In the C High Level Interface

The following new C function was added to this release:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| H5DOread\_chunk]() | Reads a raw data chunk directly from a dataset in a file |
 

In the C++ API

The following C++ wrappers were added:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| H5Lcreate\_soft]() | Creates a soft link from link\_name to target\_name |
H5Lcreate\_hard]() | Creates a hard link from new\_name to curr\_name |
H5Lcopy]() | Copy an object from a group of file |
H5Lmove]() | Rename an object in a group or file |
H5Ldelete]() | Removes the specified link from this location |
H5Tencode]() | Creates a binary object description of this datatype |
H5Tdecode]() | Returns the decoded type from the binary object description |
H5Lget\_info]() | Returns the information of the named link |
 

These were also added:

Class LinkCreatPropList for link create property list

Overloaded functions H5Location::createGroup to take a link creation property list

See the API Compatibility report for complete details.

 

In the Java API

The following Java wrappers were added:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
H5Pset\_evict\_on\_close]() | Controls the library's behavior of evicting metadata associated with a closed object |
H5Pget\_evict\_on\_close]() | Retrieves the file access property list setting that determines whether an HDF5 object will be evicted from the library's metadata cache when closed |
H5Pset\_chunk\_opts]() | Sets the edge chunk option in a dataset creation property list |
H5Pget\_chunk\_opts]() | Retrieves the edge chunk option setting from a dataset creation property list |

H5Pset\_efile\_prefix]() | Sets the external dataset storage file prefix in the dataset access property list |

H5Pget\_efile\_prefix]() | Retrieves the prefix for external raw data storage files as set in the dataset access property list |

H5Pset\_virtual\_prefix]() | Sets prefix to be applied to VDS source file paths |

H5Pget\_virtual\_prefix]() | Retrieves prefix applied to VDS source file paths |

See the Release.txt file for details.

Tools
New options were added to the h5clear utility:

--filesize	Print the file's EOA and EOF
--increment=C	
Set the file's EOA to the maximum of (EOA, EOF) + C for the file

C is >= 0; C is optional and will default to 1M when not set

 

A new option was added to h5diff:

--enable-error-stack	Enable the error stack

### Compatibility Notes and Report

See the [API compatibility report between 1.10.4 and 1.10.3](https://htmlpreview.github.io/?https://github.com/HDFGroup/hdf5doc/blob/master/html/ADGuide/Compatibility_Report/hdf5-1.10.6-interface_compatibility_report.html) for details.

<h2 id="1versus0">Release 1.10.1 versus 1.10.0</h2>

This section lists interface-level changes and other user-visible changes in behavior in the transition from HDF5 Release 1.10.0 (and HDF5-1.10.0-patch1) to Release 1.10.1.

New Features
Several new features are introduced in HDF5 Release 1.10.1.

Metadata Cache Image

Metadata Cache Evict on Close

Paged Aggregation

Page Buffering

New Features, including associated C Functions
The following features are described and documented in New Features in HDF5 Release 1.10. Each new feature in 1.10.1 is listed below along with the associated C functions:

Metadata Cache Image:
 

| Function              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [H5Pget\_mdc\_image\_config](/documentation/hdf5/latest/group___f_a_p_l.html#ga3012f7f3310c7d25ada7617896bef1ee)
| Retrieves the metadata cache image configuration values for a file access property list. |
| [H5Pset\_mdc\_image\_config](/documentation/hdf5/latest/group___f_a_p_l.html#gaf234199ad4cf9c708f45893f7f9cd4d3)
| Sets the metadata cache image option for a file access property list. |
| [H5Fget\_mdc\_image\_info](/documentation/hdf5/latest/group___m_d_c.html#ga7b37da15ff80c4aa5c275649f1f45b0a)
| Gets information about a metadata cache image if it exists. |

Metadata Cache Evict on Close:
 

| Function              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [H5Pget\_evict\_on\_close](/documentation/hdf5/latest/group___f_a_p_l.html#ga12789fcfeaea073c13202e6401f404a6)
| Retrieves the property list setting that determines whether an HDF5 object will be evicted from the library's metadata cache when it is closed. | 
| [H5Pset\_evict\_on\_close](/documentation/hdf5/latest/group___f_a_p_l.html#gaa44cc0e592608e12082dad9305b3c74d)
| Controls the library's behavior of evicting metadata associated with a closed object. | 

Paged Aggregation:

| Function              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [H5Pget\_file\_space\_page\_size](/documentation/hdf5/latest/group___f_c_p_l.html#gaab5e8c08e4f588e0af1d937fcebfc885) |
| Retrieves the file space page size for a file creation property list. |
| [H5Pset\_file\_space\_page\_size](/documentation/hdf5/latest/group___f_c_p_l.html#gad012d7f3c2f1e1999eb1770aae3a4963) |
| Sets the file space page size (used with paged aggregation) for a file creation property list. |
| [H5Pget\_file\_space\_strategy](/documentation/hdf5/latest/group___f_c_p_l.html#ga54cf6ca4f897ba9ee3695a15fe8e6029) |
| Retrieves the file space handling strategy for a file creation property list. |
| [H5Pset\_file\_space\_strategy](/documentation/hdf5/latest/group___f_c_p_l.html#ga167ff65f392ca3b7f1933b1cee1b9f70) |
| Sets the file space allocation strategy for a file creation property list. |

Page Buffering:

| Function              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [H5Pget\_page\_buffer\_size](/documentation/hdf5/latest/group___f_a_p_l.html#ga0da11baf31cf424d053aa7952c933d98) |
| Retrieves the maximum size for the page buffer and the minimum percentage for metadata and raw data pages. |
| [H5Pset\_page\_buffer\_size](/documentation/hdf5/latest/group___f_a_p_l.html#ga8008cddafa81bd1ddada23f6d9a161ca) |
| Sets the maximum size for the page buffer and the minimum percentage for metadata and raw data pages. |
| [H5Fget\_page\_buffering\_stats](/documentation/hdf5/latest/group___h5_f.html#ga0663defe0143631f4292267c21e94202) |
| Retrieves statistics about page access when it is enabled. |
| [H5Freset\_page\_buffering\_stats](/documentation/hdf5/latest/group___h5_f.html#ga7ef1c0aab9a7a9112a8d0a788ec8696c) |
| Resets the page buffer statistics. |

New and Changed Functions, Classes, Subroutines, Wrappers, and Macros
In the C Interface (main library)

The following new C functions were added:

| Function              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [H5PLappend](/documentation/hdf5/latest/group___h5_p_l.html#gac74200fdc02f794f3fae753fe8b850b0) |
| funcdesc |
| [H5PLget](/documentation/hdf5/latest/group___h5_p_l.html#ga64a3c5450d91455624ecba582553d905) |
| funcdesc |
| [H5PLinsert](/documentation/hdf5/latest/group___h5_p_l.html#gacc5153b0db6b3f876c3980bf34f931fc) |
| funcdesc |
| [H5PLprepend](/documentation/hdf5/latest/group___h5_p_l.html#ga1f2300ef2de6e430af330de7d194576f) |
| funcdesc |
| [H5PLremove](/documentation/hdf5/latest/group___h5_p_l.html#gaa566196b7c6970c255feac4cf9f3bf40) |
| funcdesc |
| [H5PLreplace](/documentation/hdf5/latest/group___h5_p_l.html#gab0f8d4e8d0b81cb55cf8b9de5095dc0b) |
| funcdesc |
| [H5PLsize](/documentation/hdf5/latest/group___h5_p_l.html#ga30b799ad7e9645312ef8975a610b4b18) |
| funcdesc | 

#### In the C++ API

New member functions were added to provide const versions. For example, these methods,

ArrayType::getArrayDims ( hsize\_t\* dims ) const

ArrayType::getArrayNDims ( ) const


replace these:

ArrayType::getArrayDims(hsize\_t\* dims)

ArrayType::getArrayNDims()

Several functions were moved to other classes. For example, this method,

H5Location::openDataSet (char const\* name) const

replaces:

CommonFG::openDataSet (char const\* name) const

PLEASE review the Compatibility report below for complete information on the C++ changes in this release.

### Compatibility Report

See the [API compatibility report between 1.10.1 and 1.10.0-patch1](https://htmlpreview.github.io/?https://github.com/HDFGroup/hdf5doc/blob/master/html/ADGuide/Compatibility_Report/hdf5-1.10.6-interface_compatibility_report.html) for details.

<h2 id="0versus8_16">Release 1.10.0 versus Release 1.8.16</h2>

This section lists interface-level changes and other user-visible changes in behavior in the transition from HDF5 Release 1.8.16 to Release 1.10.0.

Changed Type
hid\_t

Changed from a 32-bit to a 64-bit value.

hid\_t is the type is used for all HDF5 identifiers. This change, which is necessary to accommodate the capacities of modern computing systems, therefore affects all HDF5 applications. If an application has been using HDF5's hid\_t the type, recompilation will normally be sufficient to take advantage of HDF5 Release 1.10.0. If an application uses an integer type instead of HDF5's hid\_t type, those identifiers must be changed to a 64-bit type when the application is ported to the 1.10.x series.

New Features and Feature Sets
Several new features are introduced in HDF5 Release 1.10.0.

#### Single-Writer / Multiple-Reader or SWMR

#### Collective Metadata I/O

#### Fine-tuning the metadata cache

#### File Space Management

#### Virtual Datasets or VDS

#### Partial Edge Chunk Options

#### Relative Pathnames for External Links

#### Property List Encoding and Decoding

More substantial lists follow, including new and modified C functions and Fortran subroutines.

New Features, including associated C Functions and Fortran Wrappers
The following features are described and documented in New Features in HDF5 Release 1.10.0. On this page, we list each feature and its associated C functions and Fortran wrappers.

Single-writer / Multiple-reader, commonly called SWMR:
 

H5Fstart\_swmr\_write

Enables SWMR writing mode for a file.

H5DOappend

Appends data to a dataset along a specified dimension.
(This is a high-level API.)

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| [H5Pget\_append\_flush](/documentation/hdf5/latest/group___d_a_p_l.html#gacd6803640eebd20e408c330192b09fa6) |
| Retrieves the values of the append property that is set up in the dataset access property list. |
| [H5Pset\_append\_flush](/documentation/hdf5/latest/group___d_a_p_l.html#ga2f685a7b3f3a4fa35ddcd1659ab4a835) |
| Sets two actions to perform when the size of a dataset's dimension being appended reaches a specified boundary. |
| [H5Pget\_object\_flush\_cb](/documentation/hdf5/latest/group___f_a_p_l.html#gadb66d434fd8d2f600213b0eec539564e) |
| Retrieves the object flush property values from the file access property list. |
| [H5Pset\_object\_flush\_cb](/documentation/hdf5/latest/group___f_a_p_l.html#gab4a4a788af5b6e88381dda0df2efbf19) |
| Sets a callback function to invoke when an object flush occurs in the file. |
| [H5Odisable\_mdc\_flushes](/documentation/hdf5/latest/group___h5_o.html#ga0908be309da1fb4f771c1e264fac22ae) |
| Prevents metadata entries for an HDF5 object from being flushed from the metadata cache to storage. |
| [H5Oenable\_mdc\_flushes](/documentation/hdf5/latest/group___h5_o.html#ga21014920bdabf6973e233796d7174156) |
| Returns the cache entries associated with an HDF5 object to the default metadata flush and eviction algorithm. |
| [H5Oare\_mdc\_flushes\_disabled](/documentation/hdf5/latest/group___h5_o.html#gab2fa388aadd1ff154ee150cbb4884c1c) |
| Determines if an HDF5 object (dataset, group, committed datatype) has had flushes of metadata entries disabled. |
 
Command-line Tools:

h5watch

Allows users to output new records appended to a dataset under SWMR access as it grows. The functionality is similar to the Unix user command tail with the follow option, which outputs appended data as the file grows.

h5format\_convert

This tool allows users to convert the indexing type of a chunked dataset made with a 1.10.x version of the HDF5 Library when the latest file format is used to the 1.8.x version 1 B-tree indexing type. For example, datasets created using SWMR access, can be converted to be accessed by the HDF5 1.18 library and tools. The tool does not rewrite raw data, but it does rewrite HDF5 metadata.

Collective Metadata I/O:
 

| Function |          | Description                                                  |
|    C     | Fortran  |                                                              |
| ---------| -------- | ------------------------------------------------------------ |
| [H5Pset\_coll\_metadata\_write](myCurl) | h5pset\_coll\_metadata\_write\_f](myFurl) | Establishes I/O mode property setting, collective or independent, for metadata writes. |
| [H5Pget\_coll\_metadata\_write ](myCurl) | h5pget\_coll\_metadata\_write\_f](myFurl) | Retrieves I/O mode property setting for metadata writes. |
| [H5Pset\_all\_coll\_metadata\_ops   ](myCurl) | h5pset\_all\_coll\_metadata\_ops\_f](myFurl) | Establishes I/O mode, collective or independent, for metadata read operations. |
| [H5Pget\_all\_coll\_metadata\_ops ](myCurl) | h5pget\_all\_coll\_metadata\_ops\_f](myFurl) | Retrieves I/O mode for metadata read operations. |
 

Fine-tuning the Metadata Cache:
 

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
H5Fget\_metadata\_read\_retries\_info]() | Retrieves the collection of read retries for metadata items with checksum. |
H5Pget\_metadata\_read\_attempts]() | Retrieves the number of read attempts from a file access property list. |
H5Pset\_metadata\_read\_attempts]() | Sets the number of read attempts in a file access property list. |
H5Dflush]() | Causes all buffers associated with a dataset to be immediately written to disk without removing the data from the cache. |
H5Drefresh]() | Causes all buffers associated with a dataset to be cleared and immediately re-loaded with updated contents from disk storage. |
H5Gflush]() | Causes all buffers associated with a group to be immediately flushed to disk without removing the data from the cache. |
H5Grefresh]() | Causes all buffers associated with a group to be cleared and immediately re-loaded with updated contents from disk storage. |
H5Oflush]() | Causes all buffers associated with an object to be immediately flushed to disk without removing the data from the cache. |
H5Orefresh]() | Causes all buffers associated with an object to be cleared and immediately re-loaded with updated contents from disk storage. |
H5Tflush]() | Causes all buffers associated with a committed datatype to be immediately flushed to disk without removing the data from the cache. |
H5Trefresh]() | Causes all buffers associated with a committed datatype to be cleared and immediately re-loaded with updated contents from disk storage. |
H5Fget\_intent]() | Determines the read/write or read-only status of a file. |
 
Logging APIs:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
H5Pset\_mdc\_log\_options]() | Sets metadata cache logging options. |
H5Pget\_mdc\_log\_options]() | Gets metadata cache logging options. |
H5Fstart\_mdc\_logging]() | Starts logging metadata cache events if logging was previously enabled. |
H5Fstop\_mdc\_logging]() | Stops logging metadata cache events if logging was previously enabled and is currently ongoing. |
H5Pget\_mdc\_logging\_status]() | Gets the current metadata cache logging status. |

File Space Management:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
H5Fget\_free\_sections]() | Retrieves free-space section information for a file. |
H5Fget\_freespace]() | Returns the amount of free space in a file. |
H5Fget\_info2]() | Returns global information for a file. |
H5Pset\_file\_space]() | Sets the file space management strategy and/or the free-space section threshold for an HDF5 file. |
H5Pget\_file\_space]() | Retrieves the file space management strategy and/or the free-space section threshold for an HDF5 file. |

 
The following tool has been modified to preserve or modify file freepace information appropriately when processing files employing the VDS feature:

h5repack

Repacks HDF5 files with various options, including the ability to change the applied filters. This version of h5repack understands the file free space feature and handles the file and metadata appropriately.

Virtual Dataset or VDS:
 

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| [H5Pset\_virtual](myCurl) | h5pset\_virtual\_f](myFurl) | Sets the mapping between virtual and source datasets. |
| [H5Pget\_virtual\_count](myCurl) | h5pget\_virtual\_count\_f](myFurl) | Retrieves the number of mappings for the virtual dataset. |
| [H5Pget\_virtual\_vspace](myCurl) | h5pget\_virtual\_vspace\_f](myFurl) | Retrieves a dataspace identifier for the selection within the virtual dataset used in the mapping. |
| [H5Pget\_virtual\_srcspace](myCurl) | h5pget\_virtual\_srcspace\_f](myFurl) | Retrieves a dataspace identifier for the selection within the source dataset used in the mapping. |
| [H5Pget\_virtual\_dsetname](myCurl) | h5pget\_virtual\_dsetname\_f](myFurl) | Retrieves the name of a source dataset used in the mapping. |
| [H5Pget\_virtual\_filename](myCurl) | h5pget\_virtual\_filename\_f](myFurl) | Retrieves the filename of a source dataset used in the mapping. |
| [H5Pset\_virtual\_printf\_gap](myCurl) | h5pset\_virtual\_printf\_gap\_f](myFurl) | Sets maximum number of missing source files and/or datasets with printf-style names when getting the extent of an unlimited virtual dataset. |
| [H5Pget\_virtual\_printf\_gap](myCurl) | h5pget\_virtual\_printf\_gap\_f](myFurl) | Returns maximum number of missing source files and/or datasets with printf-style names when getting the extent for an unlimited virtual dataset. |
| [H5Pset\_virtual\_view](myCurl) | h5pset\_virtual\_view\_f](myFurl) | Sets the view of the virtual dataset to include or exclude missing mapped elements. |
| [H5Pget\_virtual\_view](myCurl) | h5pget\_virtual\_view\_f](myFurl) | Retrieves the view of a virtual dataset. |

 
Supporting Functions:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| [H5Sis\_regular\_hyperslab](myCurl) | h5sis\_regular\_hyperslab\_f](myFurl) | Determines whether a hyperslab selection is regular. |
| [H5Sget\_regular\_hyperslab   ](myCurl) | h5sget\_regular\_hyperslab\_f](myFurl) | Retrieves a regular hyperslab selection. |

 
Modified Functions:
The following pre-exising functions have been modified to understand virtual datasets.

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| [H5Pset\_layout](myCurl) | h5pset\_layout\_f](myFurl) | Specifies the layout to be used for a dataset.<\b>Virtual dataset, H5D\_VIRTUAL, has been added to the list of layouts available through this function. |
| [H5Pget\_layout](myCurl) | h5pget\_layout\_f](myFurl) | Retrieves the layout in use for a dataset.<\b> Virtual dataset, H5D\_VIRTUAL, has been added to the list of layouts. |

Partial Edge Chunks:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
H5Pset\_chunk\_opts]() | Sets a partial edge chunk option in a dataset access property list. |
H5Pget\_chunk\_opts]() | Retrieves partial edge chunk option setting from a dataset access property list. |

Relative Pathnames for External Links:

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
H5Pset\_elink\_prefix]() | Sets prefix to be applied to external link paths. |
H5Pget\_elink\_prefix]() | Retrieves prefix applied to external link paths. |

Property List Encoding and Decoding:
 

| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
H5Pencode]() | Encodes the property values in a property list into a binary buffer. |
H5Pdecode]() | Decodes property list received in a binary object buffer and returns a new property list identifier. |


Additional New Functions:
 

The following new functions appear in HDF5 Release 1.10.0 but are not yet documented:

 
| Function          | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| [H5FDlock](/documentation/hdf5/latest/_h5_f_ddevelop_8h.html#a8d1d98a681375a4203bfd74b70b3aadd) | Sets a file lock |
| [H5FDunlock](/documentation/hdf5/latest/_h5_f_ddevelop_8h.html#aebafd003d12e6ec7b56548ce5c169b9d) | Removes a file lock |
| [H5LDget\_dset\_dims](/documentation/hdf5/latest/group___h5_l_t.html#gae8ced4c8df9742761546410c214d8c3b) | Retrieves the current dimension sizes of a dataset |
| [H5LDget\_dset\_elmts](/documentation/hdf5/latest/group___h5_l_t.html#ga4a42f8b0c4d2007906361541d0d6bfdf) | Retrieves selected data from the dataset |
| [H5LDget\_dset\_type_size](/documentation/hdf5/latest/group___h5_l_t.html#gabb424859982bf8953b138372fbf7ba7f) | Returns the size in bytes of the dataset's datatype |


New and Changed Elements of the Packet Table (H5PT) High-level API
In the C Interface

Replacement functions:

H5PTcreate

Takes a property list identifier to provide flexibility on creation properties.

H5PTcreate\_fl has been removed.

H5PTfree\_vlen\_buff

Replaces H5PTfree\_vlen\_readbuff.

New functions:

Two accessor functions have been added.

H5PTget\_dataset

Returns the identifier of the dataset associated a packet table.

H5PTget\_type

Returns the identifier of the datatype used by a packet table.

H5PTis\_varlen

Determines whether a type is variable-length.

In the C++ Interface

Overloaded constructor

An overloaded constructor has been added.

FL\_PacketTable

Takes a property list identifier to provide flexibility on creation properties.</dd>

H5PTfree\_vlen\_buff

Replaces H5PTfree\_vlen\_readbuff.

Accessor wrappers

Two accessor wrappers are added to class PacketTable.

PacketTable::GetDataset()

Returns the identifier of the dataset associated a packet table.

PacketTable::GetDatatype()

Returns the identifier of the datatype used by a packet table.

Other wrappers

PacketTable::FreeBuff()

Replaces VL\_PacketTable::FreeReadBuff().

PacketTable::IsVariableLength()

Replaces VL\_PacketTable::IsVariableLength().

Overloaded functions:

Where a member functions has a char* as an argument, an overloaded functions has been added to provide the const char* argument.

The existing version will be deprecated in a future release.

Java Interface Changes
Integration into Main HDF5 Library

The Java HDF5 JNI library has been integrated into the HDF5 repository.

Configure option:

--enable-java

CMake option:

HDF5\_BUILD\_JAVA:BOOL=ON

Prior to the 1.10.x series, the HDF5 Java tools were built from an independent repository and were not as fully integrated with HDF5. were built from an independent repository and were not as fully integrated with HDF5.

Package Hierarchy Change

The package hierarchy has changed to hdf.hdflib.hdf5.

Prior to the 1.10.x series, the hierarchy was ncsa.hdf.hdflib.hdf5.

New Java APIs

A number of new APIs have been added in the Java interface, including APIs for the VDS and SWMR features.

Functions with Changed Behavior
H5Lexists

The behavior of this function has changed in this release. When testing the pathname / (a slash representing the root of an HDF5 file) H5Lexists now returns successfully with the value 1 (one). See the entry in the HDF5 Reference Manual for H5Lexists for more information.

API Compatibility
See [API Compatibility Macros](/documentation/hdf5/latest/api-compat-macros.html) in HDF5 for details on the following.

New API Compatibility Flag

A new v18 flag was added enabling the building of HDF5 such that the default API is compatible with the HDF5 Release 1.8.x API:
    --with-default-api-version=v18

New versioned functions and associated compatibility macros

Two functions and a struct have been converted to a versioned form in this release. Compatibility macros have been created for each.

H5Fget\_info

The original function is renamed to H5Fget\_info1 and deprecated.

A new version of the function, H5Fget\_info2, is introduced.

The compatibility macro H5Fget\_info is introduced.

H5F\_info\_t

This is the struct used by the H5Fget\_info functions and macro.

The original struct is renamed to H5F\_info1\_t and deprecated.

A new version of the struct, H5F\_info2\_t, is introduced.

The compatibility macro H5F\_info\_t is introduced.

H5Rdereference

The original function is renamed to H5Rdereference1 and deprecated.

A new version of the function, H5Rdereference2, is introduced.

The compatibility macro H5Rdereference is introduced.

### Autotools Configuration and Large File Support
Autotools configuration has been extensively reworked and autotool's handling of large file support has been overhauled in this release.

See the following sections in RELEASE.txt:

* Autotools Configuration Has Been Extensively Reworked
* LFS Changes

RELEASE.txt can be found in the release\_docs/ subdirectory at the root level of the HDF5 code distribution.

### Compatibility Report and Comments

[Compatibility report for Release 1.10.0 versus Release 1.8.16](https://htmlpreview.github.io/?https://github.com/HDFGroup/hdf5doc/blob/master/html/ADGuide/Compatibility_Report/CR_1.10.0.html)

Comments regarding the report

In the C interface, the hid\_t change from 32-bit to 64-bit was made in order to address a performance problem that arose when the library "ran out" of valid object identifiers to issue and thus needed to employ an expensive algorithm to find previously issued identifiers that could be re-issued. This problem is avoided by switching the size of the hid\_t type to 64-bit integers instead of 32-bit integers in order to make the pool of available integers significantly larger. (H5E\_major\_t and H5E\_minor\_t are aliased to hid\_t which is why they changed size as well). (An alternate solution to this problem was applied in release HDF5 1.8.5 but this is the cleaner/preferred solution and had to wait until 1.10.0 to be included).

hbool\_t will now be defined as a \_Bool type when configure determines that it's available.

Public structs that have members of type hid\_t or hbool\_t are affected by the above changes accordingly.

The H5Fget\_info function was renamed due to the introduction of a newer version of the function which returns additional information. The H5Rdereference function was renamed due to the introduction of a newer version of the function which allows a data access property list to be passed in. Both changes are accompanied with compatibility macros, so while existing code will need to be recompiled in order to use the newer library version, these functions do not need to be changed in application code using them provided that the HDF5 API compatibility macros are configured appropriately.
