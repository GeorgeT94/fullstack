# fullstack
## links to all repos required


## front-end : 
### runs at localhost:3000
https://github.com/tejanhu/final_project-frontend-app/tree/develop
```bash
  npm install
  npm start
```

## producer : 


## elastic search :  
needs to be run first
first
```bash
  sudo sysctl -w vm.max_map_count=262144
  ```
then
```bash
 docker run -d -p 9200:9200 -p 9300:9300 -e "http.host=0.0.0.0" -e "transport.host=0.0.0.0" docker.elastic.co/elasticsearch/elasticsearch:6.3.0
 ```
 
### runs at localhost:8182
https://github.com/oli-loades/Producer/tree/dev
```bash
  mvn spring-boot:run
```
### running producer also runs books api
books api at : localhost:8182/book/search/{term}

## questions api:
https://github.com/oli-loades/question/blob/master/src/main/java/com/qa/Application.java

## glossary api: 
https://github.com/D1efe/programmingDictionary/tree/json

## rabbit mq
```bash
  docker run -d --hostname my-rabbit --name some-rabbit -p 15672:15672 -p 5672:5672 rabbitmq:3-management
  ```
  
## consumer
https://github.com/oli-loades/Consumer/tree/master

## jbossfuse apache camel:
https://github.com/GeorgeT94/cxfrs-routing

### download jboss fuse 6.3
in cxfrs-routing:
```bash
mvn clean install 
  ```


### in jboss fuse:
```bash
   install wrap:mvn:org.apache.commons.dbcp/dbcp/4.1
   ```
download http://search.maven.org/remotecontent?filepath=commons-dbcp/commons-dbcp/1.4/commons-dbcp-1.4.jar
place commons jar file in jboss 'deploy' folder

copy mysql driver from m2 directory to fuse 'deploy' folder
run ,mysql database
```bash
  docker run -p 3306:3306 --name trainer-mysql -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=trainer -e MYSQL_USER=trainer_user -e  MYSQL_PASSWORD=trainer_pass -d mysql:5.6
  ```
### create the table used to save messages into
```bash
  sudo docker exec -it trainer-mysql bash -l
  mysql -uroot -ppassword
  use trainer
  CREATE TABLE messages (message VARCHAR(255))\g
  ```
  





