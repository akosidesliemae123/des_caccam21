# Mission Reflection

Installing an operating system on a Virtual Machine takes a lot of time: I would have to allocate resources, install the OS, boot it, and then install and configure the web server, which can take 15 minutes or more. With Docker, I only ran `docker pull nginx` and `docker run`, and the web server was live in seconds. A container does not boot a full OS because it shares the host's kernel, which is why it starts so quickly.

Port mapping with `-p 8080:80` is necessary because a container has its own isolated network. Nginx listens on port 80 inside the container, but that port is not reachable from outside by default. Mapping port 8080 on the host to port 80 in the container lets requests such as `curl http://localhost:8080` reach the web server.

When I use `docker rm`, the container and the data stored in its writable layer are deleted permanently. This showed me that containers are meant to be disposable, and that important data should be kept in volumes if it needs to survive.

Containerization changes how developers and IT operations teams work together. A container packages the application with its dependencies, so it runs the same way on a developer's laptop, in testing, and in production. This reduces the "it works on my machine" problem, speeds up deployments, and encourages shared responsibility, which is the heart of DevOps.

My GitHub portfolio is evolving from simple cloud concept notes into hands-on, documented technical work. Each laboratory adds a new skill, from cloud comparisons to containers, and I am learning to organize folders, write clear Markdown, include screenshots as evidence, and commit regularly. It now looks more like a professional record of my progress as a cloud engineer.
