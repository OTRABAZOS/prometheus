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

Un cop actualitzat el worker al mysql, reinicialitzar el sync de les aranyes i la meitat dels nodes
entrem al servidor de trawling

pm2 restart 0 (sync)
pm2 restart 1 2 3 ... (els que no estiguin dins el cron)
