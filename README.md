# What is this?

Practicing CDC using debezium.

# Memo

- Used tutorial (https://debezium.io/documentation/reference/2.3/tutorial.html)
  - But, its tutorial was for plain docker. This is triesome.
  - Use docker compose.
  - Kafka stops if zookeeper not working. So, introduce health check for zookeeper.
  - Connect have enough timeout, so we don't need health check for kafka.
