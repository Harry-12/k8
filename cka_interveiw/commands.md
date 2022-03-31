Run a simple nginx deployment:

>View the deployments in your cluster:     
      kubectl run nginx --image=nginx
 

> View the pods in the cluster:     
kubectl get deployments


> Use port forwarding to access a pod directly:   kubectl get pods


>Get a response from the nginx pod directly: 
kubectl port-forward $pod_name 8081:80

> View the logs from a pod:   
curl --head http://127.0.0.1:8081

> Run a command directly from the container:
kubectl logs $pod_name

> Create a service by exposing port 80 of the nginx deployment:          
kubectl exec -it $pod_name -- nginx -v

> List the services in your cluster:   
kubectl expose deployment nginx --port 80 --type NodePort

> Get a response from the service:   
kubectl get services

> List the nodes' status:     
curl -I localhost:$node_port

> View detailed information about the nodes:
kubectl get nodes

> View detailed information about the pods:
kubectl describe nodes


All Kube Commands: https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#-strong-getting-started-strong-