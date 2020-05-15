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


