# TAG19demo

This is a tutorial that goes over the basic setup and concepts of docker for anyone to use. It is a simple yet effective tool that can help anyone on any platform run current applications in an efficient manner.

Every so often there is a bright idea that evolves the way IT infrastructure operates. Containerization is one such idea that has been adopted and embraced blindingly fast by the tech titans. This idea addresses the question: does this application work on this operating system? Not only does containerization reduces the concern surrounding supporting multiple operating systems but it does so while simultaneously increasing security, portability, agility and efficiency. This presentation provides an overview of containerization, discusses how containerization impacts our IT infrastructures and anticipates what can we expect moving forward. It concludes with a demo of how The Kresge Foundation has used a containerization platform called Docker to deploy its applications.

## Step 1: Installation Docker and Git

(Windows & Mac)
Download Docker Desktop from

https://www.docker.com/products/docker-desktop

Git:

Windows - https://git-scm.com/download/win

Mac - https://git-scm.com/download/mac

Linux - https://docs.docker.com/install/linux/docker-ce/ubuntu/
Follow prompts for required services install, GPG key, and adding new repository

Git:

>sudo dnf install git-all

or

>sudo apt install git-all


## Step 2: Verify Docker install
Open a terminal or administrative powershell prompt and enter the following command

>docker version

If installed properly, the Docker engine details and versions should be provided.

## Step 3: Test out a few basic commands

>docker ps                   (Shows all running containers)

>docker ps -a                (Shows all containers)

>docker run hello-world      (Run command will pull and start a container image, like hello-world)

>docker stop <container id>  (Stops the specified running container)

## Step 4: Run web based application

Before you use the run command for the compose file check out where I got this from, https://hub.docker.com/

>docker run -d --name kanboard -p 80:80 -t kanboard/kanboard:v1.2.8

## Step 5: Run docker compose

Execute git (Where ever you installed it eariler)
run the command:

>git clone https://github.com/SRadatz/TAGdemo.git

Once the git package is cloned run the following command in powershell/terminal

>docker-compose -f wordpress.yml up

once the application downloads and launches go to http://127.0.0.1:8080

Afterwards you can run a "docker ps -a" and see the Wordpress container and SQL container. These containers will stay running until they are stopped or your computer is turned off.
