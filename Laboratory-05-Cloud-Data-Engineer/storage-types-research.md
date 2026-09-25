# Research: Types of Cloud Storage

## Comparison Table

| Storage Type | Description (How does it store data?) | Primary Use Case (What is it best used for?) | Cloud Provider Example |
| :--- | :--- | :--- | :--- |
| **Block Storage** | Splitting data into fixed-size chunks or blocks, each given a unique address without metadata attached. | Boot volumes, virtual machine disks, transactional databases (e.g., MySQL). | AWS EBS (Elastic Block Store)|
| **File Storage** | Storing data in a hierarchical file structure with folders and subfolders accessible over network protocols. | Shared user directories, content management systems, legacy enterprise applications. | AWS EFS (Elastic File System) |
| **Object Storage** | Storing data as discrete units (objects) containing raw data, a unique identifier, and customizable metadata in a flat namespace. | Unstructured data at scale, media files (images/videos), web assets, backups, logs. | AWS S3 (Simple Storage Service) |

---

## Storage Recommendation for Client

Object storage is the optimal choice for storing user-uploaded images because web containers are ephemeral and cannot store persistent files internally without losing them during container restarts. Object storage scales massively and cost-effectively without requiring management of complex file hierarchies or fixed-size disk partitions. Additionally, files can be accessed directly over HTTP/HTTPS APIs, allowing smooth integration with web applications.

## References link
https://aws.amazon.com/compare/the-difference-between-block-file-object-storage/?utm_source=gemini
https://aws.amazon.com/efs/when-to-choose-efs/?utm_source=gemini
