# Our first JAVA application 

#### - Set base image 
	FROM my-java-image

#### - Create a WORKDIR
	WORKDIR app

#### - Copy java file 
	COPY HelloWorld.java /app

#### - Compile
	RUN javac HelloWorld.java

#### - Set Last command 
	CMD ["java","HelloWorld"]


## Build Docker file 
	$ docker build -t my-app-image  .

#### - Run Container 
	$ docker run --name java-app my-app-image
	Hello, World 
