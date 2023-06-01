# Docker
Docker is a fantastic tool that makes our lives much easier offering us standardization, productivity, efficiency, maintainability and compatibility of our code. It allows us to continuously and rapidly deploy and test our code and it is platform-independent.

If you are unsure of what Docker is, what to use it for or how to use it; this is the article for you! I’ll try to give an explanation that’s as clear as possible for people who are new to Docker. At the end of this article you:

See a lot of advantages using Docker
Understand what Docker is and how it works
Understand why to use Docker: what it offers you and how it can make your life easier
Understand when to use Docker
Are able to use Docker to pull an image and spin up your first container
If you feel that any part of this article needs a little more explanation, if you have questions or if you think this article can be improved in any other way: please comment and let me know!

We’ll start with the advantages Docker bring you; why you should use it in the first place. I’ve chopped this up into several parts, some of which may overlap a little. This is because I’m trying to explain as simply as I can in order to make Docker accessible for as many people as possible.
After part 1 you’ll be totally convinced that you need Docker in your life; now we’re getting our feed in the mud. With a simple example-application we’ll perform all basic steps that’ll get a Docker container up and running. Let’s go!

# 1. Why use Docker?
Below are listed the main reasons to use Docker. I’ll try to explain each point as clearly as possible.

# Virtualization
Data centers are full of servers. These are powerful computers that you can access over the internet and can be use for all kinds of things. Data centers offer clients the option to rent part of a server; this is called a virtual machine; not the entire computer but a part of it that acts like a full machine. This is called virtualization because your main machine (the host) acts like it is e.g. 3 separate, independent machines (the guests) like in the image below.


# Using VM’s to host our app

You’ll see that the server hosts 3 virtual machines; one for our API, one for a webserver and one for a database. Also it has some infrastructure and some services to control all the virtual machines. The most important take away here is that each virtual machine has its own Guest OS. This is totally redundant and takes up a lot of memory.

When you use Docker you don’t need virtual machines. You package your applications in a container which runs on a machine. This can be a server but also your own laptop:


# Dockerizing our app

Notice that we save a lot of memory; our apps share an OS (the kernel at least), making it much more light-weight. Check out the article below for a great, practical example on how to containerize a Postgres database.

Compose containers
Applications rarely consist out of one part: most of the time multiple containers have to work together to create all functionalities. An example: a website, API and database have to be connected together. This is what Docker Compose allows us to do. We can create a file that defines how containers are connected with one another. We can use this file to instantiate all of the Dockerfiles for all of our containers all at once!

# 2. How Docker works: creating our first container
Let’s get our hands dirty and code something already! You can see Docker as a way to pack you code in a nice little container that contains everything it needs to run it; it containerizes your code. The benefits are numerous: containers are scalable, cost-effective and are isolated from each other. This part focusses on the docker elements:

Dockerfile: Specifications for how the image should be built
Image: Like a CD: it contains all code but it doesn’t do anything yet.
Container: A running image. Think of this as the CD that you’ve just put in the CD-player. It’s executing the image.
2.1 The Dockerfile
We’ll create a set of instructions that tells our machine how to build our image. In our case we want to create a simple website in Flask; a Python web framework. Check out the Dockerfile below:

Let’s go through it line by line.

Line 1. This tells Docker to install an OS (Debian Slim Buster) with Python 3.8 installed
Line 3. Creates a folder in the docker container called ‘app’. In here all of our code will be housed
Line 5. Copies the requirements.txt file on our machine to the WORKDIR on the docker container
Line 6. This downloads and installs all the Python dependencies we need for our app. In our case this will install Flask
Line 8. Copy everything from our current directory to the WORKDIR. This moves all of our source code
Line 10: this starts our app by calling the installed Flask module and running our app on localhost.
2.2 The Docker image
Our Dockerfile is defined, let’s use it to create an image. Run

docker build --tag python-docker
This command will take the Dockerfile and build it into an image. We’ll also give it a tag called python-docker. When the image is built we can execute docker images to find it.

We’ve just made an image. Think of this as a CD-ROM of a game; it contains all the assets, graphics and code to make it work. We can spin up the image in a container now.

2.3 A Docker container
A container is a running instance of our image. If the image is like a CD-ROM, now we put that image into our computer and run our game. The running game is our container in our analogy. In the same way we can run our image with the following command:

docker run --publish 5000:5000 python-docker
In this command we tell docker to run an image called python-docker. This is what we tagged the image with in the previous part. We also specify --publish 5000:5000. This details how we want to connect ports between our laptop (the host machine) and the docker container. Since Flask is running on port 5000 by default, the second part of this flag needs to be 5000. We’ve chosen to make the container accessible on our host machine on port 5000. To see this in action navigate to localhost:5000 and see our Flask website working!

Try to run docker run --publish 4331:5000 python-docker` and you’ll see that you have to navigate to localhost:4331.

# Conclusion
Having learnt how to pull images and spin up containers opens a lot of doors in automating, deploying and testing your software. Still, we’ve only scratched the surface when it comes to all of the benefits Docker has to offer.
