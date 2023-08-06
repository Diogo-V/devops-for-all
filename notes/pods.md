# Notes about pods

Contains common notes about pods.

## Notes

* The most common way of using pods is with a *container in a pod*. Pod is a wrapper around a container.
* We cannot tell Kubernetes to run a container. Instead, we ask it to create a Pod that wraps around a container.
* The `describe` sub-command returned details of the specified resource.
* All the processes (containers) inside a Pod share the same set of resources, and they can communicate with each other through localhost. One of those shared resources is storage.
* When we have multiple containers in a pod, we need to use a `-c` to choose the name of the container in a pod

## Common commands

* Delete a pod: `kc delete pod <pod name>`
* Get pods: `kc get pods`
* Create a pod from a file: `kubectl create -f <my yml script>`
* Get more output from a get pod: `kc get pods -o wide`
* Get more debug information from a pod `kc get pods -o yaml`
* Describe pod `kc describe pod <my pod name>`
* Exec into pod `kubectl exec <my pod name> -- ps aux`
* Multiple containers in a pod `kubectl exec -it -c <container name> <pod name> -- ps aux`
* Show labels attached to a pod `kc get pods --show-labels`
