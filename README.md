# elasticsearch-study

## command
Install `7.15.1` by using docker.  
7.x is the last version supports without any certs and passwords.  
So, This version is proper for study.
```
docker run -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.15.1
```

Supporting versions: https://hub.docker.com/_/elasticsearch/tags?page=1
