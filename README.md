# Prometheus + Grafana

### Inici:

```
docker-compose up -d
```

### Reload prometheus:

Sebla que no pero aquesta es molt fina. Aquesta senyal fara el reload de la configuracio.

```sh
docker exec prometheus killall -HUP prometheus
```

Reiniciar contenidor enter. Es mes lent i es molt mes agresiu.

```sh
docker-compose restart prometheus
```
