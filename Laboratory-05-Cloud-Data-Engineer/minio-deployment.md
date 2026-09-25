# MinIO Deployment

## Docker Command Used
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e 'MINIO_ROOT_USER=cloudadmin' \
-e 'MINIO_ROOT_PASSWORD=CloudNova2026!' \
coollabsio/minio:RELEASE.2025-10-15T17-29-55Z server /data --console-address ":9001"

## Web Console Port
9001

## Bucket Created
client-photos

## What the -e Flags Do
e-flag is like a brand new phone, once open you need to set it up like the place, the date and time and etc. That's what I did in the Killer Coda to set up the MinIo so that I can login using this credentials: 
-e 'MINIO_ROOT_USER=cloudadmin' \
-e 'MINIO_ROOT_PASSWORD=CloudNova2026!' \
