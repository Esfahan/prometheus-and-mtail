# Prometheus and mtail
To test the mtail synatx.

## Usage

```
$ docker-compose -f docker-compose-prometheus.yaml up -d --build
$ docker-compose -f docker-compose-mtail.yaml up -d --build
```

Create rules into mtail/example.mtail

Write a log line like this.

```
echo "[ERROR] This is an error." >> logs/example.log
```

Check a result of `rate(error_count[5m])` on Prometheus.

### Prometheus
http://localhost:9090

### mtail
http://localhost:3903

## Related
https://gist.github.com/Esfahan/86f56ee6a2178296be49ab3cb1a3018e
