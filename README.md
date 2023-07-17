# What is this?

Practicing CDC using debezium.

# Memo

- Used tutorial (https://debezium.io/documentation/reference/2.3/tutorial.html)
  - But, its tutorial was for plain docker. This is triesome.
  - Use docker compose.
  - Kafka stops if zookeeper not working. So, introduce health check for zookeeper.
  - Connect have enough timeout, so we don't need health check for kafka.
- Use following to connect to mysql
```
curl -i -X POST -H "Accept:application/json" -H "Content-Type:application/json" localhost:8083/connectors/ -d '{ "name": "inventory-connector", "config": { "connector.class": "io.debezium.connector.mysql.MySqlConnector", "tasks.max": "1", "database.hostname": "mysql", "database.port": "3306", "database.user": "debezium", "database.password": "dbz", "database.server.id": "184054", "topic.prefix": "dbserver1", "database.include.list": "inventory", "schema.history.internal.kafka.bootstrap.servers": "kafka:9092", "schema.history.internal.kafka.topic": "schemahistory.inventory" } }'
```
