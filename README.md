Install kafka using Docker and docker-compose

Command for kafka :
# $ docker compose -f docker-compose.yml up -d
# docker exec -it kafka /bin/sh
# ls
bin  boot  dev  etc  home  kafka  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
# cd opt
# ls
kafka  kafka_2.13-2.8.1  overrides
# cd kafka_2.13-2.8.1
<-- create topic -->
# kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic quickstart
<-- produce message -->

# kafka-console-producer.sh --topic quickstart --bootstrap-server localhost:9092
<-- consume message -->
# kafka-console-consumer.sh --topic location-update-topic --from-beginning --bootstrap-server localhost:9092
 
