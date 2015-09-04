# ELK-Docker
Dockerized ELK stack for Stackato

##Prerequisites
- Install Docker Engine https://www.docker.com/docker-engine and Docker Compose https://www.docker.com/docker-compose on the machine hosting the ELK stack.

- Setup a Stackato log drain on your Stackato cluster using the following command:
```
$ kato log drain add [NAME] -p  apptail -f '{{.app_name}} : {{.text}}' > all-apps udp://[IP_ADDRESS_OF_ELK_HOST]:5500
```

##Quickstart
On the machine hosting the ELK stack enter the follwing commands:
```
$ git clone 
$ cd elk-docker
$ docker-compose up
```

Open your browser at [IP_ADDRESS_OF_ELK_HOST]:8484

##Elasticsearch
https://hub.docker.com/r/library/elasticsearch/

##Logstash
https://hub.docker.com/r/library/logstash/

##Kibana
https://hub.docker.com/r/library/kibana/
