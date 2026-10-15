# Types of Cloud Storage

## Comparison Table

| Storage Type | Description (How it stores data) | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| **Block Storage** | Splits data into fixed-size blocks, each with its own address. Works like a raw hard drive attached to a single server, which formats it with a file system. | Operating system disks, databases, and applications that need fast, low-latency reads and writes | AWS EBS, Azure Managed Disks, Google Persistent Disk |
| **File Storage** | Stores data as files in a hierarchy of folders and directories, shared over a network using protocols such as NFS or SMB. | Shared network drives, home directories, content management, and applications where many servers need the same files | AWS EFS, Azure Files, Google Filestore |
| **Object Storage** | Stores data as objects in a flat structure. Each object contains the data, metadata, and a unique ID, and is accessed over HTTP APIs. | Images, videos, backups, logs, and other massive amounts of unstructured data | AWS S3, Azure Blob Storage, Google Cloud Storage |

## Explanation for the Client

Object Storage is the best choice for storing your user-uploaded images because it scales to millions of files without needing to resize disks or manage folder structures. Each image is stored as an independent object that can be retrieved quickly over the web, which fits a photo-sharing application. It is also cost-effective for large amounts of unstructured data and keeps your images separate from the web server container, so they are not lost when the container is stopped or replaced.
