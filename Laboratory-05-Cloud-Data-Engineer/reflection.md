# Mission Reflection

Choosing object storage over traditional block storage for millions of uploaded photos made a lot of sense once I saw how it works. Block storage acts like a regular hard drive with fixed partitions, which gets expensive and hard to manage when you have thousands of files. Object storage keeps everything organized in a simple, flat structure using unique IDs and metadata. This setup makes it much easier and cheaper to store endless image uploads that web apps can easily access.

Deploying MinIO through Docker was a huge help for me as a beginner. Instead of struggling through a complicated setup process to install software directly on Ubuntu, Docker let me launch the whole storage server with one simple terminal command. Passing the configuration flags for MINIO_ROOT_USER and MINIO_ROOT_PASSWORD showed me how easy it is to set up credentials right when the container starts.

Learning about "buckets" helped me understand how cloud systems organize data. A bucket acts like a main storage folder, but instead of nested subfolders, every uploaded file sits in a flat namespace. It also serves as the main place where administrators set up access permissions, password rules, and security policies for all the files stored inside.

I also learned how big tech companies protect their cloud data if a physical server crashes. They use techniques like erasure coding and multi-region replication. Erasure coding splits files into smaller data chunks across multiple disks, so if one drive breaks, the system can rebuild the file without losing anything.

Overall, working through this lab really built up my confidence. Running Docker commands, setting up the client-photos bucket, and successfully uploading my first test image made managing cloud infrastructure feel much less intimidating.
