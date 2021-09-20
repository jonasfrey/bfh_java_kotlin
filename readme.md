# install docker engine !
https://docs.docker.com/engine/install/#server

# install docker compose 

https://docs.docker.com/compose/install/

# setup BIOS/UEFI
if you didnt already: docker needs settings for virtualization, please checkout your mainboard 


# docker-compose build
`sudo docker-compose build`

# docker-compose up
to run the virtual docker 
`sudo docker-compose up`

# check docker status / if docker container is running
`sudo docker ps`


# connect/login/open bash in the virtual docker 

list all running containers 
`sudo docker ps`

connect to certain container    

`sudo docker-exec -it {CONTAINER ID or NAME} bash`
sometimes this works as well
`sudo docker-exec -it {CONTAINER ID or NAME} sh`


# clone your bfh repos
in this folder , the cloned repos will be kind of git submodules i think
`git clone {git_repo_url}`


# how to run java
## login to container 
`sudo docker exec -it bfh_ubuntu_1 bash`
## navigate to file 
`cd {file_location}`
## compile 
`javac {filename.java}`
## run 
`java {filename.java}`

# how to run kotlin 
## login to container 
`sudo docker exec -it bfh_ubuntu_1 bash`
## navigate to file 
`cd {file_location}`
##  create .jar file 
`kotlinc {input_filename.kt} -include-runtime -d {desired_output_filename.jar}`
##  run .jar file  
`java -jar hello.jar`
