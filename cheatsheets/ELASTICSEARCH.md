# Elasticsearch Cheatsheet

- [Using cURL](#using-curl)
  - [Cluster Health](#health-with-curl)
  - [Reindex](#reindex-using-curl)
  - [Update Replica Shards](#update-replicas-curl)
  - [Snapshots](#snapshots-with-curl)
- [using Python](#python-library)
  - [Ingest](#ingest-using-python)


## Using Curl

#### Health with Curl

View the cluster status:

```
curl -s -XGET 'http://127.0.0.1:9200_cluster/health?pretty'
```

Check all indices in yellow status:

```
curl -s -XGET 'http://127.0.0.1:9200/_cat/indices?v&health=yellow'
```

View recovery process:

```
curl -s -XGET 'http://127.0.0.1:9200/_cat/recovery?detailed&h=index,stage,time,bytes_percent'
```

#### Reindex using Curl

Reindex source index to target index:

```
$ curl -XPOST -H 'Content-Type: application/json' 'http://127.0.0.1:9200/_reindex' -d '
  {
    "source": {
      "index": ["my-metrics-2019.01.03"]
    }, 
    "dest": {
      "index": "archived-metrics-2019.01.03", 
    }
}'
```

Reindex multiple source indices to one target index:

```
$ curl -XPOST -H 'Content-Type: application/json' 'http://127.0.0.1:9200/_reindex' -d '
  {
    "source": {
      "index": ["my-metrics-2019.01.03", "my-metrics-2019.01.04"]
    }, 
    "dest": {
      "index": "archived-metrics-2019.01", 
    }
}'
```

Reindex only missing documents from source to target index. You will receive conflicts for existing documents, but the proceed value will ignore the conflicts.

```
$ curl -XPOST -H 'Content-Type: application/json' 'http://127.0.0.1:9200/_reindex' -d '
  {
    "conflicts": "proceed", 
    "source": {
      "index": ["my-metrics-2019.01.03"]
    }, 
    "dest": {
      "index": "archived-metrics-2019.01.03", 
      "op_type": "create"
    }
}'
```

Reindex filtered data to a target index, by using a query:

```
$ curl -XPOST -H 'Content-Type: application/json' 'http://127.0.0.1:9200/_reindex' -d '
  {
    "source": {
      "index": "my-metrics-2019.01.03",
      "type": "log",
      "query": {
        "term": {
          "status": "ERROR"
        }
      }
    },
    "dest": {
      "index": "archived-error-metrics-2019.01.03"
    }
}'
```

Reindex the last 500 documents based on timestamp to a target index:

```
$ curl -XPOST -H 'Content-Type: application/json' 'http://127.0.0.1:9200/_reindex' -d '
  {
    "size": 500, 
    "source": {
      "index": "my-metrics-2019.01.03",
      "sort": {
        "timestamp": "desc"
      }
    }, 
    "dest": {
      "index": "archived-last500-metrics-2019.01.03", 
      "op_type": "create"
    }
}'
```

Reindex only specific fields to a target index:

```
$ curl -XPOST -H 'Content-Type: application/json' 'http://127.0.0.1:9200/_reindex' -d '
  {
    "source": {
      "index": "my-metrics-2019.01.03",
      "_source": [
        "response_code",
        "request_method",
        "referral"
      ]
    }, 
    "dest": {
      "index": "archived-subset-metrics-2019.01.03"
    }
}'
```

#### Update Replicas Curl

Increase/Decrease the number of Replica Shards using the Settings API:

```
curl -XPUT -H 'Content-Type: application/json' 'http://127.0.0.1:9200/my-index-2018.12.31/_settings' \
  -d '{"index": {"number_of_replicas": 1, "refresh_interval": "30s"}}'
```

#### Snapshots with Curl

View snapshot repositories:

```
curl -s -XGET 'http://127.0.0.1:9200/_snapshot?pretty'
```

View snapshots under repository:

```
curl -s -XGET 'http://127.0.0.1:9200/_cat/snapshots/index-backups?v'
# id, status, start_epoch, start_time, end_epoch, end_time, duration, indices, successful_shards, failed_shards, total_shards
```

Create a snapshot with all indices and wait for completion:

```
curl -XPUT -H 'Content-Type: application/json' 'http://127.0.0.1:9200/_snapshot/index-backups/my-es-snapshot-latest?wait_for_completion=true'
```

View snapshot status:

```
curl -s -XGET 'http://127.0.0.1:9200/_cat/tasks?detailed'
# cluster:admin/snapshot/create ..
```

## Python Library

#### Ingest using Python

Create a document and specify a `id`:

```
res = es.index(index="test-index", doc_type='tweet', id=1, body=doc)
```
