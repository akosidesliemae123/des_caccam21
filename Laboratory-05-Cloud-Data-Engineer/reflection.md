# Mission Reflection

Object storage is better suited for millions of photos because it stores each file as an independent object with its own metadata and unique ID in a flat structure. Block storage is tied to a single server and has a limited size, so it must be resized or reformatted as data grows. Object storage scales almost without limit by adding capacity, each photo can be retrieved over HTTP, and it is usually cheaper for large amounts of unstructured data.

Docker made deploying MinIO much easier because I did not have to install dependencies or configure the software manually. One `docker run` command downloaded the image, started the server, mapped ports 9000 and 9001, and set the login credentials through environment variables. The same command can be repeated on any machine with the same result.

A bucket is a top-level container in cloud storage that holds objects (files). It is where permissions, policies, and settings are applied. In this lab, I created a bucket named `client-photos` and uploaded a test file to it.

Large enterprises protect object storage data through replication and redundancy. Data is copied across multiple disks, servers, and even different data centers or regions, and techniques like erasure coding allow lost pieces to be rebuilt. If one physical server crashes, other copies keep the data available, and backups and versioning add extra protection.

My confidence in the Linux command line is growing. I now understand how to read commands, use flags like `-d`, `-p`, and `-e`, check results with `docker ps`, and fix mistakes by reading the output. Commands that once looked confusing now feel logical, and I feel more ready to handle bigger cloud tasks.
