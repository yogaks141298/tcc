YOGA KURNIA SUBEKTI  
17541033  
# UTS


Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

PS C:\Users\ombloh> mkdir yoga


    Directory: C:\Users\ombloh


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-----       10/29/2019  12:41 AM                yoga


PS C:\Users\ombloh> cd yoga
PS C:\Users\ombloh\yoga>
PS C:\Users\ombloh\yoga> docker build -t yogaks1234/yoga:v1 .
Sending build context to Docker daemon  3.072kB
Step 1/2 : FROM nginx:alpine
 ---> b6753551581f
Step 2/2 : COPY . /usr/share/nginx/html
 ---> Using cache
 ---> 9f0d9eb2b720
Successfully built 9f0d9eb2b720
Successfully tagged yogaks1234/yoga:v1
SECURITY WARNING: You are building a Docker image from Windows against a non-Windows Docker host. All files and directories added to build context will have '-rwxr-xr-x' permissions. It is recommended to double check and reset permissions for sensitive files and directories.
PS C:\Users\ombloh\yoga> docker images
REPOSITORY              TAG                 IMAGE ID            CREATED             SIZE
ombloh38/ojan           v1                  9f0d9eb2b720        32 minutes ago      21.4MB
ombloh38/ojan           v2                  9f0d9eb2b720        32 minutes ago      21.4MB
yogaks1234/yoga         v1                  9f0d9eb2b720        32 minutes ago      21.4MB
<none>                  <none>              be04a82f54d2        38 minutes ago      21.4MB
ombloh38/ombloh         v1                  abf65b544924        About an hour ago   21.4MB
nginx                   alpine              b6753551581f        5 days ago          21.4MB
ubuntu                  latest              cf0f3ca922e0        9 days ago          64.2MB
redis                   latest              de25a81a5a0b        11 days ago         98.2MB
cockroachdb/cockroach   latest              82ebb27f44e8        4 weeks ago         190MB
PS C:\Users\ombloh\yoga> docker run -d -p 2020:80 --name=yogaks yogaks1234/yoga:v1
C:\Program Files\Docker\Docker\Resources\bin\docker.exe: Error response from daemon: Conflict. The container name "/yogaks" is already in use by container "c3ec199747c5b1f7741c821a8d8b31931561c525e90828cc51fe34cbf6ec5ec2". You have to remove (or rename) that container to be able to reuse that name.
See 'C:\Program Files\Docker\Docker\Resources\bin\docker.exe run --help'.
PS C:\Users\ombloh\yoga> docker run -d -p 1010:80 --name=yogak yogaks1234/yoga:v1
6e7d1b1ae4cb309c2e077eb6f28a20b3a31b2a1d1365033b3e355147a9763157
PS C:\Users\ombloh\yoga> docker build -t yogaks1234/yoga:v1 .
Sending build context to Docker daemon  3.072kB
Step 1/2 : FROM nginx:alpine
 ---> b6753551581f
Step 2/2 : COPY . /usr/share/nginx/html
 ---> Using cache
 ---> 9f0d9eb2b720
Successfully built 9f0d9eb2b720
Successfully tagged yogaks1234/yoga:v1
SECURITY WARNING: You are building a Docker image from Windows against a non-Windows Docker host. All files and directories added to build context will have '-rwxr-xr-x' permissions. It is recommended to double check and reset permissions for sensitive files and directories.
PS C:\Users\ombloh\yoga> docker run -d -p 9090:80 --name=yogas yogaks1234/yoga:v1
60e3904b07845899f4ba90fadb3224bb0d096708dd8ff4858ed1cc3b50c39c12
PS C:\Users\ombloh\yoga> docker build -t yogaks1234/yoga:v1 .
Sending build context to Docker daemon  3.072kB
Step 1/2 : FROM nginx:alpine
 ---> b6753551581f
Step 2/2 : COPY . /usr/share/nginx/html
 ---> 95563bdd3b7d
Successfully built 95563bdd3b7d
Successfully tagged yogaks1234/yoga:v1
SECURITY WARNING: You are building a Docker image from Windows against a non-Windows Docker host. All files and directories added to build context will have '-rwxr-xr-x' permissions. It is recommended to double check and reset permissions for sensitive files and directories.
PS C:\Users\ombloh\yoga> docker run -d -p 4040:80 --name=yogak1 yogaks1234/yoga:v1
f779d1a099f5912e7f32e2a835047589b3db9d8f70899bb6861faaf691f7c26a
PS C:\Users\ombloh\yoga> docker images
REPOSITORY              TAG                 IMAGE ID            CREATED             SIZE
yogaks1234/yoga         v1                  95563bdd3b7d        3 minutes ago       21.4MB
ombloh38/ojan           v1                  9f0d9eb2b720        42 minutes ago      21.4MB
ombloh38/ojan           v2                  9f0d9eb2b720        42 minutes ago      21.4MB
<none>                  <none>              be04a82f54d2        47 minutes ago      21.4MB
ombloh38/ombloh         v1                  abf65b544924        About an hour ago   21.4MB
nginx                   alpine              b6753551581f        5 days ago          21.4MB
ubuntu                  latest              cf0f3ca922e0        9 days ago          64.2MB
redis                   latest              de25a81a5a0b        11 days ago         98.2MB
cockroachdb/cockroach   latest              82ebb27f44e8        4 weeks ago         190MB
PS C:\Users\ombloh\yoga> docker tag yogaks1234/yoga:v1 yogaks1234/yogaks:v1
PS C:\Users\ombloh\yoga> docker push yogaks1234/yogaks:v1
The push refers to repository [docker.io/yogaks1234/yogaks]
b9fc26b5bddc: Preparing
bba7d2385bc1: Preparing
77cae8ab23bf: Preparing
denied: requested access to the resource is denied
PS C:\Users\ombloh\yoga> docker push yogaks1234/yogaks:v1
The push refers to repository [docker.io/yogaks1234/yogaks]
b9fc26b5bddc: Pushed
bba7d2385bc1: Pushed
77cae8ab23bf: Pushed
v1: digest: sha256:f324cf09a26a4dc9d901a08a333867d41359ea2dc4699723ad274e7753f9dba1 size: 946
PS C:\Users\ombloh\yoga>


![1](image/1.png)