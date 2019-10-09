Make sure given volume exist in host.

For Data: `/home/ubuntu/neo4j/data`
For Plugins: `/home/ubuntu/neo4j/plugins`
For Configuration: `/home/ubuntu/neo4j/conf`

Configuration volume must have default configuration file.

Or you can use `named volumes`


docker stack deploy neo4j --compose-file docker-compose.yml