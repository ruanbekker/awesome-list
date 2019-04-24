## Get Resource Information

### Setup Kubernetes 

- [Kubernetes on Ubuntu](https://gist.github.com/ruanbekker/38a38aea5f325f7fa4a19e795ef4f0d0)
- [[K3s](https://github.com/rancher/k3s#quick-start)

### Nodes

Getting information about nodes:

```
$ kubectl get nodes
$ kubectl get nodes -o wide
$ kubectl describe nodes
$ kubectl get nodes -o yaml
$ kubectl get node --selector=[label_name]
$ kubectl get nodes -o jsonpath='{.items[*].status.addresses[?(@.type=="External IP")].address}'
$ kubectl top node [node_name]
```
