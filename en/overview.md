<a id="overview"></a>
## Storage > NAS for BigData > Overview

NAS for BigData is a fully managed network-attached storage (NAS) service that enables easy use of large-capacity file storage in a cloud environment. Based on the standard network file system (NFS) protocol, it can be easily mounted on cloud instances, allowing data to be read and written like a local disk.

It provides scalable large-capacity storage and is well-suited for various tasks such as file sharing between instances, large-scale data analysis, and backups.

<a id="features"></a>
## Features

<a id="features.capacity"></a>
### Large-capacity storage

In projects that handle large-scale data, storage capacity can be adjusted in real time from the console without the need to scale out physical hardware, reducing operational overhead. Volume size changes are applied without data loss, and the scalability and elasticity enable flexible data management.

<a id="features.sharing"></a>
### Efficient file sharing based on NFS

With NFS protocol support, file sharing between instances can be implemented easily and quickly. A single volume can be mounted simultaneously on multiple servers, making it suitable for parallel processing and distributed workloads in multi-node environments.

<a id="features.access_control"></a>
### Easy creation and flexible access control

File-level storage can be configured quickly from the web console without complex setup. In addition, IP-based access control policies can be configured in the Network ACL service, providing both security and flexibility, even in environments with multiple connected instances.

<a id="glossary"></a>
## Terminology

<a id="glossary.NAS"></a>
### NAS

NAS is a file-based storage device accessible over a network. Users can mount NAS like a local disk to store or retrieve files, making it suitable for sharing data across multiple servers. Basic security features such as access control are also provided.

<a id="glossary.volume"></a>
### Volume

A volume is a logical storage space in NAS that can be mounted on an instance to store or read data.

<a id="glossary.snapshots"></a>
### Snapshot

A snapshot is a read-only copy of a volume created at a specific point in time. When unexpected data corruption or deletion occurs, the data can be quickly restored to that point in time.
In NAS for BigData, the time for automatic snapshot creation can be set once per day, and created snapshots consume a portion of the storage space.
