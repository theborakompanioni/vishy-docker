vishy-docker
=====

a simple openmrc demo application

- [cadvisor](https://github.com/google/cadvisor)
- [grafana](https://github.com/grafana/grafana)
- [influxdb](https://www.influxdata.com/time-series-platform/influxdb/)
- [kafka](https://kafka.apache.org/)
- [zookeeper](https://zookeeper.apache.org/)

# getting started
```
> git clone https://github.com/theborakompanioni/vishy-docker.git
> cd vishy-docker
> docker-compose up --build
```

# environment

## metrics
- grafana: [http://localhost:9000/](http://localhost:9000/)
- influxdb: [http://localhost:8083/](http://localhost:8083/)

## monitoring
- cadvisor: [http://localhost:8082/](http://localhost:8082/)

## ui
- vishy-ui: [http://localhost:8080/](http://localhost:8080/)
