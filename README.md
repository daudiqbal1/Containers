This is a demo to set up a container from scratch


List of commands in order to create the image and running the container:
Enter these commands in your working directory

# check docker status using
docker info
docker stats
# in case deeamon set is not running just restart the docker

# Build the image
docker build .


# Check the new image
docker images


# Set a name for the new image, currently you only have IMAGE ID (I set it to helloworld)
docker build -t hello-internet .


# Run the image, -d means deamon, -p to expose to some ports
docker run -d -p 80:80 ed00d9af65a4


# Check the container running
docker ps


# Check the website on localhost:80
# Stop the container, using container name
docker stop serene_elgamal


# To execute into container, use following commmand, -it is for interactive mode, continaer ID and the location you want to execute, it can also be bash
docker exec -it f6c1f552d323 /bin/sh


# Docker ignore file, will stop you from adding certain files to your image "**" finds the file located anywhere in your project and you dont have to specify absolute path, can be used as safety feature and also to keep the size of image small. This image has been based of Alpine linux which is really tiny sized linux distro, it keeps images very small which is our primary goal, but it doesn't support some of basic linux features. BUT there is no limit to the sources you can use to create container images. 







