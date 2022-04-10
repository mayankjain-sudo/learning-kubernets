# Commands
## To get pod list
kubectl get pods
## To get deployments
kubectl get deployments
## To get Cluster-IP, Name of service
kubectl get services
## To get pod IP, Status, node
kubectl get pod podname -o wide
## To deploy pod from yml file 
kubectl create -f nginxpod.yaml
## To change or edit in running pod, change in the yaml file then run.
kubectl apply -f nginxpod.yaml
## To create YAML file from command and run a pod 
kubectl run nginx --image=nginx --dry-run=client -o yaml > nginx-definition.yaml
