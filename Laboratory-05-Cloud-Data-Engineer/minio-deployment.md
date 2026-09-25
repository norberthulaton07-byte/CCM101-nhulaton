# MinIO Deployment Documentation

This document outlines the technical steps taken to deploy MinIO, an S3-compatible object storage server, using Docker.

## Docker Command Used

Since MinIO's official Docker Hub image (`minio/minio`) and its Quay.io mirror were both discontinued after MinIO archived their open-source repository in April 2026 (they moved to a commercial product called AIStor), I had to use a community-maintained alternative image instead. The exact command used was: docker run -d -p 9000:9000 -p 9001:9001 --name minio-server -e "MINIO_ROOT_USER=cloudadmin" -e "MINIO_ROOT_PASSWORD=CloudNova2026!" -e "MINIO_BROWSER=on" bitnamilegacy/minio:2024


## Port Used to Access the Web Console

The MinIO Web Console was accessed through **port 9001**. This port was mapped from the container to the host using the `-p 9001:9001` flag, and made accessible externally through KillerCoda's Traffic/Ports feature.

## Bucket Created

The bucket created for storing the client's uploaded files is named **client-photos**.

## Explanation of the -e Flags (Environment Variables)

The `-e` flag in the Docker command is used to pass environment variables into the container at runtime. In this deployment:

- `-e "MINIO_ROOT_USER=cloudadmin"` sets the root/admin username used to log into the MinIO server and web console.
- `-e "MINIO_ROOT_PASSWORD=CloudNova2026!"` sets the root/admin password paired with the username above.
- `-e "MINIO_BROWSER=on"` explicitly enables MinIO's web-based console/browser interface, ensuring it starts and listens on port 9001.

These environment variables let us configure the container's behavior and security credentials without having to rebuild the image or manually edit configuration files inside the container — everything is set at the moment the container starts.

## Troubleshooting Notes

During deployment, the original image specified in the assignment (`minio/minio`) could not be pulled from either Docker Hub or Quay.io, both returning "access denied" or "unauthorized" errors. Research confirmed that MinIO's open-source GitHub repository was archived on April 25, 2026, discontinuing free public Docker images for the official product. As a workaround, I used the `bitnamilegacy/minio` image, a community-maintained legacy image that provides the same MinIO functionality. I also had to explicitly add the `MINIO_BROWSER=on` environment variable, since the console did not start automatically with the default configuration.
