# Notes about K3D

To install k3d: `brew install k3d`.
The command `kubectl` will be shortened to `kc`.

## Common commands

* Creating a cluster: `k3d cluster create <name of the cluster>`
* Checking all running containers in a node: `docker exec -it <name of the node> ctr container ls`
* List current clusters: `k3d cluster list`
* Stop all clusters: `k3d cluster stop --all`
* Start cluster: `k3d cluster start <name of the cluster>`
* Delete everything: `k3d cluster delete <name of the cluster> --all`
