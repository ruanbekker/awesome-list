## Provisioning 

### Setup Kubernetes 

- [Kubernetes on Ubuntu](https://gist.github.com/ruanbekker/38a38aea5f325f7fa4a19e795ef4f0d0)
- [[K3s](https://github.com/rancher/k3s#quick-start)

## Get Resource Information


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

### Pods

* Pods: The single smallest interactable unit in Kubernetes. 
* Pod can be comprimised of multiple containers that will form a unit deployed on a single node together
* Pod receives one IP which is shared between containers

```
$ kubectl get pods
$ kubectl get pods --all-namespaces
$ kubectl get pods --namespace kube-system
$ kubectl get pods --namespace --output yaml
$ kubectl get pods -o wide
$ kubectl describe pods --all-namespaces
$ kubectl get pods --show-labels --all-namespaces
$ kubectl get pods --selector app=svclb-traefik --namespace kube-system
$ kubectl get pod svclb-traefik-79556fd88b-p6qp9 --namespace kube-system
$ kubectl get pod svclb-traefik-79556fd88b-p6qp9 --namespace kube-system -o yaml --export
$ kubectl get pod svclb-traefik-79556fd88b-p6qp9 --namespace kube-system -o yaml --export > exported.yml

```
