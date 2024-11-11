# Flow-2: Create a Custome-Docker Image and Push to Docker Hub

## Pre-requisite Step
- Create your Docker hub account. 
- https://hub.docker.com/
- **Important Note**: In the below listed commands wherever you see **maliazhar** you can replace with your docker hub account id. 


## Step-1: Run the base Nginx container
docker run --name mynginxdefault -p 3666:80 -d nginx
docker ps
go to browser and type localhost:3666
here you see nginx default page

## Step-2: login to the container shell and create index.html file
docker exec -it containerid /bin/bash
cd /usr/share/nginx/html
echo "Welcome to Docker" > index.html
exit
go to browser and type localhost:3666
here you see your nginx custom page


## Step-3: Create Docker Image from that container
```
docker commit containerid newimagename
docker commit 456722da8434 mycustom-nginx
```

## Step-4: Tag & push your custom Docker image to you docker hub account
```
docker images
docker tag imagename  dockerhubusername/imagename:tag
docker tag mycustom-nginx maliazhar/mycustom-nginx:v1-release

## Step-6: Verify the image on docker hub
docker login
** here when you see login succeeded then push the image
docker push maliazhar/mycustom-nginx:v1-release
```
## Step-5: Verify the image on docker hub
- Login to docker hub and verify the image we have pushed
- Url: https://hub.docker.com/repositories

## Step-6: Go to another machine and pull that image and run conatiner from that image