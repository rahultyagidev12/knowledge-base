- To setup a local cluster for kubernetes it's recommended to use [kind](https://kind.sigs.k8s.io/)

- Install kind using the steps in the above documentation

- Define your cluster with required number of control nodes and worker nodes, see the kind.yaml file for an example

- Start the cluster using kind and the yaml file:

```bash
kind create cluster --config kind.yaml   
```

- Add a default namespace to the current context so you can run kubectl comamnds with the current cluster

```
kubectl config set-context --current  --current --namespace default 
```

- Add a pod definition file, see the go_service.yaml for an example golang image

- Run the pod using the apply command of kubectl
```
kubectl Applyfg -f go_service.yaml  
```
