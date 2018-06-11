# Graylog on Docker

This configuration builds a Graylog, ElasticSearch and Kafka setup in a Docker topology. Graylog is an enterprise log management tool which many people liken with the ELK stack. Although it shares some similarities, such as storing data as ElasticSearch indexes, that's where the similaries end. Metadata is stored in MongoDB.

## Running the cluster

    $ git clone https://github.com/jamesattard/graylog-docker
    $ cd graylog-docker
    $ docker-compose up


## Troubleshooting

If you have trouble running the ElasticSearch cluster, you might need to increase the memory limits. It depends on the operating system that you are using, but for a Centos 7 setup, you might need to do something like this:

    $ sudo sysctl -w vm.max_map_count=262144
