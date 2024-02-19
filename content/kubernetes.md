---
created_at: 2022-12-21
type: technology
aliases: [k8s]
---

# Kubernetes

- Used to run a bunch of various [[docker]] containers, and have them communicate with each other.
- Deployments.
	- For scaling, can make sure that a certain number of pods are running an image.
	- It can also manage the upgrading of pods.
	- Defined through a configuration file.
- Services provide networking between pods, and allow ports to be reached from the outside world.
	- Cluster IP services sets up communication for the nodes in a cluster to communicate with each other.
		- Within our services, we can request to other services by using `http://` followed by the name of the service.
	- Node ports allow a pod to be accessible from outside of the cluster *(usually only used for dev purposes).*
	- Load balancers route and expose a cluster’s pods to the outside world.
		- The load balancer service isn’t actually created inside our cluster.
		- It directly tells AWS, GCP, Azure to make a load balancer on the cloud service.
	- Ingress/Ingress Controller.
		- Is a service that runs inside the cluster.
		- Has routing rules for redirecting a request to certain pods.

## Common pod commands.

```sh
kubectl apply -f <config-file>
```

- Used to spin up a pod based on the configuration file.

```sh
kubectl get pods
```

- List all pods.

```sh
kubectl exec -it <pod-name> sh
```

- Open a shell into the running pod instance.

```sh
kubectl logs <pod-name>
```

- Print logs from a pod.

```sh
kubectl delete pod <pod-name>
```

- Delete a pod.

```sh
kubectl describe pod <pod-name>
```

- Gives you some info about the pod, including an event log.

## Common deployment commands.

- Basically the same as for pods, but just replace `pod` with `deployment`.

## Updating a deployment.

- Deployment configuration should be set to use the latest tag of our image.
- We should update our image on version latest, upload it to Docker Hub.
- Then just run this:

```sh
kubectl rollout restart deployment <depl-name>
```
