#  Push image to docker hub - docker : nginx-welcome

**Docker - Welcome Image(Nginx)**

  File Structure:

```  
  ├── CHANGELOG.md
  ├── README.md
  ├── docker
  │   └── nginx
  │       ├── Dockerfile
  │       └── default.conf
  ├── docker-compose.yml
  └── html
      └── index.html
```

  Push docker image(nginx) to docker hub:
  
  1. Clone the files.
  
  2. Run Docker compose up command: 

```  
  docker-compose up -d
```  

  3. Commit to a new image name: 
  
```
    docker commit {{CONTAINER ID}} {{docker hub - username}}/{{image name}}: {{tag}}
    
    docker commit 857b1d643ac0 nithincninan/nginx-welcome-image:latest
    sha256:XXXXXXXXXXXXXXXXXXXXXXXXXXXXe78f209cc6ee53b6
```
  
  4. Verify the newly created image in image list:
```
    docker images
    REPOSITORY                                   TAG              IMAGE ID       CREATED          SIZE
    nithincninan/nginx-welcome-image             latest           926264f40cbc   18 minutes ago   185MB 
```  
     
  5. Login with docker hub account):

```
    docker login
    username: XXXXXXX
    password: XXXXXXX
```  
     

  5. Push the image to the registry hub using docker push:

```
   docker 

    docker push nithincninan/nginx-welcome-image:latest
    The push refers to repository [docker.io/nithincninan/nginx-welcome-image]
    85638dbdf387: Pushed
    db1a35fb3199: Pushed
    475bac2f3e0e: Pushed
    7318ebc54f15: Pushed
    c6d74dcb7fe7: Mounted from library/nginx
    b50a193ebf2e: Mounted from library/nginx
    165eb6c3c0d3: Mounted from library/nginx
    cf388fcf3527: Mounted from library/nginx
    2418679ca01f: Mounted from library/nginx
    764055ebc9a7: Mounted from library/nginx
    latest: digest: sha256:XXXXXXXXXXXXXXXXXXXXXdd83cd1b6a907081b85c53 size: 2403
```  

<img width="1680" alt="nginx-localhost" src="https://user-images.githubusercontent.com/2525741/124376899-bbf59000-dcc6-11eb-9be4-6150fcac044a.png">

    
