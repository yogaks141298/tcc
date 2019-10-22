Yoga Kurnia Subekti  
175410033
TI-9  

## Container  
1. Raining A Container
![1](image/1.png)
  
2. Finding Running Containers  
![2](image/2.PNG)

3. Accessing Redis
![3](image/3.PNG)

4. Accessing Redis
After experimenting, Jane discovers that just using the option -p 6379 enables her to expose Redis but on a randomly available port. She decides to test her theory using 

        docker run -d --name redisDynamic -p 6379 redis:latest 

While this works, she now doesn't know which port has been assigned. Thankfully, this is discovered via   

        docker port redisDynamic 6379   
  
Jane also finds that listing the containers displays the port mapping information,   
        docker ps   
![4](image/4.png)
  
5. Persisting Data
Using the Docker Hub documentation for Redis, Jane has investigated that the official Redis image stores logs and data into a /data directory.Any data which needs to be saved on the Docker Host, and not inside containers, should be stored in /opt/docker/data/redis. The complete command to solve the task is   
    docker run -d --name redisMapped -v /opt/docker/data/redis:/data redis
![5](image/5.png)
6. Running A Container In The Foreground  
The command "docker run ubuntu ps" launches an Ubuntu container and executes the command ps to view all the processes running in a container.

Using "docker run -it ubuntu bash" allows Jane to get access to a bash shell inside of a container.  
![6](image/6.png)
  
## Nginx 
1.  Create Dockerfile  
![7](image/7.png)
2. Build Docker Image
![8](image/8.png)
3. Run
![9](image/9.png)  
![91](image/91.png)

## Docker 2
1. Base Images
