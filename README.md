# Kubernetes Local Development

Presentation of useful tools to develop with Kubernetes locally

## Local cluster

- [Minikube](https://github.com/kubernetes/minikube) : Run Kubernetes locally on Windows, Mac or Linux.

- [MicroK8S](https://microk8s.io/) : A single package of k8s that installs on 42 flavours of Linux.

- [kubeadm-dind-cluster](https://github.com/kubernetes-sigs/kubeadm-dind-cluster) : A Kubernetes multi-node test cluster based on kubeadm.

## Remote cluster

### Improve K8S command line UX
  
- [kubectx+kubens](https://github.com/ahmetb/kubectx) : Fast way to switch between clusters and namespaces
- [kube-shell](https://github.com/cloudnativelabs/kube-shell) : An integrated shell for working with the Kubernetes CLI
- [kube-prompt](https://github.com/c-bata/kube-prompt) : An interactive kubernetes client featuring auto-complete 
- [K9S](https://github.com/derailed/k9s)
- [kube-ps1](https://github.com/jonmosco/kube-ps1) : Kubernetes prompt info for bash and zsh
- [Stern](https://github.com/wercker/stern) : Multi pod and container log tailing
- [Kail](https://github.com/boz/kail) : Kubernetes log viewer
- [KubeSpy](https://github.com/pulumi/kubespy) : Tools for observing Kubernetes resources in real time
```
kubectl create ns gd
kubens gd

# In one shell (keep it displayed)
kubespy trace deploy gd/nginx-deployment
# In another shell
kubectl create -f https://k8s.io/examples/controllers/nginx-deployment.yaml 

# In one shell (keep it displayed)
kubespy status v1 Pod gd/nginx
# In another shell
kubectl create -f https://github.com/pulumi/kubespy/raw/master/examples/trivial-pulumi-example/yaml/nginx.yaml

# In one shell (keep it displayed)
kubespy status v1 Pod gd/nginx
# In another shell
kubectl create -f https://github.com/pulumi/kubespy/raw/master/examples/trivial-pulumi-example/yaml/nginx.yaml
```
- [Krew](https://github.com/GoogleContainerTools/krew) : Package manager for "kubectl plugins"

### Development

- [kubefwd](https://github.com/txn2/kubefwd) : Bulk port forwarding Kubernetes services for local development
- [Skaffolfd](https://github.com/GoogleContainerTools/skaffold) : Easy and Repeatable Kubernetes Development
- [Telepresence](https://www.telepresence.io/) : Debug your Kubernetes service locally
- [KubeSquash](https://github.com/solo-io/kubesquash/blob/master/README.md)

### GUI/TUI

- [K8S Dashboard](https://github.com/kubernetes/dashboard)
- [Kube-ops-view](https://github.com/hjacobs/kube-ops-view) : Read-only system dashboard for multiple K8s clusters


## Useful links

https://cloud.google.com/blog/products/containers-kubernetes/easier-kubernetes-development-from-your-laptop
https://medium.com/@wso2tech/multi-node-kubernetes-cluster-with-vagrant-virtualbox-and-kubeadm-9d3eaac28b98
