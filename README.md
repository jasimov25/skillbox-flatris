# skillbox-flatris
 intensive homework
 
Skillbox What is Devops intensive, Timur Batyrshin

lecture notes:


Requirements: Git, Docker, kubernetes

github.com/timurb/flatris
cloud.yandex.ru
install Ubuntu image
ssh-keygen // generate private and public keys
ls -l ~/.ssh/id_rsa* // show available keys
cat ~/.ssh/id_rsa.pub
git docker.io vim nano
apt-get update // update if some link missing during install
sugo gpasswd -a admin docker // add user admin to group docker
Ctrl + d // logout
Ctrl + l // clear screen
Ctrl + r // search last commands

get app from Github
github.com/timurb/flatris Code - https

git clone https://github.com/timurb/flatris.git
cd flatris
nano Dockerfile
FROM node

docker build . // get NodeJS app
docker run -it 2d840844f8e7 // get inside node container

docker run -it 2d840844f8e7 /bin/bash // ssh to node container (isolated server)
ls -l // list files in current directory
ps -ef // list all processes in RAM

create Dockerfile and copy flatris into container

docker build .
a new container 46d3f0d396c1 is created, logon to it:
docker run -it 46d3f0d396c1 /bin/bash
and we can see /flatris files in it

docker build . -t skillbox
docker run -it -p 3000:3000 skillbox // our app is accessible via http://localhost:3000 now

docker-compose.yml
docker-compose build
docker-compose up
docker-compose up -d // run as daemon
docker container prune // delete all stopped containers
docker image prune // delete all unnamed images
docker mi <image> // delete image name
