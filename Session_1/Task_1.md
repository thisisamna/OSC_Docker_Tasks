﻿1. `docker images`  
   3 images

2. `docker run alpine cat /etc/hostname`  
   (852233dd5128)

3. `docker pull ubuntu:noble`

4. `docker run -d erseco/alpine-php-webserver`  
   No, it doesn't

5. `docker run -d -p 55:8080 erseco/alpine-php-webserver`

6. [Screenshot](Q6.png)

7.

```
docker ps
docker stop d183247c316c
docker rm d183247c316c
```
