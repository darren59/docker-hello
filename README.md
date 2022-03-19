## 1: Get Source

`Forked https://github.com/u1i/docker-hello`

## 2: Publish to Dockerhub
Added the required steps below:

1) Checks-out the repository, so our workflow can access it.
2) Inserted the username, passowrd to log into Docker Hub.
3) Edited setting, "secrets", inserted a) DOCKER_USER and b) DOCKER_PASSWORD with DOcker Hub username and password.
 -
    name: Checkout 
    uses: actions/checkout@v2
 -
    name: Login to Docker Hub
    uses: docker/login-action@v1
    with:
       username: ${{ secrets.DOCKER_USER }}
       password: ${{ secrets.DOCKER_PASSWORD }}

## 3: Test by editing Dockerfile
Added a new line just to see if workflows will auto-trigger updated and check into DockerHub.
