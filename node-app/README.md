### Solution

1. Building image :
    - navigate into the node app
        `cd ./node-app`
    - create Dockerfile :

        ```Docker
        FROM node

        WORKDIR /app

        COPY . /app

        RUN npm install

        EXPOSE 3000

        CMD ["node","server.js"]

        ```

    - Build node docker image:
        `docker build .`

2. Launch node app without name.
    `docker run -p 3000:3000 <IMAGE NAME | ID>`

3. Recreate container and assign name:
    `docker run -p 3000:3000 --name express <IMAGE NAME | ID>`

4. Clean up all stopped containers and images
    - containers :
        `docker container prune`
    - images :
        `docker image prune`

5. Re-build the images - this time with names and tags assigned to them.
    `docker build -t node:latest .`
