# elasticsearch_example
Example for setup a elasticsearch.

## Objective

Build a template for quick and easy launching for the elasticsearch and kibana. Including the sample dataset and kibana configurations.

It would be easy to launch on the docker-compose system. Furthermore, kubernetes would help with mulitple node maintain.


## Set up your elasticsearch with docker

### Pull the elasticsearch image

```shell=
docker pull docker.elastic.co/elasticsearch/elasticsearch:8.13.0
```

## Run the elasticsearch and kibana on the docker-compose

```shell=
docker-compose up
```

### Set up K8S

For work on a cloud infrastructure. The K8S would be a great tool for deploying mulitple node services.

Here are few step for users to setup a cluster on local machine quickly.

#### Helm

brew install helm
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update

helm install kube-prometheus-stack prometheus-community/kube-prometheus-stack --create-namespace --namespace monitoring
helm install prometheus-elasticsearch-exporter prometheus-community/prometheus-elasticsearch-exporter --set es.uri=http://elasticsearch:9200 --namespace monitoring


#### Minikube

- Installtion
```shell=
brew install minikube
```

- Start
```shell=
minikube start
```

```shell=
minikube start --mount --mount-string={Mount Path}
```

- Stop
```shell
minikube stop
```

**Opertions**

- Check status
```shell=
minikube status
```

- Start Minikube
```shell=
minikube start
```

- Stop Minikube
```shell=
minikube stop
```

- Access the minikube by ssh
```shell=
minikube ssh
```

- Check the informations on the Minikube dashboard
```shell=
minikube dashboard
```

#### Kubectl

Command line tool for K8S.

- Check if the Kubectl are already installed on your machine.
```shell=
kubectl version --client
```

- Installtion
```shell=
brew install kubectl
```
##### General Error

* How to descirble error

```shell=
kubectl describe pod
```


**Container image "docker.elastic.co/elasticsearch/elasticsearch:8.13.0" already present on machine**

### Setup Jenkins



## Reference

- [Installing Elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html)
