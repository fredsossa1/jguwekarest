# JGU WEKA Rest Service

Here is a summary of the commands to be executed to consult the monitoring and
"scaler" the WekaRest app

## Start services
To have Weka's monitoring, just start the services with the following command, from the root of the project:

```
$ docker-compose up
```

## Monitoring
Monitoring is added to the docker-compose file. Once started, it is possible to access the monitoring via the address [http: // localhost: 9090] (http: // localhost: 8080). This page is served by the Prometheus service.

To see the percentage of CPU usage for a single container, the following command can be inserted into the Prometheus query line. Replace <container_name> with the name of the container.

`Spleen (container_cpu_user_seconds_total {name = <container_name>} [10s])` `

This query smooths the retrieved data by averaging the last 10 seconds. The specification of the container name can be omitted.

To get the name of the docker containers, use the following command (the contents must be started):

```
$ docker-compose ps
```

## Scaling
In order to scale the application, it is possible to start the services by adding the scale flag:

```
$ docker-compose up --scale jguweka = <numberReplicates>
```

The docker-compose file includes a load-balancer that will automatically dispatch queries to different replicas of jguweka.
