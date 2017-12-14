# Current features

# Preparation

## Requirements

* Python 2.7

## Install Python modules

```
$ pip install -r requirements.txt
Successfully installed Jinja2-2.8.1 MarkupSafe-1.0 PyYAML-3.12 ansible-2.2.2.0 asn1crypto-0.22.0 
awscli-1.11.70 botocore-1.5.33 cffi-1.10.0 colorama-0.3.7 cryptography-1.8.1 
docutils-0.13.1 enum34-1.1.6 futures-3.0.5 idna-2.5 ipaddress-1.0.18 
jmespath-0.9.2 netaddr-0.7.19 paramiko-2.1.2 pyasn1-0.2.3 pycparser-2.17 
pycrypto-2.6.1 python-dateutil-2.6.0 rsa-3.4.2 s3transfer-0.1.10
```

## Install binaries

Install kube-aws and kubectl binaries.

List of binaries:
* kube-aws
* kubectl

```
$ ./scripts/install-kube-binaries.sh
```

## Deploy kubernetes cluster

The main deployment procedure is being started by the following script.
It creates all required assets and deploys a new kubernetes cluster to AWS.

```
$ ./scripts/deploy-kubernetes-cluster.sh
```

## Switch kubectl context to the current kubernetes cluster

```
$ ./scripts/switch-kubectl-context.sh
```

## Get cluster information

Kubernetes-dashboard has own web interface.
The rest applications are API servers with no web interface.

```
$ kubectl cluster-info
Kubernetes master is running at https://35.158.72.194.xip.io
Heapster is running at https://35.158.72.194.xip.io/api/v1/proxy/namespaces/kube-system/services/heapster
KubeDNS is running at https://35.158.72.194.xip.io/api/v1/proxy/namespaces/kube-system/services/kube-dns
kubernetes-dashboard is running at https://35.158.72.194.xip.io/api/v1/proxy/namespaces/kube-system/services/kubernetes-dashboard
```
