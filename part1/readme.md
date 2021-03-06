# Part 1

## Task 1.1

`docker ps -a`

![task 1.1](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-1.png)

## Task 1.2

`docker ps -as`

![task 1.2](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-2a.png)

`docker images`

![task 1.2](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-2b.png)

## Task 1.3

`docker run -it devopsdockeruh/pull_exercise`

![task 1.3](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-3.png)

## Task 1.4

`docker run -d --name task1-4 devopsdockeruh/exec_bash_exercise`

`docker exec -it task1-4 bash`

![task1.4](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-4.png)

## Task 1.5

`docker run --rm -it --name task1.5 ubuntu:16.04 sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'`

In another terminal:

`docker exec task1.5 apt-get update`

`exec task1.5 apt-get install -y curl wget`

Back to the first:

![task1.5](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-5.png)

## Task 1.6

[Dockerfile](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-6/Dockerfile)

`docker build -t docker-clock .`

`docker run docker-clock`

## Task 1.7

[Dockerfile](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-7/Dockerfile)

[Script file](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-7/curler.sh)

`docker build -t curler .`

`docker run -it curler`

Output same as task 1.5

## Task 1.8

`touch logs.txt`

`docker run -d -v $(pwd)/logs.txt:/usr/app/logs.txt devopsdockeruh/first_volume_exercise`

Continues to write the logs until the container is stopped. 

## Task 1.9

`docker run -p 8080:80 devopsdockeruh/ports_exercise`

Open browser, type localhost:8080

Message visible in browser: "Ports configured correctly!!"

## Task 1.10

[Dockerfile](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-10/Dockerfile)

`docker build -t task10 .`

`docker run -p 5000:5000 task10`

## Task 1.11

[Dockerfile](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-11/Dockerfile)

`docker build -t task11 .`

`docker run -d -v $(pwd)/logs.txt:/mydir/logs.txt -p 8000:8000 task11`

## Task 1.12

[Dockerfile front](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-12/front/Dockerfile)

`docker build -t front .`

`docker run -p 5000:5000 front`

[Dockerfile back](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-12/back/Dockerfile)

`docker build -t back .`

`docker run -d -v $(pwd)/logs.txt:/mydir/logs.txt -p 8000:8000 back`

## Task 1.13

[Dockerfile](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-13/Dockerfile)

`docker build -t spring .`

`docker run -p 8080:8080 spring`

## Task 1.14

[Dockerfile](https://github.com/mshroom/DevOpsWithDocker/blob/master/part1/ex-1-14/Dockerfile)

`docker build -t rails .`

`docker run -p 3000:3000 rails`

## Task 1.15

[Project in Dockerhub](https://hub.docker.com/r/mshroom/cats)

## Task 1.16

[Heroku app](https://devops-1-16.herokuapp.com/)
