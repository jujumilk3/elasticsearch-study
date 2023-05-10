# elasticsearch-study

## command
### install
Install `7.15.1` by using docker.  
7.x is the last version supports without any certs and passwords.  
So, This version is proper for study.
```
docker run -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.15.1
```

Supporting versions: https://hub.docker.com/_/elasticsearch/tags?page=1

### check status
```
 % curl -X GET "localhost:9200"
{
  "name" : "4f981f80cdf7",
  "cluster_name" : "docker-cluster",
  "cluster_uuid" : "axLxNqEpTraVlluFEo73Rg",
  "version" : {
    "number" : "7.15.1",
    "build_flavor" : "default",
    "build_type" : "docker",
    "build_hash" : "83c34f456ae29d60e94d886e455e6a3409bba9ed",
    "build_date" : "2021-10-07T21:56:19.031608185Z",
    "build_snapshot" : false,
    "lucene_version" : "8.9.0",
    "minimum_wire_compatibility_version" : "6.8.0",
    "minimum_index_compatibility_version" : "6.0.0-beta1"
  },
  "tagline" : "You Know, for Search"
}
```
```
% curl -X GET "localhost:9200/_cat/health?v&pretty"
epoch      timestamp cluster        status node.total node.data shards pri relo init unassign pending_tasks max_task_wait_time active_shards_percent
1683730403 14:53:23  docker-cluster green           1         1      1   1    0    0        0             0                  -                100.0%
```