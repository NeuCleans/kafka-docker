## Usage

* UPDATE `KAFKA_ADVERTISED_HOST_NAME` to be your [docker host ip address](https://github.com/istresearch/scrapy-cluster/issues/140#issuecomment-475774738)

```
cd /kafka-docker
docker-compose -f docker-compose-single-broker.backend.yml up -d --scale kafka=3
docker-compose -f docker-compose-single-broker.backend.yml down
```