---
title: New Features in HDF5 1.12
redirect from: 
  - display/HDF5/New+Features+in+HDF5+Release+1.12
---

# New Features in HDF5 1.12

This release includes changes in the HDF5 storage format. PLEASE NOTE that HDF5-1.10 and earlier releases cannot read files created with the new features described below that are marked with a \*.

HDF5 1.12 introduces several new features in the HDF5 library:

* <a href="#encode-decode">H5Sencode / H5Sdecode Format Change</a>
<a href="#vol">Virtual Object Layer (VOL)</a>
<a href="#references">Update to References</a>
<a href="#selections">Update to Selections</a>
<a href="#hyperslab">Hyperslab Performance Improvement</a>

<h2 id="encode-decode">H5Sencode / H5Sdecode Format Change</h2>

Several new H5S APIs were introduced to allow a user to more flexibly operate on two hyperslab selections.  See the [Selection I/O update RFC](https://support.hdfgroup.org/releases/hdf5/documentation/rfc/H5Sencode_format.docx.pdf) for details.


<h2 id="vol">Virtual Object Layer (VOL)</h2>

The Virtual Object Layer (VOL) is an abstraction layer within the HDF5 library that enables different methods for accessing data and objects that conform to the HDF5 data model. The VOL intercepts all HDF5 API calls that potentially modify data on disk and forwards those calls to a plugin "object driver". The data on disk can be a different format than the HDF5 format.


The plugins can actually store the objects in variety of ways. A plugin could, for example, have objects be distributed remotely over different platforms, provide a raw mapping of the model to the file system, or even store the data in other file formats (like native netCDF or HDF4 format). The user still gets the same data model where access is done to a single HDF5 \"container\"; however the plugin object driver translates from what the user sees to how the data is actually stored. Having this abstraction layer maintains the object model of HDF5 and allows better usage of new object storage file systems that are targeted for Exascale systems.

See the [Virtual Object Layer](/documentation/hdf5/latest/_h5_v_l__u_g.html#sec_vol) page for more information.


<h2 id="references">Update to References</h2>

See the [References update RFC](https://support.hdfgroup.org/releases/hdf5/documentation/rfc/RFC_Update_to_HDF5_References.pdf) for details on the changes in HDF5-1.12.

HDF5 references were extended to support attributes, as well as object and dataset selections that reside in another HDF5 file. In order to support these features several functions were introduced:

* Create (H5R_CREATE\*) functions were added for each reference type: object, dataset region and attribute.
* A function was added to release a reference (H5R_DESTROY). This is required because a region reference no longer modifies the original file.
* Functions were added to query references (H5R_GET\*).
* Other functions were added to simplify or clarify the API.

<h2 id="selections">Update to Selections</h2>

Several new H5S APIs were introduced to allow a user to more flexibly operate on two hyperslab selections.  See the [Selection I/O update RFC](https://support.hdfgroup.org/releases/hdf5/documentation/rfc/selection_io_RFC_210610.pdf) for details.

<h2 id="hyperslab">Hyperslab Performance Improvements</h2>

In 1.12.0 the hyperslab selection code was optimized to achieve better performance. In general, performance improved by an order of a magnitude. In the case of reading a regular selection from a 20 GB dataset into a one dimensional array, performance improved by a factor of 6000. If you are interested in the benchmark we ran, please see issue HDFFV-10930 by logging into jira.hdfgroup.org with your hdfgroup.org login.

