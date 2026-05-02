# My personal monitoring infrastructure

## Get k8s working first

[K3s](https://k3s.io/)

```shell
curl -sfL https://get.k3s.io | sh -
sudo cp /etc/rancher/k3s/k3s.yaml ~/.kube/config
sudo apt install kubectx
```

## Loki config

validate config:

```shell
docker run --rm -v $(pwd)/k8s/loki-config.yml:/etc/loki/config.yaml \
  grafana/loki:latest \
  -config.file=/etc/loki/config.yaml \
  -verify-config
```

```shell
kubectl create configmap loki-config --from-file=k8s/loki-config.yml
```
