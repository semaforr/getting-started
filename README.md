# Getting started
Scripts to get semaforr running in your k8s cluster

## 1 Set up priviledges

Add a clusterrolebinding to allow your user to perform some admin tasks

```bash
kubectl create clusterrolebinding cluster-admin-binding --clusterrole=cluster-admin --user=<<your user email>
```

## 2 Create the namespace
```bash
kubectl apply -f 1-namespace.yaml
```

## 3 Deploy ActiveMQ
```bash
kubectl apply -f 2-activemq.yaml
```

## 4 Deploy the event hub
```bash
kubectl apply -f 3-event-hub.yaml
```