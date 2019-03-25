## Usage

```
cd /kafka-docker
docker-compose -f docker-compose-single-broker.backend.yml up -d --scale kafka=3
docker-compose -f docker-compose-single-broker.backend.yml down
```