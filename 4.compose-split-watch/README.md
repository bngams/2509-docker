# Resources

Original scenario here: https://docs.docker.com/compose/gettingstarted/#step-1-set-up

# Use compose watch

Use the [watch](https://docs.docker.com/compose/how-tos/file-watch/) option with docker compose

```
docker compose watch
[+] Running 2/2
 Container docs-redis-1 Created                                                                                                                                                                                                        0.0s
 Container docs-web-1    Recreated                                                                                                                                                                                                      0.1s
 Attaching to redis-1, web-1
 @watch enabled
...
```

# Split you compose files

Split the conf with two files infra.yml and compose.yaml.

In your compose.yaml file, add the include top-level attribute along with the path to the infra.yaml file.

````
docker compose up -d

Starting composetest_redis_1...
Starting composetest_web_1...

docker compose ps

       Name                      Command               State           Ports         
-------------------------------------------------------------------------------------
composetest_redis_1   docker-entrypoint.sh redis ...   Up      6379/tcp              
composetest_web_1     flask run                        Up      0.0.0.0:8000->5000/tcp
```