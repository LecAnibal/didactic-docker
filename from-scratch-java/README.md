# JAVA IMAGE
we will install a version of java, for that do you remember
our docker image  my-docker-image.

#### - Set a  base  image
     FROM my-docker-image

#### - build a image 
    $ docker build -t my-java-image  .

#### - Usage
   $ docker run --name java-cntnr   my-java-image java -version 
    openjdk version "1.8.0_212"
    OpenJDK Runtime Environment (IcedTea 3.12.0) (Alpine 8.212.04-r0)
    OpenJDK 64-Bit Server VM (build 25.212-b04, mixed mode)