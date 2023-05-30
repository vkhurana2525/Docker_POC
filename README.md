# Docker_POC
## Commands to install Docker
* sudo apt update
* sudo apt install apt-transport-https ca-certificates curl software-properties-common
* curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
* echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
* sudo apt update
* sudo apt install docker-ce docker-ce-cli containerd.io
* sudo service docker start
* sudo docker info
* sudo docker run hello-world
* sudo docker images(To view images present in docker)
We can pull the images from website 

## Commands to containerize Mysql in Docker
* First pull the mqsl from docker hub
  docker pull mysql
* Build the connection between docker   
  sudo docker run -d -p 3307:3306 --name mysqldb -e MYSQL_ROOT_PASSWORD=ttn -e MYSQL_DATABASE=test  mysql
* sudo docker logs mysqldb
* sudo docker ps -a (This tells what containers are running)
* Command to remove the container from docker
   sudo docker rm -f mysqldb
* To go into container in docker
  sudo docker exec -it container_id bash
  
