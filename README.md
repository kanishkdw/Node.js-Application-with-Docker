# Node.js-Application-with-Docker

Node.js is an open-source, cross-platform JavaScript runtime environment.
For information on using Node.js, see the [Node.js Application](https://nodejs.org/en).

#  Prerequisites
1. I assume you have installed Docker and it is running.  
See the [Docker website](https://www.docker.com/get-started/#h_installation) for installation instructions.
Hope you know how to create the folder and edit it.     

2. If you are using Ubuntu version 16.04 or below, we recommend you upgrade to a more latest version since Ubuntu no longer provides support for these versions.This [collection of guides](https://www.digitalocean.com/community/tutorial-collections/ubuntu-lts-upgrades) will help you in upgrading your Ubuntu version.

# Build
## Step 1-Installing the application dependencies 
1. Clone this repo  


    `https://github.com/kanishkdw/Node.js-Application-with-Docker.git` 


2. Change the node-project directory path cd node_project  
    
    
    `cd node_project`

3. To install your project’s dependencies, run the following command:  
    `npm install`
**Note- All the command need to be run while in the root directory that is node-project.

## Step 2. Create a Dockerimage and the Docker container
 Run the below command to build the image  

    sudo docker build -t your_dockerhub_username/nodejs-image-demo .

  **Make sure to replace `your_dockerhub_username` to your Docker hub Username;

Run the following command to build the container:

    sudo docker run --name nodejs-image-demo -p 80:8080 -d your_dockerhub_username/nodejs-image-demo

With your container running, you can now visit your application by visitng;

`localhost:80`

![Screenshot 2024-07-26 142638](https://github.com/user-attachments/assets/b9fc9e7a-1a5e-4da0-ab9f-35b4d3e0e79c)


![Screenshot 2024-07-26 142721](https://github.com/user-attachments/assets/ac43c0d3-6350-4ae4-8877-c32cfc34d1fc)

## Step 4. Push the repository to Docker-hub

To push the image first log in to the Docker Hub account you created in the prerequisites:

    sudo docker login -u your_dockerhub_username

**Replace `your_dockerhub_username` with your dockerhub Username

1. The first step to pushing the image is to log in to the Docker Hub account you created in the prerequisites

    `sudo docker login -u your_dockerhub_username`

2. You can now push the application image to Docker Hub using the tag you created earlier, your_dockerhub_username/nodejs-image-demo:

    `sudo docker push your_dockerhub_username/nodejs-image-demo`

**Replace `your_dockerhub_username` with your dockerhub Username


## Conclusion
In this tutorial you created a static web application with Express and Bootstrap, as well as a Docker image for this application. You used this image to create a container and pushed the image to Docker Hub.
