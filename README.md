## Usage

### Multibroker on docker network

* UPDATE `KAFKA_ADVERTISED_HOST_NAME` to be your [docker host ip address](https://github.com/istresearch/scrapy-cluster/issues/140#issuecomment-475774738)

```
cd /kafka-docker
docker-compose -f docker-compose-single-broker.backend.yml up -d --scale kafka=3 --force-recreate
docker-compose -f docker-compose-single-broker.backend.yml down -v
```

### Multibroker on localhost

* Update the `KAFKA_ADVERTISED_HOST_NAME` in the `docker-compose-single-broker.scale.yml` by running `> ipconfig getifaddr en0`

```
> docker-compose -f docker-compose-single-broker.scale.yml up -d \
--scale kafka=3 --force-recreate --renew-anon-volumes

```

### Notes:

* [https://github.com/docker/compose/issues/4476#issuecomment-279399509](https://github.com/docker/compose/issues/4476#issuecomment-279399509)
* [https://github.com/docker/compose/issues/2127#issuecomment-428392434](https://github.com/docker/compose/issues/2127#issuecomment-428392434)