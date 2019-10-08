YOGA KURNIA SUBEKTI  
175410033  
TEKNOLOGI CLOUD COMPUTING 
***  
 
## install cockroachDB
1. Install Docker for Windows.

        Docker for Windows requires 64bit Windows 10 Pro and Microsoft Hyper-V. Please see the official documentation for more details. Note that if your system does not satisfy the stated requirements, you can try using Docker Toolbox.
Open PowerShell and confirm that the Docker daemon is running in the background:


PS C:\Users\username> docker version
If you do not see the server listed, start Docker for Windows.

2. Share your local drives. This makes it possible to mount local directories as data volumes to persist node data after containers are stopped or deleted.

3. Pull the image for the v19.1.5 release of CockroachDB from Docker Hub:

PS C:\Users\username> docker pull cockroachdb/cockroach:v19.1.5
![1](image/1.png)


