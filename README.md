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

#### Minikube

- Installtion
```shell=
brew install minikube
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

### Setup Jenkins



## Reference

- [Installing Elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html)
