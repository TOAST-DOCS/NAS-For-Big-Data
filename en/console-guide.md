## Storage > NAS for BigData > Console User Guide

<a id="volume"></a>
## Volume
A volume is a logical storage space in NAS that can be mounted on an instance to store or read data.

<a id="create_volume"></a>
### Create a Volume

Creates a new volume. The created volume can be accessed from instances by using the network file system (NFS) protocol.

| Item | Description |
| --- | --- |
| Name | Name of the volume to be created. The NFS access path is created using the volume name. The volume name is limited to up to 100 characters, including letters, numbers, and some symbols (-, \_). |
| Description | Description of the volume. |
| VPC | The virtual private cloud (VPC) to access the volume. |
| Subnet | The subnet to access the volume. Only subnets in the selected VPC can be chosen. |
| Size | Size of the volume to be created. It can be entered from a minimum of 1,000 GB to a maximum of 50,000 GB. |
| Access Control List (ACL) | Access control lists (ACLs) can be configured in the Network ACL service. For more information, see the [Network ACL service user guide](/Network/Network%20ACL/ko/overview). |
| Auto Create Snapshot | A snapshot is automatically created at the specified time every day. If you exceed the set number, it is gradually deleted from the oldest snapshot. |

<a id="delete_volume"></a>
### Delete a Volume

Deletes a volume.

> [Caution]
It is recommended to unmount the volume from connected instances before deleting it. Deleting a volume while it is still mounted may cause issues on the user system.
>
> If you delete a volume, all data, including snapshots, is deleted. Data cannot be recovered after deletion.

<a id="change_volume_size"></a>
### Change a Volume size

Changes the size of a volume. The size can be changed even while the volume is in use.

<a id="change_acl"></a>
### Change Access Control Settings

Access control lists (ACLs) can be configured in the Network ACL service. For more information, see the [Network ACL service user guide](/Network/Network%20ACL/ko/overview).

<a id="snapshots"></a>
## Snapshot
A snapshot is a read-only copy that saves the state of a volume at a specific point in time. Snapshots can be used to restore a volume to the state it was in at the time the snapshot was created.

| Item | Description |
| --- | --- |
| Name | Name of the snapshot. If created by the system, the name is determined according to specified rules. |
| Created on | The time the snapshot was created. |

<a id="snapshots.create"></a>
### Create a Snapshot Immediately

Creates a snapshot immediately. The name is limited to up to 32 characters, including letters, numbers, and some symbols (-, \_, .). Each snapshot must have a unique name within the volume.

<a id="snapshots.restore"></a>
### Restore a Snapshot

Restores the volume to the point in time when the snapshot was created. Contact [customer support](https://www.nhncloud.com/kr/support/inquiry) to restore the snapshot.

<a id="snapshots.delete"></a>
### Delete a Snapshot

Deletes the specified snapshot. Deleted snapshots cannot be recovered.

<a id="connect_volume"></a>
## Connect to Volume

The created volume can be mounted on an instance using the connection information. However, the instance to be mounted must be connected to the same subnet as the volume.

<a id="connect_volume.nfs"></a>
### Install NFS Package

#### Debian, Ubuntu

```
sudo apt-get install nfs-common rpcbind
```
<br/>

#### Rocky

```
sudo dnf install nfs-utils rpcbind
```
<br/>

<a id="connect_volume.rpcbind"></a>
### Run rpcbind Service

```
sudo service rpcbind start
```
<br/>

<a id="connect_volume.mount"></a>
### Volume Mount

```
sudo mount -t nfs <nas source> <mount point>
```

| Item | Description |
| --- | --- |
| <nas source> | Volume information<br>Example: 192.168.0.11:/GJ_SHARE_FS8/bacb62d4-f271-44ad-a5d2-505d21037b45 |
| <mount point> | Directory to mount the volume<br>Example: /mnt |
