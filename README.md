# Just image with alpine + kubectl + bash 
# Check opened ports
lsof -i -P -n | grep LISTEN

# Log into pod
kubectl exec -c coordinator --stdin --tty presto-coordinator-blue-84649f586f-wvzxv -- /bin/bash

kubectl port-forward presto-coordinator-blue-84649f586f-l45kz 34275:34275

kubectl get deployments
kubectl describe deploy presto-worker-green
 
kubectl describe configmaps
kubectl describe configmaps presto.coordinator
