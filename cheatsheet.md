# Basic Commands
### To get pod list
kubectl get pods
### To get deployments
kubectl get deployments
### To get Cluster-IP, Name of service
kubectl get services
### To get pod IP, Status, node
kubectl get pod podname -o wide
### To deploy pod from yml file 
kubectl create -f nginxpod.yaml
### To change or edit in running pod, change in the yaml file then run.
kubectl apply -f nginxpod.yaml
### To create YAML file from command and run a pod 
kubectl run nginx --image=nginx --dry-run=client -o yaml > nginx-definition.yaml
### To view list of replication controller 
kubectl get replicationcontroller
### To view list of replica set 
kubectl get replicaset
### To update the replicaset, change in the yaml file then run.
kubectl replace -f replicaset-definition.yaml
#### or 
kubectl scale --replicas=6 -f replicaset-definition.yaml
#### or 
kubectl scale replicaset --replicas=2 myapp-replicaset(Name of replicaset)
#### or
kubectl edit replicaset (replicasetName)
### To delete replicaset
kubectl delete replicaset (Name of Replicaset)
### To create deployment
kubectl create -f deployment.yaml
### To delete deployment 
kubectl delete deployment deploymentName
### To get details of deployment
kubectl describe deployment deploymentName
### To get all the elements of kubernetes 
kubectl get all 
### To check status of rollout
kubectl rollout status deployment/myapp-deployment
### To check revision or history of deployment 
kubectl rollout history deployment/myapp-deployment