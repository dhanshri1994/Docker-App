# Docker-App

deploy.yaml--- not of any use/not working.

In this project I built a jenkins freestyle project to start build once he commit happens in git repo. Then jenkins will build the docker image using Dockerfile
Once it is built it will push it to my public dockerhub repo and then it will run an ansible playbook that will cpoy docker-compose file to webserver and also
run the container using docker-compose up command.

Few prereq:
1. There are ywo servers needed for this one is jenkins and other one is webserver
2. I installed jenkins, ansible, git and docker on jenkins server
3. I installed docker and  docker-compose on web server. But same can be done using ansible-playbook
4. Need to create entry of webserver in /etc/ansible/hosts file
5. Need to disable host ssh key check in /etc/ansible/ansible.cfg file
6. Server ip is hard-coded in index.html and server.js file that nneds to be changed as per your ip of webserver

