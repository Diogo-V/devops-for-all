# Notes about kubernetes details

Notes about kubernetes

## Notes

* There are 3 major components in the scheduling of pods:
  * The API server is the central component of a Kubernetes cluster and it runs on the master node.
  * The scheduler is also running on the master node. Its job is to watch for unassigned pods and assign them to a node that has available resources (CPU and memory) matching Pod requirements.
  * *Kubelet runs on each node*. Its primary function is to make sure that assigned pods are running on the node. It watches for any new Pod assignments for the node.

* All other components interact with API server and keep watch for changes. Most of the coordination in Kubernetes consists of a component writing to the API Server resource that another component is watching. The second component will then react to changes almost immediately.

* *Liveness probe* can be used to confirm whether a container should be running or not. If not running, kubernetes will kill the container and restart it

* The *Readiness probe* should be used as an indication that the service is ready to serve requests. When combined with Services construct, only containers with the readinessProbe state set to Success will receive requests.

* Almost everything in Kubernetes is operated using label selectors. It’s just that sometimes that is obscured from us.
