# kubernetes

### Terms
- **Node** Is a worker machine - where the kubernetes will run the containers
- **Cluster** Set of nodes set together - this way if one node failed, the application will be accessible from a different node
- **Master** node responsible for manging to cluster
- **Kubernetes Components**
	- *API Server* The interface to kubernetes
	- *etcd* Key Value store to store all data used to manged the cluster
	- *Scheduler* Responsible for finding the best nodes to run pods
	- *Controller* The brain behind the orchestrator. It watch the state of the cluster and make changes where it needed, in order to get to the desired state 
	- *Container Runtime* The software that runs the containers (Like Docker)
	- *kubelet* The agent that runs on each node on the cluster. It responsible for the pods will run on the node as expected.

# Mater vs Worker Nodes
![alt text](attachments/master-vs-worker-nodes.png "Logo Title Text 1")

## Common comands
- `kubectl get pod -o wide` get all pods with extract details
- `kubectl run redis --image=redis123 --dry-run=client -o yaml > pod.yaml` create yaml file from run command (the dry-run parameter is for not executing the command on cluster)
- `kubectl describe pod myapp-pod` get full description of the pod