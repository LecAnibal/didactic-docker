# Docker from scratch 

Create an empty directory for this task and create an empty file in that directory with the name Dockerfile. You can do this easily by issuing the command touch Dockerfile in your empty directory.

Congratulations, you just created your first Dockerfile! Let’s open the file in your favorite text editor!

Every Dockerfile must start with the FROM instruction. The idea behind is that you need a starting point to build your image. You can start FROM scratch, scratch is an explicitly empty image on the Docker store that is used to build base images like Alpine, Debian and so on.
The follow is a Dockerfile example :

```sh
FROM  scratch
ADD alpine-minirootfs-3.9.3-x86_64.tar.gz /
CMD ["/bin/echo", "hi my friends"]
```

next step , we have to compile this Dockerfile to generate a image

```sh
$ docker build -t my-docker-image  .
Sending build context to Docker daemon  2.687MB
Step 1/3 : FROM  scratch
 --->
Step 2/3 : ADD alpine-minirootfs-3.9.3-x86_64.tar.gz /
 ---> fa0357769f10
Step 3/3 : CMD ["/bin/echo", "hi my friends"]
 ---> Running in 72b23f871bae
Removing intermediate container 72b23f871bae
 ---> 703841ae90b1
Successfully built 703841ae90b1
Successfully tagged my-docker-image:latest

$ docker images
REPOSITORY        TAG       IMAGE ID     CREATED              SIZE
my-docker-image  latest   703841ae90b1    8 seconds ago       5.53MB
```


# Congratulations 
you have the base image for everything you want.
