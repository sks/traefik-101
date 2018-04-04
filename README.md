# Steps

1.  Start the service

Navigate to the [dashboard](http://localhost:8080/)

```
docker-compose up -d
```

2.  Check the proxy is working

```
curl -H Host:whoami.docker.localhost http://127.0.0.1:8090/
```

3.  Scale up instances of `whoami`

```
    docker-compose up --scale whoami=4 -d
```

4.  Using `ab` to some load testing

```
ab -H Host:whoami.docker.localhost -n 10000 -c 100 http://127.0.0.1:8090/
```
