# DevOps-with-Docker-AYTKT21025en
Exercises for the course AYTKT21025en DevOps with Docker

//This is a test
Microsoft Windows [Version 10.0.17134.829]
(c) 2018 Microsoft Corporation. Kaikki oikeudet pidätetään.

C:\Users\krist>docker run hello-world
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
1b930d010525: Pull complete
Digest: sha256:41a65640635299bab090f783209c1e3a3f11934cf7756b09cb2f1e02147c6ed8
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/


C:\Users\krist>docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
hello-world         latest              fce289e99eb9        6 months ago        1.84kB

C:\Users\krist>docker run hello-world

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/


C:\Users\krist>docker run hello-world

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/


C:\Users\krist>docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
hello-world         latest              fce289e99eb9        6 months ago        1.84kB

C:\Users\krist>docker rmi hello-world
Error response from daemon: conflict: unable to remove repository reference "hello-world" (must force) - container abf8ae62cb08 is using its referenced image fce289e99eb9

C:\Users\krist>docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

C:\Users\krist>docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                     PORTS               NAMES
603e688d66e6        hello-world         "/hello"            2 minutes ago       Exited (0) 2 minutes ago                       gallant_gagarin
41d4675dd090        hello-world         "/hello"            2 minutes ago       Exited (0) 2 minutes ago                       frosty_dirac
abf8ae62cb08        hello-world         "/hello"            3 minutes ago       Exited (0) 3 minutes ago                       xenodochial_wilson

C:\Users\krist>docker ps -a | grep hello-world
'grep' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\krist>docker ps -a | grep hello-world
'grep' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\krist>docker rm 60
60

C:\Users\krist>docker container prune
WARNING! This will remove all stopped containers.
Are you sure you want to continue? [y/N] y
Deleted Containers:
41d4675dd09078de6c377e6d476c8907369ab8708db321c85a3b4a938d7036ab
abf8ae62cb081ddb3a98b368fb252849f8b6d1256c546cab1ca3ac3f49c40c04

Total reclaimed space: 0B

C:\Users\krist>docker rmi hello-world
Untagged: hello-world:latest
Untagged: hello-world@sha256:41a65640635299bab090f783209c1e3a3f11934cf7756b09cb2f1e02147c6ed8
Deleted: sha256:fce289e99eb9bca977dae136fbe2a82b6b7d4c372474c9235adc1741675f587e
Deleted: sha256:af0b15c8625bb1938f1d7b17081031f649fd14e6b233688eea3c5483994a66a3

C:\Users\krist>docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE

C:\Users\krist>docker pull hello-world
Using default tag: latest
latest: Pulling from library/hello-world
1b930d010525: Pull complete
Digest: sha256:41a65640635299bab090f783209c1e3a3f11934cf7756b09cb2f1e02147c6ed8
Status: Downloaded newer image for hello-world:latest

C:\Users\krist>docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
hello-world         latest              fce289e99eb9        6 months ago        1.84kB

C:\Users\krist>docker rmi hello-world
Untagged: hello-world:latest
Untagged: hello-world@sha256:41a65640635299bab090f783209c1e3a3f11934cf7756b09cb2f1e02147c6ed8
Deleted: sha256:fce289e99eb9bca977dae136fbe2a82b6b7d4c372474c9235adc1741675f587e
Deleted: sha256:af0b15c8625bb1938f1d7b17081031f649fd14e6b233688eea3c5483994a66a3

C:\Users\krist>docker run nginx
Unable to find image 'nginx:latest' locally
latest: Pulling from library/nginx
fc7181108d40: Pull complete
d2e987ca2267: Pull complete
0b760b431b11: Pull complete
Digest: sha256:96fb261b66270b900ea5a2c17a26abbfabe95506e73c3a3c65869a6dbe83223a
Status: Downloaded newer image for nginx:latest

C:\Users\krist>docker run -d nginx
5c31d953fe12958c2285b0bcc226a82cc6216ecd6f57b8425ff1760b1bd8bb79

C:\Users\krist>docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
5c31d953fe12        nginx               "nginx -g 'daemon of…"   17 seconds ago      Up 16 seconds       80/tcp              goofy_thompson
ff36ab7c543e        nginx               "nginx -g 'daemon of…"   55 seconds ago      Up 54 seconds       80/tcp              hungry_shtern

C:\Users\krist>docker rm <5c>
The syntax of the command is incorrect.

C:\Users\krist>docker rm <ff>
The syntax of the command is incorrect.

C:\Users\krist>docker stop <goofy_thompson>
The syntax of the command is incorrect.

C:\Users\krist>docker container prune
WARNING! This will remove all stopped containers.
Are you sure you want to continue? [y/N] y
Total reclaimed space: 0B

C:\Users\krist>docker ps -a
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
5c31d953fe12        nginx               "nginx -g 'daemon of…"   3 minutes ago       Up 3 minutes        80/tcp              goofy_thompson
ff36ab7c543e        nginx               "nginx -g 'daemon of…"   3 minutes ago       Up 3 minutes        80/tcp              hungry_shtern

C:\Users\krist>docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
nginx               latest              f68d6e55e065        6 days ago          109MB

C:\Users\krist>docker rm <5c31d953fe12>
The syntax of the command is incorrect.

C:\Users\krist>docker rm --force <5c>
The syntax of the command is incorrect.

C:\Users\krist>docker ps -aq
5c31d953fe12
ff36ab7c543e

C:\Users\krist>docker stop $(docker ps -aq)
unknown shorthand flag: 'a' in -aq)
See 'docker stop --help'.

C:\Users\krist>docker stop --help

Usage:  docker stop [OPTIONS] CONTAINER [CONTAINER...]

Stop one or more running containers

Options:
  -t, --time int   Seconds to wait for stop before killing it (default 10)

C:\Users\krist>docker kill $(docker ps -q)
unknown shorthand flag: 'q' in -q)
See 'docker kill --help'.

C:\Users\krist>docker stop ps -a
unknown shorthand flag: 'a' in -a
See 'docker stop --help'.

C:\Users\krist>docker stop 5c
5c

C:\Users\krist>docker stop ff
ff

C:\Users\krist>docker ps -a
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                      PORTS               NAMES
5c31d953fe12        nginx               "nginx -g 'daemon of…"   11 minutes ago      Exited (0) 17 seconds ago                       goofy_thompson
ff36ab7c543e        nginx               "nginx -g 'daemon of…"   12 minutes ago      Exited (0) 10 seconds ago                       hungry_shtern

C:\Users\krist>docker rm 5c ff
5c
ff

C:\Users\krist>docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

C:\Users\krist>
