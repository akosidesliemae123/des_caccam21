# Laboratory 05: The Cloud Data Engineer

## Mission Overview

CloudNova Technologies has a client building a photo-sharing application that needs a place to store millions of user-uploaded images. Since containers are ephemeral, the images cannot be stored inside the web server container. In this mission, I researched the types of cloud storage, deployed an S3-compatible object storage server (MinIO) using Docker, created a bucket named `client-photos`, and uploaded a test file through the MinIO web console.

## Objectives

- Differentiate between Block, File, and Object Storage.
- Deploy an S3-compatible Object Storage server (MinIO) using Docker.
- Access a cloud service via a web interface using port forwarding.
- Create a storage bucket and upload objects (files) to the cloud.
- Document cloud storage operations using Markdown.
- Continue expanding a professional GitHub Cloud Computing Portfolio.

## Tools Used

- KillerCoda Playground (Ubuntu environment)
- Docker
- MinIO (S3-compatible object storage), using the `cgr.dev/chainguard/minio` image
- MinIO Web Console (port 9001)
- GitHub
- Markdown
- Web browser

## Skills Learned

- Explaining the differences between block, file, and object storage.
- Deploying a containerized service using Docker environment variables.
- Mapping multiple ports (API and web console) for a container.
- Accessing a cloud service running on a specific port through a web browser.
- Creating a bucket and uploading objects to object storage.
- Troubleshooting a failed image pull by finding an alternative image source.
- Documenting technical configurations clearly using Markdown and maintaining an organized GitHub repository.

## Challenges Encountered

- The command in the activity sheet used the `minio/minio` image, but Docker returned `pull access denied` because the image is no longer available on Docker Hub.
- I tried `quay.io/minio/minio`, but it returned `unauthorized: access to the requested resource is not authorized`.
- I solved this by using `cgr.dev/chainguard/minio:latest` instead and adding `--user 0` to avoid permission problems with the `/data` folder. After that, the container ran successfully and `docker ps` showed it as **Up**.
- This taught me that container images can be moved or removed by their publishers, so I should read error messages carefully and look for an alternative source.
