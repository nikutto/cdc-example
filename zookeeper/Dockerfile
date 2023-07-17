FROM quay.io/debezium/zookeeper:2.3

COPY zoo.cfg /zookeeper/conf/zoo.cfg

USER root
RUN microdnf -y install nc
