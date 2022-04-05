# A Demonstration of WebDNA in a Docker Container!

Documentation will continuously be added in future updates. Right now the goal is to create a very basic docker container with WebDNA and demonstrate its capabilities. This project is **NOT** meant for production use and is just the bare minimum as a proof of concept. Best practices are not always followed in this project- utilize in production at your own risk!

[Docker Desktop](https://www.docker.com/products/docker-desktop/) should be installed in order to run and build the containers. 

[VSCode](https://code.visualstudio.com/) is recommended for building/running/working with containers- due to the many extensions and integrations it has built in- but is not required. The use of powershell/terminal to build the images is required.

## Why would I want to run WebDNA in a container?
There are a lot of reason why you might want to run WebDNA in a container, [containers](https://www.docker.com/resources/what-container/) are a powerful technology for developing, managing, and running web applications.

The biggest reason though would be having a highly portable, cross platform, easily set up environment for WebDNA development. Build your own or pull a public image from the docker repository, spin it up in docker desktop and start coding in WebDNA on localhost!

## Demonstration Images Quick Start

### Build the project:
[Download the repository](https://github.com/deepworks-net/docker-webdna-demo/archive/refs/heads/main.zip) and place it somewhere on your computer. Open a terminal and navigate to the location of the repository:
```SHELL
cd '/YOUR/LOCATION/TO/REPO'
```
Then choose the service to build from the [docker-compose.yml](docker-compose.yml) file. Current services are:
- centos7-fcgi (CentOS 7.9.2009, WebDNA FCGI 8.6.5)
- centos8-fcgi (CentOS 8.4.2105, WebDNA FCGI 8.6.5)
- ubuntu16-fcgi (Ubuntu 16.04, WebDNA FCGI 8.6.5)
- ubuntu18-fcgi (Ubuntu 18.04, WebDNA FCGI 8.6.5)
- ubuntu20-fcgi (Ubuntu 20.04, WebDNA FCGI 8.6.5)
- ubuntu21-fcgi (Ubuntu 21.10, WebDNA FCGI 8.6.5)
- ubuntu22-fcgi (Ubuntu 22.04, WebDNA FCGI 8.6.5)

From there run the following command to build the demo substituting {SERVICE} with service name:
```SHELL
# docker-compose build {SERVICE}
# To build ubuntu22-fcgi:
docker-compose build ubuntu22-fcgi
```

Then use the following command to run the demo by again substituting {SERVICE} with service name:
```SHELL
# docker-compose up -d {SERVICE}
# To run ubuntu22-fcgi after building:
docker-compose up -d ubuntu22-fcgi
```
Once the container is running, navigate to http://localhost/public/index.dna to see it in action and can be modified from the public folder in this repository. 

The WebDNA admin pages are located at http://localhost/WebDNA with the default username:password of admin:admin.