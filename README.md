# Docker 3 tier architecture project 


install docker in server


mkdir /data       # this directory is linked to sql container

docker network create --driver bridge --subnet  10.1.2.0/24 mybridge     # create your own bridge network #mybridge is network name


docker run -dit --name mywp -p 8080:80 --network mybridge wordpress 


docker run -dit --name db --network mybridge -e MYSQL_ROOT_PASSWORD=Gh@777 -e MYSQL_DATABASE=mydb -e MYSQL_USER=Ghn -e MYSQL_PASSWORD=Gh@111 -v /data:/var/lib/mysql mysql

publicip:8080  

word press setup page



wordpress dashboard
![welcome](https://user-images.githubusercontent.com/111174366/211018304-f34668ce-35be-40c3-b14e-8631470c668b.png)



sample post
![happy](https://user-images.githubusercontent.com/111174366/211018411-00f87040-e1bf-4cd3-a8ec-ea80daf769a7.png)
