# Basic Dockerfile Usage

1. Create Dockerfile.
2. `docker build -t USERNAME/REPONAME .`  
3. `docker push USERNAME/REPONAME`
4. If you need to update Dockerfile, repeat steps **2** and **3**.
5. If you want to make changes within the image: 
    - Start the image:
        - `docker run -d USERNAME/REPONAME bash`
    - Enter the image and make changes:
        - `docker exec -it CONTAINER`
    - `exit` the container
    - Commit changes:
        - `docker commit CONTAINER USERNAME/REPONAME`
    - Push changes:
        - `docker push USERNAME/REPONAME`  

***Note:** If using the included httpd Dockerfile you must `run` with something like `-p 80:80` to map the ports properly.*
