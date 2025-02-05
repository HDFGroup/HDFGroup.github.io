---
title: HDF5 Advanced Topics
redirect_from:
  - display/HDF5/Advanced+Topics+in+HDF5
  - documentation/hdf5-docs/advanced_topics
---

## Advanced Topics in HDF5

| Topic                         | Description                                                  |
| ----------------------------- | ------------------------------------------------------------ |
| [Chunking in HDF5](https://support.hdfgroup.org/releases/hdf5/documentation/advanced_topics/chunking_in_hdf5.html) | Provides detailed information regarding chunking in HDF5 |
| [HDF5 File Image Operations (PDF)](https://docs.hdfgroup.org/hdf5/rfc/HDF5FileImageOperations.pdf) | Describes how to work with HDF5 files in memory. Disk I/O is not required when file images are opened, created, read from, or written to |
| [Copying Committed Datatypes with H5Ocopy (PDF)](https://support.hdfgroup.org/releases/hdf5/documentation/advanced_topics/CopyingCommittedDatatypesWithH5Ocopy.pdf) | Describes how to copy to another file a dataset that uses a committed datatype or an object with an attribute that uses a committed datatype so that the committed datatype in the destination file can be used by multiple objects|
| [Collective Metadata I/O](https://support.hdfgroup.org/releases/hdf5/documentation/advanced_topics/CollectiveMetadataIO.html) | Describes optimizing HDF5 by collecting metadata I/O |
| [Enabling a Strict Consistency Semantics Model in Parallel HDF5 (PDF)](https://docs.hdfgroup.org/hdf5/rfc/RFC%20PHDF5%20Consistency%20Semantics%20MC%20120328.docx.pdf) | Describes how to improve file access consistency semantics with the Parallel HDF5 library |
| [File Space Management](https://support.hdfgroup.org/releases/hdf5/documentation/advanced_topics/FileSpaceManagement.html) | Describes mechanisms to manage space in an HDF5 file |
| [Fine-tuning the Metadata Cache](https://support.hdfgroup.org/releases/hdf5/documentation/advanced_topics/FineTuningMetadataCache.html) | Describes how to provide better control of the metadata cache |
| [Freeing Memory Allocated by the HDF5 Library (PDF)](https://docs.hdfgroup.org/hdf5/rfc/RFC%20H5free_memory%20v2.pdf) | Describes how inconsistent memory management can cause heap corruption or resource leaks and possible solutions |
| [HDF5 Data Flow Pipeline for H5Dread](https://support.hdfgroup.org/releases/hdf5/documentation/advanced_topics/data_flow_pline_H5Dread.html) | Describes data flow when reading raw data from an HDF5 dataset |
| [HDF5 Metadata](https://support.hdfgroup.org/releases/hdf5/documentation/advanced_topics/) | Provides a comprehensive overview of the types of metadata used in HDF5 |
| [Introduction to Single-Writer_Multiple-Reader (SWMR)](https://support.hdfgroup.org/releases/hdf5/documentation/advanced_topics/intro_SWMR.html) | Enables writing to a file while multiple readers are accessing it |
| [Introduction to the Virtual Dataset - VDS](https://support.hdfgroup.org/releases/hdf5/documentation/advanced_topics/intro_VDS.html) | Describes how to present data stored in several HDF5 datasets and files as a single dataset and access the data using HDF5 APIs |
| [Modified Region Writes (PDF)](https://support.hdfgroup.org/releases/hdf5/documentation/advanced_topics/ModifiedRegionWrites.pdf) | Describes how to set write operations for in-memory files so that only modified regions are written to storage. Available when the Core (Memory) VFD is used |
| [Page Buffering (PDF)](https://docs.hdfgroup.org/hdf5/rfc/RFC-Page_Buffering.pdf) | Describes how to reduce the number of small accesses in HDF5 by buffering metadata and raw data accesses |
| [Partial Edge Chunks]() | Describes how to control the filtering of partial edge chunks to improve performance when extending datasets |
| [Thread-safe HDF5]() | Information on thread-safety and concurrent access in HDF5 |
| [Using the Direct Chunk Write Function (PDF)](https://docs.hdfgroup.org/hdf5/rfc/DECTRIS%20Integration%20RFC%202012-11-29.pdf) | Describes another way that chunks can be written to datasets |
| [Virtual Object Layer](https://docs.hdfgroup.org/hdf5/develop/_h5_v_l__u_g.html) | An abstraction layer within the HDF5 library that enables different methods for accessing data and objects that conform to the HDF5 data model |

