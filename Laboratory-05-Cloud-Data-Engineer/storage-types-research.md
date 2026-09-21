# Types of Cloud Storage

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| Block Storage | Splits data into fixed-size blocks, each with its own address, and attaches to a server like a hard drive. | Operating systems, databases, and apps needing fast, low-latency disk access. | AWS EBS |
| File Storage | Stores data as files in a hierarchy of folders and shares it over a network. | Shared drives, home directories, and content that multiple servers access. | AWS EFS |
| Object Storage | Stores data as objects (data + metadata + unique ID) in a flat structure, accessed through an API or HTTP. | Images, videos, backups, and other large amounts of unstructured data. | AWS S3 |

## Why Object Storage for the Client's Photos

Object storage is the best choice because it scales to millions of images without the limits of a single disk or folder tree. Each photo is stored with its own metadata and unique ID and can be retrieved over HTTP, which suits a photo-sharing app. It is also cost-effective and durable, and unlike a container's temporary storage, the images persist independently of the web server.
