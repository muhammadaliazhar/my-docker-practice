Docker_Lab_1 :
Pull nginx default image and make our own customize image with multiple versions and push our custom image on our docker hub repo.

1. first start docker desktop verify docker version
   # docker --version
   
2. Then pull nginx default image from docker hub repo
   # docker pull nginx
   
3. verify docker images using command
   # docker images
![image](https://github.com/user-attachments/assets/42b41f33-1566-4b26-b36c-30dbf9a4e0a7)

4. create container from image using command
   # docker run -d --name containername  imagename -p external-traffic-port#:internal-traffic-port#

   





