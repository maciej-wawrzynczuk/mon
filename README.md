# My personal monitoring infrastructure

## Get k8s working first

[K3s](https://k3s.io/)

```shell
curl -sfL https://get.k3s.io | sh -
sudo cp /etc/rancher/k3s/k3s.yaml ~/.kube/config
sudo apt install kubectx
```
