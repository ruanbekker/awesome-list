###  Docker Template Variables:

Service Name:

```
docker service create \
  --env "SERVICE_NAME={{.Service.Name}}" \
  --name helloworld \
  alpine /bin/sh -c 'echo $SERVICE_NAME'
```

```
docker service create \
  --name=coordinator \
  --env "SERVICE_NAME={{.Service.Name}}" \
  arangodb/arangodb /bin/sh -c 'arangod --server.authentication=false --server.endpoint tcp://0.0.0.0:8529 --cluster.my-address tcp://${SERVICE_NAME}:8529 --cluster.my-local-info ${SERVICE_NAME} --cluster.my-role COORDINATOR --cluster.agency-endpoint tcp://agency:8529 --log.file /var/log/arangodb3/arangod.log'
```

Task Slot:

```
docker service create --name mariadb-cluster \
	--network default \
	--replicas=1 \
	--mount type=volume,src=mariadb-cluster."{{.Task.Slot}}",dst=/var/lib/mysql \
	--env DB_SERVICE_NAME=mariadb-cluster \
	toughiq/mariadb-cluster:10.2
```

Others:

```
{{.Service.ID}}
{{.Service.Name}}
{{.Service.Labels}}
{{.Node.ID}}
{{.Node.Hostname}}
{{.Task.ID}}
{{.Task.Name}}
{{.Task.Slot}}
```

#### Docker Service PS

```
$ docker service ps api --format '{{.Name}} {{.CurrentState}}'
api.1 Running about an hour ago
```

#### Docker Service Inspect

Inspect the Service:

```
$ docker service inspect my-service
[
    {
        "ID": "abcdef",
        "Version": {
            "Index": 123
        },
        "CreatedAt": "2018-05-30T00:00:00.452848973Z",
        "UpdatedAt": "2018-05-30T00:00:00.457986437Z",
        "Spec": {
            "Name": "my-service",
            "TaskTemplate": {
                "ContainerSpec": {
                ...
                "LogDriver": {
                    "Name": "sumologic",
                    "Options": {
                        "sumo-compress": "false",
                        "sumo-sending-frequency": "500ms",
                        "sumo-url": "https://endpoint.sumologic.com/receiver/..."
                    }
                    ...
```

Inspect the LogDriver:

```
$ docker service inspect my-service --format='{{.Spec.TaskTemplate.LogDriver}}'
{sumologic map[sumo-compress:false sumo-sending-frequency:500ms sumo-url:https://endpointsumologic.com/receiver/...]}
```

Getting only the sumo-url value:

```
$ docker service inspect my-service -f '{{index .Spec.TaskTemplate.LogDriver.Options "sumo-url"}}'
https://endpoint.sumologic.com/receiver/...
```

Getting the Swarm Service and Task Name by inspecting the container:

```
$ docker inspect abc123def --format '{{index .Config.Labels "com.docker.swarm.task.name"}}'
my-app-ui.1.209jdwldi38jd
```

```
$ docker inspect abc123def --format '{{index .Config.Labels "com.docker.swarm.node.id"}}'
2093123jahas3d3
```

```
$ docker inspect abc123def --format '{{index .Config.Labels "com.docker.swarm.service.name"}}'
my-app-ui
```

Docs:
- https://docs.docker.com/engine/reference/commandline/service_ps/

