### Assignment Solution

1. Building image :
    - navigate into the python app
        `cd ./python-app`
    - create Dockerfile :

        ```Docker
        FROM python:3.8

        WORKDIR /app

        COPY . /app

        CMD ["python","bmi.py"]
        ```

    - Build python docker image:
        `docker build .`

2. Launch python app without name.
    `docker run -it <IMAGE NAME | ID>`

3. Recreate container and assign name:
    `docker run -it --name bmi <IMAGE NAME | ID>`

4. Clean up all stopped containers and images
    - containers :
        `docker container prune`
    - images :
        `docker image prune`

5. Re-build the images - this time with names and tags assigned to them.
    `docker build -t python:3.8 .`
