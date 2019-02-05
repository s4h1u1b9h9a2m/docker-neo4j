# Neo4j Docker Setup

## Standalone Cluster

### For details
Check ReadMe of Neo4j Standalone.

### To Run
```
docker stack deploy neo4j --compose-file Neo4j\ Standalone/docker-compose-cores.yml
```

## Causal Cluster (Pending)

For Casual Cluster, neo4j require at least 3 instances. 

### Neo4j
```
docker stack deploy neo4j --compose-file Neo4j\ Causal\ Cluster/docker-compose-cores.yml
```

### Nginx
```
docker stack rm nginx
docker stack deploy nginx --compose-file Nginx/docker-compose.yml
```

### HA Proxy
```
docker stack deploy haproxy --compose-file HAProxy/docker-compose.yml
```

## Grafana
For monitoring Neo4j
```
docker stack deploy grafana --compose-file Grafana/docker-compose.yml
```

## Docker instructions

### To Run as Service
```
docker stack deploy neo4j --compose-file docker-compose.yml
```

### To Run as Container
```
docker-compose up
```