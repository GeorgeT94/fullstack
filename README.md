# fullstack
links to all repos required


front-end : 
runs at localhost:3000
https://github.com/tejanhu/final_project-frontend-app/tree/develop
```bash
  npm install
  npm start
```

producer : 
runs at localhost:
https://github.com/oli-loades/Producer/tree/dev
```bash
  mvn spring-boot:run
```
running producer also runs books api
books api at : localhost:8182/book/search/{term}

elastic search :     
```bash
 docker run -d -p 9200:9200 -p 9300:9300 -e "http.host=0.0.0.0" -e "transport.host=0.0.0.0" docker.elastic.co/elasticsearch/elasticsearch:6.3.0
 ```

glossary api: https://github.com/D1efe/programmingDictionary/tree/json




