# POC of Loki for school

## Getting Started

You have to configure your local IP in the `datasource.yaml`, it will configure your datasource in grafana.
```yaml
url: http://192.168.1.10:3100
```

And in the `promtail-config.yaml` to allow your promtail agent to talk to your loki instance. 
```yaml
client:
  url: http://192.168.1.10:3100/loki/api/v1/push
```

After that, just `up` your docker-compose with: 
```bash
docker-compose up -d
```