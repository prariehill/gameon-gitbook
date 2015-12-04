# Setting up Local Docker Environment

**NOTE**: These instructions apply to Windows and OSX users only.

[Docker Toolbox](https://www.docker.com/docker-toolbox) allows you to run a Docker host in a 
virtual machine that will run inside your laptop/desktop.

Download Docker Toolbox for your operating system and run through the installer.

When the installation completes, select `Docker QuickStart Terminal` in the window that pops up 
to get started using your local VM that  will function as your Docker host.  

![image](http://docs.docker.com/mac/images/mac-page-quickstart.png)

You should see something like the following in the terminal that comes up:

```
Creating Machine default...
Creating CA: /Users/programsam/.docker/machine/certs/ca.pem
Creating client certificate: /Users/programsam/.docker/machine/certs/cert.pem
Creating VirtualBox VM...
Creating SSH key...
Starting VirtualBox VM...
Starting VM...
```

**NOTE**: The first time you run this process, it can take some time to start the VM.  Be patient.

When the installer is finished, you should see something like this:

```


                        ##         .
                  ## ## ##        ==
               ## ## ## ## ##    ===
           /"""""""""""""""""\___/ ===
      ~~~ {~~ ~~~~ ~~~ ~~~~ ~~~ ~ /  ===- ~~~
           \______ o           __/
             \    \         __/
              \____\_______/


docker is configured to use the default machine with IP 192.168.99.100
For help getting started, check out the docs at https://docs.docker.com
```

Take special note of the IP address that is similar to my example of `192.168.99.100`.  This is your
Docker host, and any containers you run on Docker will be accessible from this IP if you have mapped
their ports.

At the prompt, type

```
$ docker run hello-world
```

To test that Docker installed correctly.  You should see something like the following:

```
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world

b901d36b6f2f: Pull complete 
0a6ba66e537a: Pull complete 
Digest: sha256:517f03be3f8169d84711c9ffb2b3235a4d27c1eb4ad147f6248c8040adb93113
Status: Downloaded newer image for hello-world:latest

Hello from Docker.
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker Hub account:
 https://hub.docker.com

For more examples and ideas, visit:
 https://docs.docker.com/userguide/
```