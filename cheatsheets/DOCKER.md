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
